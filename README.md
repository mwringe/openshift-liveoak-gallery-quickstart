#LiveOak Gallery Example QuickStart

This OpenShift QuickStart will create and configure a DIY gear to host the LiveOak Gallery example's HTML 5 client side code. It will requires access to a LiveOak instance already configured for the Gallery's backend logic.

For more information on how to configure a LiveOak gear in OpenShift with the example's backend already configured, please refer to the following quickstart:

https://github.com/liveoak-io/openshift-liveoak-examples-quickstart

Or refer it its application.json file available [here] (TODO: insert link here)

The Gallery example showcases how to load and unload binary content in LiveOak using the MongoDB GridFS system.

If you wish to run the Gallery example locally on your own machine, please see the Gallery example available here:

https://github.com/liveoak-io/liveoak-examples/tree/master/gallery

#Installing the Gallery Client Example

To install the quick start from the 'rhc' tool :

```
rhc app create myGalleryApp diy --from-code git://github.com/liveoak/openshift-liveoak-client-gallery-quickstart
```

or install from the openshift console using the DIY cartridge with the source code option set to git://github.com/liveoak/openshift-liveoak-client-gallery-quickstart 


This example assumes that you have your LiveOak instance running on a gear under your same account called 'liveoak'. If you have your liveoak instance running on another machine, please edit the diy/js/app.js.erb file to modify the host and or port to point to the LiveOak instance you want to use.

For example, if your LiveOak is running on a site called 'myAwesomeMBaaS.com' on port 80, you would modify the following line in diy/js/app.js.erb from

```
var HOST = 'http://liveoak-<%= ENV['OPENSHIFT_NAMESPACE'] %>.<%= ENV['OPENSHIFT_CLOUD_DOMAIN'] %>';
```

to

```
var HOST = 'http://myAwesomeMBaaS.com';
```

This example assumes that you have already configured your LiveOak instance for the 'gallery' example. 

The easiest way to do so is to install the LiveOak example quickstart which can be found here: https://github.com/liveoak-io/openshift-liveoak-examples-quickstart

#Configuring the Gallery Client Example

No other configurations are needed.

#Accessing the Gallery Client

After you your gear has been created, you should be presented with a link to access the website. Accessing the website will take you to the gallery example, which allows you to view and upload photos. Note that these photos are publicaly available to anyone in the example. 
