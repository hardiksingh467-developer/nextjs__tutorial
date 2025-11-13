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

To initialize a NextJS project, we will use the command: npx create-next-app@latest my-app --yes

There is a new feature in NextJS 16 that is TurboPack file system caching, which allows fir significantly faster compile tines between restarts.

## Project Structure
-- tsconfig.json
This is the configuration file for TypeScript. It defines what should be type checked, ignored and which rules to follow.
-- README.md
A simple markdown file which explains how to run the project and provides all other information
--postcss.config.mjs
This is a configuration file for postCSS which is a tool used to process CSS with different plugins, this is where tailwindCSS is added as a plugin
-- next-env.d.ts
This file should not be touched. It's simply used as a Next.js TypeScript configuration.
-- next.config.ts
This allows us to configure our NextJS features such as experimental options, image settings, build settings and more
-- eslint.config.mjs
This allows us to configure eslint 
-- public
We always need to put publicly available data in this folder
-- app
This is the primary folder in which we create our application 



To run our application write command: npm run dev

favicon.ico: any file in the root of our app with this name and extension will become the logo of our application 
globals.css: This is where you write all your custom css or tailwind css utilities
layout.tsx: This is the entry point of our application


## React Client and Server Components 
We can write 2 types of components, Client and Server Components
By default, the React Components we write are server components, but are they really
If we head to page.tsx, we have our home page component
If we write console.log("What Type of Component am I ?") before the return statement
Now it shouldn't have appear in the Browser log because it is a server component but in recent version of NextJS they actually extended that server component console.log, so that it appears in the browser console as well. But do not let this confuse you, this browser log, this server log is not happening in the browser, Next.js is just sharing it with us for convenience
Server Components are rendered on the server and their HTML output is then sent to the client, Since they are rendered in the server they can access server side resources directly like databases or file systems, this helps reduce the amount of JS sent to the client side application thus improving performance 

If server components really are that great, why can't every thing be a server component

If your component requires Browser interactivity, such as clicking buttons, navigation different pages, submitting forms, then you need to turn it into client component
For a client side component simply add a 'use client' simply at the top of the component

### Create a component folder in the app