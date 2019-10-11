# com-chilipeppr-widget-robot-axes
This widget lets you see the axes information for the 6 actuators on a robot arm plus grippers or other end units. It enables you to jog, home, and change units.

![alt text](screenshot.png "Screenshot")

## ChiliPeppr Widget / Robot Arm Axes

All ChiliPeppr widgets/elements are defined using cpdefine() which is a method
that mimics require.js. Each defined object must have a unique ID so it does
not conflict with other ChiliPeppr widgets.

| Item                  | Value           |
| -------------         | ------------- | 
| ID                    | com-chilipeppr-widget-robot-axes |
| Name                  | Widget / Robot Arm Axes |
| Description           | This widget lets you see the axes information for the 6 actuators on a robot arm plus grippers or other end units. It enables you to jog, home, and change units. |
| chilipeppr.load() URL | https://raw.githubusercontent.com/chilipeppr/widget-robot-axes/master/auto-generated-widget.html |
| Edit URL              | (Local dev. No edit URL) |
| Github URL            | https://github.com/chilipeppr/widget-robot-axes |
| Test URL              | http://localhost:9005/widget.html |

## Example Code for chilipeppr.load() Statement

You can use the code below as a starting point for instantiating this widget 
inside a workspace or from another widget. The key is that you need to load 
your widget inlined into a div so the DOM can parse your HTML, CSS, and 
Javascript. Then you use cprequire() to find your widget's Javascript and get 
back the instance of it.

```javascript
// Inject new div to contain widget or use an existing div with an ID
$("body").append('<' + 'div id="myDivWidgetRobotAxes"><' + '/div>');

chilipeppr.load(
  "#myDivWidgetRobotAxes",
  "https://raw.githubusercontent.com/chilipeppr/widget-robot-axes/master/auto-generated-widget.html",
  function() {
    // Callback after widget loaded into #myDivWidgetRobotAxes
    // Now use require.js to get reference to instantiated widget
    cprequire(
      ["inline:com-chilipeppr-widget-robot-axes"], // the id you gave your widget
      function(myObjWidgetRobotAxes) {
        // Callback that is passed reference to the newly loaded widget
        console.log("Widget / Robot Arm Axes just got loaded.", myObjWidgetRobotAxes);
        myObjWidgetRobotAxes.init();
      }
    );
  }
);

```

## Publish

This widget/element publishes the following signals. These signals are owned by this widget/element and are published to all objects inside the ChiliPeppr environment that listen to them via the 
chilipeppr.subscribe(signal, callback) method. 
To better understand how ChiliPeppr's subscribe() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-pub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr><td colspan="2">(No signals defined in this widget/element)</td></tr>    
      </tbody>
  </table>

## Subscribe

This widget/element subscribes to the following signals. These signals are owned by this widget/element. Other objects inside the ChiliPeppr environment can publish to these signals via the chilipeppr.publish(signal, data) method. 
To better understand how ChiliPeppr's publish() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-sub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr><td colspan="2">(No signals defined in this widget/element)</td></tr>    
      </tbody>
  </table>

## Foreign Publish

This widget/element publishes to the following signals that are owned by other objects. 
To better understand how ChiliPeppr's subscribe() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-foreignpub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr valign="top"><td>/com-chilipeppr-widget-robot-axes/com-chilipeppr-widget-cayenn/sendToDeviceNameViaTcp</td><td>We publish to the Cayenn widget so it can send jog values to the Cayenn device by name like Wrist1, Wrist2, Wrist3, etc.</td></tr>    
      </tbody>
  </table>

## Foreign Subscribe

This widget/element publishes to the following signals that are owned by other objects.
To better understand how ChiliPeppr's publish() method works see amplify.js's documentation at http://amplifyjs.com/api/pubsub/

  <table id="com-chilipeppr-elem-pubsubviewer-foreignsub" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Signal</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr valign="top"><td>/com-chilipeppr-widget-robot-axes/com-chilipeppr-widget-cayenn/onRecvFromDeviceName</td><td>We subscribe to the Cayenn widget so when it tells us the step value of axes like Wrist1, Wrist2, Wrist3, etc we can update our widget.</td></tr>    
      </tbody>
  </table>

## Methods / Properties

The table below shows, in order, the methods and properties inside the widget/element.

  <table id="com-chilipeppr-elem-methodsprops" class="table table-bordered table-striped">
      <thead>
          <tr>
              <th style="">Method / Property</th>
              <th>Type</th>
              <th style="">Description</th>
          </tr>
      </thead>
      <tbody>
      <tr valign="top"><td>id</td><td>string</td><td>"com-chilipeppr-widget-robot-axes"</td></tr><tr valign="top"><td>url</td><td>string</td><td>"https://raw.githubusercontent.com/chilipeppr/widget-robot-axes/master/auto-generated-widget.html"</td></tr><tr valign="top"><td>fiddleurl</td><td>string</td><td>"(Local dev. No edit URL)"</td></tr><tr valign="top"><td>githuburl</td><td>string</td><td>"https://github.com/chilipeppr/widget-robot-axes"</td></tr><tr valign="top"><td>testurl</td><td>string</td><td>"http://localhost:9005/widget.html"</td></tr><tr valign="top"><td>name</td><td>string</td><td>"Widget / Robot Arm Axes"</td></tr><tr valign="top"><td>desc</td><td>string</td><td>"This widget lets you see the axes information for the 6 actuators on a robot arm plus grippers or other end units. It enables you to jog, home, and change units."</td></tr><tr valign="top"><td>publish</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>subscribe</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>foreignPublish</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>foreignSubscribe</td><td>object</td><td>Please see docs above.</td></tr><tr valign="top"><td>init</td><td>function</td><td>function () </td></tr><tr valign="top"><td>send</td><td>function</td><td>function(name, obj) <br><br>Method for sending to Cayenn device</td></tr><tr valign="top"><td>setupOnRecvFromDeviceName</td><td>function</td><td>function() <br><br>Setup to get incoming data from Cayenn devices by their name.</td></tr><tr valign="top"><td>onRecvFromDeviceName</td><td>function</td><td>function(payload) <br><br>Called when we get incoming data from Cayenn devices by their name.</td></tr><tr valign="top"><td>setAxesStepVal</td><td>function</td><td>function(name, val) <br><br>Set the axes value by name</td></tr><tr valign="top"><td>createDomAxes</td><td>function</td><td>function() </td></tr><tr valign="top"><td>onPerAxisClick</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>perAxisPosInputKeypress</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>onPerAxisPosClick</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>onPerAxisPosBlur</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>onPerAxisGotoZero</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>onPerAxisZeroOut</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>onPerAxisHome</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>onJogFwdClick</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>onJogRevClick</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>titleCase</td><td>function</td><td>function(str) </td></tr><tr valign="top"><td>pencilSetup</td><td>function</td><td>function() </td></tr><tr valign="top"><td>pencilOnMouseover</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>pencilOnMouseout</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>pencilClick</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>pencilCtr</td><td>number</td><td></td></tr><tr valign="top"><td>pencilKeypress</td><td>function</td><td>function(evt) </td></tr><tr valign="top"><td>pencilHide</td><td>function</td><td>function(tgtEl) </td></tr><tr valign="top"><td>toolbarSetup</td><td>function</td><td>function () </td></tr><tr valign="top"><td>bodyShowSmall</td><td>function</td><td>function () </td></tr><tr valign="top"><td>bodyShowNormal</td><td>function</td><td>function () </td></tr><tr valign="top"><td>options</td><td>object</td><td></td></tr><tr valign="top"><td>setupUiFromCookie</td><td>function</td><td>function () </td></tr><tr valign="top"><td>saveOptionsCookie</td><td>function</td><td>function () </td></tr><tr valign="top"><td>toggleInMm</td><td>function</td><td>function () </td></tr><tr valign="top"><td>currentUnits</td><td>object</td><td></td></tr><tr valign="top"><td>updateUnitsFromStatus</td><td>function</td><td>function (units) </td></tr><tr valign="top"><td>lastCoords</td><td>object</td><td></td></tr><tr valign="top"><td>onCoordsUpdate</td><td>function</td><td>function (coords) </td></tr><tr valign="top"><td>publishSend</td><td>function</td><td>function(gcode) </td></tr><tr valign="top"><td>gotoZeroM</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>gotoZero</td><td>function</td><td>function (evt, m) </td></tr><tr valign="top"><td>zeroOutAxisG10</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>zeroOutAxisG28</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>zeroOutAxisG92</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>unzeroOutAxisG92</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>homeAxis</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>btnSetup</td><td>function</td><td>function () </td></tr><tr valign="top"><td>jogFocusIndicate</td><td>function</td><td>function () </td></tr><tr valign="top"><td>jogFocusUnindicate</td><td>function</td><td>function () </td></tr><tr valign="top"><td>isInCustomMenu</td><td>boolean</td><td></td></tr><tr valign="top"><td>customMenuSetVal</td><td>function</td><td>function (itemNum) </td></tr><tr valign="top"><td>jogSetup</td><td>function</td><td>function () </td></tr><tr valign="top"><td>jogBtn</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>baseval</td><td>number</td><td></td></tr><tr valign="top"><td>accelBaseval</td><td>number</td><td></td></tr><tr valign="top"><td>customOrigVal</td><td>object</td><td></td></tr><tr valign="top"><td>accelBaseValHilite</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>accelBaseValUnhilite</td><td>function</td><td>function () </td></tr><tr valign="top"><td>changeBaseVal</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>jog</td><td>function</td><td>function (direction, isFast, is100xFast, is1000xFast, is10000xFast) </td></tr><tr valign="top"><td>initBody</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>toggleBody</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>showBody</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>hideBody</td><td>function</td><td>function (evt) </td></tr><tr valign="top"><td>forkSetup</td><td>function</td><td>function () </td></tr><tr valign="top"><td>round</td><td>function</td><td>function (num, places) </td></tr>
      </tbody>
  </table>


## About ChiliPeppr

[ChiliPeppr](http://chilipeppr.com) is a hardware fiddle, meaning it is a 
website that lets you easily
create a workspace to fiddle with your hardware from software. ChiliPeppr provides
a [Serial Port JSON Server](https://github.com/johnlauer/serial-port-json-server) 
that you run locally on your computer, or remotely on another computer, to connect to 
the serial port of your hardware like an Arduino or other microcontroller.

You then create a workspace at ChiliPeppr.com that connects to your hardware 
by starting from scratch or forking somebody else's
workspace that is close to what you are after. Then you write widgets in
Javascript that interact with your hardware by forking the base template 
widget or forking another widget that
is similar to what you are trying to build.

ChiliPeppr is massively capable such that the workspaces for 
[TinyG](http://chilipeppr.com/tinyg) and [Grbl](http://chilipeppr.com/grbl) CNC 
controllers have become full-fledged CNC machine management software used by
tens of thousands.

ChiliPeppr has inspired many people in the hardware/software world to use the
browser and Javascript as the foundation for interacting with hardware. The
Arduino team in Italy caught wind of ChiliPeppr and now
ChiliPeppr's Serial Port JSON Server is the basis for the 
[Arduino's new web IDE](https://create.arduino.cc/). If the Arduino team is excited about building on top
of ChiliPeppr, what
will you build on top of it?

