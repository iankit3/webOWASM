# Performant Web Applications using WebAssembly
**INTRO**

## Why JavaScript is Slow
The Art of writing a fast and performant web application is quite limited due to sheer ability of Web technologies especially JavaScript of using all available CPU cores. It is due to the fact that JavaScript is Single threaded. And it was a well thought through and deliberate design decision by [Brendan Eich](https://en.wikipedia.org/wiki/Brendan_Eich) the creator of JavaScript who completed it in just 10 days, in the year 1995.    
Considering the time it was designed it was quite sufficient and fast. But in this modern era, Web Applications are doing a lot of complex and intensive tasks such as Video Editing, 3D Graphics and even Video Games. This requires the applications to be fast and responsive to keep the experince smooth.

## General ways to make fast Web Applications
SMALL size, fast load time, lazy-load,cache, Minimizing CRP .... This works well and proves to be sufficient for most of the web applications but not for the above mentioned use cases. They require a lot parallel threads running and doing the job but JavaScript lask it.

## Traditional/Ideal ways to make fast applications (Desktop applications)
In a traditional Desktop application, one can add more cores of CPU/GPU to get a faster and smoother experience.
This is all because the languages in which Desktop applications are written support multithreading and they give the programmer the ability to churn out all the CPU/GPU.

## Ways to bring those traditional patterns in Web
  * Approaches
  1. Add multi thread capabilities to JS
  2. Use a well established fast language
#Presented solutions 
 * Sols :-
   1. Nacl
   2. ASMjs
   3. WASM


__EXPLAIN WHY JS cannot.. It has Single Thread__
Why didn't it had multi-threading from day one.
The language was built in some 10 days and was to designed to be easy and approachable. And just to reiterate a well established notion 
 >Writing a multi-threaded code is hard.
