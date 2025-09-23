# This repository is now archived!

I created this a few years ago to try to resolve an issue I faced with integrating Clever's SSO into one of my projects. It was my first creating an `npm` package, and it felt really cool to see another stranger on the internet, [milanmdev](https://github.com/milanmdev), bring it to [a much more robust state](https://github.com/milanmdev/clever-passport)!

I don't believe that this exists on NPM anymore, but there's probably many more of these out there! 

---
# Clever Instant Login for Passport.js 

Passport strategy for Instant Login with Clever

## Installation 
Install the package via npm: `npm install passport-clever`

## Usage 
Initialize the strategy as follows: 

    ```js
    const CleverStrategy = require('passport-clever');
    passport.use(new CleverStrategy({
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
This repository is NOT developed, endorsed by, or related at all to Clever. This library was implemented solely by the community, and based on information that is public on Clever Developer's website. The library acts as a helper tool for anyone trying to implement Clever's Instant Login.
