# [www.microfrontend.org](https://www.microfrontend.org/)





## Current Technologies at 2021

+ Single Page Application (SPA)
+ Progressive Web App (PWA)
+ Application as a Stream (AaaS)
    + javascript    
    + native
    + json based communication
    




## The Stack

How your stack looks will depend on how you want to render your application. Here is a comprehensive discussion about that, but in a nutshell:

### Client-side rendering(CSR); SPA; JSON APIs 
This is perhaps the most popular approach. It's great for building interactive web applications. But be aware of its downsides and steps to mitigate them. This is the approach I took, so we will talk about it in a lot of detail.

### Hybrid CSR; Both client-side and server-side rendering(SSR) 
With this approach, you still build your SPA. But when a user requests your app, for example, the homepage, you render the homepage's component into its static HTML in your server and serve it to the user. Then at the user's browser, hydration will happen so the whole thing becomes the intended SPA.

### Downsides
But there are downsides too. 
Apart from the extra maintenance costs, we will have to download the same payload twice—First, the HTML, and second, its Javascript counterpart for the 'hydration' which will exert significant work on the browser's main thread. 
This prolongs the 'First time to interactive', and hence diminishes the benefits gained from a faster 'First meaningful paint'.

### Examples
The technologies that are adopted for this approach are NextJs, NuxtJs, and GatsbyJs.



### Turbolinks
https://github.com/turbolinks/turbolinks
Turbolinks® makes navigating your web application faster. Get the performance benefits of a single-page application without the added complexity of a client-side JavaScript framework. Use HTML to render your views on the server side and link to pages as usual. When you follow a link, Turbolinks automatically fetches the page, swaps in its <body>, and merges its <head>, all without incurring the cost of a full page load.




### Phoenix LiveView
https://github.com/phoenixframework/phoenix_live_view

Phoenix LiveView enables rich, real-time user experiences with server-rendered HTML.

After you [install Elixir](https://elixir-lang.org/install.html)
in your machine, you can create your first LiveView app in two
steps:

    $ mix archive.install hex phx_new
    $ mix phx.new demo --live

#### Features

* Use a declarative model to render HTML on the server over WebSockets with optional LongPolling fallback

* Smart templating and change tracking - after connected, LiveView sends only what changed to the client, skipping the template markup and reducing the payload

* Live form validation with file upload support

* A rich integration API with the client with `phx-click`, `phx-focus`, `phx-blur`, `phx-submit`, etc. `phx-hook` is included for the cases where you have to write JavaScript

* Code reuse via components, which break templates, state, and event handling into reusable bits, which is essential in large applications

* Live navigation to enrich links and redirects to only load the minimum amount of content as users navigate between pages

* A latency simulator so you can emulate how slow clients will interact with your application

* Testing tools that allow you to write a confident test suite without the complexity of running a whole browser alongside your tests


## AaaS - Application as a Stream

AaaS is supported by WebStream.

+ WebStream is an ecosystem for web-development

## How WebStream work's?

Load any media on website without reload page, now stream each website without reload.
Over modularity each website can talk to another without barrier...

### Unikatowe ID

Id elementów DOM muszą być unikatowe dla aplikacji i jej elementów gdy są wyświetlane razem.
Rozwiązaliśmy ten problem poprzez dodanie nazwy aplikacji przed każdym id np. web-chat-header, web-admin-header, ...

    
### Supported media

Ładowanie mediów tekstowych, kodu aplikacji, filmów, głosu, itp.

+ html
+ txt
+ markdown
+ mp3
+ wav
+ js
+ php
+ python


# why?
Because we can improve our stack without clouds

[more about limitations of CLOUDS](CLOUDS.md)

## story
    
Gdy korzystamy z własnej implementacji frontend <-> mikroserwisy możemy napotkać niektóre z tych problemów:

+ wiele wersji tej samej biblioteki ładujących się z losową kolejnością i nadpisujących się,
+ style z jednej aplikacji nadpisywały drugą,
+ brak prostego sposobu na dodanie kolejnej aplikacji utworzonej w innym frameworku,
+ problemy z routingiem,
+ brak lazy loading.


## The Stack

How your stack looks will depend on how you want to render your application. Here is a comprehensive discussion about that, but in a nutshell:

    Client-side rendering(CSR); SPA; JSON APIs —
    This is perhaps the most popular approach. It's great for building interactive web applications. But be aware of its downsides and steps to mitigate them. This is the approach I took, so we will talk about it in a lot of detail.

    Hybrid CSR; Both client-side and server-side rendering(SSR) —
    With this approach, you still build your SPA. But when a user requests your app, for example, the homepage, you render the homepage's component into its static HTML in your server and serve it to the user. Then at the user's browser, hydration will happen so the whole thing becomes the intended SPA.

The main benefits of this approach are that you get good SEO and users can see your stuff sooner (faster 'First Meaningful Paint').

But there are downsides too. Apart from the extra maintenance costs, we will have to download the same payload twice—First, the HTML, and second, its Javascript counterpart for the 'hydration' which will exert significant work on the browser's main thread. This prolongs the 'First time to interactive', and hence diminishes the benefits gained from a faster 'First meaningful paint'.

The technologies that are adopted for this approach are NextJs, NuxtJs, and GatsbyJs.


### iframe
    
Wykorzystanie iframe, pozwala na łatwe wdrożeni, niestety ostylowanie jest trudne i niewygodne a dostępność dla ludzi korzystających z czytników ekranowych jest jeszcze gorzej. 

Najprostszy sposób, aby zacząć: możemy użyć okna postMessage() do komunikacji między aplikacjami.

   
### Single SPA


Jest to framework do komponowania ze sobą aplikacji frontendowych. Jeśli chcesz rozpocząć prawdziwy projekt, wybierz ten poniżej:

Mikrofrontend pozwala nam łączyć kilka aplikacji napisanych nawet w różnych frameworkach
Frameworki są tylko narzędziem, najważniejsza natomiast dla nas jest możliwość podzielenia aplikacji funkcjonalnie i przydzielenia tych części zespołom.

https://single-spa.js.org
    
    

### Frint

To kolejny framework do komponowania ze sobą aplikacji frontendowych. Bardziej elastyczny niż Single SPA, ale nowszy i mniej popularny:

https://frint.js.org

    
    
### Komponenty webowe

Nie jest to framework, ale funkcja przeglądarki i być może przyszłość Internetu. Oto artykuł na ten temat:

https://www.webcomponents.org/introduction
    
    

### Taylor

Framework ten wykorzystuje inne podejście, tworząc stronę routingu na backendzie za pomocą node.js. Jeśli pomysł Ci się podoba, warto zobaczyć:

https://github.com/zalando/tailor
    

## Current Technologies at 2021

+ Single Page Application (SPA)
+ Progressive Web App (PWA)
+ Application as a Stream (AaaS)
    + javascript
    + native
    + json based communication




### Turbolinks
    
https://github.com/turbolinks/turbolinks
Turbolinks® makes navigating your web application faster. Get the performance benefits of a single-page application without the added complexity of a client-side JavaScript framework. Use HTML to render your views on the server side and link to pages as usual. When you follow a link, Turbolinks automatically fetches the page, swaps in its <body>, and merges its <head>, all without incurring the cost of a full page load.




### Phoenix LiveView

https://github.com/phoenixframework/phoenix_live_view

Phoenix LiveView enables rich, real-time user experiences with server-rendered HTML.

After you [install Elixir](https://elixir-lang.org/install.html)
in your machine, you can create your first LiveView app in two
steps:

    $ mix archive.install hex phx_new
    $ mix phx.new demo --live
    

## More
+ [How to create a better front-end developer experience](https://developers.redhat.com/articles/2021/06/01/how-create-better-front-end-developer-experience)    
    
---
+ [edit](https://github.com/microfrontend-org/www/edit/main/README.md)
+ [git](https://github.com/microfrontend-org/www)
```
https://github.com/microfrontend-org/www.git
```
