# prespa
An implementation of half ssr SPAs, with minimum tweaks in the frontend code.

## Purpose

### Why?

Modern web developments are often based on SPA (single page application), which provides a smoother user experience. But at the cost of potentially losing SEO (search engine optimization). 

SPAs are simply just an *index.html* and some *js* files, and most **meaningful** data are loaded through asynchronous requests. Which web crawlers might not be able to fetch.

There are lots of solutions such as **SSR**, **Prerender**, and are all great solutions. But SSR needs a whole lot more of configurations and are mainly feasible only with Node.js servers, and prerender will suffer long initial builds if there's too many routes.

### Idea

So the idea is to server the index.html through the server, add title, meta tags, and inject the ajax call into the window script. So that the SPA doesn't need to be changed much, and can improve SEO to a certain level.
