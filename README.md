jQuery Page Walkthrough
================================

Page Walkthrough is a flexible system for designing interactive, multimedia, educational walkthroughs.

<h2>Example:</h2>
To view jQuery Page Walkthrough example <a href="example/example.html">Click Here</a>
<h2>Install:</h2>
<pre>
&lt;!-- CSS --&gt;
&lt;link type="text/css" rel="stylesheet" href="css/jquery.pagewalkthrough.css" /&gt;

&lt;!-- JQUERY --&gt;
&lt;script type="text/javascript" src="js/jquery-1.7.2.min.js"></script>
&lt;script type="text/javascript" src="js/jquery.pagewalkthrough-1.1.0.js"></script>
</pre>
<h2>jQuery Page Walkthrough Default Options:</h2>
<pre>
steps: [

  {
        wrapper: '', //an ID of page element HTML that you want to highlight
        margin: 0, //margin for highlighted area, may use CSS syntax i,e: '10px 20px 5px 30px' or '20px 20px' and so on
        popup:
            {
              content: '', //ID content of the walkthrough
              type: 'modal', //tooltip, modal, nohighlight
              position:'top',//position for tooltip and nohighlight type only: top, right, bottom, left
              offsetHorizontal: 0, //horizontal offset for the walkthrough
              offsetVertical: 0, //vertical offset for the walkthrough
              width: '320', //default width for each step,
              draggable: false, // set true to set walkthrough draggable,
              contentRotation: 0 //content rotation : i.e: 0, 90, 180, 270 or whatever value you add. minus sign (-) will be CCW direction
           },          
        overlay: true, //use overlay or not, default: true   
        accessable: false, //if true - you can access html element such as form input field, button etc
        autoScroll: true, //is true - this will autoscroll to the arror/content every step 
        scrollSpeed: 1000, //scroll speed
        stayFocus: false, //if true - when user scroll down/up to the page, it will scroll back the position it belongs
        onLeave: null, // callback when leaving the step
        onEnter: null // callback when entering the step
  }

],
name: '',
onLoad: true, //load the walkthrough at first time page loaded
onBeforeShow: null, //callback before page walkthrough loaded
onAfterShow: null, // callback after page walkthrough loaded
onRestart: null, //callback for onRestart walkthrough
onClose: null, //callback page walkthrough closed
onCookieLoad: null //when walkthrough closed, it will set cookie and tells the walkthrough to not load automaticly
</pre>
<h2>Public Methods:</h2>
<pre>
<strong>show</strong>       :   $.pagewalkthrough('show', target)
This method allows you to open page walkthrough. Target is your walkthrough ID, i.e: #selector

<strong>next</strong>       :   $.pagewalkthrough('next', event)
This method allows you to go the NEXT step. Event is needed as a param to call next method

<strong>prev</strong>       :   $.pagewalkthrough('prev', event)
This method allows you to go the PREVIOUS step. Event is needed as a param to call prev method

<strong>restart</strong>    :   $.pagewalkthrough('restart', event)
This method allows you to go the RESTART step. Event is needed as a param to call restart method

<strong>close</strong>      :   $.pagewalkthrough('close', target)
This method allows you to go the CLOSE step. Target is optional. It could be filled with walkthrough ID or leave it blank

<strong>isPageWalkthroughActive</strong>   :   $.pagewalkthrough('isPageWalkthroughActive')
This property will return status of page walkthrough

<strong>currIndex</strong>  :   $.pagewalkthrough('currIndex')
This property will return current index of current walkthrough step
</pre>

<h2>Browser Support:</h2>
<p>IE7+, Firefox (Win &amp; Mac), Safari (Win &amp; Mac), Chrome (Win &amp; Mac)</p>
<p><strong>Note:</strong> Because chrome doesn't support running cookie in local file, if you want to test this plugin on chrome, you should run this plugin from webserver i.e: wamp, mamp, etc</p>

<h2>Theme:</h2>
<p>Will be added soon...</p>
