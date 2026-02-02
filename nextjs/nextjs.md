Q1) What is SSR, CSR, SSG, ISR in next js?
Ans:- 
**Server-Side Rendering (SSR):-**
--SSR means the server prepares fully rendered HTML pages with dynamic data on every request.
--Examples include traditional frameworks like PHP, Ruby on Rails, and modern React frameworks like Next.js.
--Generates fresh HTML on each request, server sends ready-to-use HTML with dynamic data.

Pros:
--SEO-friendly as web crawlers get fully rendered HTML content.
--Fast initial page load with ready-to-display HTML.

Cons:
--Full page reload on every navigation causing slower user experience.
--Every request triggers dynamic HTML generation, increasing server load.
--Loading JS and assets on each page load can affect speed.

**CSR (Client-Side Rendering):-**
--Client downloads minimal HTML + JS bundle; all rendering and routing happen in the browser.
--An empty index.html loads a JavaScript bundle controlling routing and page rendering client-side.
--Navigation between pages (home, about, contact) happens without server reloads, ensuring fast UI transitions but poor SEO.

Pros:
Fast navigation, good for internal apps without SEO needs.

Cons:
Bad SEO and slow initial load.

**SSG (Static Site Generation):-**
--Pages are pre-rendered during the build process, stored as static HTML.
--Ideal for content that rarely changes (e.g., blog posts, documentation).
--Signified in Next.js by a “dot” or circle icon indicating static prerendered pages.

Pros:
Best for rarely changing data (blogs, docs); very fast, SEO-friendly

Cons:
data updates require rebuild.

**ISR (Incremental Static Regeneration):-**
--Extends SSG by allowing static pages to be periodically refreshed/updated after build.
--Builds on SSG by specifying a revalidate time interval (e.g., 30 seconds).
--After the interval, the static HTML is regenerated on the server with fresh data without requiring a full rebuild.
--Solves the stale content problem of SSG while maintaining performance benefits.

Pros:-
Combines benefits of SSG with fresh data

Cons:-
solves stale content problem with configurable revalidation time.

**Emergence of Single Page Applications (SPA) and Client-Side Rendering (CSR)**
--SPA architecture downloads a minimal index.html (mostly empty except for a div and a linked JS bundle).
--All routing and page rendering happen on the client side via JavaScript.

Advantages:
--No full page reloads on navigation; fast and snappy user interactions.
--Only one JS bundle is downloaded initially; subsequent navigation happens without server requests.

Disadvantages:
--index.html is almost empty, causing poor SEO because crawlers can’t access content easily.
--Large JS bundles can cause slow initial load times.
--Data fetching happens via APIs (e.g., REST), fully on the client side.


