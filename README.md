# woden

Woden - JavaScript client for woden
Specification for Woden REST API
This SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.JavascriptClientCodegen

## Installation

### For [Node.js](https://nodejs.org/)

#### npm

To publish the library as a [npm](https://www.npmjs.com/),
please follow the procedure in ["Publishing npm packages"](https://docs.npmjs.com/getting-started/publishing-npm-packages).

Then install it via:

```shell
npm install woden --save
```

##### Local development

To use the library locally without publishing to a remote npm registry, first install the dependencies by changing 
into the directory containing `package.json` (and this README). Let's call this `JAVASCRIPT_CLIENT_DIR`. Then run:

```shell
npm install
```

Next, [link](https://docs.npmjs.com/cli/link) it globally in npm with the following, also from `JAVASCRIPT_CLIENT_DIR`:

```shell
npm link
```

Finally, switch to the directory you want to use your woden from, and run:

```shell
npm link /path/to/<JAVASCRIPT_CLIENT_DIR>
```

You should now be able to `require('woden')` in javascript files from the directory you ran the last 
command above from.

#### git
#
If the library is hosted at a git repository, e.g.
https://github.com/YOUR_USERNAME/woden
then install it via:

```shell
    npm install YOUR_USERNAME/woden --save
```

### For browser

The library also works in the browser environment via npm and [browserify](http://browserify.org/). After following
the above steps with Node.js and installing browserify with `npm install -g browserify`,
perform the following (assuming *main.js* is your entry file, that's to say your javascript file where you actually 
use this library):

```shell
browserify main.js > bundle.js
```

Then include *bundle.js* in the HTML pages.

### Webpack Configuration

Using Webpack you may encounter the following error: "Module not found: Error:
Cannot resolve module", most certainly you should disable AMD loader. Add/merge
the following section to your webpack config:

```javascript
module: {
  rules: [
    {
      parser: {
        amd: false
      }
    }
  ]
}
```

## Getting Started

Please follow the [installation](#installation) instruction and execute the following JS code:

```javascript
var Woden = require('woden');

var defaultClient = Woden.ApiClient.instance;

// Configure API key authorization: Bearer
var Bearer = defaultClient.authentications['Bearer'];
Bearer.apiKey = "YOUR API KEY"
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//Bearer.apiKeyPrefix['Authorization'] = "Token"

var api = new Woden.FileSystemApi()

var body = new Woden.CreateFolder(); // {CreateFolder} 


var callback = function(error, data, response) {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
};
api.createFolder(body, callback);

```

## Documentation for API Endpoints

All URIs are relative to *http://localhost:8080/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*Woden.FileSystemApi* | [**createFolder**](docs/FileSystemApi.md#createFolder) | **POST** /folder | Create folder
*Woden.FileSystemApi* | [**downloadFile**](docs/FileSystemApi.md#downloadFile) | **GET** /file/{hash} | Download file
*Woden.FileSystemApi* | [**getFolder**](docs/FileSystemApi.md#getFolder) | **GET** /folder/{hash} | Get folder
*Woden.FileSystemApi* | [**search**](docs/FileSystemApi.md#search) | **GET** /search/{name} | Search
*Woden.FileSystemApi* | [**updateFile**](docs/FileSystemApi.md#updateFile) | **PUT** /file | Update file
*Woden.FileSystemApi* | [**uploadFile**](docs/FileSystemApi.md#uploadFile) | **POST** /file | Upload file
*Woden.FileSystemApi* | [**versions**](docs/FileSystemApi.md#versions) | **GET** /versions/{hash} | Versions of file
*Woden.UserApi* | [**changeUser**](docs/UserApi.md#changeUser) | **PUT** /user | Update user password
*Woden.UserApi* | [**createUser**](docs/UserApi.md#createUser) | **POST** /user | Create user
*Woden.UserApi* | [**login**](docs/UserApi.md#login) | **POST** /user/auth | Login user into the system
*Woden.UserApi* | [**logout**](docs/UserApi.md#logout) | **DELETE** /user/logout | Logout user from the system


## Documentation for Models

 - [Woden.ChangePassword](docs/ChangePassword.md)
 - [Woden.CreateFolder](docs/CreateFolder.md)
 - [Woden.CreateUser](docs/CreateUser.md)
 - [Woden.Login](docs/Login.md)


## Documentation for Authorization


### Bearer

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header

