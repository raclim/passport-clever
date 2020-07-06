# Clever Instant Login for Passport.js 

Passport strategy for Instant Login with Clever

## Installation 
Install the package via npm: `npm install passport-clever`

## Usage 
Initialize the strategy as follows: 

    ```
    const AppleStrategy = require('passport-apple');
    passport.use(new AppleStrategy({
        clientID: "",
        clientSecret: "",
        callbackURL: "",
        passReqToCallback: true
    }, function(req, accessToken, refreshToken, profile, cb) {
    cb(null, accessToken);
    }));
    ```

Add the login route: 
`app.get("/login", passport.authenticate('clever'));`

## Disclaimer 
This repository is NOT developed, endorsed by, or even related at all to Clever. This library was implemented solely by the community's hardwork, and based on information that is public on Clever Developer's website. The library merely acts as a helper tool for anyone trying to implement Clever's Instant Login.