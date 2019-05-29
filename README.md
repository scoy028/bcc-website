# Brooklyn Community Chorus

_Come Sing With Us!_

The Brooklyn Community Chorus (BCC) is a self-governing, egalitarian organization, open to all singers from diverse backgrounds, ages, and musical experiences. BCC is dedicated to exploring a variety of musical styles, including classical, spiritual, show tunes, folk, world, jazz, rock, and pop, and performed in both large-group and smaller ensemble settings. BCC focuses on vocal and choral techniques, creating a sense of musical and group harmony, and having serious fun.

We gather and rehearse weekly on Wednesday evenings from 7:30pm-9:40pm at the Old First Reformed Church in Park Slope, Brooklyn. If you are interested in singing with us in a future semester, please [fill out the waitlist form here](https://goo.gl/forms/wUYMNkjKZo2PtULP2)! Performances are held a few times a year at our home location and elsewhere.

## Deployment

Check out the final site, deployed through Heroku: [Brooklyn Community Chorus](https://brooklyncommunitychorus.herokuapp.com/)

## Dev Setup

* Run the following command:

```
git clone https://github.com/scoy028/bcc-website.git
```

Now that you've got the code, follow these steps to get acclimated:

* `npm install`, or `yarn install` - whatever you're into
* Create two postgres databases: `bcc-website` and `bcc-website-test`
  * By default, running `npm test` will use `bcc-website-test`, while regular development uses `bcc-website`
* Create a file called `secrets.js` in the project root

  * This file is `.gitignore`'d, and will _only_ be required in your _development_ environment
  * Its purpose is to attach the secret env variables that you'll use while developing
  * However, it's **very** important that you **not** push it to Github! Otherwise, _prying eyes_ will find your secret API keys!
  * It might look like this:

  ```
    process.env.GOOGLE_CLIENT_ID = 'hush hush'
    process.env.GOOGLE_CLIENT_SECRET = 'pretty secret'
    process.env.GOOGLE_CALLBACK = '/auth/google/callback'
  ```

* To use OAuth with Google, complete the step above with a real client ID and client secret from Google
  * You can get them here: https://console.developers.google.com/apis/credentials

## Dev Start

`npm run start-dev` will make great things happen!

If you want to run the server and/or webpack separately, you can also `npm run start-server` and `npm run build-client`.

From there, just follow your bliss.
