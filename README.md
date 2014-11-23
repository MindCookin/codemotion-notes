What if everything is awesome?
--
https://twitter.com/codepo8

* addy osmani talk in web speed
* http://webpagetest.org
* Polyfill as a service
* Flexbox
* Webrtc for data not only media
* Offline
* Web components and shadow dom
* state in the componentised web
* Talk live! In javascript

Lean NodeJs
--
https://twitter.com/borillo

__Development:__
* Gulp
* browserync
* vb en karma
* Google Web starter kit

__Test:__
* Protraktor
* ModernIE

__Deploy:__
* Unix upstart
* Nodejitsu > forever (antiguo)
* Fusion passenge
* PM2 (moderno)
* (Cluster, no downtime, proxy)

W3C perf
--
https://twitter.com/igrigorik
http://bit.ly/1xHpjJY

High performance networking in Google Chrome (web)
* window.performance
* timing.js

Introduction to __Resource Timing API__ (coming from users device feedback) (web)

Perf best practices:
* Perf regression tests (on every build)
* Synthetic perf test (uptime + perf monitoring)
* RUM-based performance analytics (real world user experience)

Resource Timing + Navigation timing (which protocol you use?, what was the http overhead, transfer size, decoded size?)

User perceived performance:
* Moving beyond window.onload
* Measuring perf from user experience

__User-timing__ (from window.performance) -> Pat Mills polyfill

__Page Visibility API__
// more things I didn’t write
“blocking beacons” → a tag ping=URL → Beacon API (best) navigator.sendBeacon() → supported by google analytics

__New API’s and proposals:__
* Sometimes user cannot reach our site (DNS fail, TCP, TLS) → Error Logging API → browser sends navigation error reports in the background → in Chrome, Domain Reliability
* Server Timing API → why it tooked so long?: time spent (slow DB, app server), delay in provide, etc… → server provides metrics via HTTP response header → Client exposes server metrics via Javascript API → (w3c.org /….../public-web-perf/2014Nov/0029.html)
* Client fetching a resource → chrome://dns, chrome://histogram, chrome://predictors → browser try hard to hide latency
* Early fetch of critical resources makes things fast →  Chrome preloader → rel=”preload” → github.com/w3c/resource-hints
rel=“preconnect" + speculative fetching (based in user action, anticipate next user action)
* Communicating hints via http link headers(s)
* Frame Timing API: RUM (real user management) for rendering performance → how render and composite stuff (animation, scrolling) works in our user device → github.com/w3c/frame-timing

_public-webperf@ mailing list_

Mobile Backend
--

__Firebase__ → client is more than rendering (codinghorror.com/the-tablet-turning-point) → Smart client + Client Library

_Realtime Database:_
NoSQL, JSON Database
Push updates in milliseconds
Simple Security model
data mapped to URL

_Firebase authentication:_
email & pass
OAuth
custom auth tokens

Coding is simple (Java and JS API)
Authentication Offline
Offline Capabilities →  store in device much of the app
Detect presence

How Web Standards are born ¿?
--
https://twitter.com/brucel

Standarisation madness:
* sausages and laws
* saussages and politicians
* two horses asses as railways
* unstandards railways in spain to prevent france invations
* css colours and porn actors
* retrospective standarization

canvas first in Safari → reverse ingeneering by IE ¿? →

html5doctor: interview with Ian Hickson
canvas → closing tag for fallback
video → closing tag for fallback
picture → closing tag for fallback

XHTML2 → “brain standards” → didn’t work
95% doesn’t validate

HTML5 was made to support old content
“Wilbur” XHTML 3.2 → XHTML3 too differnet, just as XHTML2 → full of weird things that does not have to do with real life
Always backwards compatibility
Appcache → not the right way to work offline (read Hixie) → Service Workers were made to fix it (GOOD)

Jake Archibald @ Google

https://extensiblewebmanifesto.org

standards tend to be slow → give developers the ability to make whatever they need i.e: appcache vs service workers → There’s an API for that
open standards → Not one enterprise, let people add → web components → you can extend the existing elements
openwebmanifesto?
w3c specifiction forum
WebAPI/DesignGuidelines → use case 1st

Redis
--
https://twitter.com/supercoco9

speed, open source, makes you think (antes de guardar saber cómo lo voy a leer), atomicity (monothread), flexible data persistence, data distribution

The redis manifesto: poem, against complexity, optimize for joy

Fworks: Crashlytics

SVG (Sara Soueidan)
--
https://twitter.com/SaraSoueidan
https://slides.com/sarasoueidan/working-with-svg-a-primer/

_FirefoxDevelopmentEdition_

SVG since 1999. Good for resolution madness. scalable & resolution-independent. SVG human-readable. easily minified & Gzipped. smaller than jpeg and gif except:
* complex images
* dimensions
* graphic effects
* continous tones
* icons are the best candidate for SVG
* good browser support.

__Are accessible__ (title and desc)(role and aria for old browsers).
sitepoint/tips-accesible-svg

_Have Photoshop-like capabilities_ (filters, shadows, etc..). Stylobate and interactive: you can animate, JS, SMIL and Web Animations API
* smashing-magazine.com/“aninmation in SVG”
* Snap.svg (jQ for SVG)
* css trick
* cordons making SVGS responsive with CSS

_SVG Optimization_
* Outlines (break SVG in parts) vs accesibility
* SVG Editor by Peter Collin
* SVGO NodeJS based (use with care) optimizations as plugins
* SVG Now (SVGO in Adobe Illustrator)

_SVG Embedding techniques_
* inside an img
* as a background-image in CSS
* as an <object> (old, but lot of advantages)
* iframe
* embed (don’t use. old)
* svg tag. Everything great but it cannot be cached
* Fallback tip: don’t insert an img tag inside a fallback: doubles requests —> better as a background of the fallback div
* Use the technique you need, none is better for all implementations

_Inline SVGs as Data URIs :_
* can get svg inside ut8: Don’t use base64 —> CSS tricks —> inlining SVG in CSS could be bad for performance
* SVG Sprites
* SVG icons better than Icon Fonts —> csstricks
* Folder containing SVG icons > create SVG sprites > HTML-Inline SVG Sprites (<symbol> elements to create svg sprite) > <use> tag (to show particular icon fron an sprite sheet)
* svgsprites use better than fonts —> csstricks
* grunt-svgstore
* viewBox (interesting, she recommends to read more)
* svg4everybody —> PNG fallback
* CSS-Embedded SVG Sprite > allows fallback for fallback > grunticon

http://css-tricks.com
http://smashing-magazine.com
http://codrops.com
http://sarasoueidan.com

Coffe ES6
--
https://twitter.com/Serabe

ESNext
Traceur

Babylon
--

Pointer Events polyfill —> Hands.js (developed by Microsoft)
babylon/playground —> in TypeScript
babylon/sandbox —> drag and drop assets

Mozilla: asm.js, simd.js

Practical Introduction to Functional Programming in ES6
--

https://github.com/dialelo/practical-fp-intro-workshop

Tech And Ladies
--

http://techandladies.com
