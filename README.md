This example demonstrates how to use [Express](http://expressjs.com/) 4.x and
[Passport](http://passportjs.org/) to authenticate users using Snapchat.  Use
this example as a starting point for your own web applications.
## Configure SnapKit App

Login to the Snapchat developer portal using your Snapchat account.
https://kit.snapchat.com/portal/apps

Create a new testing app using these configurations:
* Skip the Analytics section
* Skip the App Info section
* Kits: choose Login Kit
* Skip the Permissions section
* Redirect URIs:  add http://localhost:3000/login/snapchat/callback
* Development Environment: select Web
* Save your client ID in another file
* Generate and save a client secret (save it in the file with the client ID)

Ensure that node is installed on your computer
https://nodejs.org/en/

## Instructions

To install this example on your computer, clone the repository and install
dependencies.

```bash
$ git clone https://github.com/SyraD/express-4.x-passport-snapchat-example.git
$ cd express-4.x-passport-snapchat-example
$ npm install
$ npm install express --save
```

The example uses environment variables to configure the consumer key and
consumer secret needed to access snapchat's API.  Start the server with those
variables set to the appropriate credentials.

Edit the line below (easiest not on the command line, copy and paste when done)
* CLIENT_ID = your client ID (in the saved file)
* CLIENT_SECRET = your client secret (in saved file)

Be sure to keep all of the changes in one line, as this is what launches the project. 
See link: https://nodejs.org/en/docs/guides/getting-started-guide/
* node starts the NODE app
* server.js is the file that we want to launch

So, calling the command below launches our project with the specificed variables.

```bash
$ CLIENT_ID=CLIENT_ID CLIENT_SECRET=CLIENT_SECRET SESSION_SECRET=whatever node server.js
```

Open a web browser and navigate to [http://localhost:3000/](http://localhost:3000/)
to see the example in action.
