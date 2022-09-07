# Cypress bug reproduction

### STR

- run `npm run start` to bring up static test server and open Cypress
- Run the test in Chrome (I used 105)
- Open network inspector, filter to Fetch/XHR requests
- In the request headers section `Origin` is missing

- Remove `chromeWebSecurity: false` from `cypress.config.js`
- Do a full restart!! (automatic reload does not seem to be enough!)
- Run the same test, `origin` request header is present

Screenshot is also attached to this repo /Screenshot.png
