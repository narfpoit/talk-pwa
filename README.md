[![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)](https://generalassemb.ly/education/web-development-immersive)

# Progressive Web Apps

It is widely believed that the next frontier of web development is creating web apps that are more powerful, faster to load, faster to use, and more accessible and responsive.

Enter **progressive web apps (a/k/a PWAs)**.

These are only a few of the enhanced features of web development that make progressive web apps exciting.  In this talk, we'll go through a high level overview of PWAs and what sets them apart.

## Prerequisites

-   Basic knowledge of web development and mobile app development
-   A mobile device that runs the latest version of [Google Chrome](https://www.google.com/chrome/browser/mobile/)
-   HTML, CSS, and JavaScript

## Objectives

By the end of this, developers should be able to:

-   Describe what a progressive web app (a/k/a PWA) is.
-   Identify characteristics and benefits of PWAs.
-   Use terminology to describe PWA development tools and technologies: manifest, service workers, and application shell architecture.

## Preparation

1.  Fork and clone this repository
2.  Open a 2nd browser window in [Google Chrome](https://www.google.com/chrome/browser/features.html?brand=CHBD&gclid=CjwKCAjwo4jOBRBmEiwABWNaMVaLRHvNRYZcUmAFh33hX-8NuSekPEYlVcL0HNOM6SC-9MRUgSTYYxoC-coQAvD_BwE&dclid=CLHHtZfWtdYCFcZGNwod7TMG8A)

## What is a Progressive Web App?

According to [Wikipedia](https://en.wikipedia.org/wiki/Progressive_web_app), Progressive Web App(s):

> is a term used to denote web applications that use the latest web technologies.

> are also known as Installable Web Apps or Hybrid Web Apps

> are regular web pages or websites, but can appear to the user like traditional applications or native mobile applications. The application type attempts to combine features offered by most modern browsers with the benefits of mobile experience.

What does this mean, exactly?  Allow me to show you...

## Follow-Along

In your Chrome browser, copy and paste the following text into your url bar:

```chrome://flags/#enable-add-to-shelf```

In the highlighted section, select "Enabled" in the drop down menu. Then, do the same for the following link:

```chrome://flags/#bypass-app-banner-engagement-checks```

Now navigate to:

https://deanhume.github.io/beer/

Disclaimer: Always drink responsibly!

## Characteristics of a Progressive Web App

![Characteristics of a PWA](https://i.imgur.com/hqot73Dh.jpg "Characteristics of a PWA")

What differences can you point out when you navigated to the [site](https://deanhume.github.io/beer/) above?

### Characteristics

These main technologies are what make PWAs distinctive. They are the core of components that set PWAs apart from what we commonly know as downloadable native apps and other standard web sites which require a fast internet connection to function optimally in your browser.

According to Google developers, now the leading champions of PWAs, the distinctive characteristics of PWAs are:

>**Progressive** - Work for every user, regardless of browser choice because they’re built with progressive enhancement as a core tenet.

>**Responsive** - Fit any form factor: desktop, mobile, tablet, or forms yet to emerge.

>**Connectivity independent** - Service workers allow work offline, or on low quality networks.

>**App-like** - Feel like an app to the user with app-style interactions and navigation.

>**Fresh** - Always up-to-date thanks to the service worker update process.

>**Safe** - Served via HTTPS to prevent snooping and ensure content hasn’t been tampered with.

>**Discoverable** - Are identifiable as “applications” thanks to W3C manifests and service worker registration scope allowing search engines to find them.

>**Re-engageable** - Make re-engagement easy through features like push notifications.

>**Installable** - Allow users to “keep” apps they find most useful on their home screen without the hassle of an app store.

>**Linkable** - Easily shared via a URL and do not require complex installation.

## Technologies

To develop PWAs, there is a set of commonly used technologies used:

### Manifest

A JSON-based centralized place to put metadata associated with a web application including:

* The name of the web application
* Links to the web app icons or image objects
* The preferred URL to launch or open the web app
* The web app configuration data for a number of characteristics
* Declaration for default orientation of the web app
* Enables to set the display mode e.g. full screen

A manifest is what enables users to have native-like mobile experiences on PWAs.

Code example of a **manifest**:

```{
  "name": "HackerWeb",
  "short_name": "HackerWeb",
  "start_url": ".",
  "display": "standalone",
  "background_color": "#fff",
  "description": "A simply readable Hacker News app.",
  "icons": [{
    "src": "images/touch/homescreen48.png",
    "sizes": "48x48",
    "type": "image/png"
  }, {
    "src": "images/touch/homescreen72.png",
    "sizes": "72x72",
    "type": "image/png"
  }, {
    "src": "images/touch/homescreen96.png",
    "sizes": "96x96",
    "type": "image/png"
  }, {
    "src": "images/touch/homescreen144.png",
    "sizes": "144x144",
    "type": "image/png"
  }, {
    "src": "images/touch/homescreen168.png",
    "sizes": "168x168",
    "type": "image/png"
  }, {
    "src": "images/touch/homescreen192.png",
    "sizes": "192x192",
    "type": "image/png"
  }],
  "related_applications": [{
    "platform": "web"
  }, {
    "platform": "play",
    "url": "https://play.google.com/store/apps/details?id=cheeaun.hackerweb"
  }]
}
```

### Service Workers

 > Technically, Service Workers provide a scriptable network proxy in the web browser to manage the web/HTTP requests programmatically. The Service Workers lie between the network and device to supplement the content. They are capable of using the cache mechanisms efficiently and allow error-free behavior during offline periods.
 - Wikipedia



Benefits

* Capable of handling the push notification easily
* Synchronise data in the background
* Capable of responding to the resource requests originate elsewhere
* Receive centralized updates

### Application Shell Structure

The Basic User Interface or "shell" of the Responsive Web Design (RWD) is stored by Service Workers in the cache.  This enables users to rapidly use the app regardless of connectivity.

<!-- refer to atom project here -->

## Caveats

Although most browsers support PWAs, one notable exception is Safari.  There's been an on-going debate about whether Apple should support this type of app development, whether they do remains to be seen.

Another downside of PWAs is building a large app that is highly interactive (like a game) or performs intense tasks, PWAs may not be the way to go as there are storage limits in browsers.

## Framework Support

Currently, the following frameworks support PWA development, though there could be other ways to integrate into your existing application.

* React
* Angular
* Vue.js

## Additional Resources

-   [Intro to Progressive Web Apps by Google](https://www.udacity.com/course/intro-to-progressive-web-apps--ud811)
-   [Service Workers: An introduction](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers)
-   [Web App Manifest](https://developer.mozilla.org/en-US/docs/Web/Manifest)
-   [Service Workers](https://developers.google.com/web/ilt/pwa/introduction-to-service-worker)
-  [The Ultimate Guide to PWAs](https://scotch.io/tutorials/the-ultimate-guide-to-progressive-web-applications


## [License](LICENSE)

1.  All content is licensed under a CC­BY­NC­SA 4.0 license.
1.  All software code is licensed under GNU GPLv3. For commercial use or
    alternative licensing, please contact legal@ga.co.
