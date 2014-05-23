#LiveOak Gallery Example QuickStart

This Openshift QuickStart will install the LiveOak Gallery example. The Gallery example show cases how to install binary objects to LiveOak using the MongoDB GridFS system.

Documentation for the Gallery example can be found here:

https://github.com/liveoak-io/liveoak-examples/tree/master/gallery

#Instruction

To install the quick start from the 'rhc' tool:

```
rhc app create myGalleryApp diy --from-code git://github.com/liveoak/openshift-liveoak-gallery-quickstart
```

or install from the openshift console using the DIY cartridge with the source code option set to git://github.com/liveoak/openshift-liveoak-gallery-quickstart 


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

The easiest way to do so is to install the LiveOak example quickstart which can be found here: https://github.com/liveoak-io/openshift-liveoak-example-quickstart
