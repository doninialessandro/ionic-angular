# ionic-angular

[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

App development to learn ionic with angular. The focus is on learning the framework and not creating a production ready application, so testing and CD are out of scope.

## Roadmap and features

- [x] CI with [CircleCI](https://circleci.com/) to enable continuos integration.
- [x] [semantic-release](https://github.com/semantic-release/semantic-release) integrated with CI and [commitizen](https://github.com/commitizen/cz-cli) to use formalized commit message convention to document changes in the codebase
- [x] Navigation and routing
- [x] User input
- [x] State management with RxJS
- [x] [Firebase](https://firebase.google.com/) setup
- [x] env variables management without hardcoding them inside angular environments files.
- [x] Http requests
- [x] Google Maps
- [ ] Authentication

## How to start

#### `npm install`

Install the dependencies to run the app.

#### `npm start`

Runs the app in the development mode.<br /> Open
[http://localhost:4200/](http://localhost:4200/) to view it in the browser.

The page will reload if you make edits.<br /> You will also see errors in the console.

**IMPORTANT**
This application used behind the scenes [Firebase](https://firebase.google.com/). To test it be sure to have a Firebase account, create a Realtime Database, add the following rules to your DB:

```json
"bookings":{
".indexOn": ["userId"]
}
```

and last but not least export an `API_URL` env variable (in the same env where you will run `npm start`) with your db adress e.g.:

```
export API_URL=https://your-firebase-db-project-00a00.firebaseio.com
```

There is also Google Map service. Be sure to enable Geocoding API, Maps JavaScript API and Maps Static API from you GCP account and export your key as env variable as for API_URL. The env variable associeted with this service is `GOOGLE_MAPS_KEY`.

If you want to use the application with limited functionalites but without firebase and env variables download the app from [feat/state-management](https://github.com/doninialessandro/ionic-angular/tree/feat/state-management) branch.
