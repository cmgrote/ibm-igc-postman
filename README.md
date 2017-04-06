The IGC REST API Explorer interface is nice and handy, but not always the easiest to use (e.g. given its tiny input text boxes, needing to manually decipher how to invoke the same API through a program, etc).

Enter Postman -- a tool that makes it easy to invoke API endpoints, generate code snippets for a variety of languages, and copy / paste / save responses.

# Using these assets

First and foremost, you'll of course need to grab Postman (https://www.getpostman.com).  The collection and environment files can both be imported simply by using the `Import` button in the upper-left of the Postman UI.

## Overview

After importing, all of the REST API endpoints are available under the "Collections" tab of Postman (on the left), and the environment(s) will be available in the drop-down in the upper-right.  In the following example, `IGC - 11.5.0.1ru7` is a collection containing all the API endpoints in various sub-folders, and `CAP - InfoSvr` is an environment.

![Overview](https://github.com/cmgrote/ibm-igc-postman/blob/master/wiki-images/overview.png)

## Calling an endpoint

The endpoints are all listed within the folders under the collection, in the same groupings (and order) as they appear in the REST API Explorer.  Simply click one, and the details for it will be pre-entered into the rest of the screen.  For example, after clicking an endpoint that takes parameters you can click the `Params` button just to the right of the URL and see a form to enter any values for those parameters before calling the endpoint by clicking the big blue `Send` button.

![Params](https://github.com/cmgrote/ibm-igc-postman/blob/master/wiki-images/params.png)

**Quick note on environments**: note that the host name, port, username and password of the request are parameterised -- this is where environments come in.  If you are using your own environment, you can add its details in the upper-right by defining a new environment, or simply edit the environment you've imported.  You just need to define `username`, `password`, `host`, and `port` in your environment, select your environment from the list, and then you'll be able to then make use of all the endpoints without any changes to the endpoints themselves.

## Viewing the response details

The response details are then displayed at the bottom of the screen, along with some basic metrics on the call (e.g. response time, status code, etc).  The response can be easily saved by clicking the `Save Response` button, copied to the clipboard with the copy icon, or re-formatted using the data format drop-down (`JSON` in this example).

![Response](https://github.com/cmgrote/ibm-igc-postman/blob/master/wiki-images/response.png)

## Generating code to do the same invocation programmatically

Finally, you can generate a quick code snippet for how to do the same API call programmatically by clicking the orange `Code` link just under the `Send` and `Save` buttons towards the upper-right of the screen.  This pops up a code generator, in which you can select the particular language you'd like to generate the snippet for:

![Code-gen](https://github.com/cmgrote/ibm-igc-postman/blob/master/wiki-images/code-gen.png)

For example, if you prefer using NodeJS and its popular `request` module:

![NodeJS-request](https://github.com/cmgrote/ibm-igc-postman/blob/master/wiki-images/code-gen-node-request.png)
