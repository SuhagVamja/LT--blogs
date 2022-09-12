
<!DOCTYPE html>
<!--[if IE 7]>
<html class="ie ie7" lang="en-US" prefix="og: http://ogp.me/ns#">
<![endif]-->
<!--[if IE 8]>
<html class="ie ie8" lang="en-US" prefix="og: http://ogp.me/ns#">
<![endif]-->
<!--[if !(IE 7) & !(IE 8)]><!-->
<html lang="en-US" prefix="og: http://ogp.me/ns#">
<!--<![endif]-->
<head>
<meta name="twitter:card" />
<meta charset="UTF-8"><script type="807212fb32e79fd549d9754a-text/javascript">(window.NREUM||(NREUM={})).init={ajax:{deny_list:["bam.nr-data.net"]}};(window.NREUM||(NREUM={})).loader_config={licenseKey:"NRJS-15a9ea9b6e428dbd49e",applicationID:"1241459542"};window.NREUM||(NREUM={}),__nr_require=function(t,e,n){function r(n){if(!e[n]){var i=e[n]={exports:{}};t[n][0].call(i.exports,function(e){var i=t[n][1][e];return r(i||e)},i,i.exports)}return e[n].exports}if("function"==typeof __nr_require)return __nr_require;for(var i=0;i<n.length;i++)r(n[i]);return r}({1:[function(t,e,n){function r(){}function i(t,e,n,r){return function(){return s.recordSupportability("API/"+e+"/called"),o(t+e,[u.now()].concat(c(arguments)),n?null:this,r),n?void 0:this}}var o=t("handle"),a=t(9),c=t(10),f=t("ee").get("tracer"),u=t("loader"),s=t(4),d=NREUM;"undefined"==typeof window.newrelic&&(newrelic=d);var p=["setPageViewName","setCustomAttribute","setErrorHandler","finished","addToTrace","inlineHit","addRelease"],l="api-",v=l+"ixn-";a(p,function(t,e){d[e]=i(l,e,!0,"api")}),d.addPageAction=i(l,"addPageAction",!0),d.setCurrentRouteName=i(l,"routeName",!0),e.exports=newrelic,d.interaction=function(){return(new r).get()};var m=r.prototype={createTracer:function(t,e){var n={},r=this,i="function"==typeof e;return o(v+"tracer",[u.now(),t,n],r),function(){if(f.emit((i?"":"no-")+"fn-start",[u.now(),r,i],n),i)try{return e.apply(this,arguments)}catch(t){throw f.emit("fn-err",[arguments,this,t],n),t}finally{f.emit("fn-end",[u.now()],n)}}}};a("actionText,setName,setAttribute,save,ignore,onEnd,getContext,end,get".split(","),function(t,e){m[e]=i(v,e)}),newrelic.noticeError=function(t,e){"string"==typeof t&&(t=new Error(t)),s.recordSupportability("API/noticeError/called"),o("err",[t,u.now(),!1,e])}},{}],2:[function(t,e,n){function r(t){if(NREUM.init){for(var e=NREUM.init,n=t.split("."),r=0;r<n.length-1;r++)if(e=e[n[r]],"object"!=typeof e)return;return e=e[n[n.length-1]]}}e.exports={getConfiguration:r}},{}],3:[function(t,e,n){var r=!1;try{var i=Object.defineProperty({},"passive",{get:function(){r=!0}});window.addEventListener("testPassive",null,i),window.removeEventListener("testPassive",null,i)}catch(o){}e.exports=function(t){return r?{passive:!0,capture:!!t}:!!t}},{}],4:[function(t,e,n){function r(t,e){var n=[a,t,{name:t},e];return o("storeMetric",n,null,"api"),n}function i(t,e){var n=[c,t,{name:t},e];return o("storeEventMetrics",n,null,"api"),n}var o=t("handle"),a="sm",c="cm";e.exports={constants:{SUPPORTABILITY_METRIC:a,CUSTOM_METRIC:c},recordSupportability:r,recordCustom:i}},{}],5:[function(t,e,n){function r(){return c.exists&&performance.now?Math.round(performance.now()):(o=Math.max((new Date).getTime(),o))-a}function i(){return o}var o=(new Date).getTime(),a=o,c=t(11);e.exports=r,e.exports.offset=a,e.exports.getLastTimestamp=i},{}],6:[function(t,e,n){function r(t,e){var n=t.getEntries();n.forEach(function(t){"first-paint"===t.name?l("timing",["fp",Math.floor(t.startTime)]):"first-contentful-paint"===t.name&&l("timing",["fcp",Math.floor(t.startTime)])})}function i(t,e){var n=t.getEntries();if(n.length>0){var r=n[n.length-1];if(u&&u<r.startTime)return;var i=[r],o=a({});o&&i.push(o),l("lcp",i)}}function o(t){t.getEntries().forEach(function(t){t.hadRecentInput||l("cls",[t])})}function a(t){var e=navigator.connection||navigator.mozConnection||navigator.webkitConnection;if(e)return e.type&&(t["net-type"]=e.type),e.effectiveType&&(t["net-etype"]=e.effectiveType),e.rtt&&(t["net-rtt"]=e.rtt),e.downlink&&(t["net-dlink"]=e.downlink),t}function c(t){if(t instanceof y&&!w){var e=Math.round(t.timeStamp),n={type:t.type};a(n),e<=v.now()?n.fid=v.now()-e:e>v.offset&&e<=Date.now()?(e-=v.offset,n.fid=v.now()-e):e=v.now(),w=!0,l("timing",["fi",e,n])}}function f(t){"hidden"===t&&(u=v.now(),l("pageHide",[u]))}if(!("init"in NREUM&&"page_view_timing"in NREUM.init&&"enabled"in NREUM.init.page_view_timing&&NREUM.init.page_view_timing.enabled===!1)){var u,s,d,p,l=t("handle"),v=t("loader"),m=t(8),g=t(3),y=NREUM.o.EV;if("PerformanceObserver"in window&&"function"==typeof window.PerformanceObserver){s=new PerformanceObserver(r);try{s.observe({entryTypes:["paint"]})}catch(h){}d=new PerformanceObserver(i);try{d.observe({entryTypes:["largest-contentful-paint"]})}catch(h){}p=new PerformanceObserver(o);try{p.observe({type:"layout-shift",buffered:!0})}catch(h){}}if("addEventListener"in document){var w=!1,b=["click","keydown","mousedown","pointerdown","touchstart"];b.forEach(function(t){document.addEventListener(t,c,g(!1))})}m(f)}},{}],7:[function(t,e,n){function r(t,e){if(!i)return!1;if(t!==i)return!1;if(!e)return!0;if(!o)return!1;for(var n=o.split("."),r=e.split("."),a=0;a<r.length;a++)if(r[a]!==n[a])return!1;return!0}var i=null,o=null,a=/Version\/(\S+)\s+Safari/;if(navigator.userAgent){var c=navigator.userAgent,f=c.match(a);f&&c.indexOf("Chrome")===-1&&c.indexOf("Chromium")===-1&&(i="Safari",o=f[1])}e.exports={agent:i,version:o,match:r}},{}],8:[function(t,e,n){function r(t){function e(){t(c&&document[c]?document[c]:document[o]?"hidden":"visible")}"addEventListener"in document&&a&&document.addEventListener(a,e,i(!1))}var i=t(3);e.exports=r;var o,a,c;"undefined"!=typeof document.hidden?(o="hidden",a="visibilitychange",c="visibilityState"):"undefined"!=typeof document.msHidden?(o="msHidden",a="msvisibilitychange"):"undefined"!=typeof document.webkitHidden&&(o="webkitHidden",a="webkitvisibilitychange",c="webkitVisibilityState")},{}],9:[function(t,e,n){function r(t,e){var n=[],r="",o=0;for(r in t)i.call(t,r)&&(n[o]=e(r,t[r]),o+=1);return n}var i=Object.prototype.hasOwnProperty;e.exports=r},{}],10:[function(t,e,n){function r(t,e,n){e||(e=0),"undefined"==typeof n&&(n=t?t.length:0);for(var r=-1,i=n-e||0,o=Array(i<0?0:i);++r<i;)o[r]=t[e+r];return o}e.exports=r},{}],11:[function(t,e,n){e.exports={exists:"undefined"!=typeof window.performance&&window.performance.timing&&"undefined"!=typeof window.performance.timing.navigationStart}},{}],ee:[function(t,e,n){function r(){}function i(t){function e(t){return t&&t instanceof r?t:t?u(t,f,a):a()}function n(n,r,i,o,a){if(a!==!1&&(a=!0),!l.aborted||o){t&&a&&t(n,r,i);for(var c=e(i),f=m(n),u=f.length,s=0;s<u;s++)f[s].apply(c,r);var p=d[w[n]];return p&&p.push([b,n,r,c]),c}}function o(t,e){h[t]=m(t).concat(e)}function v(t,e){var n=h[t];if(n)for(var r=0;r<n.length;r++)n[r]===e&&n.splice(r,1)}function m(t){return h[t]||[]}function g(t){return p[t]=p[t]||i(n)}function y(t,e){l.aborted||s(t,function(t,n){e=e||"feature",w[n]=e,e in d||(d[e]=[])})}var h={},w={},b={on:o,addEventListener:o,removeEventListener:v,emit:n,get:g,listeners:m,context:e,buffer:y,abort:c,aborted:!1};return b}function o(t){return u(t,f,a)}function a(){return new r}function c(){(d.api||d.feature)&&(l.aborted=!0,d=l.backlog={})}var f="nr@context",u=t("gos"),s=t(9),d={},p={},l=e.exports=i();e.exports.getOrSetContext=o,l.backlog=d},{}],gos:[function(t,e,n){function r(t,e,n){if(i.call(t,e))return t[e];var r=n();if(Object.defineProperty&&Object.keys)try{return Object.defineProperty(t,e,{value:r,writable:!0,enumerable:!1}),r}catch(o){}return t[e]=r,r}var i=Object.prototype.hasOwnProperty;e.exports=r},{}],handle:[function(t,e,n){function r(t,e,n,r){i.buffer([t],r),i.emit(t,e,n)}var i=t("ee").get("handle");e.exports=r,r.ee=i},{}],id:[function(t,e,n){function r(t){var e=typeof t;return!t||"object"!==e&&"function"!==e?-1:t===window?0:a(t,o,function(){return i++})}var i=1,o="nr@id",a=t("gos");e.exports=r},{}],loader:[function(t,e,n){function r(){if(!M++){var t=T.info=NREUM.info,e=m.getElementsByTagName("script")[0];if(setTimeout(u.abort,3e4),!(t&&t.licenseKey&&t.applicationID&&e))return u.abort();f(x,function(e,n){t[e]||(t[e]=n)});var n=a();c("mark",["onload",n+T.offset],null,"api"),c("timing",["load",n]);var r=m.createElement("script");0===t.agent.indexOf("http://")||0===t.agent.indexOf("https://")?r.src=t.agent:r.src=l+"://"+t.agent,e.parentNode.insertBefore(r,e)}}function i(){"complete"===m.readyState&&o()}function o(){c("mark",["domContent",a()+T.offset],null,"api")}var a=t(5),c=t("handle"),f=t(9),u=t("ee"),s=t(7),d=t(2),p=t(3),l=d.getConfiguration("ssl")===!1?"http":"https",v=window,m=v.document,g="addEventListener",y="attachEvent",h=v.XMLHttpRequest,w=h&&h.prototype,b=!1;NREUM.o={ST:setTimeout,SI:v.setImmediate,CT:clearTimeout,XHR:h,REQ:v.Request,EV:v.Event,PR:v.Promise,MO:v.MutationObserver};var E=""+location,x={beacon:"bam.nr-data.net",errorBeacon:"bam.nr-data.net",agent:"js-agent.newrelic.com/nr-1216.min.js"},O=h&&w&&w[g]&&!/CriOS/.test(navigator.userAgent),T=e.exports={offset:a.getLastTimestamp(),now:a,origin:E,features:{},xhrWrappable:O,userAgent:s,disabled:b};if(!b){t(1),t(6),m[g]?(m[g]("DOMContentLoaded",o,p(!1)),v[g]("load",r,p(!1))):(m[y]("onreadystatechange",i),v[y]("onload",r)),c("mark",["firstbyte",a.getLastTimestamp()],null,"api");var M=0}},{}],"wrap-function":[function(t,e,n){function r(t,e){function n(e,n,r,f,u){function nrWrapper(){var o,a,s,p;try{a=this,o=d(arguments),s="function"==typeof r?r(o,a):r||{}}catch(l){i([l,"",[o,a,f],s],t)}c(n+"start",[o,a,f],s,u);try{return p=e.apply(a,o)}catch(v){throw c(n+"err",[o,a,v],s,u),v}finally{c(n+"end",[o,a,p],s,u)}}return a(e)?e:(n||(n=""),nrWrapper[p]=e,o(e,nrWrapper,t),nrWrapper)}function r(t,e,r,i,o){r||(r="");var c,f,u,s="-"===r.charAt(0);for(u=0;u<e.length;u++)f=e[u],c=t[f],a(c)||(t[f]=n(c,s?f+r:r,i,f,o))}function c(n,r,o,a){if(!v||e){var c=v;v=!0;try{t.emit(n,r,o,e,a)}catch(f){i([f,n,r,o],t)}v=c}}return t||(t=s),n.inPlace=r,n.flag=p,n}function i(t,e){e||(e=s);try{e.emit("internal-error",t)}catch(n){}}function o(t,e,n){if(Object.defineProperty&&Object.keys)try{var r=Object.keys(t);return r.forEach(function(n){Object.defineProperty(e,n,{get:function(){return t[n]},set:function(e){return t[n]=e,e}})}),e}catch(o){i([o],n)}for(var a in t)l.call(t,a)&&(e[a]=t[a]);return e}function a(t){return!(t&&t instanceof Function&&t.apply&&!t[p])}function c(t,e){var n=e(t);return n[p]=t,o(t,n,s),n}function f(t,e,n){var r=t[e];t[e]=c(r,n)}function u(){for(var t=arguments.length,e=new Array(t),n=0;n<t;++n)e[n]=arguments[n];return e}var s=t("ee"),d=t(10),p="nr@original",l=Object.prototype.hasOwnProperty,v=!1;e.exports=r,e.exports.wrapFunction=c,e.exports.wrapInPlace=f,e.exports.argsToArray=u},{}]},{},["loader"]);</script>
<meta name="viewport" content="width=device-width">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
<title>How To Identify Locators In Appium [With Examples] | LambdaTest</title>
<link rel="profile" href="http://gmpg.org/xfn/11">
<link rel="pingback" href="https://www.lambdatest.com/blog/xmlrpc.php">
<script src="/cdn-cgi/scripts/7d0fa10a/cloudflare-static/rocket-loader.min.js" data-cf-settings="807212fb32e79fd549d9754a-|49"></script><link media="print" onload="this.onload=null;this.removeAttribute('media');" href="https://fonts.googleapis.com/css2?family=Inter:wght@100;200;300;400;500;600;700;800&display=swap" rel="stylesheet" />
<link rel="stylesheet" type="text/css" href="https://www.lambdatest.com/blog/wp-content/themes/blog/css/bootstrap.css" />
<link rel="stylesheet" type="text/css" href="https://www.lambdatest.com/blog/wp-content/themes/blog/css/style.css" />
<link rel="stylesheet" type="text/css" href="https://www.lambdatest.com/blog/wp-content/themes/blog/css/blog.css" />

<!--[if lt IE 9]>
        <script src="https://www.lambdatest.com/blog/wp-content/themes/blog/js/html5.js"></script>
        <![endif]-->

<meta name="description" content="This Appium testing tutorial focuses on the Appium automation tool to automate Android and iOS applications using different locators in Appium." />
<meta name="robots" content="follow, index, max-snippet:-1, max-video-preview:-1, max-image-preview:large" />
<link rel="canonical" href="https://www.lambdatest.com/blog/locators-in-appium/" />
<meta property="og:locale" content="en_US">
<meta property="og:type" content="article">
<meta property="og:title" content="How To Identify Locators In Appium [With Examples] | LambdaTest">
<meta property="og:description" content="This Appium testing tutorial focuses on the Appium automation tool to automate Android and iOS applications using different locators in Appium.">
<meta property="og:url" content="https://www.lambdatest.com/blog/locators-in-appium/">
<meta property="og:site_name" content="LambdaTest">
<meta property="article:publisher" content="https://www.facebook.com/lambdatest">
<meta property="article:author" content="https://www.linkedin.com/in/wasiqbhamla/">
<meta property="article:section" content="Mobile App Testing">
<meta property="article:published_time" content="2022-09-09T16:55:34+00:00">
<meta property="article:modified_time" content="2022-09-09T17:48:06+00:00">
<meta property="og:updated_time" content="2022-09-09T17:48:06+00:00">
<meta property="og:image" content="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/How-To-Identify-Locators-In-Appium_-With-Examples-1-1-2.png">
<meta property="og:image:secure_url" content="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/How-To-Identify-Locators-In-Appium_-With-Examples-1-1-2.png">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="627">
<meta property="og:image:alt" content="How To Identify Locators In Appium_ [With Examples]">
<meta property="og:image:type" content="image/png">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="How To Identify Locators In Appium [With Examples] | LambdaTest">
<meta name="twitter:description" content="This Appium testing tutorial focuses on the Appium automation tool to automate Android and iOS applications using different locators in Appium.">
<meta name="twitter:creator" content="@WasiqBhamla">
<meta name="twitter:image" content="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/How-To-Identify-Locators-In-Appium_-With-Examples-1-1-2.png">
<script type="application/ld+json">{"@context":"https:\/\/schema.org","@graph":[{"@type":"Article","headline":"How To Identify Locators In Appium [With Examples] | LambdaTest","datePublished":"2022-09-09T16:55:34+00:00","dateModified":"2022-09-09T17:48:06+00:00","publisher":{"@type":"Organization","name":"LambdaTest","logo":{"@type":"ImageObject","url":"https:\/\/www.lambdatest.com\/blog\/wp-content\/uploads\/2020\/08\/LambdaTest-320-180.png"}},"mainEntityOfPage":{"@type":"WebPage","@id":"https:\/\/www.lambdatest.com\/blog\/locators-in-appium\/"},"author":{"@type":"Person","name":"Wasiq Bhamla"},"description":"This Appium testing tutorial focuses on the Appium automation tool to automate Android and iOS applications using different locators in Appium.","image":{"@type":"ImageObject","url":"https:\/\/www.lambdatest.com\/blog\/wp-content\/uploads\/2022\/09\/How-To-Identify-Locators-In-Appi-1-1-1-1-1-1-1-1.png","width":480,"height":270}}]}</script>

<link rel='dns-prefetch' href='//fonts.googleapis.com' />
<link rel='dns-prefetch' href='//s.w.org' />
<link href='https://fonts.gstatic.com' crossorigin rel='preconnect' />
<link rel="alternate" type="application/rss+xml" title="LambdaTest &raquo; Feed" href="https://www.lambdatest.com/blog/feed/" />
<link rel="alternate" type="application/rss+xml" title="LambdaTest &raquo; Comments Feed" href="https://www.lambdatest.com/blog/comments/feed/" />
<link rel="alternate" type="application/rss+xml" title="LambdaTest &raquo; How To Identify Locators In Appium [With Examples] Comments Feed" href="https://www.lambdatest.com/blog/locators-in-appium/feed/" />
<script type="807212fb32e79fd549d9754a-text/javascript">
			window._wpemojiSettings = {"baseUrl":"https:\/\/s.w.org\/images\/core\/emoji\/12.0.0-1\/72x72\/","ext":".png","svgUrl":"https:\/\/s.w.org\/images\/core\/emoji\/12.0.0-1\/svg\/","svgExt":".svg","source":{"concatemoji":"https:\/\/www.lambdatest.com\/blog\/wp-includes\/js\/wp-emoji-release.min.js?ver=5.2.15"}};
			!function(e,a,t){var n,r,o,i=a.createElement("canvas"),p=i.getContext&&i.getContext("2d");function s(e,t){var a=String.fromCharCode;p.clearRect(0,0,i.width,i.height),p.fillText(a.apply(this,e),0,0);e=i.toDataURL();return p.clearRect(0,0,i.width,i.height),p.fillText(a.apply(this,t),0,0),e===i.toDataURL()}function c(e){var t=a.createElement("script");t.src=e,t.defer=t.type="text/javascript",a.getElementsByTagName("head")[0].appendChild(t)}for(o=Array("flag","emoji"),t.supports={everything:!0,everythingExceptFlag:!0},r=0;r<o.length;r++)t.supports[o[r]]=function(e){if(!p||!p.fillText)return!1;switch(p.textBaseline="top",p.font="600 32px Arial",e){case"flag":return s([55356,56826,55356,56819],[55356,56826,8203,55356,56819])?!1:!s([55356,57332,56128,56423,56128,56418,56128,56421,56128,56430,56128,56423,56128,56447],[55356,57332,8203,56128,56423,8203,56128,56418,8203,56128,56421,8203,56128,56430,8203,56128,56423,8203,56128,56447]);case"emoji":return!s([55357,56424,55356,57342,8205,55358,56605,8205,55357,56424,55356,57340],[55357,56424,55356,57342,8203,55358,56605,8203,55357,56424,55356,57340])}return!1}(o[r]),t.supports.everything=t.supports.everything&&t.supports[o[r]],"flag"!==o[r]&&(t.supports.everythingExceptFlag=t.supports.everythingExceptFlag&&t.supports[o[r]]);t.supports.everythingExceptFlag=t.supports.everythingExceptFlag&&!t.supports.flag,t.DOMReady=!1,t.readyCallback=function(){t.DOMReady=!0},t.supports.everything||(n=function(){t.readyCallback()},a.addEventListener?(a.addEventListener("DOMContentLoaded",n,!1),e.addEventListener("load",n,!1)):(e.attachEvent("onload",n),a.attachEvent("onreadystatechange",function(){"complete"===a.readyState&&t.readyCallback()})),(n=t.source||{}).concatemoji?c(n.concatemoji):n.wpemoji&&n.twemoji&&(c(n.twemoji),c(n.wpemoji)))}(window,document,window._wpemojiSettings);
		</script>
<style type="text/css">
img.wp-smiley,
img.emoji {
	display: inline !important;
	border: none !important;
	box-shadow: none !important;
	height: 1em !important;
	width: 1em !important;
	margin: 0 .07em !important;
	vertical-align: -0.1em !important;
	background: none !important;
	padding: 0 !important;
}
</style>
<link rel='stylesheet' id='crayon-css' href='https://www.lambdatest.com/blog/wp-content/plugins/crayon-syntax-highlighter/css/min/crayon.min.css?ver=_2.7.2_beta' type='text/css' media='all' />
<link rel='stylesheet' id='crayon-theme-classic-css' href='https://www.lambdatest.com/blog/wp-content/plugins/crayon-syntax-highlighter/themes/classic/classic.css?ver=_2.7.2_beta' type='text/css' media='all' />
<link rel='stylesheet' id='crayon-font-liberation-mono-css' href='https://www.lambdatest.com/blog/wp-content/plugins/crayon-syntax-highlighter/fonts/liberation-mono.css?ver=_2.7.2_beta' type='text/css' media='all' />
<link rel='stylesheet' id='wp-block-library-css' href='https://www.lambdatest.com/blog/wp-includes/css/dist/block-library/style.min.css?ver=5.2.15' type='text/css' media='all' />
<link rel='stylesheet' id='awpa-wp-post-author-style-css' href='https://www.lambdatest.com/blog/wp-content/plugins/wp-post-author//assets/css/awpa-frontend-style.css?ver=5.2.15' type='text/css' media='all' />
<link rel='stylesheet' id='twentythirteen-fonts-css' href='https://fonts.googleapis.com/css?family=Source+Sans+Pro%3A300%2C400%2C700%2C300italic%2C400italic%2C700italic%7CBitter%3A400%2C700&#038;subset=latin%2Clatin-ext' type='text/css' media='all' />
<link rel='stylesheet' id='genericons-css' href='https://www.lambdatest.com/blog/wp-content/themes/blog/genericons/genericons.css?ver=3.03' type='text/css' media='all' />
<link rel='stylesheet' id='twentythirteen-style-css' href='https://www.lambdatest.com/blog/wp-content/themes/blog/style.css?ver=2013-07-18' type='text/css' media='all' />
<!--[if lt IE 9]>
<link rel='stylesheet' id='twentythirteen-ie-css'  href='https://www.lambdatest.com/blog/wp-content/themes/blog/css/ie.css?ver=2013-07-18' type='text/css' media='all' />
<![endif]-->
<link rel='stylesheet' id='addtoany-css' href='https://www.lambdatest.com/blog/wp-content/plugins/add-to-any/addtoany.min.css?ver=1.15' type='text/css' media='all' />
<script type="807212fb32e79fd549d9754a-text/javascript" src='https://www.lambdatest.com/blog/wp-includes/js/jquery/jquery.js?ver=1.12.4-wp'></script>
<script type="807212fb32e79fd549d9754a-text/javascript" src='https://www.lambdatest.com/blog/wp-includes/js/jquery/jquery-migrate.min.js?ver=1.4.1'></script>
<script type="807212fb32e79fd549d9754a-text/javascript">
/* <![CDATA[ */
var CrayonSyntaxSettings = {"version":"_2.7.2_beta","is_admin":"0","ajaxurl":"https:\/\/www.lambdatest.com\/blog\/wp-admin\/admin-ajax.php","prefix":"crayon-","setting":"crayon-setting","selected":"crayon-setting-selected","changed":"crayon-setting-changed","special":"crayon-setting-special","orig_value":"data-orig-value","debug":""};
var CrayonSyntaxStrings = {"copy":"Press %s to Copy, %s to Paste","minimize":"Click To Expand Code"};
/* ]]> */
</script>
<script type="807212fb32e79fd549d9754a-text/javascript" src='https://www.lambdatest.com/blog/wp-content/plugins/crayon-syntax-highlighter/js/min/crayon.min.js?ver=_2.7.2_beta'></script>
<script type="807212fb32e79fd549d9754a-text/javascript" src='https://www.lambdatest.com/blog/wp-content/plugins/add-to-any/addtoany.min.js?ver=1.1'></script>
<link rel='https://api.w.org/' href='https://www.lambdatest.com/blog/wp-json/' />
<link rel="EditURI" type="application/rsd+xml" title="RSD" href="https://www.lambdatest.com/blog/xmlrpc.php?rsd" />
<link rel="wlwmanifest" type="application/wlwmanifest+xml" href="https://www.lambdatest.com/blog/wp-includes/wlwmanifest.xml" />
<meta name="generator" content="WordPress 5.2.15" />
<link rel='shortlink' href='https://www.lambdatest.com/blog/?p=35835' />
<link rel="alternate" type="application/json+oembed" href="https://www.lambdatest.com/blog/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fwww.lambdatest.com%2Fblog%2Flocators-in-appium%2F" />
<link rel="alternate" type="text/xml+oembed" href="https://www.lambdatest.com/blog/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fwww.lambdatest.com%2Fblog%2Flocators-in-appium%2F&#038;format=xml" />
<script data-cfasync="false">
window.a2a_config=window.a2a_config||{};a2a_config.callbacks=[];a2a_config.overlays=[];a2a_config.templates={};
a2a_config.icon_color="transparent,#707070";
(function(d,s,a,b){a=d.createElement(s);b=d.getElementsByTagName(s)[0];a.async=1;a.src="https://static.addtoany.com/menu/page.js";b.parentNode.insertBefore(a,b);})(document,"script");
</script>
<style type="text/css" id="simple-css-output">@media(max-width:1030px) and (min-width:1000px){ .widget .widget-title(font-size:14px !important)}.thank{display:none}.try_blog button.subscribe-btn{height:30px; padding:5px 0!important; display:block; width:93%; margin-top:10px}.blog_parent_email{background-color: #fafafa;border-radius: 5px;border: solid 1px #f1f1f1;padding:15px 10px 30px}.blog_heading_email{font-size: 20px;letter-spacing: 0.63px;color: #000000;margin:0}.blog_description_email{font-size: 14px;line-height: 1.36;letter-spacing: 0.4px;color: #000000;} .emailBlock{display: flex; justify-content: center; } .email-box{margin-top:20px;position: relative;} .trybox_section{margin-top:10px;} .subscribe-btn {font-size: 14px;font-weight: bold;line-height: 1.43;letter-spacing: 1px;text-align: center;color: #FFFFFF; border-radius: 3px;height: 40px;background-color:#EF6C00; border:1px solid #EF6C00; padding-left: 20px; padding-right: 20px;} .emailer_subscribe{padding: 20px 40px;background-color: #FFEAEA;} .trybox_content h2{font-size: 18px;color: #17192F;line-height: 1.40;} .email-box input[type="email"] { width: 270px; height: 40px;border-radius: 3px; border: solid 1px #000000;font-size: 12px;font-weight: 300;line-height: 1.67;color: #4A4A4A;} .email-box .emailid {position: absolute;top: 45px; left: 5px; color: red; font-size: 12px;width: 100%;} .submittedform .h1 {font-size: 40px;font-weight: 100;letter-spacing: 1.15px; margin-bottom: 0px; display: block;margin-left: -10px;}.submittedform p {font-size: 18px; line-height: 1.8; color: #17192F; margin-bottom: 10px;margin-top: 40px;}.submittedform{display: none;}.tryit{float: right; margin-left: 10px;}.inputBlock{float:left;} .codejaglogo{width:100%; max-width:150px;}.sitekitwebinar a {color: #fff!important;font-weight:600!important;text-decoration: none;}.sitekitwebinar a:hover{text-decoration:underline; color:#fff!important;} @media (max-width: 768px){ .email-box input[type="email"] { width: 145px;} .subscribe-btn { font-size: 12px; padding:10px!important;} .emailer_subscribe {padding: 20px 20px;} }.faq_lambda{padding:40px 0px;} .faq_lambda h3{font-size:22px;font-weight:bold;line-height: 1.2; margin-bottom: 40px; margin-top: 5px} .faq_list_lambda{margin: 40px 0px; border:1px solid #ccc;padding:20px;} .faq_list_lambda h4{font-size:22px;font-weight:bold;line-height: 1.2; margin-bottom: 10px; margin-top: 5px} .faq_list_lambda p{font-size:18px; margin-bottom: 10px; margin-top: 5px}.arrow.down{border: solid black; border-width: 0 2px 2px 0; display: inline-block; padding: 2px; margin-bottom: 2px; margin-left: 5px; transform: rotate(45deg); -webkit-transform: rotate(45deg);}.ft-menu { padding-left: 0px!important; }.main-popup-blog{background:#000; display:flex; padding:10px;min-height:280px}.right-popup-inner{padding:0px 10px 0px 40px}#credential_picker_container{position: fixed;z-index: 999999!important;height: 184px;top: 125px!important;animation: cssAnimation 0s 3s forwards; visibility: hidden; display:none;} @keyframes cssAnimation { to { visibility: visible; }}.lambda-floating-banner {display: none; z-index: 9999;position: fixed;bottom: 5%;left: 50%; -ms-transform: translateX(-50%); transform: translateX(-50%);transition: bottom 150ms ease;}.lambda-floating-banner img {width: auto;height: 30px;}.lambda-floating-banner span.bannerText {font-size: 16px;padding-left: 21px; padding-right: 21px;color: #fff;vertical-align: middle;display: inline-block;margin-bottom:0px;}.lambda-floating-banner .btn-sm {width: 150px;}.lambda-floating-banner a {padding: 10px 15px;font-size: 12px;font-weight: bold;background-color: #fff;color: #1E84B4;border-radius:5px; text-transform:uppercase;}.lambda-floating-banner div.close {position: absolute;cursor: pointer;top: -15px;right: -10px;padding: 5px; min-width: auto;line-height: 0;font-size: 12px;color: #fff;opacity: 1!important;background: #999;border-radius: 50%; width: 22px;height: 22px;font-weight: 500;}.lambda-floating-banner a:hover{background:#1E84B4; color:#ffffff; text-decoration:none; border:2px solid #fff;}.btnclose{display:none!important}.nav>li.login>a{width:150px!important; padding:0px 15px!important;}@media(max-width:1024px){.lambda-floating-banner {display:none!important}}@media(max-width:767px){.main-popup-blog{background:#000; display:block !important; padding:10px;min-height:280px} .main-popup-blog img{display:none !important} .right-popup-inner{padding:0px 10px !important} #credential_picker_container,#credential_picker_iframe{display:none!important;} .lt_video .modal-body{width:300px;}}@media(min-width:768px){.right-inner-popup-content{ position: absolute;padding-right:10px; top: 50%;-ms-transform: translateY(-50%);transform: translateY(-50%); }}@media(min-width:769px){.awpa-author-block img{width:100% !important}}@media(max-width:500px){.table{width:300px; overflow-x:scroll} .table table{margin-left: auto !important; margin-right: auto !important;}}@media(max-width:576px){.sidebar_mob{z-index:-1}}@media(min-width:768px) and (max-width:1200px){ .navbar-nav>li>a{padding-right: 7px!important; padding-left: 7px!important;} .nav>li.login>a{width:125px!important; padding:0px 10px!important;}}.blog_breadCrumb{display:flex; margin:10px 0px;}.blog_breadCrumb a{color:#000; margin-left:10px;}.blog_breadCrumb a:hover{color:#0ebac5;}.blog_breadCrumb a .arrow_right{ border: solid #0ebac5;border-width: 0 2px 2px 0;display: inline-block;padding: 3px;transform: rotate(-45deg); -webkit-transform: rotate(-45deg);}.blog_breadCrumb .blog_breadcrumb_content:hover{color:#000; text-decoration:underline;}.custom__social__icons .a2a_button_facebook span{border:1px solid #10375C!important; background-color:transparent!important;width: 25px!important;height: 25px!important;display: flex!important;}.custom__social__icons .a2a_button_facebook svg path, .custom__social__icons .a2a_button_twitter svg path, .custom__social__icons .a2a_button_linkedin svg path{fill:#10375C;}.custom__social__icons .a2a_button_facebook svg, .custom__social__icons .a2a_button_twitter svg, .custom__social__icons .a2a_button_linkedin svg{width:26px}.custom__social__icons .a2a_button_twitter span{border:1px solid #10375C!important; background-color:transparent!important;width: 25px!important;height: 25px!important;display: flex!important;margin-top:10px!important}.custom__social__icons .a2a_button_linkedin span{border:1px solid #10375C!important; background-color:transparent!important;width: 25px!important;height: 25px!important;display: flex!important;margin-top:10px!important}@media(max-width:767px){ .addtoany_shortcode{margin-top:-5px!important} .sitekitwebinar{display:none !important;} .hasSitekit .tagline{top:60px !important;} .hasSitekit .blog-sec{margin-top:126px !important;} .custom__social__icons .a2a_button_facebook span, .custom__social__icons .a2a_button_linkedin span, .custom__social__icons .a2a_button_twitter span{width: initial!important;height: initial!important;display: initial!important;margin-top:0px!important}}</style> <style type="text/css" id="twentythirteen-header-css">
			.site-header {
			background: url(https://www.lambdatest.com/blog/wp-content/themes/blog/images/headers/circle.png) no-repeat scroll top;
			background-size: 1600px auto;
		}
		@media (max-width: 767px) {
			.site-header {
				background-size: 768px auto;
			}
		}
		@media (max-width: 359px) {
			.site-header {
				background-size: 360px auto;
			}
		}
		</style>

<script defer src="https://www.googletagmanager.com/gtag/js?id=AW-833407987" type="807212fb32e79fd549d9754a-text/javascript"></script>
<script type="807212fb32e79fd549d9754a-text/javascript">
	function getCookie(name) {
            var value = "; " + document.cookie;
            var parts = value.split("; " + name + "=");
            if (parts.length == 2) return parts.pop().split(";").shift();
        }</script>
<script type="807212fb32e79fd549d9754a-text/javascript">
		window.dataLayer = window.dataLayer || [];

		function gtag() {
			dataLayer.push(arguments);
		}
		gtag('js', new Date());
		gtag('config', 'AW-833407987');
	</script>

<script type="807212fb32e79fd549d9754a-text/javascript">
		(function(w, d, s, l, i) {
			w[l] = w[l] || [];
			w[l].push({
				'gtm.start': new Date().getTime(),
				event: 'gtm.js'
			});
			var f = d.getElementsByTagName(s)[0],
				j = d.createElement(s),
				dl = l != 'dataLayer' ? '&l=' + l : '';
			j.defer = true;
			j.src =
				'https://www.googletagmanager.com/gtm.js?id=' + i + dl;
			f.parentNode.insertBefore(j, f);
		})(window, document, 'script', 'dataLayer', 'GTM-53DM3BZ');
	</script>

<script defer src="https://www.lambdatest.com/assets/js/jwt-decode.min.js" type="807212fb32e79fd549d9754a-text/javascript"></script>
<script defer src="https://www.lambdatest.com/resources/js/zohoscript.js" type="807212fb32e79fd549d9754a-text/javascript"></script>
<style>
	.offer{font-weight: bold; margin-right:5px;}
    #timer{margin-left:5px;}
			
			.sitekitwebinar p{font-weight:500!important;}
.sitekitwebinar{text-align: center; background: #1e183a;  padding: 24px 15px 15px 15px!important; position: relative; display: none; }
.sitekitwebinar p{color: #fff; margin-bottom: 0; display: inline-block; font-size: 16px!important; letter-spacing: 0.4px;}
.sitekitwebinar .regbtn{background: none; color: #000000 !important; text-decoration: underline; padding: 8px 10px; border-radius: 3px; font-size: 16px; font-weight: bold!important; letter-spacing: 1.83px; }
.sitekitwebinar .regbtn .fa{font-size: 18px; font-weight: bold; font-style: initial; position: relative; top: 1px;}
.closesitewebinar{position: absolute; right: 0; top: 12px; color: #000!important; padding: 13px 20px; font-size:15px; }
.closesitewebinar .fa{ font-style: initial; font-weight: bold;}
.sitekitwebinar.d-none{display: none !important;}
	
	.hasSitekit .tagline{top: 135px;}
	.hasSitekit .taglinePrime{top: 60px;}
	.hasSitekit .blog-sec{margin-top: 196px;}
	.contact{display:none!important;}
	@media (max-width: 767px) {
		.hasSitekit .tagline {top: 174px; }
		.hasSitekit .taglinePrime { top: 60px; }
		.hasSitekit .blog-sec {margin-top: 225px; }
	}

	.rs-dropdown:hover .dropdown-menu{display: block; padding-top: 0px; padding-bottom: 0px; margin-top: 0;}
	.rs-dropdown .dropdown-menu{ padding: 0; border: 0; box-shadow: 0px 2px 10px #ccc;}
	.rs-dropdown .dropdown-menu .dropdown-item{ padding: 10px 20px; color: #000000; font-size: 13px; font-weight: 500;  background-color: #ffffff !important; line-height: initial;
		width: 100%; display: block;
	}
	.rs-dropdown .dropdown-menu .dropdown-item:hover{background-color: #f5f5f5 !important;}
			@media(min-width:991px)
{
	header .dropdown-menu{column-count: 2 !important;
		left: -100% !important;
		min-width: 320px !important;
	}
}
	@media(max-width: 767px) {
		.rs-dropdown .dropdown-menu{ position: initial; float: none; }
		.ft-menu a {display:flex;}
		.contact{display:block!important;}
		.startchat{display:none!important;}
	
	}
	}
			
	

		</style>
</head>
<body class="post-template-default single single-post postid-35835 single-format-standard sidebar">
<header class="header">
<div class="sitekitwebinar" style="">
<div class="container">
<div class="row">
<div class="col-sm-12">
<div style="disply:flex; align-items:center;">
<p>
Free Live Workshop: Clean Coding Practices for Test Automation | Programmers' Day Special <img loading="lazy" src="https://www.lambdatest.com/resources/images/webinar/tech.svg" class="ml-5 w-18" alt="Testμ Conf 2022 " width="29" height="32">
<a href="https://www.lambdatest.com/webinar/clean-coding-practices-for-test-automation" class="">Register Now &gt;&gt;</a>
</p>
</div>
</div>
</div>
<a href="#none" class="closesitewebinar">
X
</a>
</div>
</div>
<nav>
<div class="container">

<div class="navbar-header">
<div class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
<img src="https://www.lambdatest.com/blog/wp-content/themes/blog/images/humburger.png" alt="Menu" width="30" height="25">
<img src="https://www.lambdatest.com/blog/wp-content/themes/blog/images/sticky-humburger.png" alt="Menu" class="hidden" width="30" height="25">
</div>
<a class="navbar-brand" href="https://www.lambdatest.com">
<img alt="LambdaTest Logo" src="https://www.lambdatest.com/resources/images/logos/logo.svg" width="147" height="26">
<img alt="LambdaTest Logo" src="https://www.lambdatest.com/resources/images/logos/logo.svg" class="hidden" width="147" height="26">
</a>
</div>

<div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
<div class="nav navbar-nav dropdown_blog_nav">
<div class="header__menu__items">
<div class="dropdown rs-dropdown dropdown_blog item_link">
<a class="dropdown-toggle feature_link" data-toggle="dropdown" href="https://www.lambdatest.com/feature">Platform <i class="arrow down"></i></a>
<div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
<div class="table__main">
<div class="col-sm-12 col-xs-12 header_col">
<div class="col-sm-8 col-xs-12 header_inner_col">
<div class="row">
<div class="col-sm-6 col-xs-12 header_col">
<ul class="header-icon">
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/online-browser-testing">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/Browser-testing.svg" alt="Browser Testing" width="25" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Online Browser Testing</h3>
<p>Manual live-interactive cross browser testing</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/selenium-automation">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/selenium.svg" alt="Selenium" width="26" height="26" loading="lazy">
</div>
<div class="content_items">
<h3>Selenium Testing</h3>
<p>Run Selenium scripts on cloud-based infrastructure</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/cypress-testing">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header_cypress.svg" alt="Lambdatest Cypress" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Cypress Testing</h3>
<p>Run Cypress scripts on cloud-based infrastructure</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/hyperexecute">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/Hypertest.svg" alt="Lambdatest Cypress" width="26" height="26" loading="lazy">
</div>
<div class="content_items">
<h3>HyperExecute</h3>
<p>Blazing fast next-gen Automation Testing Cloud</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/on-premise-selenium-grid">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/selenium.svg" alt="Lambdatest Cypress" width="26" height="26" loading="lazy">
</div>
<div class="content_items">
<h3>On-Premise Selenium Grid</h3>
<p>Our cloud infrastructure paired with security of your firewall</p>
</div>
</div>
</a>
</li>
</ul>
</div>
<div class="col-sm-6 col-xs-12 header_col">
<ul class="header_inner header-icon">
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/mobile-app-testing">
<div class="dropdown-item-content">
<div>
<img loading="lazy" src="https://www.lambdatest.com/resources/images/header/Native-app-testing.svg" alt="LambdaTest Native App Testing" width="24" height="24">
</div>
<div class="content_items">
<h3>Native App Testing</h3>
<p>Live-interactive app testing on Android and iOS devices</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/real-device-cloud">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/Real-devices.svg" alt="Real Devices Cloud" width="24" height="23" loading="lazy">
</div>
<div class="content_items">
<h3>Real Devices Cloud</h3>
<p>Test websites and applications on real devices</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/smart-visual-ui-testing">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/Visual-Regression.svg" alt="Visual Regression" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Visual Regression Cloud</h3>
<p>Pixel-by-pixel comparison among images</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/test-at-scale">
<div class="dropdown-item-content ">
<div>
<img src="	https://www.lambdatest.com/resources/images/header/TAS.svg" alt="TAS" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Test At Scale</h3>
<p>Open source test selection and flaky test management platform</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/automation-testing">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/Automation-testing-cloud.svg" alt="Automation Testing Cloud" width="24" height="20" loading="lazy">
</div>
<div class="content_items">
<h3>Automation Testing Cloud</h3>
<p>Run automation test on a scalable cloud-based infrastructure</p>
</div>
</div>
</a>
</li>
</ul>
</div>
 </div>
</div>
<div class="col-sm-4 col-xs-12 header_col">
<div class="platform_tool">
<div class="tool_section">
<h3>TOOLS</h3>
<a href="https://www.lambdatest.com/downloads" class="">All Tools<img loading="lazy" src="https://www.lambdatest.com/resources/images/headerArrow.webp" alt="Arrow" width="16" height="16" style="margin-left:10px;"></a>
</div>
<ul class="header-icon">
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/underpass">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/logo-Underpass.webp" alt="Underpass" width="24" height="18" loading="lazy">
</div>
<div class="content_items">
<h3>Underpass</h3>
<p>A GUI desktop application for secure localhost testing</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/lt-browser">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/LT-Browser.webp" alt="LambdaTest LT Browser" width="22" height="22" loading="lazy">
</div>
<div class="content_items">
<h3>LT Browser</h3>
<p> Next-gen browser to build, test & debug responsive websites</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://chrome.google.com/webstore/detail/lt-debug/kofahhnmgobkidipanhejacffiigppcd">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/lt-debug.svg" alt="LambdaTest LT Debug" width="22" height="22" loading="lazy">
</div>
<div class="content_items">
<h3>LT Debug</h3>
<p>Chrome extension to debug web issues and accelerate your development</p>
</div>
</div>
</a>
</li>
</ul>
<div class="tool_section intergration_section">
<h3>INTEGRATIONS</h3>
<a href="https://www.lambdatest.com/integrations" class="">See all 120+<img src="https://www.lambdatest.com/resources/images/headerArrow.webp" alt="Arrow" width="16" height="16" style="margin-left:10px;" loading="lazy"></a>
</div>
<ul class="hover-integration">
<li>
<a href="https://www.lambdatest.com/support/docs/jenkins-with-lambdatest/">
<img src="https://www.lambdatest.com/resources/images/header/logo-jenkin.webp" alt="Jenkin" width="27" height="38" title="Jenkin" loading="lazy">
</a>
</li>
<li>
<a href="https://www.lambdatest.com/support/docs/github-integration/">
<img src="https://www.lambdatest.com/resources/images/header/integration-github.webp" class="Github" alt="Github" width="32" height="31" title="Github" loading="lazy">
</a>
</li>
<li>
<a href="https://www.lambdatest.com/support/docs/slack-integration/">
<img src="https://www.lambdatest.com/resources/images/header/integration-slack.webp" alt="Slack" width="33" height="32" title="Slack" loading="lazy">
</a>
</li>
<li>
<a href="https://www.lambdatest.com/support/docs/katalon-integration-with-lambdatest/">
<img src="https://www.lambdatest.com/resources/images/header/Katalon.webp" alt="Katalon" width="29" height="29" title="Katalon" loading="lazy">
</a>
</li>
<li>
<a href="https://www.lambdatest.com/support/docs/jasmine-with-karma-running-jasmine-tests-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/Jasmine.webp" alt="Jasmine" width="33" height="33" title="Jasmine" loading="lazy">
</a>
</li>
<li>
<a href="https://www.lambdatest.com/support/docs/trello-integration/">
<img src="https://www.lambdatest.com/resources/images/header/intergration-window.webp" alt="Trello" width="28" height="28" title="Trello" loading="lazy">
</a>
</li>
</ul>
</div>
</div>
</div>
</div>
<div class="col-xs-12 header_col" style="background: #fdfbf4; border-top: 1px solid #fdfbf4; border-bottom: 1px solid #fdfbf4;">
<div class="table__main">
<div class="header__bottom">
<ul class="product_logo platform_header_bottom">
<li class="automation_tool">Automation tools</li>
<li>
<a href="https://www.lambdatest.com/selenium-automation">
<img src="https://www.lambdatest.com/resources/images/header/selenium_logo_square_green.png" alt="selenium" width="31" height="33" title="Selenium" loading="lazy">
</a>
</li>
<li>
<a href="https://www.lambdatest.com/cypress-testing">
<img src="https://www.lambdatest.com/resources/images/header/Cypress.png" alt="Cypress" width="74" height="25" title="Cypress" loading="lazy">
</a>
</li>
<li>
<a href="https://www.lambdatest.com/support/docs/npm-plugin-for-testcafe-integration-with-lambdatest/">
<img src="https://www.lambdatest.com/resources/images/header/testcafe.png" alt="testcafe" width="100" height="19" title="TestCafe" loading="lazy">
</a>
</li>
<li>
<a href="https://www.lambdatest.com/playwright-testing">
<img loading="lazy" src="https://www.lambdatest.com/resources/images/header/Playwright_logo.svg" alt="Playwright" width="155" height="30" title="Playwright"></a>
</li>
<li>
<a href="https://www.lambdatest.com/puppeteer-testing"><img loading="lazy" src="https://www.lambdatest.com/resources/images/header/puppteer-icon.png" alt="Puppeteer" width="226" height="84" style="width:120px!important; height:auto!important;" title="Puppeteer"></a>
</li>
<li>
<a href="https://www.lambdatest.com/appium-mobile-testing">
<img src="https://www.lambdatest.com/resources/images/header/Appium-logo.png" alt="Appium" width="98" height="25" title="Appium" loading="lazy">
</a>
</li>
<li>
<a href="https://www.lambdatest.com/xcuitest-app-testing"><img loading="lazy" src="https://www.lambdatest.com/resources/images/header/XCUITest.svg" alt="XCUITest Testing" width="347" height="100" style="width:140px!important; height:auto!important;" title="XCUITest Testing"></a>
</li>
<li>
<a href="https://www.lambdatest.com/espresso-automation-testing"><img loading="lazy" src="https://www.lambdatest.com/resources/images/header/espresso.svg" alt="Espresso" width="347" height="100" style="width:140px!important; height:auto!important;" title="Espresso"></a>
</li>
</ul>
</div>
</div>
</div>
</div>
</div>
<a class="item_hover item_link" href="https://www.lambdatest.com/enterprise">Enterprise</a>
<div class="dropdown rs-dropdown dropdown_blog item_link">
<span class="dropdown-toggle" data-toggle="dropdown">Resources<i class="arrow down"></i></span>
<div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
<div class="table__main">
<div class="col-sm-12 col-xs-12 header_col">
<div class="col-sm-8 col-xs-12 header_inner_col">
<div class="row">
<div class="col-sm-6 col-xs-12 header_col">
<div class="dropdown_header">
<h2 class="header_heading">LEARN</h2>
<ul class="header-icon">
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/blog">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header-blog.svg" alt="Lambdatest Blog" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Blog</h3>
<p> Blogs on Selenium automation testing, CI/CD, and more</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/webinar/">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header-webinar.svg" alt="Lambdatest Webinar" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Webinars</h3>
<p>Live virtual workshops around test automation</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/learning-hub/">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/hub.svg" alt="Lambdatest LearningHub" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Learning Hub</h3>
<p>End-to-end guides on Selenium, cross browser testing, CI/CD, and more</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/video/">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header-video-logo.svg" alt="Lambdatest Videos" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Videos</h3>
<p> Video tutorials around automation testing and LambdaTest</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/customers/">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/study.svg" alt="Lambdatest Case Studies" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Customer Stories</h3>
<p> Read the success stories of industry leaders</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/community">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header-community.svg" alt="Lambdatest Community &amp; Support" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3> Community &amp; Support</h3>
<p> Learn about our programs and get support</p>
</div>
</div>
</a>
</li>
</ul>
</div>
</div>
<div class="col-sm-6 col-xs-12 header_col">
<div class="dropdown_header">
<h2 class="header_heading">ENGAGE</h2>
<ul class="header-icon">
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/support">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/LambdaTest-Documentation.svg" alt="Lambdatest Documentation" width="20" height="20" loading="lazy">
</div>
<div class="content_items">
<h3>Documentation</h3>
<p>Step-by-step guides to get started with LambdaTest</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/support/api-doc/">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/api.svg" alt="Lambdatest API" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>API</h3>
<p>Extract, delete &amp; modify data in bulk using LambdaTest API</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/newsletter/">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header-newsletter-logo.svg" alt="Lambdatest Newsletter" width="26" height="26" loading="lazy">
</div>
<div class="content_items">
<h3>Newsletter</h3>
<p>Testing insights and tips delivered weekly</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://community.lambdatest.com/" rel="noopener noreferrer">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header-community.svg" alt="Lambdatest Community" width="22" height="22" loading="lazy">
</div>
<div class="content_items">
<h3>Community</h3>
<p>Connect, ask &amp; learn with tech-savvy folks</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/certifications/">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header-certificate.svg" alt="Lambdatest Certifications" width="22" height="22" loading="lazy">
</div>
<div class="content_items">
<h3>Certifications</h3>
<p> Advance your career with LambdaTest Certifications</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/lambdatest-write-for-us">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/WriteusIcon.svg" alt="Lambdatest write for us" width="22" height="22" loading="lazy">
</div>
<div class="content_items">
<h3> Write for Us</h3>
<p> Join the guest blogger program to share insights</p>
</div>
</div>
</a>
</li>
</ul>
</div>
</div>
</div>
</div>
<div class="col-sm-4 col-xs-12 header_col">
<div class="platform_tool resources_bottom">
<div class="tool_section">
<h3>WHAT’S NEW</h3>
</div>
<div class="header_blog_section" style="margin-top:20px;">
<a href="https://www.lambdatest.com/webinar/clean-coding-practices-for-test-automation">
<img src="https://www.lambdatest.com/resources/images/webinar/webinar_cta.png" alt="LambdaTest Webinar" width="336" height="280" style="width:100%;height:auto;" loading="lazy">
</a>
<a href="https://www.lambdatest.com/webinar/clean-coding-practices-for-test-automation">Clean Coding Practices for Test Automation</a>
<p>This Programmers' Day, LambdaTest invites you to a 1-hour live workshop with Srinivasan Sekar, Lead Consultant, ThoughtWorks on 'Clean Coding Practices for Test Automation'.</p>
<a href="https://www.lambdatest.com/webinar/clean-coding-practices-for-test-automation" style="color:#0ebac5!important;">Resgister Now
<img loading="lazy" src="https://www.lambdatest.com/resources/images/slider/arrow.svg" class="ml-10 w-16 h-16" alt="Arrow" width="16" height="16"></a>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
<div class="dropdown rs-dropdown dropdown_blog item_link">
<span class="dropdown-toggle" data-toggle="dropdown">Developers <i class="arrow down"></i></span>
<div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
<div class="table__main">
<div class="col-sm-12 col-xs-12 header_col">
<div class="col-sm-8 col-xs-12 header_inner_col">
<div class="row">
<div class="col-sm-6 col-xs-12 header_col">
<div class="dropdown_header">
<h2 class="header_heading">GET STARTED</h2>
<ul class="header-icon">
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/support/docs/getting-started-with-lambdatest-automation/">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/selenium.svg" alt="Selenium" width="28" height="25" loading="lazy">
</div>
<div class="content_items">
<h3>Selenium</h3>
<p>Run first Selenium test on LambdaTest Grid</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/support/docs/getting-started-with-cypress-testing/">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header_cypress.svg" alt="Lambdatest Cypress" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Cypress</h3>
<p>Run first Cypress test on LambdaTest Grid</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/support/docs/mobile-web-automation-on-real-devices/">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/Mobile-App-Testing.svg" alt="Lambdatest Mobile App Testing" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3> Mobile App Testing</h3>
<p>Test native apps on 50+ devices </p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/support/docs/real-time-browser-testing/">
<div class="dropdown-item-content">
<div>
<img src="https://www.lambdatest.com/resources/images/header/RealTime-web-testing.svg" alt="Lambdatest Real Time Web Testing" width="22" height="22" loading="lazy">
</div>
<div class="content_items">
<h3>Real Time Web Testing</h3>
<p> Test websites or web apps on 3000+ browsers</p>
</div>
</div>
</a>
</li>
</ul>
</div>
</div>
<div class="col-sm-6 col-xs-12 header_col">
<div class="dropdown_header">
<h2 class="header_heading">GUIDES</h2>
<ul class="header-icon">
<li class="">
<a class="item_hover" href="https://changelog.lambdatest.com/">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/Lambda-Changelog.svg" alt="Changelog" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>Changelog</h3>
<p> All LambdaTest announcements</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/support">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/LambdaTest-Documentation.svg" alt="Lambdatest Documentation" width="20" height="20" loading="lazy">
</div>
<div class="content_items">
<h3>Documentation</h3>
<p>Step-by-step guides to get started with LambdaTest</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://www.lambdatest.com/support/api-doc/">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/api.svg" alt="Lambdatest API" width="24" height="24" loading="lazy">
</div>
<div class="content_items">
<h3>API</h3>
<p>Extract, delete &amp; modify data in bulk using LambdaTest API</p>
</div>
</div>
</a>
</li>
<li class="">
<a class="item_hover" href="https://github.com/LambdaTest">
<div class="dropdown-item-content ">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header_github.svg" alt="LambdaTest GitHub" width="22" height="22" loading="lazy">
</div>
<div class="content_items">
<h3>GitHub Repositories <img src="https://www.lambdatest.com/resources/images/slider/arrow.svg" class="gitrepo_img" alt="Arrow" width="16" height="16" style="margin-left:10px;"></h3>
<p> Check GitHub repos for ready-to-run code</p>
</div>
</div>
</a>
</li>
</ul>
</div>
</div>
</div>
</div>
<div class="col-sm-4 col-xs-12 header_col">
<div class="platform_tool">
<div class="tool_section border_line">
<h3>LANGUAGES &amp; FRAMEWORKS</h3>
</div>
<div id="frameworks_section" class="frameworks_line">
<div id="frameworks_logo_main" class="hover-framework">
<div>
<a href="https://www.lambdatest.com/support/docs/selenide-tests-with-lambdatest-online-selenium-grid-for-automated-cross-browser-testing/">
<img src="https://www.lambdatest.com/resources/images/header/selenide-logo.png" alt="selenide" width="55" height="29" title="Selenide" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/running-gauge-tests-on-lambdatest-selenium-grid/" class="mr-20">
<img src="https://www.lambdatest.com/resources/images/header/Gauge-Logo.svg" alt="Gauge" width="62" height="18" title="Gauge" class="framework_icon" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/testng-with-selenium-running-java-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/testng.png" alt="testng" width="42" height="22" title="TestNG" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/run-geb-tests-on-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/g23.png" alt="geb" width="43" height="14" title="Geb" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/junit-with-selenium-running-junit-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/junit.png" alt="junit" width="33" height="33" title="JUnit" loading="lazy">
</a>
</div>
</div>
<div id="frameworks_heading">
Java
</div>
</div>
<div id="frameworks_section" class="frameworks_line">
<div id="frameworks_logo_main" class="hover-framework">
<div>
<a href="https://www.lambdatest.com/support/docs/webdriverio-5-6-2-with-selenium-running-automation-scripts-on-lambdatest-selenium-grid/"><img src="https://www.lambdatest.com/resources/images/header/WebDriverIO.png" alt="WebDriverIO" width="25" height="27" title="WebDriverIO" loading="lazy"></a>
<a href="https://www.lambdatest.com/support/docs/nightwatch-with-selenium-running-nightwatch-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/NightwatchJS.png" alt="NightwatchJS" width="28" height="29" title="NightwatchJS" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/automation-testing-with-mocha-and-selenium/">
<img src="https://www.lambdatest.com/resources/images/header/Mocha.png" alt="Mocha" width="33" height="33" title="Mocha" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/jasmine-with-karma-running-jasmine-tests-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/Jasmine.png" alt="Jasmine" width="27" height="27" title="Jasmine" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/npm-plugin-for-testcafe-integration-with-lambdatest/">
<img src="https://www.lambdatest.com/resources/images/header/testcafe.png" alt="testcafe" width="70" height="14" title="TestCafe" loading="lazy">
</a>
</div>
</div>
<div id="frameworks_heading">
Node.js
</div>
</div>
<div id="frameworks_section" class="frameworks_line">
<div id="frameworks_logo_main" class="hover-framework">
<div>
<a href="https://www.lambdatest.com/support/docs/specflow-with-selenium-running-specflow-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/SpecFlow.png" alt="SpecFlow" width="75" height="25" title="SpecFlow" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/mstest-with-selenium-running-mstest-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/MSTest.png" alt="MSTest" width="37" height="32" title="MSTest" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/nunit-with-selenium-running-nunit-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/NUnit.png" alt="NUnit" width="47" height="25" title="NUnit" loading="lazy">
</a>
</div>
</div>
<div id="frameworks_heading" class="text-size-14 font-medium text-ltBlack-300 tracking-wide leading-normal">C#</div>
</div>
<div id="frameworks_section" class="frameworks_line">
<div id="frameworks_logo_main" class="hover-framework">
<div>
<a href="https://www.lambdatest.com/support/docs/laravel-dusk-with-selenium-running-laravel-dusk-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/laravel.png" alt="laravel" width="30" height="26" title="Laravel" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/codeception-integration-with-lambdatest/">
<img src="https://www.lambdatest.com/resources/images/header/Codeception.png" alt="Codeception" width="30" height="30" title="Codeception" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/phpunit-with-selenium-running-phpunit-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/PHPUnit.png" alt="PHPUnit" width="54" height="21" title="PHPUnit" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/behat-with-selenium-running-behat-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/Behat.png" class="framework_icon" alt="Behat" width="49" height="15" title="Behat" loading="lazy">
</a>
</div>
</div>
<div id="frameworks_heading" class="text-size-14 font-medium text-ltBlack-300 tracking-wide leading-normal">PHP</div>
</div>
<div id="frameworks_section" class="frameworks_line">
<div id="frameworks_logo_main" class="hover-framework">
<div>
<a href="https://www.lambdatest.com/support/docs/pytest-with-selenium-running-pytest-automation-script-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/pytest.png" alt="pytest" width="25" height="25" title="Pytest" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/behave-with-selenium-running-behave-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/Behave.png" alt="Behave" width="31" height="29" title="Behave" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/robot-with-selenium-running-robot-automation-scripts-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/Robot.png" alt="Robot" width="25" height="24" title="Robot" class="framework_icon" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/running-unit-testing-in-python-on-lambdatest-selenium-grid/">
<img src="https://www.lambdatest.com/resources/images/header/unitTest.png" alt="unitTest" width="21" height="31" title="Unittest" loading="lazy">
</a>
</div>
</div>
<div id="frameworks_heading" class="text-size-14 font-medium text-ltBlack-300 tracking-wide leading-normal">Python</div>
</div>
<div id="frameworks_section" class="frameworks_line">
<div id="frameworks_logo_main" class="hover-framework">
<div class="flex items-center">
<a href="https://www.lambdatest.com/support/docs/rspec-with-selenium-running-rspec-automation-scripts-on-lambdatest-selenium-grid/" class="mr-20">
<img src="https://www.lambdatest.com/resources/images/header/RSpec.png" alt="RSpec" width="29" height="29" title="RSpec" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/cucumberjs-with-selenium-running-cucumberjs-automation-scripts-on-lambdatest-selenium-grid/" class="mr-20">
<img src="https://www.lambdatest.com/resources/images/header/Cucumber.png" alt="Cucumber" width="93" height="30" title="Cucumber" loading="lazy">
</a>
<a href="https://www.lambdatest.com/support/docs/testunit-with-selenium-running-testunit-automation-scripts-on-lambdatest-selenium-grid/" class="mr-20">
<img src="https://www.lambdatest.com/resources/images/header/TestUnit.png" alt="TestUnit" width="33" height="33" title="Test::Unit" loading="lazy">
</a>
</div>
</div>
<div id="frameworks_heading" class="text-size-14 font-medium text-ltBlack-300 tracking-wide leading-normal">Ruby</div>
</div>
<div class="frameworks_all" style="margin-top:20px;">
<a href="https://www.lambdatest.com/support/docs/getting-started-with-lambdatest-automation/">See all
<img src="https://www.lambdatest.com/resources/images/slider/arrow.svg" style="margin-left:10px" alt="Arrow" width="16" height="16" loading="lazy">
</a>
</div>
</div>
</div>
</div>
</div>
<div class="col-xs-12 header_col" style="background: #f4fdf4!important;border-top: 1px solid #f4fdf4!important; border-bottom: 1px solid #f4fdf4!important;">
<div class="table__main">
<div class="header__bottom">
<ul class="product_logo developer_logo">
<li>
<a href="https://www.lambdatest.com/support/faq/">
<div class="developer_items">
<div>
<img src="https://www.lambdatest.com/resources/images/header/Logo_FAQ.svg" alt="Lambdatest FAQs" width="24" height="24" loading="lazy">
</div>
<div class="developer_items_content">
<h3>FAQs</h3>
</div>
</div>
</a>
</li>
<li>
<a href="https://www.lambdatest.com/selenium">
<div class="developer_items">
<div>
<img src="https://www.lambdatest.com/resources/images/header/selenium_black_logo.svg" alt="Selenium" width="24" height="24" loading="lazy">
</div>
<div class="developer_items_content">
<h3>Selenium Guide</h3>
</div>
</div>
</a>
</li>
<li>
<a href="https://www.lambdatest.com/blog/category/cypress-testing/">
<div class="developer_items">
<div>
<img src="https://www.lambdatest.com/resources/images/header/header_cypress.svg" alt="Lambdatest Cypress" width="24" height="24" style="filter: brightness(0);" loading="lazy">
</div>
<div class="developer_items_content">
<h3> Cypress Guide</h3>
</div>
</div>
</a>
</li>
<li class="browser_testing">
<a href="https://www.lambdatest.com/web-technologies">
<div class="developer_items">
<div>
<img src="https://www.lambdatest.com/resources/images/header/browsers.svg" alt="Lambdatest Cross Browser Testing" width="24" height="24" loading="lazy">
</div>
<div class="developer_items_content">
<h3>Web Technologies Compatibility</h3>
</div>
</div>
</a>
</li>
<li class="browser_testing">
<a href="https://www.lambdatest.com/automation-testing-advisor">
<div class="developer_items">
<div>
<img src="https://www.lambdatest.com/resources/images/header/browsers.svg" alt="Lambdatest Cross Browser Testing" width="24" height="24" loading="lazy">
</div>
<div class="developer_items_content">
<h3>Automation Testing Advisor</h3>
</div>
</div>
</a>
</li>
</ul>
</div>
</div>
</div>
</div>
</div>
<a class="item_hover item_link" href="https://www.lambdatest.com/pricing">Pricing</a>
</div>
</div>
<ul class="nav navbar-nav navbar-right navbar_right_blog">
<li class="header_login"><a href="https://accounts.lambdatest.com/login" onclick="if (!window.__cfRLUnblockHandlers) return false; onLogin()" data-cf-modified-807212fb32e79fd549d9754a-="">Login</a></li>
<li class="header_demo_btn"><a href="https://www.lambdatest.com/demo" onclick="if (!window.__cfRLUnblockHandlers) return false; onDemo()" data-cf-modified-807212fb32e79fd549d9754a-="">Book A Demo</a></li>
<li class="login"><a style="background: #000000; font-weight: 700;" href="https://accounts.lambdatest.com/register" onclick="if (!window.__cfRLUnblockHandlers) return false; onStartTesting()" data-cf-modified-807212fb32e79fd549d9754a-="">Sign Up</a></li>
</ul>
</div>
</div>
</nav>
</header>
<section class="blog-sec">
<section>
<div class="container">
<div id="primary" class="content-area">
<div id="content" class="site-content" role="main">
<div class="col-md-10" style="margin:auto; float:initial;">
<button class="back_blogbtn" style="color:#000;background:none!important; border:none;" onclick="if (!window.__cfRLUnblockHandlers) return false; handleBackToblog()" data-cf-modified-807212fb32e79fd549d9754a-="">&#9001; Back To Blog</button>
<div class="top-sect">
<div>
<h2>Continuous Test Orchestration And Execution Platform Online</h2>
<p>Perform automated and live-interactive testing on 3000+ real desktop and mobile devices online.</p>
</div>
<div class="top-sect-content">
<a href="https://accounts.lambdatest.com/register" class="top-sect-anch" onclick="if (!window.__cfRLUnblockHandlers) return false; handleSignupCta()" data-cf-modified-807212fb32e79fd549d9754a-="">Start Free Testing</a>
<a href="https://www.lambdatest.com/demo" class="top-demo-anch" onclick="if (!window.__cfRLUnblockHandlers) return false; handleBookDemoCta()" data-cf-modified-807212fb32e79fd549d9754a-="">Book a Demo</a>
</div>
</div>
<div style="margin-top:20px;">
<p style="display:inline-block;font-weight: 500;font-size: 14px;line-height: 15px;border-radius: 4px;text-align: center;color: #0EBAC5;" class="category_name_blog">
• <a href='https://www.lambdatest.com/blog/category/mobile-application-testing/'>Mobile App Testing</a> </p>
</div>
</div>
<div class="col-md-12 blog-padd0 sigl-page">
<div class="col-md-1 col-sm-1 col-xs-12 csi__blog">
<div class="social-list divsect custom__social__icons">
<div class="addtoany_shortcode"><div class="a2a_kit a2a_kit_size_26 addtoany_list" data-a2a-url="https://www.lambdatest.com/blog/locators-in-appium/" data-a2a-title="How To Identify Locators In Appium [With Examples]"><a class="a2a_button_facebook" href="https://www.addtoany.com/add_to/facebook?linkurl=https%3A%2F%2Fwww.lambdatest.com%2Fblog%2Flocators-in-appium%2F&amp;linkname=How%20To%20Identify%20Locators%20In%20Appium%20%5BWith%20Examples%5D" title="Facebook" rel="nofollow noopener" target="_blank"></a><a class="a2a_button_twitter" href="https://www.addtoany.com/add_to/twitter?linkurl=https%3A%2F%2Fwww.lambdatest.com%2Fblog%2Flocators-in-appium%2F&amp;linkname=How%20To%20Identify%20Locators%20In%20Appium%20%5BWith%20Examples%5D" title="Twitter" rel="nofollow noopener" target="_blank"></a><a class="a2a_button_linkedin" href="https://www.addtoany.com/add_to/linkedin?linkurl=https%3A%2F%2Fwww.lambdatest.com%2Fblog%2Flocators-in-appium%2F&amp;linkname=How%20To%20Identify%20Locators%20In%20Appium%20%5BWith%20Examples%5D" title="LinkedIn" rel="nofollow noopener" target="_blank"></a></div></div> </div>
</div>
<div class="col-lg-7 col-sm-11 col-xs-12">
<div>
<h1 class="detail-titel" style="font-size:48px;font-weight: 700;line-height: 55px;color: #000000;margin-bottom:30px;">How To Identify Locators In Appium [With Examples]</h1>
<div style="display:flex; align-items: center; justify-content:space-between; margin-bottom:40px;" class="inner_blog_top_auth">
<div style="display:flex; align-items: center;">
<div class="header_author">
<a href="https://www.lambdatest.com/blog/author/wasiqbhamla/"><img alt='' src='https://secure.gravatar.com/avatar/ae57536f69729f511f5b0f9f8879dd57?s=60&#038;d=mm&#038;r=r' srcset='https://secure.gravatar.com/avatar/ae57536f69729f511f5b0f9f8879dd57?s=120&#038;d=mm&#038;r=r 2x' class='avatar avatar-60 photo' height='60' width='60' /></a></div>
<div>
<h3 style="font-weight: 600;font-size: 16px;line-height: 26px;color: #10375C;margin:0; padding-left:0px;">Wasiq Bhamla</h3>
<p style="font-weight: 400;font-size: 14px;line-height: 26px;color: #10375C;margin:0;">Posted On: September 9, 2022</p>
</div>
</div>
<div>
<p style="font-weight: 500;font-size: 14px;line-height: 26px;color: #10375C;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-view-count.png" width="21" height="21" alt="view count" style="height:21px!important; margin-right:10px;" />1406 Views </p>
<p style="font-weight: 500;font-size: 14px;line-height: 26px;color: #10375C;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-Clock.png" width="19" height="19" alt="Read time" style="height:19px!important;margin-right:10px;" />19 Min Read
</p>
</div>
</div>
</div>
<div style="border-bottom: 1px solid #EEEFF0;">
<ul id="breadcrumbs" class="breadcrumbs"><li class="item-home"><a class="bread-link bread-home" href="https://www.lambdatest.com/" title="Home">Home</a></li><li class="separator separator-home"> &gt; </li><li class="item-cat"><a href="https://www.lambdatest.com/blog/">Blog</a></li><li class="separator"> &gt; </li><li class="item-current item-35835"><strong class="bread-current bread-35835" title="How To Identify Locators In Appium [With Examples]">How To Identify Locators In Appium [With Examples]</strong></li></ul> </div>
<div class="blog_content" style="margin-top:15px;">
<p><script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [{
    "@type": "Question",
    "name": "What are the locators used in Appium?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "Some of the commonly used locators in Appium include:
-ID.
-Accessibility ID.
-Class Name.
-XPath.
-Android UI Automator (UI Automator 2)
-Android View Tag (Espresso Only)
-iOS UIAutomation"
    }
  },{
    "@type": "Question",
    "name": "How do you inspect locators in Appium?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "As compared to other mobile automation tools, Appium is unique in that it provides the capability to inspect any element on the screen using very simple steps. This helps a lot in identifying the UI elements. The following steps explain how you can inspect your mobile application elements in Appium:
1) Launch your desired app on your local system and then launch the Appium server.
2) Open your browser and open the desired URL of the app (http://127.0.0.1:4723)
3) Now click on the \"Inspect\" button in Advanced Settings (This will open a new window with all the elements on the screen).
4) Now, simply click on the element in the app view and see the DOM/Source in the next panel and the properties on the right side of the selected element. Done!"
    }
  },{
    "@type": "Question",
    "name": "How do I write XPath in Appium?",
    "acceptedAnswer": {
      "@type": "Answer",
      "text": "To create a simple XPath query in Appium, click on the Spy icon button to get the Native/Web properties of all the objects on the screen. Then, right-click on one or more properties and then click on Copy XPath."
    }
  }]
}
</script></p>
<p><script type="application/ld+json">
{
  "@context": "https://schema.org/", 
  "@type": "BreadcrumbList", 
  "itemListElement": [{
    "@type": "ListItem", 
    "position": 1, 
    "name": "Home",
    "item": "https://www.lambdatest.com/"  
  },{
    "@type": "ListItem", 
    "position": 2, 
    "name": "Blog",
    "item": "https://www.lambdatest.com/blog/"  
  },{
    "@type": "ListItem", 
    "position": 3, 
    "name": "How To Identify Locators In Appium? [With Examples]",
    "item": "https://www.lambdatest.com/blog/locators-in-appium/"  
  }]
}
</script></p>
<p>Nowadays, automation is becoming integral to the overall quality of the products being developed. Especially for mobile applications, it&#8217;s even more important to implement automation robustly.<span id="more-35835"></span></p>
<p>As per <a href="https://www.statista.com/statistics/218984/number-of-global-mobile-users-since-2010/" target="_blank" rel="nofollow noopener">Statista</a>, the number of mobile users is likely to be 7.26 billion by 2022 and will increase up to 7.46 billion by 2025. This indicates how mobile applications will grow in the coming years, making <a href="https://www.lambdatest.com/learning-hub/mobile-app-testing" target="_blank">mobile app testing</a> extremely important.</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Statista-1-1-1-1.png" alt="Statista " width="825" height="534" class="aligncenter size-full wp-image-35843" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Statista-1-1-1-1.png 825w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Statista-1-1-1-1-200x129.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Statista-1-1-1-1-300x194.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Statista-1-1-1-1-768x497.png 768w" sizes="(max-width: 825px) 100vw, 825px" /></p>
<p>There are many <a href="https://www.lambdatest.com/blog/best-mobile-app-testing-framework/" target="_blank">mobile testing frameworks</a> available for performing <a href="https://www.lambdatest.com/mobile-automation-test" target="_blank">mobile automation tests</a>, but in this <a href="https://www.lambdatest.com/blog/appium-tutorial/" target="_blank">Appium testing tutorial</a>, we will focus on the Appium automation tool to automate Android and iOS applications. To learn more about mobile automation, you can refer to my earlier blog on <a href="https://www.lambdatest.com/blog/appium-with-testng-tutorial/" target="_blank">Appium with TestNG</a> to perform <a href="https://www.lambdatest.com/android-automation-testing" target="_blank">Android automation testing</a> and <a href="https://www.lambdatest.com/ios-automation-testing" target="_blank">iOS automation testing</a>. </p>
<p>In my experience, I have seen many Test engineers, whether newbies or experienced, using XPaths blindly, which later resulted in flaky tests. Thus, to make automation robust, it’s important to understand which locator strategies are supported in Appium and what locator strategy is ideal for better automation performance.</p>
<p>By the end of this tutorial on using locators in <a href="https://www.lambdatest.com/appium-mobile-testing" target="_blank">Appium testing</a>, you’ll learn about:</p>
<ul>
<li>Common locator strategies are provided by Appium.</li>
<li>Android-specific locator strategies when the Automation name is UIAutomator2.</li>
<li>Android-specific locator strategies when the Automation name is Espresso.</li>
<li>iOS-specific locator strategies.</li>
</ul>
<p>The code snippets and examples used in this blog on locators in Appium are available on <a href="https://github.com/WasiqB/appium-locator-sample" target="_blank" rel="nofollow noopener">GitHub</a>. You can clone the repository and follow along.</p>
<p>We will be using the Proverbial app for <a href="https://prod-mobile-artefacts.lambdatest.com/assets/docs/proverbial_android.apk" target="_blank" rel="nofollow noopener">Android</a> and <a href="https://prod-mobile-artefacts.lambdatest.com/assets/docs/proverbial_ios.ipa" target="_blank" rel="nofollow noopener">iOS</a> for most of the locator strategies while we will use the <a href="https://github.com/appium/android-apidemos/releases/download/v3.1.0/ApiDemos-debug.apk" target="_blank" rel="nofollow noopener">API-demo Android</a> app for the <code>UIAutomator -> UiScrollable</code> locator and Espresso-specific <code>Data Matcher</code> and <code>View Matcher</code> locator strategies.</p>
<div class="border-box">
<p><strong>TABLE OF CONTENTS</strong></p>
<ul>
<li><a class="hashSmoothScroll" href="#a">Strategies to use locators in Appium</a></li>
<li><a class="hashSmoothScroll" href="#b">ID locator in Appium</a></li>
<li><a class="hashSmoothScroll" href="#c">Accessibility ID locator in Appium</a></li>
<li><a class="hashSmoothScroll" href="#d">Class Name locator in Appium</a></li>
<li><a class="hashSmoothScroll" href="#e">XPath locator in Appium</a></li>
<li><a class="hashSmoothScroll" href="#f">Strategies to use Android-specific locators in Appium</a></li>
<li><a class="hashSmoothScroll" href="#g">Strategies to use iOS-specific locators in Appium</a></li>
<li><a class="hashSmoothScroll" href="#h">Demo: Using Locators in Appium</a></li>
<li><a class="hashSmoothScroll" href="#i">Frequently Asked Questions (FAQs)</a></li>
</ul>
</div>
<h2>Strategies to use locators in Appium </h2>
<p>In <a href="https://www.lambdatest.com/appium" target="_blank">Appium</a>, there are some locator strategies that you can use for Android and iOS platforms. These strategies are very straightforward and almost identical to <a href="https://www.lambdatest.com/learning-hub/selenium-locators" target="_blank">Selenium locators</a>, which we are already used to; thus, all these locators are very easy to use.</p>
<p>Let’s look at all the common strategies to use locators in Appium:</p>
<div id="BottomCTA"></div>
<h2>ID locator in Appium</h2>
<p>The first common locator that Appium supports is <code>ID.</code> The <code>ID</code> is the <code>resource-id</code> defined in the Android app, while in iOS, it’s the <code>name</code> property for the element.</p>
<p>While using Java, we can use this locator in Appium as shown below:</p>
<p></p>
<div id="crayon-631f0bbf6cfbd417740781" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import io.appium.java_client.MobileBy;
import org.openqa.selenium.By;
. . .
private final By colorById = MobileBy.id ("color");</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfbd417740781-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfbd417740781-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfbd417740781-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfbd417740781-4">4</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfbd417740781-1"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfbd417740781-2"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfbd417740781-3"><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfbd417740781-4"><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorById</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">id</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"color"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p><a href="https://www.lambdatest.com/blog/appium-inspector-for-apps/" target="_blank">Appium Inspector</a> also suggests using <code>ID</code> if it is declared for the element. The same is shown below:</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1.png" alt="Appium Inspector " width="1600" height="1048" class="aligncenter size-full wp-image-35845" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1.png 1600w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1-200x131.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1-300x197.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1-768x503.png 768w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1-1024x671.png 1024w" sizes="(max-width: 1600px) 100vw, 1600px" /></p>
<p>ID locator and Accessibility ID locator are very similar, making finding the element easy due to its uniqueness. If these IDs are set for the locator, then you should always prefer using this locator in Appium over other strategies to use locators in Appium. It is preferred to use an ID locator in Appium because it makes the element unique and results in finding the element much more quicker.</p>
<p>Normally the format of the ID locator for the Android platform is <code>< package-name >:id/< id-name >.</code> So while finding the element, you can use the whole text or only the <code>< id-name >.</code> In the example screenshot, you can either use <code>com.lambdatest.proverbial:id/geoLocation</code> or simply <code>geoLocation</code>.</p>
<h2>Accessibility ID locator in Appium</h2>
<p>This is also the most preferred strategy after the <code>ID</code> locator in Appium. Accessibility ID for Android is the <code>content-desc</code> property of the element, while in iOS, it’s the <code>accessibility-id</code> property. It is also one of the fastest performing locator strategies.</p>
<p>While using Java, we can use this locator in Appium as shown below:</p>
<p></p>
<div id="crayon-631f0bbf6cfc2195465848" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import io.appium.java_client.MobileBy;
import org.openqa.selenium.By;
. . .
private final By colorByAccessibilityId = MobileBy.AccessibilityId ("color");</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfc2195465848-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfc2195465848-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfc2195465848-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfc2195465848-4">4</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfc2195465848-1"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfc2195465848-2"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfc2195465848-3"><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfc2195465848-4"><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByAccessibilityId</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">AccessibilityId</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"color"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>Appium Inspector will suggest using <code>Accessibility id</code> if it is defined for the element. The same is shown below:</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Accessibility-ID-locator-in-Appium-1-1-1-1.png" alt="Accessibility ID locator in Appium " width="1600" height="1048" class="aligncenter size-full wp-image-35848" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Accessibility-ID-locator-in-Appium-1-1-1-1.png 1600w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Accessibility-ID-locator-in-Appium-1-1-1-1-200x131.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Accessibility-ID-locator-in-Appium-1-1-1-1-300x197.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Accessibility-ID-locator-in-Appium-1-1-1-1-768x503.png 768w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Accessibility-ID-locator-in-Appium-1-1-1-1-1024x671.png 1024w" sizes="(max-width: 1600px) 100vw, 1600px" /></p>
<p>If you find that in your application under test if there is any element that is not dynamic but still does not have the <code>accessibility id</code> set, nor does it have any <code>ID</code> set, then you should ask your development team to add those attributes. This will help you save so much time that you may have to build other locators in Appium like XPath, UISelector, etc.</p>
<h2>Class Name locator in Appium</h2>
<p>Class name is another common strategy to identify the element in the application. The class is the full name of the <code>XCUI</code> element for iOS, which starts with <code>XCUIElementType</code>, and for Android is the fully qualified name of the element, which normally starts with <code>android.widget.*</code> when you select <code>UIAutomator2</code> as the Automation name in the capability.</p>
<p>While using Java, you can use this locator in Appium as shown below:</p>
<p></p>
<div id="crayon-631f0bbf6cfc4270944688" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import io.appium.java_client.MobileBy;
import org.openqa.selenium.By;
. . .
private final By colorByClassName = MobileBy.className ("android.widget.Button");</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfc4270944688-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfc4270944688-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfc4270944688-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfc4270944688-4">4</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfc4270944688-1"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfc4270944688-2"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfc4270944688-3"><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfc4270944688-4"><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByClassName</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">className</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"android.widget.Button"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>You can find exactly what class name there is for any element in Appium Inspector, as shown below:</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Class-Name-locator-in-Appium-1-1.png" alt="Class Name locator in Appium" width="1600" height="1048" class="aligncenter size-full wp-image-35851" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Class-Name-locator-in-Appium-1-1.png 1600w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Class-Name-locator-in-Appium-1-1-200x131.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Class-Name-locator-in-Appium-1-1-300x197.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Class-Name-locator-in-Appium-1-1-768x503.png 768w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Class-Name-locator-in-Appium-1-1-1024x671.png 1024w" sizes="(max-width: 1600px) 100vw, 1600px" /></p>
<p>Normally, you won’t need the use of the class name unless the element is a dynamic one. There is only one element for that particular class name. Use cases would be many where you can use the <code>class name</code> locator, but it is highly suggested to use <code>ID</code> or <code>accessibility id</code> wherever possible.</p>
<h2>XPath locator in Appium</h2>
<p>XPath scans the whole XML source tree of the application screen. It is the only locator in Appium that is not recommended by the Appium team out of all the locator strategies that Appium supports. The reason is that it has performance issues and is also the slowest performing locator strategy. Normally this locator is still supported when in the rare scenario when all the other locator strategies do not work, we can use XPath to find the element.</p>
<p>While using Java, you can use the XPath locator in Appium as shown below:</p>
<p></p>
<div id="crayon-631f0bbf6cfc6199503445" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import io.appium.java_client.MobileBy;
import org.openqa.selenium.By;
. . .
private final By colorByXpath = MobileBy.xpath (".//android.widget.Button[@text='COLOR']");</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfc6199503445-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfc6199503445-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfc6199503445-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfc6199503445-4">4</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfc6199503445-1"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfc6199503445-2"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfc6199503445-3"><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfc6199503445-4"><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByXpath</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">xpath</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">".//android.widget.Button[@text='COLOR']"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>Appium Inspector also helps you with pre-built XPath expressions, which you can use directly. The same is shown below:</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/XPath-locator-in-Appium-1-1.png" alt="XPath locator in Appium" width="1600" height="1048" class="aligncenter size-full wp-image-35853" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/XPath-locator-in-Appium-1-1.png 1600w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/XPath-locator-in-Appium-1-1-200x131.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/XPath-locator-in-Appium-1-1-300x197.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/XPath-locator-in-Appium-1-1-768x503.png 768w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/XPath-locator-in-Appium-1-1-1024x671.png 1024w" sizes="(max-width: 1600px) 100vw, 1600px" /></p>
<p>It is preferred not to use this locator strategy because even if there is no <code>ID</code> or <code>accessibility id,</code> you can still use other platform-specific locator strategies (which we will look at in some time) to find the element.</p>
<div class="blog_content_signup_cta">
<p> Run Appium test automation across 3000+ real devices and OS. <a href="https://accounts.lambdatest.com/register" target="_blank" rel="noopener">Try LambdaTest Now!</a> </p>
</div>
<h2>Strategies to use Android-specific locators in Appium</h2>
<p>After commonly supported strategies to use locators in Appium, there are few platforms and automation type-specific locator strategies. Let&#8217;s look into the Android-specific locators in Appium in detail.</p>
<h3>UIAutomator2: UIAutomator Selector</h3>
<p>The UIAutomator selector locator in Appium is one of the unique locator strategies where you have to create a Java statement and pass it as the locator text to the method. In this statement, you need to use the <code>UiSelector</code> class to build the Java statement.</p>
<p></p>
<div id="crayon-631f0bbf6cfc7622689774" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
new UiSelector().&lt;method_name&gt;</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfc7622689774-1">1</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfc7622689774-1"><span class="crayon-r">new</span><span class="crayon-h"> </span><span class="crayon-e">UiSelector</span><span class="crayon-sy">(</span><span class="crayon-sy">)</span><span class="crayon-sy">.</span><span class="crayon-o">&lt;</span><span class="crayon-v">method_name</span><span class="crayon-o">&gt;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>Shown below is an example of using this locator in our Java tests:</p>
<p></p>
<div id="crayon-631f0bbf6cfc9551398767" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import io.appium.java_client.MobileBy;
import org.openqa.selenium.By;
. . .
private final By colorByUiSelector = MobileBy.AndroidUIAutomator ("new UiSelector().text(\"COLOR\")");</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfc9551398767-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfc9551398767-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfc9551398767-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfc9551398767-4">4</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfc9551398767-1"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfc9551398767-2"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfc9551398767-3"><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfc9551398767-4"><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByUiSelector</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">AndroidUIAutomator</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"new UiSelector().text(\"COLOR\")"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>Here, we are creating an instance for <code>UiSelector</code> and informing the server that we need to find an element that has the text <code>COLOR</code>.</p>
<p>Some of the frequently used methods in the <code>UiSelector</code> class are as follows:</p>
<ul>
<li><strong><code>checked</code>:</strong> This method takes the expected value for the element to find an element that is checked. Mostly it is used with a checkbox element.</li>
<li><strong><code>className</code>:</strong> This method takes a class name string, which you can find from Appium Inspector.</li>
<li><strong><code>classNameMatches</code>:</strong> This method takes a regex expression to find an element based on its class name.</li>
<li><strong><code>description</code>:</strong> This method takes in the content description attribute for the element, which can be found in Appium Inspector</li>
<li><strong><code>descriptionContains</code>:</strong> This method takes in full or partial content description attributes for the element.</li>
<li><strong><code>descriptionMatches</code>:</strong> This method uses a regex expression to find the element based on its content description.</li>
<li><strong><code>descriptionStartsWith</code>:</strong> This method takes a starting part or full content description to find the element.</li>
<li><strong><code>enabled</code>:</strong> This method takes a boolean value to determine whether it&#8217;s enabled.</li>
<li><strong><code>index</code>:</strong> This method takes the element&#8217;s index from the list of elements.</li>
<li><strong><code>resourceId</code>:</strong> This method takes in the resource id equivalent to the ID locator.</li>
<li><strong><code>resourceIdMatches</code>:</strong> This method takes a regex expression for resource id to find the element based on its resource id.</li>
<li><strong><code>selected</code>:</strong> This method takes a boolean value to find the selected or unselected element.</li>
<li><strong><code>text</code>:</strong> This method takes in a text value to find an element by its text value.</li>
<li><strong><code>textContains</code>:</strong> This method takes a partial text to find an element by its partial text value.</li>
<li><strong><code>textMatches</code>:</strong> This method takes a regex value to find an element.</li>
<li><strong><code>textStartsWith</code>:</strong> This method takes in a text value for an element to find it based on the text starting value.</li>
</ul>
<p>You can verify if your selector is working or not by executing the locator expression in the <code>Search for element</code> window in the Appium Inspector.</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1.png" alt="UIAutomator Selector " width="1392" height="912" class="aligncenter size-full wp-image-35854" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1.png 1392w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1-200x131.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1-300x197.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1-768x503.png 768w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1-1024x671.png 1024w" sizes="(max-width: 1392px) 100vw, 1392px" /></p>
<p>In Appium Inspector, click on the magnifying glass icon and select locator strategy as <code>UIAutomator Selector</code>, create your selector, and click on the <code>Search</code> button. You will see the element once it&#8217;s found on the next screen, as shown below:</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1-1.png" alt="UIAutomator Selector 1 " width="1392" height="912" class="aligncenter size-full wp-image-35855" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1-1.png 1392w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1-1-200x131.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1-1-300x197.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1-1-768x503.png 768w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UIAutomator-Selector-1-1-1-1-1024x671.png 1024w" sizes="(max-width: 1392px) 100vw, 1392px" /></p>
<p>You can also use the <code>UiScrollable</code> class to make the element move into view along with the <code>UiSelector</code> class.</p>
<p>Let&#8217;s check out the <code>UiScrollable</code> example where normal <code>UiSelector</code> cannot find the element not in the viewport, whereas <code>UiScrollable</code> was able to find the element and scroll it into view.</p>
<p></p>
<div id="crayon-631f0bbf6cfca232656694" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import io.appium.java_client.MobileBy;
import org.openqa.selenium.By;
. . .
private final By colorByUiSelector = MobileBy.AndroidUIAutomator ("new UiScrollable(new UiSelector().scrollable(true)).scrollIntoView(new UiSelector().text(\"PathEffects\"))");</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfca232656694-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfca232656694-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfca232656694-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfca232656694-4">4</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfca232656694-1"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfca232656694-2"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfca232656694-3"><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfca232656694-4"><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByUiSelector</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">AndroidUIAutomator</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"new UiScrollable(new UiSelector().scrollable(true)).scrollIntoView(new UiSelector().text(\"PathEffects\"))"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>The above snippet is added as an example here but the same is not there in our demo project.</p>
<p>In Appium Inspector, we can validate that the UiSelector was not able to find the element as shown below:</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UiSelector-1.gif" alt="UiSelector " width="600" height="377" class="aligncenter size-full wp-image-35856" /></p>
<p>However, with UiScrollable, it was able to find and scroll to the element without any problems, the same can be seen below:</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/UiScrollable-1.gif" alt="UiScrollable " width="600" height="377" class="aligncenter size-full wp-image-35857" /></p>
<p>These locator strategies are more useful while finding dynamic elements, which normally is difficult to find using other commonly used locator strategies.</p>
<h3>Espresso: Data Matcher</h3>
<p>In Android, when you want to find any element, only the element visible in the viewport can be found. You cannot find an element at the bottom of the list with 100s of items unless you scroll through the list until you find that element or if you’re using <code>UiScrollable</code> with the <code>UiSelector</code> locator strategy. This is possible when you use <a href="https://www.lambdatest.com/espresso" target="_blank">Espresso</a> as the Automation type in Appium.</p>
<p>In Appium Espresso driver, there is a specific locator strategy that you can use to find the element anywhere in the list, and it does not matter how many items are in that list. That locator strategy is <code>Data Matcher</code>.</p>
<p>Data matcher will only work on elements that are part of a view, a subtype of <code>AdapterViews</code>, for example, <code>ScrollView,</code> <code>ListView,</code> and <code>GridView.</code> If you were to use native Espresso directly to find that element, then you would write something like shown below:</p>
<p></p>
<div id="crayon-631f0bbf6cfce330172156" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
onData (hasEntry ("title", "App")
 .inAdapterView (withId ("android:id/list"))
 .perform (click ());</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfce330172156-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfce330172156-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfce330172156-3">3</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfce330172156-1"><span class="crayon-e">onData</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-e">hasEntry</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"title"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"App"</span><span class="crayon-sy">)</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfce330172156-2"><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-e">inAdapterView</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-e">withId</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"android:id/list"</span><span class="crayon-sy">)</span><span class="crayon-sy">)</span></div><div class="crayon-line" id="crayon-631f0bbf6cfce330172156-3"><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-e">perform</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-e">click</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-sy">)</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>In Appium you can write the locator similar to this by using <a href="http://hamcrest.org/JavaHamcrest/javadoc/1.3/org/hamcrest/Matchers.html" target="_blank" rel="nofollow noopener">Hamcrest exposed methods</a> and create JSON string and pass it to the Data matcher locator method. Let’s see how to do this in Java.</p>
<p></p>
<div id="crayon-631f0bbf6cfd0693069827" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import com.google.common.collect.ImmutableList;
import com.google.common.collect.ImmutableMap;
import io.appium.java_client.MobileBy;
import org.openqa.selenium.By;
import org.openqa.selenium.json.Json;
. . .
private final By appItemDataMatcher = MobileBy.androidDataMatcher (new Json ().toJson (ImmutableMap.of (
  "name", "hasEntry",
  "args", ImmutableList.of ("title", "App")
)));</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfd0693069827-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd0693069827-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd0693069827-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd0693069827-4">4</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd0693069827-5">5</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd0693069827-6">6</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd0693069827-7">7</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd0693069827-8">8</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd0693069827-9">9</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd0693069827-10">10</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfd0693069827-1"><span class="crayon-e">import </span><span class="crayon-v">com</span><span class="crayon-sy">.</span><span class="crayon-v">google</span><span class="crayon-sy">.</span><span class="crayon-v">common</span><span class="crayon-sy">.</span><span class="crayon-v">collect</span><span class="crayon-sy">.</span><span class="crayon-v">ImmutableList</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd0693069827-2"><span class="crayon-e">import </span><span class="crayon-v">com</span><span class="crayon-sy">.</span><span class="crayon-v">google</span><span class="crayon-sy">.</span><span class="crayon-v">common</span><span class="crayon-sy">.</span><span class="crayon-v">collect</span><span class="crayon-sy">.</span><span class="crayon-v">ImmutableMap</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd0693069827-3"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd0693069827-4"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd0693069827-5"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">json</span><span class="crayon-sy">.</span><span class="crayon-v">Json</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd0693069827-6"><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd0693069827-7"><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">appItemDataMatcher</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">androidDataMatcher</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-r">new</span><span class="crayon-h"> </span><span class="crayon-e">Json</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-sy">)</span><span class="crayon-sy">.</span><span class="crayon-e">toJson</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-v">ImmutableMap</span><span class="crayon-sy">.</span><span class="crayon-e">of</span><span class="crayon-h"> </span><span class="crayon-sy">(</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd0693069827-8"><span class="crayon-h">&nbsp;&nbsp;</span><span class="crayon-s">"name"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"hasEntry"</span><span class="crayon-sy">,</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd0693069827-9"><span class="crayon-h">&nbsp;&nbsp;</span><span class="crayon-s">"args"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-v">ImmutableList</span><span class="crayon-sy">.</span><span class="crayon-e">of</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"title"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"App"</span><span class="crayon-sy">)</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd0693069827-10"><span class="crayon-sy">)</span><span class="crayon-sy">)</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>If you compare this locator values with the native Espresso expression we used earlier, we are breaking the <code>hasEntry</code> call and creating the JSON string.</p>
<p>Let’s see how you can find the element using the data matcher locator in Appium Inspector.</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/data-matcher-locator-in-Appium-Inspector-1-1-1-1-1.png" alt="data matcher locator in Appium Inspector" width="1392" height="912" class="aligncenter size-full wp-image-35858" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/data-matcher-locator-in-Appium-Inspector-1-1-1-1-1.png 1392w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/data-matcher-locator-in-Appium-Inspector-1-1-1-1-1-200x131.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/data-matcher-locator-in-Appium-Inspector-1-1-1-1-1-300x197.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/data-matcher-locator-in-Appium-Inspector-1-1-1-1-1-768x503.png 768w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/data-matcher-locator-in-Appium-Inspector-1-1-1-1-1-1024x671.png 1024w" sizes="(max-width: 1392px) 100vw, 1392px" /></p>
<p>Since we want to find elements from the list, first, we will select the main listview and get the value from its <code>adapters</code> attribute, as shown in the screenshot above.</p>
<p>Let’s see what value is there in the adapters attribute:</p>
<p><script src="https://gist.github.com/SarahElson/3b8a4fef694fed1843ed8babeeda3937.js" type="807212fb32e79fd549d9754a-text/javascript"></script></p>
<p>Notice the values we used in the Java example for the data matcher locator in Appium for the <code>args</code> field? As mentioned above, we have used the <code>title</code> property, which is part of the <code>adapters</code> attribute. You can use any combination of key/value pairs from these attributes, for example, <code>contentDescription</code> or <code>intent</code> apart from <code>title</code>.</p>
<p><strong>Bonus Tip:</strong></p>
<p>Appium Inspector behaves weirdly when you try to find the element by clicking on it. Instead, you need to find the element from the XML tree. Also, Appium Inspector won’t help provide you with a pre-built locator as it does for other locators in Appium. To ascertain whether the data matcher locator you created works, you can check it by using the <code>Search for element</code> button in the inspector, as shown below.</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Search-for-element-in-appium-inspector-1-1-1.png" alt="Search for element in appium inspector" width="1392" height="912" class="aligncenter size-full wp-image-35860" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Search-for-element-in-appium-inspector-1-1-1.png 1392w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Search-for-element-in-appium-inspector-1-1-1-200x131.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Search-for-element-in-appium-inspector-1-1-1-300x197.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Search-for-element-in-appium-inspector-1-1-1-768x503.png 768w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Search-for-element-in-appium-inspector-1-1-1-1024x671.png 1024w" sizes="(max-width: 1392px) 100vw, 1392px" /></p>
<h2>Espresso: View Matcher</h2>
<p>View matcher locator strategy is very similar to the data matcher strategy, where we create a JSON string and pass it to the locator in Appium. The only difference is we use <a href="https://developer.android.com/reference/androidx/test/espresso/matcher/ViewMatchers" target="_blank" rel="nofollow noopener">ViewMatchers class methods</a> instead of Hamcrest class. Three fields are passed in the JSON string:</p>
<ul>
<li><strong><code>name</code>:</strong> This is the method&#8217;s name.</li>
<li><strong><code>args</code>:</strong> This will have the parameter value for the method.</li>
<li><strong><code>class</code>:</strong> This will have the class name which contains the method. Mostly, it will be <code>androidx.test.espresso.matcher.ViewMatchers.</code></li>
</ul>
<p>While using Java, we can use the View Matcher locator in Appium, as shown below.</p>
<p></p>
<div id="crayon-631f0bbf6cfd2394024578" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import com.google.common.collect.ImmutableMap;
import io.appium.java_client.MobileBy;
import org.openqa.selenium.By;
import org.openqa.selenium.json.Json;
. . .
private final By animationItemViewMatcher = MobileBy.androidViewMatcher (new Json ().toJson (ImmutableMap.of (
  "name", "withText",
  "args", "Animation",
  "class", "androidx.test.espresso.matcher.ViewMatchers"
)));</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfd2394024578-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd2394024578-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd2394024578-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd2394024578-4">4</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd2394024578-5">5</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd2394024578-6">6</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd2394024578-7">7</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd2394024578-8">8</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd2394024578-9">9</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd2394024578-10">10</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfd2394024578-1"><span class="crayon-e">import </span><span class="crayon-v">com</span><span class="crayon-sy">.</span><span class="crayon-v">google</span><span class="crayon-sy">.</span><span class="crayon-v">common</span><span class="crayon-sy">.</span><span class="crayon-v">collect</span><span class="crayon-sy">.</span><span class="crayon-v">ImmutableMap</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd2394024578-2"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd2394024578-3"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd2394024578-4"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">json</span><span class="crayon-sy">.</span><span class="crayon-v">Json</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd2394024578-5"><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd2394024578-6"><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">animationItemViewMatcher</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">androidViewMatcher</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-r">new</span><span class="crayon-h"> </span><span class="crayon-e">Json</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-sy">)</span><span class="crayon-sy">.</span><span class="crayon-e">toJson</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-v">ImmutableMap</span><span class="crayon-sy">.</span><span class="crayon-e">of</span><span class="crayon-h"> </span><span class="crayon-sy">(</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd2394024578-7"><span class="crayon-h">&nbsp;&nbsp;</span><span class="crayon-s">"name"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"withText"</span><span class="crayon-sy">,</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd2394024578-8"><span class="crayon-h">&nbsp;&nbsp;</span><span class="crayon-s">"args"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"Animation"</span><span class="crayon-sy">,</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd2394024578-9"><span class="crayon-h">&nbsp;&nbsp;</span><span class="crayon-s">"class"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"androidx.test.espresso.matcher.ViewMatchers"</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd2394024578-10"><span class="crayon-sy">)</span><span class="crayon-sy">)</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<h2>Strategies to use iOS-specific locators in Appium</h2>
<p>In iOS, there is only one Automation type, <a href="https://www.lambdatest.com/xcuitest" target="_blank">XCUITest</a>, which supports the following strategies to use locators in Appium.</p>
<h3>XCUITest: Predicate String</h3>
<p>Predicate string locator strategy is similar to a SQL query where you query for a particular element using a combination of its attributes.</p>
<p>While using Java, you can use the predicate string locator in Appium, as shown below.</p>
<p></p>
<div id="crayon-631f0bbf6cfd4011251875" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import io.appium.java_client.MobileBy;
import org.openqa.selenium.By;
. . .
private final By colorByPredicate = MobileBy.iOSNsPredicateString ("label == \"Colour\" AND name == \"color\"");</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfd4011251875-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd4011251875-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd4011251875-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd4011251875-4">4</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfd4011251875-1"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd4011251875-2"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd4011251875-3"><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd4011251875-4"><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByPredicate</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">iOSNsPredicateString</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"label == \"Colour\" AND name == \"color\""</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>Appium Inspector also helps in providing a pre-built predicate string which you simply copy and use in your test. Below is the screenshot showing how Appium Inspector shows the pre-built locator in Appium.</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1-1-1.png" alt="Appium Inspector " width="1600" height="1048" class="aligncenter size-full wp-image-35850" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1-1-1.png 1600w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1-1-1-200x131.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1-1-1-300x197.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1-1-1-768x503.png 768w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-1-1-1-1-1024x671.png 1024w" sizes="(max-width: 1600px) 100vw, 1600px" /></p>
<p>While creating the predicate string, you can also use the following comparison expressions,</p>
<p><strong>Basic comparisons:</strong></p>
<ul>
<li><code>=</code>, <code>==</code>: Left-hand expression is equal to right-hand expression.</li>
<li><code>>=</code>, <code>=></code>: Left-hand expression is greater than and equal to right-hand expression.</li>
<li><code><=</code>, <code>=<</code>: Left-hand expression is less than and equal to right-hand expression.</li>
<li><code>></code>: Left-hand expression is greater than right-hand expression.</li>
<li><code><</code>: Left-hand expression is less than right-hand expression.</li>
<li><code>!=</code>, <code><></code>: Left-hand expression is not equal to right-hand expression.</li>
<li> <code>< INPUT > BETWEEN { lower range, upper range }</code>: Left-hand expression value lies between the range mentioned in the right-hand expression, with both the values inclusive.</li>
</ul>
<p><strong>Basic predicates:</strong></p>
<ul>
<li><code>AND</code>, <code>&&</code>: Logical <code>and</code> will check both the connected expressions to be <code>true.</code></li>
<li><code>OR</code>, <code>||</code>: Logical <code>or</code> will check if any of the connected expressions are <code>true.</code> </li>
<li><code>NOT</code>, <code>!</code>: Negating an expression will negate the outcome of the expression with which it is used.</li>
</ul>
<p><strong>String comparisons:</strong></p>
<ul>
<li><code>BEGINSWITH</code>: Checks if the attribute starts with the provided string.</li>
<li><code>CONTAINS</code>: Checks if the attribute contains the provided string.</li>
<li><code>ENDSWITH</code>: Checks if the attribute ends with the provided string.</li>
<li><code>LIKE</code>: Checks if the attribute has the provided string containing wildcards like <code>?</code> and <code>*.</code> Here, <code>?</code> will try to match only one char, while <code>*</code> will try to match 0 or more chars from that position.</li>
<li><code>MATCHES</code>: Checks if the attribute matches the regex string.</li>
</ul>
<h3>XCUITest: Class chain</h3>
<p>Class chain locator in Appium is similar to XPath but more stable than XPath. With Class chains, you can combine predicate strings or directly reference child or descendent indexes to get a particular element.</p>
<p>While using Java, you can use the iOS class chain locator in Appium, as shown below.</p>
<p></p>
<div id="crayon-631f0bbf6cfd6011597221" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import io.appium.java_client.MobileBy;
import org.openqa.selenium.By;
. . .
private final By colorByClassChain = MobileBy.iOSClassChain ("**/XCUIElementTypeButton[`label == \"Colour\"`]");</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfd6011597221-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd6011597221-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd6011597221-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd6011597221-4">4</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfd6011597221-1"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd6011597221-2"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd6011597221-3"><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span><span class="crayon-h"> </span><span class="crayon-sy">.</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd6011597221-4"><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByClassChain</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">iOSClassChain</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"**/XCUIElementTypeButton[`label == \"Colour\"`]"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>Appium Inspector also helps with providing pre-built iOS class chain locator in Appium as shown below,</p>
<p><img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-IOS-Class-1-1-1-1.png" alt="Appium Inspector IOS Class" width="1600" height="1048" class="aligncenter size-full wp-image-35852" srcset="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-IOS-Class-1-1-1-1.png 1600w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-IOS-Class-1-1-1-1-200x131.png 200w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-IOS-Class-1-1-1-1-300x197.png 300w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-IOS-Class-1-1-1-1-768x503.png 768w, https://www.lambdatest.com/blog/wp-content/uploads/2022/09/Appium-Inspector-IOS-Class-1-1-1-1-1024x671.png 1024w" sizes="(max-width: 1600px) 100vw, 1600px" /></p>
<p><strong>Tips when creating a class chain expression:</strong></p>
<ul>
<li>You can chain multiple classes in your expression, e.g.: <code>**/< parent-class >/< target-class ></code></li>
<li>You can use indexes to get a specific element from the list of locators identified with the expression before the index, e.g.: <code>< parent-class >[1]/< target-class >[2]</code>, where the parent class first instance will be used and then target class 2nd instance will be found with this expression.</li>
<ul>
<li>Indexes here start from 1 instead of normally 0 index.</li>
<li>Indexes can also be negative. For example, <code>-1</code> means the last element from the list of elements. Similarly, <code>-2</code> means the second last item.</li>
</ul>
<li>You can also combine predicate string expression with class chains like we use indexes, e.g.: <code><code>< target-class >[</code>name CONTAINS[cd] "text"<code>]</code></code> means it will find the target element where its name contains a particular text irrespective of its casing.</li>
<ul>
<li>Predicate strings should always be enclosed in ticks, as shown in the example.</li>
</ul>
<li>You can also combine index and predicate strings in the same expression at any level of the hierarchy, e.g.:<code> <code>**/< parent-class >[</code>name BEGINSWITH "Some Text"<code>][-1]/< target-class >[3]</code> </code> which will interpret as find the last parent out of the list of parents whose name starts with some text and find the third instance of target element from that parent.</li>
</ul>
<p>If you like XPath more, this locator in Appium is the perfect replacement for XPath but is more stable and one of the best-performing locator strategies. Here also, it is suggested that if you can use <code>ID</code> or <code>Accessibility ID</code> or ask the development team to add these IDs to the element, you should use them instead of the Class chain locator in Appium.</p>
<h2>Demo: Using Locators in Appium</h2>
<p>Until now, we have seen the code snippets. Now let us see the page object and the test we have in the demo project shared on <a href="https://github.com/WasiqB/appium-locator-sample" target="_blank" rel="nofollow noopener">GitHub</a>. You can download and clone the same and follow along.</p>
<h3>DriverManager class</h3>
<p>This class is used to create driver sessions for different Automation types to demonstrate different locators in Appium specific for that particular Automation type.</p>
<p><script src="https://gist.github.com/SarahElson/99e69d95eda952feb5dd097cc3395985.js" type="807212fb32e79fd549d9754a-text/javascript"></script></p>
<p>Here, we have created a few different create-driver methods to create different driver instances for different automation types. Only for the Espresso driver, we have two methods, one for local execution and one for the cloud. This is because most cloud platform providers are not yet supporting the Espresso driver, due to which we will encounter errors like <code>Data matcher locator strategy not implemented</code> or <code>View matcher locator strategy not implemented</code>.</p>
<p>For cloud <a href="https://www.lambdatest.com/learning-hub/test-execution" target="_blank">test execution</a>, we are using the LambdaTest cloud platform, while for local execution, we start and stop the Appium server from this class directly.</p>
<p><a href="https://www.lambdatest.com/blog/cloud-testing-tutorial/" target="_blank">Cloud testing</a> platforms like LambdaTest provide an <a href="https://www.lambdatest.com/online-device-farm" target="_blank">online device farm</a> of 3000+ real devices and operating systems to perform <a href="https://www.lambdatest.com/app-test-automation" target="_blank">app test automation</a> at scale over a cloud Appium grid. You can perform <a href="https://www.lambdatest.com/mobile-automation-test" target="_blank">mobile automation testing</a> on real Android and iOS devices.</p>
<p>Here’s how you can use LambdaTest’s <a href="https://www.lambdatest.com/blog/real-device-cloud/" target="_blank">real device cloud</a> to perform <a href="https://www.lambdatest.com/appium-mobile-testing" target="_blank">Appium mobile testing</a>:</p>
<div class="blog__ytframe">
<div class="blog__youtube" data-embed="_gC5igQyJf8">
<div class="blog__play-button"></div>
</div>
</div>
<p>You can also subscribe to the <a href="https://www.youtube.com/channel/UCCymWVaTozpEng_ep0mdUyw?sub_confirmation=1" target="_blank" rel="noopener">LambdaTest YouTube Channel</a> and stay updated with the latest tutorials around <a href="https://www.lambdatest.com/selenium-automation" target="_blank">Selenium testing</a>, <a href="https://www.lambdatest.com/cypress-testing" target="_blank">Cypress testing</a>, CI/CD, and more.</p>
<h3>Page object</h3>
<p>There is one page object for Android and one for iOS to demonstrate different locators in Appium. First, let's see the <code>AndroidLocators</code> page object.</p>
<p></p>
<div id="crayon-631f0bbf6cfd8801265150" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import com.google.common.collect.ImmutableList;
import com.google.common.collect.ImmutableMap;
import io.appium.java_client.MobileBy;
import lombok.Getter;
import org.openqa.selenium.By;
import org.openqa.selenium.json.Json;
 
@Getter
public class AndroidLocators {
   private final By animationItemViewMatcher = MobileBy.androidViewMatcher (new Json ().toJson (ImmutableMap.of ("name", "withText", "args", "Animation", "class", "androidx.test.espresso.matcher.ViewMatchers")));
   private final By appItemDataMatcher = MobileBy.androidDataMatcher (new Json ().toJson (ImmutableMap.of (
  "name", "hasEntry",
  "args", ImmutableList.of ("title", "App")
)));
   private final By colorByClassName = MobileBy.className ("android.widget.Button");
   private final By colorById = MobileBy.id ("color");
   private final By colorByUiSelector = MobileBy.AndroidUIAutomator ("new UiSelector().text(\"COLOR\")");
   private final By colorByXpath = MobileBy.xpath (".//android.widget.Button[@text='COLOR']");
}</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfd8801265150-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd8801265150-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd8801265150-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd8801265150-4">4</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd8801265150-5">5</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd8801265150-6">6</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd8801265150-7">7</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd8801265150-8">8</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd8801265150-9">9</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd8801265150-10">10</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd8801265150-11">11</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd8801265150-12">12</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd8801265150-13">13</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd8801265150-14">14</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd8801265150-15">15</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd8801265150-16">16</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd8801265150-17">17</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfd8801265150-18">18</div><div class="crayon-num" data-line="crayon-631f0bbf6cfd8801265150-19">19</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfd8801265150-1"><span class="crayon-e">import </span><span class="crayon-v">com</span><span class="crayon-sy">.</span><span class="crayon-v">google</span><span class="crayon-sy">.</span><span class="crayon-v">common</span><span class="crayon-sy">.</span><span class="crayon-v">collect</span><span class="crayon-sy">.</span><span class="crayon-v">ImmutableList</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd8801265150-2"><span class="crayon-e">import </span><span class="crayon-v">com</span><span class="crayon-sy">.</span><span class="crayon-v">google</span><span class="crayon-sy">.</span><span class="crayon-v">common</span><span class="crayon-sy">.</span><span class="crayon-v">collect</span><span class="crayon-sy">.</span><span class="crayon-v">ImmutableMap</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd8801265150-3"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd8801265150-4"><span class="crayon-e">import </span><span class="crayon-v">lombok</span><span class="crayon-sy">.</span><span class="crayon-v">Getter</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd8801265150-5"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd8801265150-6"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">json</span><span class="crayon-sy">.</span><span class="crayon-v">Json</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd8801265150-7"><span class="crayon-h"> </span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd8801265150-8"><span class="crayon-sy">@</span><span class="crayon-e">Getter</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd8801265150-9"><span class="crayon-m">public</span><span class="crayon-h"> </span><span class="crayon-t">class</span><span class="crayon-h"> </span><span class="crayon-e">AndroidLocators</span><span class="crayon-h"> </span><span class="crayon-sy">{</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd8801265150-10"><span class="crayon-h">&nbsp;&nbsp; </span><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">animationItemViewMatcher</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">androidViewMatcher</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-r">new</span><span class="crayon-h"> </span><span class="crayon-e">Json</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-sy">)</span><span class="crayon-sy">.</span><span class="crayon-e">toJson</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-v">ImmutableMap</span><span class="crayon-sy">.</span><span class="crayon-e">of</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"name"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"withText"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"args"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"Animation"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"class"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"androidx.test.espresso.matcher.ViewMatchers"</span><span class="crayon-sy">)</span><span class="crayon-sy">)</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd8801265150-11"><span class="crayon-h">&nbsp;&nbsp; </span><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">appItemDataMatcher</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">androidDataMatcher</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-r">new</span><span class="crayon-h"> </span><span class="crayon-e">Json</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-sy">)</span><span class="crayon-sy">.</span><span class="crayon-e">toJson</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-v">ImmutableMap</span><span class="crayon-sy">.</span><span class="crayon-e">of</span><span class="crayon-h"> </span><span class="crayon-sy">(</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd8801265150-12"><span class="crayon-h">&nbsp;&nbsp;</span><span class="crayon-s">"name"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"hasEntry"</span><span class="crayon-sy">,</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd8801265150-13"><span class="crayon-h">&nbsp;&nbsp;</span><span class="crayon-s">"args"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-v">ImmutableList</span><span class="crayon-sy">.</span><span class="crayon-e">of</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"title"</span><span class="crayon-sy">,</span><span class="crayon-h"> </span><span class="crayon-s">"App"</span><span class="crayon-sy">)</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd8801265150-14"><span class="crayon-sy">)</span><span class="crayon-sy">)</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd8801265150-15"><span class="crayon-h">&nbsp;&nbsp; </span><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByClassName</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">className</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"android.widget.Button"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd8801265150-16"><span class="crayon-h">&nbsp;&nbsp; </span><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorById</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">id</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"color"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd8801265150-17"><span class="crayon-h">&nbsp;&nbsp; </span><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByUiSelector</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">AndroidUIAutomator</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"new UiSelector().text(\"COLOR\")"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfd8801265150-18"><span class="crayon-h">&nbsp;&nbsp; </span><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByXpath</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">xpath</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">".//android.widget.Button[@text='COLOR']"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfd8801265150-19"><span class="crayon-sy">}</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>The class seems very straightforward where we have declared all the Android-specific locators. Now let’s see the <code>IOSLocator</code> page object.</p>
<p></p>
<div id="crayon-631f0bbf6cfdb436811631" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
import io.appium.java_client.MobileBy;
import lombok.Getter;
import org.openqa.selenium.By;
 
@Getter
public class IOSLocators {
   // Demoed with iOS.
   private final By colorByAccessibilityId = MobileBy.AccessibilityId ("color");
   private final By colorByClassChain = MobileBy.iOSClassChain ("**/XCUIElementTypeButton[`label == \"Colour\"`]");
   private final By colorByPredicate = MobileBy.iOSNsPredicateString ("label == \"Colour\" AND name == \"color\"");
}</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfdb436811631-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfdb436811631-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfdb436811631-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfdb436811631-4">4</div><div class="crayon-num" data-line="crayon-631f0bbf6cfdb436811631-5">5</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfdb436811631-6">6</div><div class="crayon-num" data-line="crayon-631f0bbf6cfdb436811631-7">7</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfdb436811631-8">8</div><div class="crayon-num" data-line="crayon-631f0bbf6cfdb436811631-9">9</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfdb436811631-10">10</div><div class="crayon-num" data-line="crayon-631f0bbf6cfdb436811631-11">11</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfdb436811631-1"><span class="crayon-e">import </span><span class="crayon-v">io</span><span class="crayon-sy">.</span><span class="crayon-v">appium</span><span class="crayon-sy">.</span><span class="crayon-v">java_client</span><span class="crayon-sy">.</span><span class="crayon-v">MobileBy</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfdb436811631-2"><span class="crayon-e">import </span><span class="crayon-v">lombok</span><span class="crayon-sy">.</span><span class="crayon-v">Getter</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfdb436811631-3"><span class="crayon-e">import </span><span class="crayon-v">org</span><span class="crayon-sy">.</span><span class="crayon-v">openqa</span><span class="crayon-sy">.</span><span class="crayon-v">selenium</span><span class="crayon-sy">.</span><span class="crayon-v">By</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfdb436811631-4"><span class="crayon-h"> </span></div><div class="crayon-line" id="crayon-631f0bbf6cfdb436811631-5"><span class="crayon-sy">@</span><span class="crayon-e">Getter</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfdb436811631-6"><span class="crayon-m">public</span><span class="crayon-h"> </span><span class="crayon-t">class</span><span class="crayon-h"> </span><span class="crayon-e">IOSLocators</span><span class="crayon-h"> </span><span class="crayon-sy">{</span></div><div class="crayon-line" id="crayon-631f0bbf6cfdb436811631-7"><span class="crayon-h">&nbsp;&nbsp; </span><span class="crayon-c">// Demoed with iOS.</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfdb436811631-8"><span class="crayon-h">&nbsp;&nbsp; </span><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByAccessibilityId</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">AccessibilityId</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"color"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfdb436811631-9"><span class="crayon-h">&nbsp;&nbsp; </span><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByClassChain</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">iOSClassChain</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"**/XCUIElementTypeButton[`label == \"Colour\"`]"</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfdb436811631-10"><span class="crayon-h">&nbsp;&nbsp; </span><span class="crayon-m">private</span><span class="crayon-h"> </span><span class="crayon-m">final</span><span class="crayon-h"> </span><span class="crayon-e">By </span><span class="crayon-v">colorByPredicate</span><span class="crayon-h"> </span><span class="crayon-o">=</span><span class="crayon-h"> </span><span class="crayon-v">MobileBy</span><span class="crayon-sy">.</span><span class="crayon-e">iOSNsPredicateString</span><span class="crayon-h"> </span><span class="crayon-sy">(</span><span class="crayon-s">"label == \"Colour\" AND name == \"color\""</span><span class="crayon-sy">)</span><span class="crayon-sy">;</span></div><div class="crayon-line" id="crayon-631f0bbf6cfdb436811631-11"><span class="crayon-sy">}</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>Here also, we have declared all the iOS specific locators in Appium.</p>
<h3>Test classes</h3>
<h4>BaseTest</h4>
<p>Before writing the tests, we have a common <code>BaseTest</code> class, which will be extended to all of our tests. Let’s see what we have in the Base test.</p>
<p><script src="https://gist.github.com/SarahElson/2a005849a0a4ff2fd09e52190a3a8467.js" type="807212fb32e79fd549d9754a-text/javascript"></script></p>
<p>In this class, we have only two methods, one where we quit the driver session and close the local Appium server if it’s running. At the same time, the other method is used to find the element using the locator strategy passed to this method and also prints the time it took to find the element so we can identify which locator strategy is the fastest and which one is the slowest.</p>
<h4>LocatorsAndroidEspressoTest</h4>
<p>In this class, we will test the locators specific to the <a href="https://www.lambdatest.com/espresso-automation-testing" target="_blank">Espresso automation</a> type. This test will execute on the local Appium server.</p>
<p><script src="https://gist.github.com/SarahElson/98060a8e45c0b0dff619f6487e030bf8.js" type="807212fb32e79fd549d9754a-text/javascript"></script></p>
<p>We have one more similar class which runs on LambdaTest cloud platform. But that class will fail, as mentioned earlier.</p>
<h4>LocatorsAndroidUiAutomatorTest</h4>
<p>In this test, we will test all the locator strategies specific to the <code>UiAutomator2</code> Automation type along with a few common locators in Appium.</p>
<p><script src="https://gist.github.com/SarahElson/09660205b4aaca9af464c5aaa0f8f8f0.js" type="807212fb32e79fd549d9754a-text/javascript"></script></p>
<h4>LocatorsIOSTest</h4>
<p>In this class we will test all the iOS specific locator strategies for <code>XCUITest</code> automation name.</p>
<p><script src="https://gist.github.com/SarahElson/b21f6d4501a9dac5348183ca1da0fc81.js" type="807212fb32e79fd549d9754a-text/javascript"></script></p>
<div class="blog_content_signup_cta">
<p>Test your native apps on XCUITest cloud. <a href="https://accounts.lambdatest.com/register" onclick="if (!window.__cfRLUnblockHandlers) return false; handleContentCta()" target="_blank" rel="noopener" data-cf-modified-807212fb32e79fd549d9754a-="">Try LambdaTest Now!</a></p>
</div>
<h3>Test output</h3>
<p>When you execute all the tests which we saw until now, you’ll see an output something as the one shown below.</p>
<p></p>
<div id="crayon-631f0bbf6cfdd816043977" class="crayon-syntax crayon-theme-classic crayon-font-liberation-mono crayon-os-pc print-yes notranslate" data-settings=" minimize scroll-mouseover" style=" margin-top: 12px; margin-bottom: 12px; font-size: 12px !important; line-height: 15px !important;">
<div class="crayon-toolbar" data-settings=" mouseover overlay hide delay" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><span class="crayon-title"></span>
<div class="crayon-tools" style="font-size: 12px !important;height: 18px !important; line-height: 18px !important;"><div class="crayon-button crayon-nums-button" title="Toggle Line Numbers"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-plain-button" title="Toggle Plain Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-wrap-button" title="Toggle Line Wrap"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-expand-button" title="Expand Code"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-copy-button" title="Copy"><div class="crayon-button-icon"></div></div><div class="crayon-button crayon-popup-button" title="Open Code In New Window"><div class="crayon-button-icon"></div></div></div></div>
<div class="crayon-info" style="min-height: 16.8px !important; line-height: 16.8px !important;"></div>
<div class="crayon-plain-wrap"><textarea wrap="soft" class="crayon-plain print-no" data-settings="dblclick" readonly style="-moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4; font-size: 12px !important; line-height: 15px !important;">
Time taken by View Matcher: 36ms
Time taken by Data Matcher: 209ms
Time taken by Ui Selector: 230ms
Time taken by ID: 251ms
Time taken by Predicate: 266ms
Time taken by Class Chain: 272ms
Time taken by Class Name: 337ms
Time taken by Accessibility Id: 376ms
Time taken by Xpath: 517ms</textarea></div>
<div class="crayon-main" style=" max-height: 500px;">
<table class="crayon-table">
<tr class="crayon-row">
<td class="crayon-nums " data-settings="show">
<div class="crayon-nums-content" style="font-size: 12px !important; line-height: 15px !important;"><div class="crayon-num" data-line="crayon-631f0bbf6cfdd816043977-1">1</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfdd816043977-2">2</div><div class="crayon-num" data-line="crayon-631f0bbf6cfdd816043977-3">3</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfdd816043977-4">4</div><div class="crayon-num" data-line="crayon-631f0bbf6cfdd816043977-5">5</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfdd816043977-6">6</div><div class="crayon-num" data-line="crayon-631f0bbf6cfdd816043977-7">7</div><div class="crayon-num crayon-striped-num" data-line="crayon-631f0bbf6cfdd816043977-8">8</div><div class="crayon-num" data-line="crayon-631f0bbf6cfdd816043977-9">9</div></div>
</td>
<td class="crayon-code"><div class="crayon-pre" style="font-size: 12px !important; line-height: 15px !important; -moz-tab-size:4; -o-tab-size:4; -webkit-tab-size:4; tab-size:4;"><div class="crayon-line" id="crayon-631f0bbf6cfdd816043977-1"><span class="crayon-e">Time </span><span class="crayon-e">taken </span><span class="crayon-e">by </span><span class="crayon-e">View </span><span class="crayon-v">Matcher</span><span class="crayon-o">:</span><span class="crayon-h"> </span><span class="crayon-cn">36ms</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfdd816043977-2"><span class="crayon-e">Time </span><span class="crayon-e">taken </span><span class="crayon-e">by </span><span class="crayon-e">Data </span><span class="crayon-v">Matcher</span><span class="crayon-o">:</span><span class="crayon-h"> </span><span class="crayon-cn">209ms</span></div><div class="crayon-line" id="crayon-631f0bbf6cfdd816043977-3"><span class="crayon-e">Time </span><span class="crayon-e">taken </span><span class="crayon-e">by </span><span class="crayon-e">Ui </span><span class="crayon-v">Selector</span><span class="crayon-o">:</span><span class="crayon-h"> </span><span class="crayon-cn">230ms</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfdd816043977-4"><span class="crayon-e">Time </span><span class="crayon-e">taken </span><span class="crayon-e">by </span><span class="crayon-v">ID</span><span class="crayon-o">:</span><span class="crayon-h"> </span><span class="crayon-cn">251ms</span></div><div class="crayon-line" id="crayon-631f0bbf6cfdd816043977-5"><span class="crayon-e">Time </span><span class="crayon-e">taken </span><span class="crayon-e">by </span><span class="crayon-v">Predicate</span><span class="crayon-o">:</span><span class="crayon-h"> </span><span class="crayon-cn">266ms</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfdd816043977-6"><span class="crayon-e">Time </span><span class="crayon-e">taken </span><span class="crayon-e">by </span><span class="crayon-t">Class</span><span class="crayon-h"> </span><span class="crayon-v">Chain</span><span class="crayon-o">:</span><span class="crayon-h"> </span><span class="crayon-cn">272ms</span></div><div class="crayon-line" id="crayon-631f0bbf6cfdd816043977-7"><span class="crayon-e">Time </span><span class="crayon-e">taken </span><span class="crayon-e">by </span><span class="crayon-t">Class</span><span class="crayon-h"> </span><span class="crayon-v">Name</span><span class="crayon-o">:</span><span class="crayon-h"> </span><span class="crayon-cn">337ms</span></div><div class="crayon-line crayon-striped-line" id="crayon-631f0bbf6cfdd816043977-8"><span class="crayon-e">Time </span><span class="crayon-e">taken </span><span class="crayon-e">by </span><span class="crayon-e">Accessibility </span><span class="crayon-v">Id</span><span class="crayon-o">:</span><span class="crayon-h"> </span><span class="crayon-cn">376ms</span></div><div class="crayon-line" id="crayon-631f0bbf6cfdd816043977-9"><span class="crayon-e">Time </span><span class="crayon-e">taken </span><span class="crayon-e">by </span><span class="crayon-v">Xpath</span><span class="crayon-o">:</span><span class="crayon-h"> </span><span class="crayon-cn">517ms</span></div></div></td>
</tr>
</table>
</div>
</div>

<p></p>
<p>Here, all the locators are mentioned from fastest executing ones to the slowest one.</p>
<h2>Conclusion</h2>
<p>Now, you might have a fair idea of when to use which locator in Appium, depending on your needs. There are a few other locators in Appium, which were skipped from this blog on locators in Appium because it was either deprecated or an experimental feature by Appium. I hope you liked this blog and learned something new from it.</p>
<div class="faq_lambda">
<h2 id="">Frequently Asked Questions (FAQs)</h2>
<div class="faq_list_lambda">
<h2>What are the locators used in Appium?</h2>
<ul>
<li>Some of the commonly used locators in Appium include:</li>
<li>ID.</li>
<li>Accessibility ID.</li>
<li>Class Name.</li>
<li>XPath.</li>
<li>Android UI Automator (UI Automator 2)</li>
<li>Android View Tag (Espresso Only)</li>
<li>iOS UIAutomation</li>
</ul>
</div>
<div class="faq_list_lambda">
<h2>How do you inspect locators in Appium?</h2>
<p>As compared to other mobile automation tools, Appium is unique in that it provides the capability to inspect any element on the screen using very simple steps. This helps a lot in identifying the UI elements. The following steps explain how you can inspect your mobile application elements in Appium:</p>
<ol>
<li> Launch your desired app on your local system and then launch the Appium server.</li>
<li> Open your browser and open the desired URL of the app (http://127.0.0.1:4723)</li>
<li> Now click on the "Inspect" button in Advanced Settings (This will open a new window with all the elements on the screen).</li>
<li> Now, simply click on the element in the app view and see the DOM/Source in the next panel and the properties on the right side of the selected element. Done!</li>
</ol>
</div>
<div class="faq_list_lambda">
<h2>How do I write XPath in Appium?</h2>
<p>To create a simple XPath query in Appium, click on the Spy icon button to get the Native/Web properties of all the objects on the screen. Then, right-click on one or more properties and then click on Copy XPath.</p>
</div>
</div>
<div class="wp-post-author-wrap wp-post-author-shortcode left">
<h3 class="awpa-title"></h3>
<div class="wp-post-author">
<div class="awpa-img awpa-author-block square">
<a href="https://www.lambdatest.com/blog/author/wasiqbhamla/"><img alt='' src='https://secure.gravatar.com/avatar/ae57536f69729f511f5b0f9f8879dd57?s=150&#038;d=mm&#038;r=r' srcset='https://secure.gravatar.com/avatar/ae57536f69729f511f5b0f9f8879dd57?s=300&#038;d=mm&#038;r=r 2x' class='avatar avatar-150 photo' height='150' width='150' /></a>
</div>
<div class="wp-post-author-meta awpa-author-block">
<h4 class="awpa-display-name">
<a href="https://www.lambdatest.com/blog/author/wasiqbhamla/">Wasiq Bhamla</a>
</h4>
<div class="wp-post-author-meta-bio">
<p>Wasiq is a Test Automation specialist having more than 15 years of experience in Manual and Automation testing. He has vast experience in automating Desktop, Web, API, Android, and iOS based applications. He is also an active open source contributor on GitHub, a freelancer, a mentor, and a blogger.</p>
</div>
<div class="wp-post-author-meta-more-posts">
<p class="awpa-more-posts"> 
<a href="https://www.lambdatest.com/blog/author/wasiqbhamla/" class="awpa-more-posts">See author&#039;s profile</a>
</p>
</div>
<ul class="awpa-contact-info">
<li class="awpa-twitter-li">
<a href="https://twitter.com/WasiqBhamla" class="awpa-twitter awpa-icon-twitter" target="_blank" rel="noopener"></a>
</li>
<li class="awpa-linkedin-li">
<a href="https://www.linkedin.com/in/wasiqbhamla/" class="awpa-linkedin awpa-icon-linkedin" target="_blank" rel="noopener"></a>
</li>
</ul>
</div>
</div>
</div>
</div>
<div style="border:1px solid #EEEFF0; margin-bottom:40px; margin-top:40px;"></div>
<div class="author_custom" style="background: #FAF7FF;border-radius: 10px;position:relative">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/pink-bottom.png" alt="Author Profile" class="green-middle" width="82" height="31" />
<img src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blue-bottom.png" alt="Author Profile" class="green-top" width="82" height="100" loading="lazy" />
<img src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/green-bottom.png" alt="Author Profile" class="green-bottom" width="92" height="98" loading="lazy" />
<h2 style="text-align: center;">Author’s Profile</h2>
<div class="cus_author">
<div class="cus_author_pro">
<div class="bottom_author_bio">
<a href="https://www.lambdatest.com/blog/author/wasiqbhamla/"><img alt='' src='https://secure.gravatar.com/avatar/ae57536f69729f511f5b0f9f8879dd57?s=60&#038;d=mm&#038;r=r' srcset='https://secure.gravatar.com/avatar/ae57536f69729f511f5b0f9f8879dd57?s=120&#038;d=mm&#038;r=r 2x' class='avatar avatar-60 photo' height='60' width='60' /></a></div>
</div>
<div>
<h3>
Wasiq Bhamla </h3>
<p>
Wasiq is a Test Automation specialist having more than 15 years of experience in Manual and Automation testing. He has vast experience in automating Desktop, Web, API, Android, and iOS based applications. He is also an active open source contributor on GitHub, a freelancer, a mentor, and a blogger. </p>
</div>
</div>
<div class="cus_social">
<h4>
Blogs: 2 </h4>
<div style="display:flex; align-items: center;">
<br /><br /><a style="width: 25px;height: 25px;margin-right:10px;margin-left:10px;" href="https://www.linkedin.com/in/wasiqbhamla/" rel="nofollow" target="_blank"><img src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/li_vector.png" width="20" height="20" alt="linkedin" loading="lazy" /></a><a style="width: 25px;height: 25px; margin-left:10px;" href="https://twitter.com/WasiqBhamla" rel="nofollow" target="_blank"><img src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/tw_vector.png" width="22" height="19" alt="twitter" loading="lazy" /></a> <br /> </div>
</div>
</div>
<div class="col-md-12 blog_content_signup_cta">
<p>Got Questions? Drop them on LambdaTest Community. <a href="https://community.lambdatest.com/" onclick="if (!window.__cfRLUnblockHandlers) return false; handleCommunityCta()" data-cf-modified-807212fb32e79fd549d9754a-="">Visit now</a></p>
</div>
</div>
<div class="col-xs-12 col-lg-3 col-sm-12 csi__blog">
<div style="background: #E6F9FF; border-radius: 10px;" class="blog_right_cta col-xs-12 col-lg-12 col-sm-6">
<div>
<h4 style="font-weight: 700;font-size: 16px;line-height: 138.52%;color: #1F1F1F;">Test your websites, web-apps or mobile apps seamlessly with <span>LambdaTest.</span></h4>
<ul>
<li>Selenium, Cypress, Playwright & Puppeteer Testing</li>
<li>Real Devices Cloud</li>
<li>Native App Testing</li>
<li>Appium Testing</li>
<li>Live Interactive Testing</li>
<li>Smart Visual UI Testing</li>
</ul>
<a href="https://www.lambdatest.com/demo" onclick="if (!window.__cfRLUnblockHandlers) return false; handleSideDemoCta()" data-cf-modified-807212fb32e79fd549d9754a-="">Book a Demo</a>
</div>
</div>
</div>

</div>
</div>
</div>
</div>
</section>
<section style="background: #F5F8FF; margin-top:80px;padding-bottom:40px">
<div class="container">
<div class="relevent-post col-md-12 col-xs-12 col-sm-12" style="margin-top: 30px; margin-bottom: 20px;text-align: center;"><h3 style="font-weight: 600; font-size:32px;color: #10375C;letter-spacing: 0.2px;padding-left:0px;">Related Articles</h3></div></div><div class="container"><div class="relevent-post col-md-12"> 
<div class="col-lg-4 col-sm-6 list-ret">
<div class="col-md-12 relevent-post-list" style="background:#fff; padding:0px;border-radius: 10px;border:none;">
<a href="https://www.lambdatest.com/blog/best-mobile-automation-testing-tools/"><img loading="lazy" style="width:100%" width="480" height="270" alt="Related Post" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/09/image7-30-1-1-1-1-1-1-1-1.png" /></a>
<div style="padding: 24px 21px;">
<p style="min-height: 140px; margin:0px; font-weight: 700;font-size: 18px;color: #10375C;letter-spacing: 0.2px;line-height: 27px;" class="relevent_head_content"><a href="https://www.lambdatest.com/blog/best-mobile-automation-testing-tools/">11 Best Mobile Automation Testing Tools In 2022</a></p>
<div class="cus_auth_detail">
<div style="display:flex; align-items: center;">
<div class="related_author">
<a href="https://www.lambdatest.com/blog/author/sushrutkm/"><img loading="lazy" width="96" height="96" alt="Author" src="https://secure.gravatar.com/avatar/2635148889cfd3f5283f1e9abf0dd78d?s=96&d=mm&r=r" /></a></div>
<div>
<h3 style="font-weight: 600;font-size: 14px;line-height: 21px;color: #10375C;margin:0; padding-left:0px;">Sushrut Kumar Mishra</h3>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0;">September 5, 2022</p>
</div>
</div>
<div>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-view-count.png" width="21" height="21" alt="view count" style="height:21px!important; margin-right:5px;" />3988 Views </p>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-Clock.png" width="19" height="19" alt="Read time" style="height:19px!important;margin-right:5px;" />19 Min Read
</p>
</div>
</div>
<div style="border-top: 1px solid #F0F0F0;">
<p style="margin:0;margin-top:10px;">
<a style='color: #8F8F8F;font-weight: 500;font-size: 12px;line-height: 14px;' href='https://www.lambdatest.com/blog/category/mobile-application-testing/'>Mobile App Testing</a> | </p>
</div>
</div>
</div>
</div>

<div class="col-lg-4 col-sm-6 list-ret">
<div class="col-md-12 relevent-post-list" style="background:#fff; padding:0px;border-radius: 10px;border:none;">
<a href="https://www.lambdatest.com/blog/how-to-automate-ios-app-using-appium/"><img loading="lazy" style="width:100%" width="480" height="270" alt="Related Post" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/08/image12-16-1-1-1-1-1-1-1-1.png" /></a>
<div style="padding: 24px 21px;">
<p style="min-height: 140px; margin:0px; font-weight: 700;font-size: 18px;color: #10375C;letter-spacing: 0.2px;line-height: 27px;" class="relevent_head_content"><a href="https://www.lambdatest.com/blog/how-to-automate-ios-app-using-appium/">How To Automate iOS App Using Appium</a></p>
<div class="cus_auth_detail">
<div style="display:flex; align-items: center;">
<div class="related_author">
<a href="https://www.lambdatest.com/blog/author/sidharth1988/"><img loading="lazy" width="96" height="96" alt="Author" src="https://secure.gravatar.com/avatar/7a85851148183a3d634af866dde38c88?s=96&d=mm&r=r" /></a></div>
<div>
<h3 style="font-weight: 600;font-size: 14px;line-height: 21px;color: #10375C;margin:0; padding-left:0px;">Sidharth Shukla</h3>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0;">August 17, 2022</p>
</div>
</div>
<div>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-view-count.png" width="21" height="21" alt="view count" style="height:21px!important; margin-right:5px;" />14643 Views </p>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-Clock.png" width="19" height="19" alt="Read time" style="height:19px!important;margin-right:5px;" />22 Min Read
</p>
</div>
</div>
<div style="border-top: 1px solid #F0F0F0;">
<p style="margin:0;margin-top:10px;">
<a style='color: #8F8F8F;font-weight: 500;font-size: 12px;line-height: 14px;' href='https://www.lambdatest.com/blog/category/mobile-application-testing/'>Mobile App Testing</a> | </p>
</div>
</div>
</div>
</div>

<div class="col-lg-4 col-sm-6 list-ret">
<div class="col-md-12 relevent-post-list" style="background:#fff; padding:0px;border-radius: 10px;border:none;">
<a href="https://www.lambdatest.com/blog/appium-parallel-testing/"><img loading="lazy" style="width:100%" width="480" height="270" alt="Related Post" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/07/Complete-Tutorial-On-Appium-Para-1-1-1-1-1-1.png" /></a>
<div style="padding: 24px 21px;">
<p style="min-height: 140px; margin:0px; font-weight: 700;font-size: 18px;color: #10375C;letter-spacing: 0.2px;line-height: 27px;" class="relevent_head_content"><a href="https://www.lambdatest.com/blog/appium-parallel-testing/">Complete Tutorial On Appium Parallel Testing [With Examples]</a></p>
<div class="cus_auth_detail">
<div style="display:flex; align-items: center;">
<div class="related_author">
<a href="https://www.lambdatest.com/blog/author/mfaisalkhatri/"><img loading="lazy" width="96" height="96" alt="Author" src="https://secure.gravatar.com/avatar/5828eff514ffcae835c98b24eabc3129?s=96&d=mm&r=r" /></a></div>
<div>
<h3 style="font-weight: 600;font-size: 14px;line-height: 21px;color: #10375C;margin:0; padding-left:0px;">Faisal Khatri</h3>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0;">July 27, 2022</p>
</div>
</div>
<div>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-view-count.png" width="21" height="21" alt="view count" style="height:21px!important; margin-right:5px;" />25921 Views </p>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-Clock.png" width="19" height="19" alt="Read time" style="height:19px!important;margin-right:5px;" />22 Min Read
</p>
</div>
</div>
<div style="border-top: 1px solid #F0F0F0;">
<p style="margin:0;margin-top:10px;">
<a style='color: #8F8F8F;font-weight: 500;font-size: 12px;line-height: 14px;' href='https://www.lambdatest.com/blog/category/mobile-application-testing/'>Mobile App Testing</a> | </p>
</div>
</div>
</div>
</div>

<div class="col-lg-4 col-sm-6 list-ret">
<div class="col-md-12 relevent-post-list" style="background:#fff; padding:0px;border-radius: 10px;border:none;">
<a href="https://www.lambdatest.com/blog/appium-with-testng-tutorial/"><img loading="lazy" style="width:100%" width="480" height="270" alt="Related Post" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/07/Automated-App-Testing-Using-Appi-1.png" /></a>
<div style="padding: 24px 21px;">
<p style="min-height: 140px; margin:0px; font-weight: 700;font-size: 18px;color: #10375C;letter-spacing: 0.2px;line-height: 27px;" class="relevent_head_content"><a href="https://www.lambdatest.com/blog/appium-with-testng-tutorial/">Automated App Testing Using Appium With TestNG [Tutorial]</a></p>
<div class="cus_auth_detail">
<div style="display:flex; align-items: center;">
<div class="related_author">
<a href="https://www.lambdatest.com/blog/author/wasiqbhamla/"><img loading="lazy" width="96" height="96" alt="Author" src="https://secure.gravatar.com/avatar/ae57536f69729f511f5b0f9f8879dd57?s=96&d=mm&r=r" /></a></div>
<div>
<h3 style="font-weight: 600;font-size: 14px;line-height: 21px;color: #10375C;margin:0; padding-left:0px;">Wasiq Bhamla</h3>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0;">July 15, 2022</p>
</div>
</div>
<div>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-view-count.png" width="21" height="21" alt="view count" style="height:21px!important; margin-right:5px;" />32020 Views </p>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-Clock.png" width="19" height="19" alt="Read time" style="height:19px!important;margin-right:5px;" />25 Min Read
</p>
</div>
</div>
<div style="border-top: 1px solid #F0F0F0;">
<p style="margin:0;margin-top:10px;">
<a style='color: #8F8F8F;font-weight: 500;font-size: 12px;line-height: 14px;' href='https://www.lambdatest.com/blog/category/mobile-application-testing/'>Mobile App Testing</a> | </p>
</div>
</div>
</div>
</div>

<div class="col-lg-4 col-sm-6 list-ret">
<div class="col-md-12 relevent-post-list" style="background:#fff; padding:0px;border-radius: 10px;border:none;">
<a href="https://www.lambdatest.com/blog/test-react-native-apps-on-ios-and-android/"><img loading="lazy" style="width:100%" width="480" height="270" alt="Related Post" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/06/How-To-Test-React-Native-Apps-On-1-1.jpg" /></a>
<div style="padding: 24px 21px;">
<p style="min-height: 140px; margin:0px; font-weight: 700;font-size: 18px;color: #10375C;letter-spacing: 0.2px;line-height: 27px;" class="relevent_head_content"><a href="https://www.lambdatest.com/blog/test-react-native-apps-on-ios-and-android/">How To Test React Native Apps On iOS And Android</a></p>
<div class="cus_auth_detail">
<div style="display:flex; align-items: center;">
<div class="related_author">
<a href="https://www.lambdatest.com/blog/author/mfaisalkhatri/"><img loading="lazy" width="96" height="96" alt="Author" src="https://secure.gravatar.com/avatar/5828eff514ffcae835c98b24eabc3129?s=96&d=mm&r=r" /></a></div>
<div>
<h3 style="font-weight: 600;font-size: 14px;line-height: 21px;color: #10375C;margin:0; padding-left:0px;">Faisal Khatri</h3>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0;">June 30, 2022</p>
</div>
</div>
<div>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-view-count.png" width="21" height="21" alt="view count" style="height:21px!important; margin-right:5px;" />38819 Views </p>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-Clock.png" width="19" height="19" alt="Read time" style="height:19px!important;margin-right:5px;" />23 Min Read
</p>
</div>
</div>
<div style="border-top: 1px solid #F0F0F0;">
<p style="margin:0;margin-top:10px;">
<a style='color: #8F8F8F;font-weight: 500;font-size: 12px;line-height: 14px;' href='https://www.lambdatest.com/blog/category/mobile-application-testing/'>Mobile App Testing</a> | </p>
</div>
</div>
</div>
</div>

<div class="col-lg-4 col-sm-6 list-ret">
<div class="col-md-12 relevent-post-list" style="background:#fff; padding:0px;border-radius: 10px;border:none;">
<a href="https://www.lambdatest.com/blog/mobile-app-usability-testing/"><img loading="lazy" style="width:100%" width="480" height="270" alt="Related Post" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/06/Quick-Guide-To-Mobile-App-Usabil-1.png" /></a>
<div style="padding: 24px 21px;">
<p style="min-height: 140px; margin:0px; font-weight: 700;font-size: 18px;color: #10375C;letter-spacing: 0.2px;line-height: 27px;" class="relevent_head_content"><a href="https://www.lambdatest.com/blog/mobile-app-usability-testing/">Quick Guide To Mobile App Usability Testing</a></p>
<div class="cus_auth_detail">
<div style="display:flex; align-items: center;">
<div class="related_author">
<a href="https://www.lambdatest.com/blog/author/salmankhan/"><img loading="lazy" width="96" height="96" alt="Author" src="https://secure.gravatar.com/avatar/5def5a94a33bf891a6672028c818696d?s=96&d=mm&r=r" /></a></div>
<div>
<h3 style="font-weight: 600;font-size: 14px;line-height: 21px;color: #10375C;margin:0; padding-left:0px;">Salman Khan</h3>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0;">June 28, 2022</p>
</div>
</div>
<div>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-view-count.png" width="21" height="21" alt="view count" style="height:21px!important; margin-right:5px;" />38617 Views </p>
<p style="font-weight: 500;font-size: 12px;line-height: 21px;color: #879DB1;margin:0px;display: flex;align-items: center;">
<img loading="lazy" src="https://www.lambdatest.com/blog/wp-content/uploads/2022/04/blog-Clock.png" width="19" height="19" alt="Read time" style="height:19px!important;margin-right:5px;" />14 Min Read
</p>
</div>
</div>
<div style="border-top: 1px solid #F0F0F0;">
<p style="margin:0;margin-top:10px;">
<a style='color: #8F8F8F;font-weight: 500;font-size: 12px;line-height: 14px;' href='https://www.lambdatest.com/blog/category/mobile-application-testing/'>Mobile App Testing</a> | </p>
</div>
</div>
</div>
</div>
</div> </div>
<div class="comment-box col-xs-12  col-md-12">
<div class="col-xs-12 comm-box">
</div>
</div>
</section>
</div>
</section>
<style>
	button:focus, button:hover, input[type=button]:focus, input[type=button]:hover, input[type=reset]:focus, input[type=reset]:hover, input[type=submit]:focus, input[type=submit]:hover {background: none !important;}
	.lt_video .modal-content {box-shadow: none!important;}
.lt_video .modal-content {background: transparent;border: none;}
	.footer ul li.cup, .footer ul li.calls {margin-bottom: 10px;}
	.copy-right-para img {width: 14px!important;height: auto!important;}
	.call-us li.heading {font-size: 14px;color: #4a4a4a;font-weight: 500;margin-bottom: 14px;list-style-type:none}
  .footer {padding: 50px 0px 0px 0px;}
  .get-touch li a {font-size: 14px; display: block; position: relative; width: 100%; max-width: 216px; text-decoration: none !important;font-weight:normal;color:#000000;padding: 5px 0px 5px 30px;}
.get-touch li a img {position: absolute; left: -20px; top: -4px; }
.call-us{margin-left: -16px!important;margin-top:35px!important}
.call-us li a{font-family: inherit; font-weight:normal;color:#4a4a4a; font-size: 12px; text-decoration: none !important;}
.footer-menu {padding: 0px !important;margin: 0px !important;max-width: auto;float: none;margin-top: -5px !important;}
.footer-menu li {display: inline-block; width: 200px; margin-bottom:8px;line-height:unset;}
.footer-menu li a {font-size: 12px; font-weight: normal;color: #4a4a4a; letter-spacing: 0.5px;}
.copy-right-para {padding: 0px; margin: 0px; font-size: 12px; font-weight: 500; color: #2d2d2d;text-align: center; margin-bottom: 25px; }
.cup img{width: 38px;height: auto;padding: 10px 7px 9px 12px;border-radius: 10px;background-color: #a0d468;}
.calls img{width: 38px;height: auto;padding: 10px 10px 9px 11px;border-radius: 10px;background-color: #ac92ec;}
.chatting img{ width: 38px;height: auto;padding: 11px 10px 9px;border-radius: 10px; background-color: #ff8a8a;}
.get-touch{margin-top: 12px!important;}
.footer-menu-heading{font-size: 14px;font-weight: bold;line-height: 2.14;color: #000000;}
.daily-items{margin-top: 25px!important;}
.footer-copy-right{background-color: #fafafa;padding: 35px 0px 25px;margin-top: 50px;border-top: 1px solid #eaeaea;}
.social-icons{margin-right:30px!important;}
.social-links li.pintrest-icon:hover a{background:#e60023;}
.social-links li.youtube-icons:hover a{background:#e60023;}
.copy-right-row {margin-top: 0px;}
.lt_fold video{width:100%}
.lt_video.show{top:5%;z-index:9999999 !important}
.lt_video .modal-dialog iframe{margin: 0 auto;display: block;}
.lt_video .modal-content{background:transparent; border:none}
.lt_video .modal-header{padding:0; border-bottom:none;}
.lt_video .modal-header .close{color:#fff; opacity:1; font-weight:300; font-size:3rem}
.modal-backdrop.show {opacity: 0.8;z-index: 99999!important;}
.lt_video .modal-dialog p{margin:0;}
.l_modal{display:inline-block; cursor:pointer; border-radius:10px;position:relative;}   
.l_modal:hover{text-decoration:underline !important}
.l_modal .playbtn{width: 15px; margin-right:5px;position: absolute;left: -20px;top: 6%;}
@media (min-width: 768px) and (max-width: 768px) {.get-touch li a img {left: -40px!important;} }
@media (max-width: 767px) {.cookiesdiv{width:100%!important}.demo__cta{width: 100%!important;z-index: 9999!important;padding: 0px 20px;text-align:center}.col-md-4.cont__group{padding-top:10px}.copy-right-row{margin-top: 30px;} .footer-menu{float: none;padding-left:10px!important;}
	.footer-menu-heading {padding-left:10px!important;margin-top:10px!important;}
  .first-col{padding-left:40px!important;}}
  @media (max-width: 1199px){.first-col{padding-left:30px;}}
@media (min-width: 992px) and (max-width: 1199px){.social-icons{padding-right:50px!important;}.copy-right-row p{padding-left: 15px;}}
@media (min-width:1300px){.lt_fold video{height:430px; width:auto} .lt_video .modal.show{top:5%;} .l_modal{margin-top:0px}}
@media (max-width: 1199px) and (min-width:768px){.hiddenCol{height:100px;}}
	.cursor-pointer{cursor: pointer;}
</style>
<footer class="footer">
<div class="container">
<div class="row">
<div class="col-lg-2 col-sm-3 first-col">
<ul class="get-touch">
<li class="cup">
<a href="https://www.lambdatest.com/demo">
<img alt="Schedule a demo with LambdaTest" src="https://www.lambdatest.com/assets_black_theme/images/coffee.svg" loading="lazy" width="19" height="19" />Book a Demo
</a>
</li>
<li class="calls">
 <a href="tel:+1-(866)-430-7087" onclick="if (!window.__cfRLUnblockHandlers) return false; onClickCallUs()" data-cf-modified-807212fb32e79fd549d9754a-="">
<img alt="Call LambdaTest Support" src="https://www.lambdatest.com/assets_black_theme/images/call.svg" loading="lazy" width="19" height="21" />Call Us</a>
</li>
<li class="chatting">
<a href="https://www.lambdatest.com/blog/" onclick="if (!window.__cfRLUnblockHandlers) return false; event.preventDefault(); openLTChatWidget(); onClickChatBtn()" data-cf-modified-807212fb32e79fd549d9754a-="">
<img alt="Chat with LambdaTest Customer Support" src="https://www.lambdatest.com/assets_black_theme/images/chat.svg" loading="lazy" width="20" height="20">
<span class="startchat">Chat with Us</span>
<span class="contact">Contact Us</span>
</a>
</li>
</ul>
<ul class="call-us">
<li class="heading">Help & Support</li>
<li><a href="tel:+1-(866)-430-7087">+1-(866)-430-7087</a>
</li>
<li><a href="/cdn-cgi/l/email-protection#6615131616091412262a070b040207320315124805090b" onclick="if (!window.__cfRLUnblockHandlers) return false; onClickEmailBtn()" data-cf-modified-807212fb32e79fd549d9754a-=""><span class="__cf_email__" data-cfemail="d7a4a2a7a7b8a5a3979bb6bab5b3b683b2a4a3f9b4b8ba">[email&#160;protected]</span></a>
</li>

</ul>
</div>
<div class="col-lg-2 col-sm-3">
<h6 class="footer-menu-heading">Products & Features</h6>
<ul class="footer-menu">
<li><a href="https://www.lambdatest.com/automation-testing">Automation Testing</a></li>
<li><a href="https://www.lambdatest.com/feature">Cross Browser Testing</a></li>
<li><a href="https://www.lambdatest.com/real-device-cloud">Real Device Cloud</a></li>
<li><a href="https://www.lambdatest.com/mobile-app-testing">Mobile App Testing</a></li>
<li><a href="https://www.lambdatest.com/hyperexecute">HyperExecute</a>
</li>
<li><a href="https://www.lambdatest.com/lt-browser">LT Browser</a></li>
<li><a href="https://www.lambdatest.com/lt-debug">LT Debug</a></li>
<li><a href="https://www.lambdatest.com/local-page-testing">Local Page Testing</a></li>
<li><a href="https://www.lambdatest.com/automated-screenshot">Automated Screenshots</a>
</li>
<li><a href="https://www.lambdatest.com/geolocation-testing">Geo-Location Testing</a></li>
<li><a href="https://www.lambdatest.com/responsive-test-online">Responsive Testing</a>
</li>
<li><a href="https://www.lambdatest.com/localization-testing">Localization Testing</a></li>
<li><a href="https://www.lambdatest.com/smart-visual-ui-testing">Smart Testing</a></li>
<li><a href="https://www.lambdatest.com/integrations">Integrations</a>
</li>
</ul>
<h6 class="footer-menu-heading">Browser Automation </h6>
<ul class="footer-menu">
<li><a href="https://www.lambdatest.com/selenium-automation">Selenium Testing</a></li>
<li><a href="https://www.lambdatest.com/cypress-testing">Cypress Testing</a></li>
<li><a href="https://www.lambdatest.com/playwright-testing">Playwright Testing</a></li>
<li><a href="https://www.lambdatest.com/puppeteer-testing">Puppeteer Testing</a></li>
</ul>
</div>
<div class="col-lg-2 col-sm-3">
<h6 class="footer-menu-heading">Test on</h6>
<ul class="footer-menu">
<li><a href="https://www.lambdatest.com/list-of-browsers">List of Browsers</a>
</li>
<li><a href="https://www.lambdatest.com/test-on-internet-explorer-browsers">Internet Explorer</a>
</li>
<li><a href="https://www.lambdatest.com/test-on-firefox-browsers">Firefox</a></li>
<li><a href="https://www.lambdatest.com/test-on-chrome-browsers">Chrome</a></li>
<li><a href="https://www.lambdatest.com/test-on-safari-browsers">Safari</a></li>
<li><a href="https://www.lambdatest.com/test-on-edge-browsers">Microsoft Edge</a></li>
<li><a href="https://www.lambdatest.com/test-on-opera-browsers">Opera</a>
</li>
<li><a href="https://www.lambdatest.com/test-on-yandex-browsers">Yandex</a></li>
<li><a href="https://www.lambdatest.com/test-on-macos-browsers">Mac OS</a></li>
<li><a href="https://www.lambdatest.com/test-on-mobile-devices">Mobile Devices</a></li>
<li><a href="https://www.lambdatest.com/test-on-ios-devices">iOS Simulator</a></li>
<li><a href="https://www.lambdatest.com/android-emulator-online">Android Emulator</a>
<li><a href="https://www.lambdatest.com/browser-emulator-online">Browser Emulator</a>
</li>
</ul>
<h6 class="footer-menu-heading footer_MAA">Mobile App Automation</h6>
<ul class="footer-menu">
<li><a href="https://www.lambdatest.com/appium-mobile-testing">Appium Testing</a></li>

<li><a href="https://www.lambdatest.com/espresso-automation-testing">Espresso Testing</a></li>
<li><a href="https://www.lambdatest.com/xcuitest-app-testing">XCUITest Testing</a></li>
</ul>
</div>
<div class="col-lg-2 col-sm-3">
<h6 class="footer-menu-heading">Resources</h6>
<ul class="footer-menu">
<li><a href="https://www.lambdatest.com/testuconf-2022" style="display:flex">Conferences <img loading="lazy" src="https://www.lambdatest.com/resources/images/fire.svg" style="margin-left:5px; width:15px; height:auto;" alt="Testμ Conf 2022" width="150" height="150" /></a></li>
<li><a href="https://www.lambdatest.com/blog/">Blogs</a>
</li>
<li><a href="https://community.lambdatest.com">Community</a></li>
<li><a href="https://www.lambdatest.com/certifications/">Certifications</a></li>
<li><a href="https://www.lambdatest.com/blog/category/lambdatest-updates/">Product Updates</a></li>
<li><a href="https://www.lambdatest.com/newsletter/">Newsletter</a>
</li>

<li><a href="https://www.lambdatest.com/webinar/">Webinars</a></li>
<li><a href="https://www.lambdatest.com/video/">Videos</a></li>
<li><a href="https://www.lambdatest.com/support-faq">FAQ</a></li>
<li><a href="https://www.lambdatest.com/web-technologies">Web Technologies</a></li>
<li><a href="https://www.lambdatest.com/automation-testing-advisor">Automation Testing Advisor</a></li>
<li><a href="https://www.lambdatest.com/free-online-tools">Free Online Tools</a></li>
<li><a href="https://www.lambdatest.com/sitemap.xml">Sitemap</a></li>
<li><a href="https://status.lambdatest.io" target="_blank">Status</a></li>
<h6 class="footer-menu-heading footer_MAA">Learning Hub</h6>
<ul class="footer-menu">
<li><a href="https://www.lambdatest.com/selenium">Selenium Tutorial</a></li>
<li><a href="https://www.lambdatest.com/cypress">Cypress Tutorial</a></li>
<li><a href="https://www.lambdatest.com/playwright">Playwright Tutorial</a></li>
<li><a href="https://www.lambdatest.com/appium">Appium Tutorial</a></li>
<li><a href="https://www.lambdatest.com/espresso">Espresso Tutorial</a></li>
<li><a href="https://www.lambdatest.com/xcuitest">XCUITest Tutorial</a></li>
<li><a href="https://www.lambdatest.com/learning-hub">More Learning Hubs</a></li>
</ul>
</ul>
</div>
<div class="hidden-lg col-sm-3 hiddenCol"></div>
<div class="col-lg-2 col-sm-3 col-sm-offset-3 col-lg-offset-0">
<h6 class="footer-menu-heading">Company</h6>
<ul class="footer-menu">
<li><a href="https://www.lambdatest.com/about">About Us</a>
</li>
<li><a href="https://www.lambdatest.com/customers/">Customers</a>
</li>
<li><a href="https://www.lambdatest.com/press/">Press</a>
</li>
<li><a href="https://www.lambdatest.com/reviews">Reviews</a></li>
<li><a href="https://www.lambdatest.com/community">Community & Support</a></li>
<li><a href="https://www.lambdatest.com/partners/">Partners</a></li>
<li><a href="https://www.lambdatest.com/open-source">Open Source</a></li>
<li><a href="https://www.lambdatest.com/lambdatest-write-for-us">Write for Us</a></li>
<li><a href="https://www.lambdatest.com/reseller">Reseller</a></li>
<li><a href="https://www.lambdatest.com/affiliate-program-partnership">Become an Affiliate</a></li>
<li><a href="https://www.lambdatest.com/legal/terms-of-service">Terms of service</a>
</li>
<li><a href="https://www.lambdatest.com/legal/privacy">Privacy Policy</a></li>
<li><a href="https://www.lambdatest.com/trust">Trust</a></li>
<li><a href="https://www.lambdatest.com/career">Careers</a>
</li>
<li><a href="https://www.lambdatest.com/team">Team</a>
</li>
<li><a href="https://www.lambdatest.com/contact-us">Contact Us</a>
</li>
</ul>
</div>
<div class="col-lg-2 col-sm-3">
<h6 class="footer-menu-heading">What’s New</h6>
<ul class="footer-menu" style="border-bottom: 2px solid #dbddec;;">
<li><a href="https://changelog.lambdatest.com">Changelog</a></li>
</ul>
<ul class="footer-menu daily-items">
<li><a href="https://www.lambdatest.com/blog/august-2022-product-updates/">August ‘22 Updates</a></li>
<li><a href="https://www.lambdatest.com/newsletter/editions/issue104">Coding Jag - Issue 104</a></li>
<li><a href="https://www.lambdatest.com/blog/testu-conf-2022-the-online-testing-summit/">Testμ Conf 2022[Conference]🔥</a></li>
<li><a href="https://www.lambdatest.com/webinar/clean-coding-practices-for-test-automation">Clean Coding Practices
for Test Automation [Webinar]</a></li>
<li><a href="https://www.lambdatest.com/customers/dashlane">Dashlane [Case Study]</a></li>
<li><a href="https://www.lambdatest.com/learning-hub/glossary">Software Testing [Glossary]</a></li>
<li><a href="https://www.lambdatest.com/learning-hub/test-plan">Test Plan [Tutorial]</a></li>
<li><a href="https://www.lambdatest.com/learning-hub/defect-management">Defect Management [Tutorial]</a></li>
<li><a href="https://www.lambdatest.com/blog/agile-testing-explained/">Agile Testing Explained [Thought Leadership]</a></li>
<li><a href="https://www.lambdatest.com/blog/locators-in-appium/">How To Identify Locators In Appium [Blog]</a></li>
<li><a href="https://www.lambdatest.com/blog/playwright-python-tutorial/">Playwright Python Tutorial [Blog]</a></li>
<li><a href="https://www.lambdatest.com/certifications/selenium-ruby-101">Selenium Ruby 101 [Certification]</a></li>
</ul>
</div>
</div>
</div>
<section class="footer-copy-right">
<div class="container">
<div class="row copy-right-row justify-content-between">
<div class="col-sm-4">
<p class="copy-right-para">© 2022 LambdaTest. All rights reserved</p>
</div>
<div class="col-sm-4">
<p class="copy-right-para">Cross Browser Testing Cloud Built With <img src="https://www.lambdatest.com/assets_black_theme/images/heart.svg" alt="Love" loading="lazy" width="512" height="512" class="img-fluid" loading="lazy" /> For Testers</p>
</div>
<div class="col-sm-4">
<ul class="list-inline list-unstyled social-links text-center">
<li class="fb">
<a target="_blank" href="https://www.facebook.com/lambdatest/" onclick="if (!window.__cfRLUnblockHandlers) return false; onClickSocialIcon('Facebook')" data-cf-modified-807212fb32e79fd549d9754a-="">
<img alt="Like Lambdatest on Facebook" width="15" height="15" src="https://www.lambdatest.com/assets_black_theme/images/facebook-logo.png" loading="lazy" />
</a>
 </li>
<li class="linkedin">
<a target="_blank" href="https://www.linkedin.com/company/lambdatest/" onclick="if (!window.__cfRLUnblockHandlers) return false; onClickSocialIcon('Linkedin')" data-cf-modified-807212fb32e79fd549d9754a-="">
<img alt="Follow LambdaTest on Linkedin" width="16" height="16" src="https://www.lambdatest.com/assets_black_theme/images/linkedin-logo.png" loading="lazy" />
</a>
</li>
<li class="twitter">
<a target="_blank" href="https://twitter.com/Lambdatesting" onclick="if (!window.__cfRLUnblockHandlers) return false; onClickSocialIcon('Twitter')" data-cf-modified-807212fb32e79fd549d9754a-="">
<img alt="LambdaTest Twitter" width="16" height="16" src="https://www.lambdatest.com/assets_black_theme/images/twitter-logo.png" loading="lazy" />
</a>
</li>
<li class="youtube-icons">
<a target="_blank" href="https://www.youtube.com/channel/UCCymWVaTozpEng_ep0mdUyw?sub_confirmation=1" onclick="if (!window.__cfRLUnblockHandlers) return false; onClickSocialIcon('YouTube')" data-cf-modified-807212fb32e79fd549d9754a-="">
<img alt="Subscribe LambdaTest on Youtube" width="16" height="16" src="https://www.lambdatest.com/assets_black_theme/images/youtube-logo.png" loading="lazy" />
</a>
</li>
<li class="github-icon">
<a href="https://github.com/LambdaTest/" target="_blank" onclick="if (!window.__cfRLUnblockHandlers) return false; onClickSocialIcon('GitHub')" data-cf-modified-807212fb32e79fd549d9754a-="">
<img src="https://www.lambdatest.com/assets_black_theme/images/github_icon.png" alt="GitHub" loading="lazy" width="16" height="16" />
</a>
</li>
<li class="pintrest-icon">
<a href="https://www.pinterest.com/lambdatest/" target="_blank">
<img src="https://www.lambdatest.com/assets_black_theme/images/pinterst.svg" alt="Pinterest" onclick="if (!window.__cfRLUnblockHandlers) return false; onClickSocialIcon('Pinterest')" style="width: 28px;" loading="lazy" width="12" height="14" loading="lazy" data-cf-modified-807212fb32e79fd549d9754a-="" />
</a>
</li>
</ul>
</div>
</div>
</div>
</section>
<div id="g_id_onload" data-client_id="520751746127-90vbtn38dcmbdeifj88jpfn2jt5pus67.apps.googleusercontent.com" data-login_uri="https://accounts.lambdatest.com/google-card/callback?redirect_uri=https://www.lambdatest.com/blog/locators-in-appium/" data-skip_prompt_cookie="accessToken"></div>
</footer>
</div>
<div class="modal fade" id="whitepaper-modal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
<div class="modal-dialog" role="document">
<div class="modal-content">
<div class="modal-body">
<span class="close" data-dismiss="modal" aria-label="Close" style="top: 4px; position: absolute; right: 10px;"><span aria-hidden="true">&times;</span></span>
<h2 class="titel">Download Whitepaper</h2>
<div class="hide-form">
<p class="details">You'll get your download link by email.</p>
<form class="form" id="whitepaper" method="POST">
<div class="form-group animated fadeInRightShort  ">
<input type="email" id="NewsletterEmail" name="email" placeholder="Enter your email" class="input-lg form-control" required />
</div>
<button type="submit" class="btn whitepaper-btn" name="subscribe">GET WHITEPAPER</button>
</form>
</div>
<p class="respons-tag" style="text-align: center;"></p>
</div>
<div class="modal-footer">
<p class="foot-text">Don't worry, we don't spam!</p>
</div>
</div>
</div>
</div>
<div class="cookiesdiv">
<img src="https://www.lambdatest.com/assets_black_theme/images/cookie.svg" alt="Cookie" class="cookie_logo">
<span class="cbtn btn_close_ck closecookiewebinar desk_button" style="cursor:pointer">X</span>
<div class="col-sm-12">
<div class="row">
<div class="col-sm-10">
<p>
We use cookies to give you the best experience. Cookies help to provide a more personalized experience and relevant advertising for you, and web analytics for us. Learn More in our <a href="https://www.lambdatest.com/legal/cookie" target="_blank">Cookies policy</a>, <a href="https://www.lambdatest.com/legal/privacy" target="_blank">Privacy </a> & <a href="https://www.lambdatest.com/legal/terms-of-service" target="_blank">Terms of service</a>.
</p>
</div>
<div class="col-sm-2">
<a href="https://www.lambdatest.com/blog/" onclick="if (!window.__cfRLUnblockHandlers) return false; event.preventDefault();" class="cbtn btn_accept_ck allow__btn" data-cf-modified-807212fb32e79fd549d9754a-="">Allow Cookie</a>
<a href="https://www.lambdatest.com/blog/" onclick="if (!window.__cfRLUnblockHandlers) return false; event.preventDefault();" class="cbtn btn_close_ck mob_button" data-cf-modified-807212fb32e79fd549d9754a-="">Cancel</a>
</div>
</div>
</div>
</div>
<style>
    .cta__demo__btn{background: #fff;display: inline-block;border: 2px solid #000;padding: 10px 40px;border-radius: 5px;box-shadow: 2px 2px 0px 0px;transition: 0.3s;}
	.cta__demo__btn:hover{box-shadow: 0 0 0 0 transparent, inset 108px 72px 0 0 transparent}
/* 	.demo__cta{background-image: linear-gradient(to bottom right, #FA9E61, #FFDD6A);display:none;z-index:1;position: fixed;border-radius: 10px;width: 100%;max-width:1110px;bottom:10px; left:50%; transform:translateX(-50%)} */
/* 	.sara__cta{width: 118px; height:102px!important; position: absolute;top: -21px;left: 20px;} */
/* 	.cont__para{color: #000;font-size: 16px;margin-bottom: 0px;font-weight: 700;} */
    .cookiesdiv{position:relative;display: none; z-index: 1111111;bottom: 10px; left: 50%;
    transform: translateX(-50%); right: 0; width: 100%; max-width:1110px;border-radius: 8px;background: #fff; position: fixed;box-shadow: 0 2px 10px 0 rgba(21, 24, 28, 0.16);padding-top: 36px;padding-bottom: 12px;}
    .cookiesdiv p{font-size: 14px; line-height: 1.7; color: #000; margin: 0;}
    .cookiesdiv p a{font-size: inherit; color: inherit; text-decoration: underline;}
    .cookiesdiv .closecookiewebinar{position: absolute;right: 0;top: 0;color: #000;padding: 13px 20px;font-size: 12px;}
	.cookiesdiv .cbtn.btn_accept_ck.allow__btn{max-width:100%; padding:9px 0px; margin-top:0px; margin-bottom:0px}
    .cookiesdiv .cbtn{padding: 7px 4px;text-align:center; background-color: #0ebac5; color: #fff; font-size: 13px; font-weight: normal; display: block; margin-left:auto;max-width:60px;margin-top: 3px; border-radius: 4px; }
    .cookiesdiv .cbtn.btn_close_ck{background: none;padding: 7px 15px; color: #b0b0b0;}
    .cookiesdiv .cbtn.btn_accept_ck{margin-top:16px; margin-bottom:5px;}
    .cookiesdiv .cookie_logo{position: absolute;top: 0%;left: 50%;transform: translate(-50%, -50%);}
    .mob_button{display:none !important}
	@media(max-width:1199px){.sara__cta, .cta__author{display:none}.cta__demo__btn{padding:5px 40px}}
	@media(min-width:768px) and (max-width:1199px){.cont__group{padding-left:60px} .cta__demo__btn{margin-top:10px}
	@media(max-width:767px){.cont__group{margin-bottom:10px} .cookiesdiv p{font-size:10px}.cookiesdiv p a{font-size:10px}.demo__cta{text-align:center; z-index:9999} .cookiesdiv .cbtn.btn_accept_ck.allow__btn{padding:7px 15px}.cookiesdiv{bottom:0px!important;margin-left:0px!important; width:100%!important} .cookiesdiv .cbtn{margin-left:initial; display:inline-block; padding: 7px 11px;border:1px solid #0ebac5; margin-right:5px; max-width:initial}  .mob_button{margin-top: 16px!important;margin-bottom: 5px!important;display:inline-block!important;} .desk_button{display:none !important}}
	.ft-menu { padding-left: 0px!important; }
	.socialtag{padding:0px}
</style>

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script src="https://www.lambdatest.com/blog/wp-content/themes/blog/js/jquery.js" type="807212fb32e79fd549d9754a-text/javascript"></script>

<script defer src="https://www.lambdatest.com/blog/wp-content/themes/blog/js/bootstrap.js" type="807212fb32e79fd549d9754a-text/javascript"></script>
<script defer src="https://www.lambdatest.com/blog/wp-content/themes/blog/js/custom.js" type="807212fb32e79fd549d9754a-text/javascript"></script>
<script defer src="https://www.lambdatest.com/blog/wp-content/themes/blog/js/formjs.js" type="807212fb32e79fd549d9754a-text/javascript"></script>
<script defer src="https://www.lambdatest.com/blog/wp-content/themes/blog/js/dynamic_cta.js?v=37" type="807212fb32e79fd549d9754a-text/javascript"></script>
<script type="807212fb32e79fd549d9754a-text/javascript" src="//script.crazyegg.com/pages/scripts/0085/1990.js" async="async"></script>
<script defer src="https://www.lambdatest.com/assets/js/click-tracking.js" type="807212fb32e79fd549d9754a-text/javascript"></script>
<script type="807212fb32e79fd549d9754a-text/javascript">
	$( document ).ready(function() {
		
// 		function getCookie(name){
// 			var re = new RegExp(name + "=([^;]+)");
// 			var value = re.exec(document.cookie);
// 			return (value != null) ? unescape(value[1]) : null;
// 		  }
// 		if (getCookie("accessToken") === undefined) {
// 		  	$('.login').html('<a href="https://accounts.lambdatest.com/register">Free Sign Up</a>');
// 		  	$('.sign-in').show();
// 		  }else{
// 		  	$('.login').html('<a href="https://accounts.lambdatest.com/dashboard">Dashboard</a>');
// 		  	$('.sign-in').hide();
// 		  }
		
		$("#whitepaper").submit(function(){
			//setup variables
			var form = $(this),
				formData = form.serialize(),
				formMethod = form.attr('method')

			$.ajax({
				type: formMethod,
				url: "https://api.lambdatest.com/lsms/api/v1.0/forms/subscribe-lambdatest-whitepapers",
				data: formData,

				success: function(data){
					$('.hide-form').css('display', 'none');
					$('.respons-tag').html('<br>Check your email! Your Whitepaper is on it&#39;s way.<br><br><i style="font-size: 50px; color: #50e3c2;" class="fa fa-check-square-o" aria-hidden="true"></i>')
				},
			});
			//prevent form from submitting
			return false;
		});
	});
</script>
<style>
.cyber_monday_alert{ z-index: 10000;bottom: 0; left: 0; width: 100%; background: #000000;position: fixed; padding-top: 15px;padding-bottom: 12px;color: #fff; }
.cyber_monday_alert.in{display: block;}
.cyber_monday_alert .border_left{border-left: 2px solid #ffffff; padding-left: 40px;}
.cyber_monday_alert h3{ font-size: 16px; margin-bottom: 0; margin-top: 0px; text-align: center;}
.cyber_monday_alert h4{ font-size: 14px; margin-bottom: 0; margin-top: 0; }
.cyber_monday_alert h4 span{ display: block; font-size: 12px; color: #d0d0d0; margin-bottom: 5px; }
.cyber_monday_alert a.btn{ background: #fff; font-size: 16px; font-weight: bold; border-radius: 3px; padding: 2px 10px; width: initial; line-height: 2; margin-left: 15px;height: 30px; line-height: initial;}
.hotoffer_icon { position: absolute; width: 75px; left: -70px; bottom: -25px; }

@media (max-width: 768px) {
    .hotoffer_icon { display: none; }
}
</style>
<script type="807212fb32e79fd549d9754a-text/javascript">
  $(document).ready(function(){
    var url1 = $("#video1 .LTVideo").attr('src');
    var url2 = $("#video2 .LTVideo").attr('src');
    if(url1){
      $("#video1").on('hide.bs.modal', function(){
        $(".LTVideo").attr('src', '');
    });
    $("#video1").on('show.bs.modal', function(){
        $(".LTVideo").attr('src', url1);
    });
    }
    if(url2){
      $("#video2").on('hide.bs.modal', function(){
        $(".LTVideo").attr('src', '');
    });
    $("#video2").on('show.bs.modal', function(){
        $(".LTVideo").attr('src', url2);
    });
    }
});
</script>
<script type="807212fb32e79fd549d9754a-text/javascript">
		$(document).ready(function() {
		function accessCookie(cookieName) {
		  var name = cookieName + "=";
		  var allCookieArray = document.cookie.split(';');
		  for(var i=0; i<allCookieArray.length; i++)
		  {
		    var temp = allCookieArray[i].trim();
		    if (temp.indexOf(name)==0)
		    return temp.substring(name.length,temp.length);
		  }
		  return "";
		}
		$('.closesitewebinar').click(function(){
		  document.cookie = "webinarCookie=true; max-age=3600"
		  $('.sitekitwebinar').hide();
		  $('body').removeClass('hasSitekit');
		});
		function checkSitekitCookie() {
		  var sitekitcookie = accessCookie("webinarCookie");
		  if (sitekitcookie!="") {
		  	$('.sitekitwebinar').hide();
		  	$('body').removeClass('hasSitekit');
		  } else {
		    $('.sitekitwebinar').show();
		    $('body').addClass('hasSitekit');
		    if (sitekitcookie!="" && sitekitcookie!=null)
		    {
		    document.cookie = "webinarCookie=true;expires=Thu, 30 Dec 2030 12:00:00 UTC"
		    }
		  }
		}

 checkSitekitCookie();
			
			$('.btn_close_ck').click(function () {
			$('.cookiesdiv').hide();
		});
			
			$('.btn_close_cta').click(function () {
				document.cookie = "close_blog_cta=true;domain=.lambdatest.com; path=/"
				$('.demo__cta').hide();
		});
	

		$('.btn_accept_ck').click(function () {
		document.cookie = "cookie_accepted=true;expires=Thu, 30 Dec 2030 12:00:00 UTC"
		$('.cookiesdiv').hide();
		});
	
		function checkctaCookie() {
			var user = accessCookie("close_cta");
			if (user!="")
					return;
			else
			{
// 				$('.demo__cta').show();
				setTimeout(function(){
   						$('.demo__cta').show();// or fade, css display however you'd like.
				}, 1500);
				if (user!="" && user!=null)
				{
						document.cookie = "close_blog_cta=true;domain=.lambdatest.com; path=/"
				}
			}
		}

		checkctaCookie();
	
		function checkCookie() {
		var user = accessCookie("cookie_accepted");
		if (user!="")
		return;
		else
		{
			$('.cookiesdiv').show();
			if (user!="" && user!=null)
			{
			document.cookie = "cookie_accepted=true;expires=Thu, 30 Dec 2030 12:00:00 UTC"
			}
		}
		}

		checkCookie();
	
	});
	
	$(window).scroll(function() {
	    scroll = $(window).scrollTop();

	    if (scroll >= 40) {
	        $('.sitekitwebinar').addClass('d-none');
	        $('.tagline').addClass('taglinePrime');
	    } else {
	        $('.sitekitwebinar').removeClass('d-none');
	        $('.tagline').removeClass('taglinePrime');
	    }
	});
		</script>
<script type="807212fb32e79fd549d9754a-text/javascript">
              /*butter scroll js starts from here*/
                $(document).ready( function(){
                $('a.hashSmoothScroll').click(function() {
                      if (location.pathname.replace(/^\//,'') == this.pathname.replace(/^\//,'') && location.hostname == this.hostname) {
                          var target = $(this.hash);
                          target = target.length ? target : $('[name=' + this.hash.slice(1) +']');
                           if (target.length) {
                            $('html, body').animate({
                              scrollTop: target.offset().top-140
                            }, 1000);
                            return false;
                          }
                      }
                  });

                });
              /* butter scroll js endsss from here*/

              function ltBrowserAppUrl(){
                let host = "https://downloads.lambdatest.com"
                if (
                  navigator.platform.indexOf("Win") >= 0 ||
                  navigator.appVersion.indexOf("Window") >= 0
                ) {
                  host = host + "/lt-browser/LTBrowser.exe";
                } else if (
                  navigator.platform.indexOf("Linux") >= 0 ||
                  navigator.appVersion.indexOf("Linux") >= 0
                ) {
                    host = host + "/lt-browser/LTBrowser.AppImage";
                  
                }else {
                host =  host + "/lt-browser/LTBrowser.dmg";
                }
                $(".download__lt__browser__link").attr('href', host)
              }
              ltBrowserAppUrl();
			
			async function sendAnalytics(eventName) {
				
				let URL = "https://backend.lambdatest.com/api/analytics/event";
				let payload = {
				event: eventName,
				properties: {
    						source: window.location.href,
							userAgent: window.navigator.userAgent
    				}
				};
				if(getLTUserID() && getLTUserID() !== '') {
					payload.userId = getLTUserID();
				}
				try {
				await fetch(URL, {
					method: "POST",
					body: JSON.stringify(payload),
					mode: 'no-cors',
					headers: {
					"Content-Type": "application/json",
					},
				});
				if(eventName=='lt-browser-downloaded'){
				  dataLayer.push({

				  'event': 'LT Browser',
				  'eventCategory': 'LT Browser',
				  'eventAction': 'Download',
				  'eventLabel': 'LT Browser downloads',
				  });
				  if(window.amplitude){
					amplitude.getInstance().logEvent('LT Browser Download',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
        		} 
					if (eventName=='Coding-Jag'){dataLayer.push({
                    'event': 'Coding Jag',
                    'eventCategory': 'Coding Jag',
                    'eventAction': 'Subscribe',
                    'eventLabel': 'Coding Jag Subscription',
                    });}
					if (eventName=='StickyFooter'){dataLayer.push({
                    'event': 'Sticky Footer',
					'eventCategory': 'LT Blog CTA',
					'eventAction': 'Click',
					'eventLabel': 'LT Blog Sticky Footer',
                    });
					if(window.amplitude){
					amplitude.getInstance().logEvent('LT Blog CTA',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
				}
					if (eventName=='RightStickyBanner'){dataLayer.push({
                    'event': 'Right Sticky Banner',
					'eventCategory': 'LT Blog Right CTA',
					'eventAction': 'Click',
					'eventLabel': 'LT Blog Right Sticky',
                    });
					if(window.amplitude){
					amplitude.getInstance().logEvent('LT Blog Right CTA',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
				}
					if (eventName=='CloseStickyFooter'){dataLayer.push({
                    'event': 'Close Sticky Footer',
					'eventCategory': 'Close LT Blog CTA',
					'eventAction': 'Click',
					'eventLabel': 'Close LT Blog Sticky Footer',
                    });
					if(window.amplitude){
					amplitude.getInstance().logEvent('Close LT Blog CTA',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
				}
				console.log("Analytics Request successful ");
				// console.log(user_id);
				} catch (err) {
				console.error("Analytics Request ", err);
				}
				
			  }
			function handleIndexCta(){
				if(window.amplitude){
					amplitude.getInstance().logEvent('LTB Index Repeat CTA',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
			}
			function handleSignupCta(){
				if(window.amplitude){
					amplitude.getInstance().logEvent('LTB Begin CTA Free Testing',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
			}
			function handleBookDemoCta(){
				if(window.amplitude){
					amplitude.getInstance().logEvent('LTB Begin CTA Book Now',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
			}
			function handleCommunityCta(){
				if(window.amplitude){
					amplitude.getInstance().logEvent('LTB End CTA Community',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
			}
			function handleContentCta(){
				if(window.amplitude){
					amplitude.getInstance().logEvent('LTB In Content CTA',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
			}
			function handleSideDemoCta(){
				if(window.amplitude){
					amplitude.getInstance().logEvent('LTB Side Banner CTA',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
			}
			function onLogin(){
				if(window.amplitude){
					amplitude.getInstance().logEvent('WH-Login',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
			}
			function onDemo(){
				if(window.amplitude){
					amplitude.getInstance().logEvent('WH-Demo',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
			}
			function onStartTesting(){
				if(window.amplitude){
					amplitude.getInstance().logEvent('WH-Signup',
						{source: window.location.href,
					  userAgent: window.navigator.userAgent});
				  }
			}
        </script>
<script type="807212fb32e79fd549d9754a-text/javascript">
    var $form = $("#bookyourseats");
      $form.submit(function(e){
        e.preventDefault();
        var formData = $form.serializeArray();
        var persondata = {};
        for (let i=0; i < formData.length; i++) {
          persondata[formData[i]['name']] = formData[i]['value']
        }
        $.ajax({
          method: "POST",
          url: 'https://api.lambdatest.com/lsms/api/v1.0/forms/webinar-registration',
          data: persondata,
          success: function (response) {
            console.log('Success', response);
            $('.briefform').hide();
            $('.submittedform').show();
             
            dataLayer.push({ 
              'event': 'eventToSend', 
              'eventCategory': 'FormSubmit', 
              'eventAction': 'WebinarForm', 
              'eventLabel': 'Success', 
            }); 

          },
          error: function (response) {
            console.log('Error', response);
            // alert(response.responseText);
          }
        });
      });

</script>
<script type="807212fb32e79fd549d9754a-text/javascript">

	function submitForm(e) {
		
		e.preventDefault();
		
		var dataEmail = $(".email").val();
		
		var settings = {
		"url": "https://backend.lambdatest.com/api/newsletter-contact",
		"method": "POST",
		"timeout": 0,
		"headers": {
			"content-type": "application/json",
			
		},
		
		"data": JSON.stringify({"email": dataEmail, "listId": "8f500c6d-a448-4fd7-81d3-134b0321b170"}),
		};
		$.ajax(settings).done(function (response) {
		console.log(response);
		var res = response;
		if(res.success) {
			$(".submittedform").css('display', 'block');
			$('.trybox_content').css('display', 'none');
			$('.emailBlock').css('display', 'none');
			sendAnalytics('Coding-Jag');
		} 
		}).fail(function(response){
  			 console.log('Fail:',response.responseText);
			  var errorData = JSON.parse(response.responseText);
            let errormsg = errorData.email;
            console.log(errormsg)
            let errorHtml = "";
            Array.from(errorData.email).forEach(child => {
            console.log(errormsg)
			 $(".emailid").html(errormsg);
			 setTimeout(() => {
					$(".emailid").hide();
								}, 5000)
        	});
  		});
  
	}
</script>
<script type="807212fb32e79fd549d9754a-text/javascript">
$(document).ready(function(){
	$('a').each(function(){
		if ( $(this).attr('href') == 'https://community.lambdatest.com/'){
			$(this).attr('rel','noopener noreferrer');
		}
	})
});

  /* JS for google landing page*/
  function accessCookie(cookieName) {
    var name = cookieName + "=";
    var allCookieArray = document.cookie.split(';');
    for(var i=0; i<allCookieArray.length; i++)
    {
      var temp = allCookieArray[i].trim();
      if (temp.indexOf(name)==0)
      return temp.substring(name.length,temp.length);
    }
    return "";
  } 

  function getUserDetails() {
    var accessToken = accessCookie("accessToken");
    if (accessToken!="") {
      $('body').addClass('userloggedIn');
      $('.landing_sign_up_form').addClass('loggedIn');
		$('.header_login').css('display','none');
    } else {
        $('.landing_sign_up_form').removeClass('loggedIn');
        $('body').removeClass('userloggedIn');
        $('.landing_sign_up_form').addClass('loggedOut');
        $('body').addClass('userloggedOut');
		$('.header_login').css('display','block');
     }
  }
  getUserDetails();

  function changeAttrofSignUpBtn() {
    var signup_link = $('body.userloggedIn li.login a');
    signup_link.attr('href', 'https://accounts.lambdatest.com/dashboard/');
    signup_link.text('Dashboard');
  }
  changeAttrofSignUpBtn();
  /* JS for google landing page*/
</script>
<script defer src="https://accounts.google.com/gsi/client" type="807212fb32e79fd549d9754a-text/javascript"></script>
<script type="807212fb32e79fd549d9754a-text/javascript">
$(window).scroll(function() {    
  var scroll = $(window).scrollTop();
  if (scroll >= 200) {
    $(".lambda-floating-banner").css("display","block");
    inViewport();
  }else{
    $(".lambda-floating-banner").css("display","none");
  }
 function inViewport(){
   $('.relevent-post').each(function(){
     var divPos = $(this).offset().top,
             topOfWindow = $(window).scrollTop();

     if( divPos < topOfWindow+600 ){
       $('.lambda-floating-banner').css({
        'display': 'none'
       });
		 $('.custom__social__icons').css({
			 'display':'none'
		 })
     } else {
      $('.lambda-floating-banner').css({
        'display': 'block'
       });
		 $('.custom__social__icons').css({
			 'display':'block'
		 })
     }
   });
 }
});
$('.close').click(function () {
            $('.lambda-floating-banner').addClass("btnclose");
        });


</script>
<script type="807212fb32e79fd549d9754a-text/javascript">
	$(".cookiesdiv").css("opacity","0");
	$(".demo__cta").css("opacity","0");
	$(window).scroll(function() { 
 if ($(window).scrollTop() > 800) { 
	$(".cookiesdiv").css("opacity","1");
	$(".demo__cta").css("opacity","1");
 } 
 else { 
	$(".cookiesdiv").css("opacity","0");
	$(".demo__cta").css("opacity","0");
 } 
}); 
	
		function handleBackToblog(){
		var previousURL = document.referrer;
// 		console.log(previousURL);
		if(previousURL.indexOf("lambdatest.com") > -1){
// 			console.log('yes')
			history.back();
		}else{
			window.location.href= "https://www.lambdatest.com/blog/";
		}
	}
	
	// 	iframe generator
	function youtubeIframe() {
  var youtube = document.querySelectorAll(".blog__youtube");
  for (var i = 0; i < youtube.length; i++) {
    var source = "https://img.youtube.com/vi/" + youtube[i].dataset.embed + "/sddefault.jpg";
    var image = new Image();
    image.src = source;
	image.alt = "Youtube Thubnail";
    image.addEventListener("load", function () {
      youtube[i].appendChild(image);
    }(i));
    youtube[i].addEventListener("click", function () {
      var iframe = document.createElement("iframe");
      iframe.setAttribute("frameborder", "0");
      iframe.setAttribute("allowfullscreen", "");
      iframe.setAttribute("src", "https://www.youtube.com/embed/" + this.dataset.embed + "?rel=0&showinfo=0&autoplay=1");
      this.innerHTML = "";
      this.appendChild(iframe);
    });
  };
}
	
	setTimeout(function () {
  if (typeof document !== "undefined") {
    youtubeIframe()
  }
}, 500);
</script>
<script type="807212fb32e79fd549d9754a-text/javascript" src='https://www.lambdatest.com/blog/wp-includes/js/comment-reply.min.js?ver=5.2.15'></script>
<script type="807212fb32e79fd549d9754a-text/javascript" src='https://www.lambdatest.com/blog/wp-includes/js/imagesloaded.min.js?ver=3.2.0'></script>
<script type="807212fb32e79fd549d9754a-text/javascript" src='https://www.lambdatest.com/blog/wp-includes/js/masonry.min.js?ver=3.3.2'></script>
<script type="807212fb32e79fd549d9754a-text/javascript" src='https://www.lambdatest.com/blog/wp-includes/js/jquery/jquery.masonry.min.js?ver=3.1.2b'></script>
<script type="807212fb32e79fd549d9754a-text/javascript" src='https://www.lambdatest.com/blog/wp-content/themes/blog/js/functions.js?ver=20160717'></script>
<script type="807212fb32e79fd549d9754a-text/javascript" src='https://www.lambdatest.com/blog/wp-includes/js/wp-embed.min.js?ver=5.2.15'></script>
<script type="807212fb32e79fd549d9754a-text/javascript">window.NREUM||(NREUM={});NREUM.info={"beacon":"bam.nr-data.net","licenseKey":"NRJS-15a9ea9b6e428dbd49e","applicationID":"1241459542","transactionName":"ZlYEZxdTWERUWxZYX18cM0EMHVRbWl9NWF5VVh4dFVpG","queueTime":0,"applicationTime":24,"atts":"ShEHEV9JS0o=","errorBeacon":"bam.nr-data.net","agent":""}</script><script src="/cdn-cgi/scripts/7d0fa10a/cloudflare-static/rocket-loader.min.js" data-cf-settings="807212fb32e79fd549d9754a-|49" defer=""></script><script defer src="https://static.cloudflareinsights.com/beacon.min.js/v652eace1692a40cfa3763df669d7439c1639079717194" integrity="sha512-Gi7xpJR8tSkrpF7aordPZQlW2DLtzUlZcumS8dMQjwDHEnw9I7ZLyiOj/6tZStRBGtGgN6ceN6cMH8z7etPGlw==" data-cf-beacon='{"rayId":"749808f95cda31e2","token":"0adfd746129e4a82882a057e9c97fd2e","version":"2022.8.1","si":100}' crossorigin="anonymous"></script>
</body>
</html>


