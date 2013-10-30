redirect_track
==============

Simple html page that redirects users to any given url and tracks a pageview for that url in your analytics account

Usage:

anlredirect.html?ai=trackingid&pn=pagename&ti=title&tg=http://www.google.com?param1=a&param2=b


Parameters:
ai = Analytics Trackng ID
pn = Pagename used in google analaytics
ti = title used to identify the target page in Analytics
tg = target url user is redirected to after pageview has been tracked. To use get parameters &tg=... MUST BE THE LAST PARAMETER!

If your tracking code for Google analytics is:
<script>
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

  ga('create', 'UA-43351596-1', 'bluesoybean.herokuapp.com');
  ga('send', 'pageview');

</script>

you need to use:
ai=UA-43351596
anlredirect.html?ai=UA-43351596-1&pn=bluesoybean.herokuapp.com


Theres a hosted version available under:
https://s3-eu-west-1.amazonaws.com/analyticsredirect/fbanlredirect.html




