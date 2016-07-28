# **Progressive Web App**
## **What is PWA?**

* > "A Progressive Web App uses modern web capabilities to deliver an app-like
user experience" - [Progressive Web Apps](https://developers.google.com/web/progressive-web-apps?hl=en)

* Native app features in mobile browsers (use them if available)
    * Offline functionality
    * Push notification
    * Content caching
    * Streams

* Internet connection is a feautre not a requirement (progressively)

## **Why you should care?!**
* Emerging markets will bring billions of new internet users
* These users will interact with your app on low end mobile devices with ~2G connection

## **App Shell**
* Design concept
* Provide the initial app UI from cache
    * Quick load time (comparable to native)
    * Improving user experience (showing something instantly)
* Load the content afterwards

## **Caching**
### Strategies
* cache first
* network first
* cache only
* network only
* fastest

### Cache busting
* Two type of resources: assets or data
* Assets: they change with every release
* Data: changes frequently
* Choose the cache invalidation strategy carefully

## **What is needed for a PWA** (subject to change)
* A manifest.json
```javascript
{
    "name": "My Progressive Web App",
    "short_name": "PWA",
    "start_url": "/index.html",
    "scope": "/",
    "display": "standalone",
    "theme_color": "#5eb3f9",
    "background_color": "#EEEEEE",
    "icons": [{
        "src": "/icon.png",
        "sizes": "128x128",
        "type": "image/png"
    }]
}
```
* Alternatively you can put everything into the index.html
* Service worker
    * Since Chrome 42.0 and Firefox 44
    * Limited in Opera 24
    * Under developement in Edge
    * Under consideration for Safari
* Fetch
* Streams (the new thing)
* HTTP2

## Alternatives (even more progressive)
* indexedDB (... pouchDB, webSQL)
* web worker (virtual DOM)
* App Cache (it is bad but also works)

## **Things to watch, read**
* [Instant Loading: Building offline-first progressive Web Apps](https://www.youtube.com/watch?v=cmGr0RszHc8) - **_Jake Archibald_**
* [Building for Billions](https://www.youtube.com/watch?v=Vmg1ECC2r2Q) - **_Tal Oppenheimer_**
* [sw-toolbox](https://github.com/GoogleChrome/sw-toolbox)
* [Service worker introduction](http://www.html5rocks.com/en/tutorials/service-worker/introduction/)
* [Offline cookbook](https://jakearchibald.com/2014/offline-cookbook/)
* [Jake Archibald resources page](https://jakearchibald.github.io/isserviceworkerready/resources.html)
* [PWA examples](https://pwa.rocks/)
* [App Shell](https://developers.google.com/web/updates/2015/11/app-shell?hl=en)
* [Service worker cookbook](https://serviceworke.rs/)

## THE END