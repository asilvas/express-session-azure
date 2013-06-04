# ExpressJS Session Store for Azure

Node.js express session store provider for Windows Azure table storage.


## Install

    npm install express-session-azure


## Usage

Typical usage for the most part:

    var express = require('express'),
        AzureSessionStore = require('express-session-azure');

    var app = express.createServer();

    app.configure(function(){
        app.use(express.cookieDecoder());
        app.use(express.session({ store: new AzureSessionStore({ name: "azure_storage_name", accessKey: "azure_storage_key" }) }));
    });
