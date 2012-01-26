# Getting set up with node.js and Azure

[Inspired by Tim Taylor](https://github.com/toolbear/easy-breezy-node-heroku)

## Resources
* [GitHub](https://github.com/)
* [Node.js Developer Center](www.windowsazure.com/en-us/develop/nodejs)
* [Develop your first Node.js web application](http://www.windowsazure.com/en-us/develop/nodejs/tutorials/web-app-with-express/)
* [Express - node web framework](http://expressjs.com/)

## 1. Install Windows Azure SDK for Node.js
* Installs a set of powershell cmdlets for working with roles hosting node
* Installs node.js for windows
* Installs iisnode wrapper
* Note that version number is not pinned under Windows Azure

Pre-requisites

* Windows 7
* Azure Account - [free trial](http://www.windowsazure.com/en-us/pricing/free-trial/)

## 2. Create the node.js web app

If you ran the install in step 1 skip to "Creating a New Node Application"
* make sure to run Powershell as Administrator
* Run in the local emulator if your account is not set up yet
* note that unlike heroku you push the node_modules associated with your project

I like to add names to each of the commands

    New-AzureService helloazure
    Add-AzureNodeWebRole helloazureweb
    
Be sure to note the line of code in the sample
    var port = process.env.port || 1337
This allows the Azure environment to handle the port assignments.

## 3. Debugging
[Set up integrated debugging](http://tomasz.janczuk.org/2011/11/debug-nodejs-applications-on-windows.html)

also for simpler projects you can run
    node server.js
to get to your console output easily