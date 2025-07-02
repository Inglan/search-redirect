# Search Redirect

1. Open uBlock settings
2. Go to the `Settings` tab
3. Scroll down and click `I am an advanced user`
4. Click the settings button next to `I am an advanced user`
5. Find `userResourcesLocation`
6. Replace `unset` with:
```
https://github.com/Inglan/search-redirect/raw/refs/heads/main/redirect.js
```
7. Go back to uBlock settings
8. Go to the `My filters`
9. Enter one of the following
For Brave Search (recommended)
```
bing.com##+js(brave.js)
```
For Google
```
bing.com##+js(google.js)
```
10. Done!

## Why is this a uBlock script
Our school force installs uBlock (nice one) and there is basically no other way to run userscripts

## How do I know this isn't a virus
Here is the code with explanations
```javascript
// Check if path is /search
if (location.pathname == "/search") {
// Set host (domain name) to google or brave
  location.host = "google.com/search.brave.com"
}
```
You can see this is basically the same code as in the URL above

## Why does our school even enforce bing
Google thinks our IP is being used for abuse. The school *could* have contacted Google about it, but they didn't. This means we get constant Captchas when using Google.
