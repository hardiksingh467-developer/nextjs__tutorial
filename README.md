# Next JS
What does NextJS has that React does not
In simple terms NextJS simplifies the development process and optimizes your application
It does that through it's primary functionalities, which we have to actively decide to use and others that we get out of the box by switching to NextJS

The very first benefit of NextJS is it's architecture

originally React has two type of components, functional and class based
but now the components are also categorized by where they run, if they run in User's browser, it is called a Client component and if it runs on the server, it is called a Server Component
Since Server components are more performant, NextJS converts every component we create into a Server component, unless if we specifically instruct it not to
The second NextJS benefit is the way it handles rendering, NextJS allows us to choose when and where will they be rendered
CSR: Browser renders, the server sends HTML document and JS code, which the browser executes to render the components, 
SSR: Renders the webpage on the server before transmitting it to the browser, this significantly improves Page SEO, CSR makes it almost impossible to crawl and index your websites as they are completely empty, sending pre-rendered code solves this issue
the third NextJS benefit is routing, in React, we need the react-router package to create routes, NextJS brings in file based routing, each folder's name becomes a route path, a folder name about will create a new /about route
NextJS evolved from a simple Frontend Library to a FullStack Framework, we can also create serverless functions to handle native backend API request