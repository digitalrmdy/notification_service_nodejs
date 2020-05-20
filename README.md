# Notification Widget UI BFF (NodeJS)

This is a Node.js backend service library to create a BFF service for the Notification Widget. The widget provides a notification. This service is matched by a [corresponding UI](https://github.com/digitalrmdy/notification_widget_angular).

There is a **demo service**, see below for instructions on running it.

## How to use

### Installing


Then install (you will need to be on the digipolis network):

```sh
> npm install @acpaas-ui-widgets/nodejs-notification-widget
```

### Using

Express example:

```js
const express = require('express');
const app = express()
const router = express.Router();
const notificationModule = require('@acpaas-ui-widgets/nodejs-notification-widget/src/notification');

notificationModule(router, '/api/v1/notifications')
app.use('', router);

app.listen(3000);
```



## Run the demo app

Create a .env file containing:

```sh
PORT=3002
API_KEY=<client id>
NOTIFICATON_API='https://api-gw-a.antwerpen.be/acpaas/in-app-notification/v2/'
```

(Remove the -a extension in the URL's to use the production api.)

Run the service:

```sh
> npm install
> npm start
```



Run the test suite:
```sh
> npm run test
```
(Coverage file generated in the coverage folder)

## Service Specification

Specifications described in the [postman collection](Notification%20Widget%20NodeJS.postman_collection.json).
Use the collection to call the demo api.

## Contributing

We welcome your bug reports and pull requests.

Please see our [contribution guide](CONTRIBUTING.md).

## License

This project is published under the [MIT license](LICENSE.md).

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.3.10.
