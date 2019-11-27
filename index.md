# Performant Web Applications using WebAssembly

With the [`write once and run anywhere`](https://en.wikipedia.org/wiki/Write_once,_run_anywhere) slogan rising again like it did in mid 70s and around 95, Developers need software that runs everywhere. Though there are many attempts to achieve that with the likes of Java, Qt which are more about making general purpose languages/tools run everywhere, including Web. Though it worked quite well for desktop applications but failed to make a mark in Mobile and Web applications scene.    
Now things have changed, developer tend to use Web Technologies for building Desktop/Mobile applications.
And it seems to be working well, thanks to great projects like [Electron](https://electronjs.org/) and [React-Native](https://facebook.github.io/react-native/) to name a few. This brought a paradigm shift and developers tend to move towards Web Technologies to build all types of applications.

Things were looking brighter but there were some bottlenecks because Web Technologies aren't mean't for general purpose Software Development. They are built specifically for making interactive web pages that why JavaScript, the language to the web is slow.

## Why JavaScript is Slow
The Art of writing a fast and performant web application is quite limited due to sheer inability of Web technologies especially JavaScript of using all available CPU cores. It is due to the fact that JavaScript is Single threaded. And it was a well thought through and deliberate design decision by [Brendan Eich](https://en.wikipedia.org/wiki/Brendan_Eich) the creator of JavaScript who completed it in just 10 days, in the year 1995.    
Considering the time it was designed it was quite sufficient and fast. But in this modern era, Web Applications are doing a lot of complex and intensive tasks such as Video Editing, 3D Graphics and even Video Games. This requires the applications to be fast and responsive to keep the experience smooth.

## Lets make it fast
Though JavaScript is slower than most of the general purpose languages, there are ways to improve the performance of web applications to get most out of it. There are many aspects to it, we won't get deeper into this.
But below are some general considerations for a performant WebApp.
 * Optimizing size and content efficiency using minification and caching.
 * Using [Service Workers](https://developers.google.com/web/fundamentals/primers/service-workers)
 * PWA using [PRPL](https://developers.google.com/web/fundamentals/performance/prpl-pattern#the_prpl_pattern)
 * Prioritizing content load order to improve [CRP](https://developers.google.com/web/fundamentals/performance/critical-rendering-path)
 * Using [CDN edge server](https://www.cloudflare.com/learning/cdn/glossary/edge-server/) for faster loading of common assets and files.

We just have scratched the surface, there are tons of ways/hacks to improve the speed of a Web Application. But all of them are still limited to a single thread with [Web workers](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API/Using_web_workers) being an exception.

## But why reinvent the wheel
The mentioned general approachs work well and are proved to be sufficient for most of the web applications but not for the above mentioned use cases. They require a lot of parallel threads running and doing the job but JavaScript lacks it.

In traditional Desktop applications scene, one can add more cores of CPU/GPU to get a faster and smoother experience of the application.
This is all because the languages in which Desktop applications are written, support multithreading and they give the programmers the ability to churn all the CPU/GPU out.

## Bringing the Wheel home
  1. Add parallel capabilities to JS.
  2. Use a well established and fast general purpose language.

## The Path to Parallel JavaScript
Not that this area is unexplored, there were quite remarkable successful attempts that carved the way for today's parallel JavaScript.    
[The Path to Parallel JavaScript](https://blog.mozilla.org/javascript/2015/02/26/the-path-to-parallel-javascript/)

         
<!-- ![PNaCl](https://raw.githubusercontent.com/iankit3/webOWASM/master/PNaCl.png) -->

<figure style="text-align:center">
  <img src="https://raw.githubusercontent.com/iankit3/webOWASM/master/PNaCl.png" alt="Program struture of Google's NaCl"/>
  <figcaption style="text-align:center">Program struture of Google's NaCl</figcaption>
</figure>


Below are some few popular ideas for parallel JS
   1. [NaCl](https://developer.chrome.com/native-client/nacl-and-pnacl)
   2. [ASMjs](http://asmjs.org/faq.html)

## Welcome WASM
Though the attempts made by NaCl and ASMjs are quite convincing, they weren't part of a standard web specification. But finally everyone with the idea of `fast` web, agreed and thus [WebAssembly](https://webassembly.org/) got adopted as [standard](https://webassembly.github.io/spec/) and is available across popular browsers.

## What's Next
Stay updated for Part 2 of the Series which will contain real world use cases where WebAssembly is solving serious business problems.


If you have any opinions about the above post feel free to comment or DM me Ankit(@iankit3)