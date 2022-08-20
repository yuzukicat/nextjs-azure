## nextjs-azure
Allows you to host your nextjs applications on azure.
The overarching goal of this library is to give you the best possible experience and performance of Azure without being too opinionated on which services you use and how your application is configured.

Currently, this library is **NOT** production ready. I use this library for my pages/api folder across 3-4 of our projects but I do not use any getInitialProps/getStaticProps, etc.
I'm in the process of making this production ready as fast as possible.

```ts
npm i nextjs-azure
npx nextjs-azure
```


### Features
- ✅ getInitialProps
- ✅ getServerSideProps
- ✅ getStaticProps
- ✅ /pages/api
- 🚧 _middleware [refer to roadmap]
- 🚧 Image optimization [refer to roadmap]
- 🚧 Rewrites/Redirects [refer to roadmap]
- 🚧 ISR [refer to roadmap]
- 🚧 Webpack plguin that allows you to have pages/api routes that trigger from native bindings [refer to roadmap]
- ❓ Localization [refer to roadmap, support = unknown]
- ❓ AMP [refer to roadmap, support = unknown]

The build output should generate 3 folders:
- ./out - The frontend folder, this contains all the pre-rendered HTML pages.
- ./api - This is your pages/api folder if you're running NextJS full stack, this contains your code wrapped in an Azure compatibility function signature.
- ./ui-backend - This contains all the backend functions and code to render your UI pages on the server if you're using getInitialProps.


You are responsible for routing depending on which respective Azure services you use. The following routers are coming in the following priority order:
1. static-web-apps-router
2.  apim-router

### Deployment
You are responsible for deployment, the recommendation would be to use IAC which is a technique to make infrastructure part of your git workflow.
The following IAC setups are coming in the following priority order:

1. pulumi
2. terraform


### Goals
- Offer best in class performance on Azure for hosting NextJS applications - Taking into account best services to use, and endless optimizations for cold start, parse time, download time and more.
- Feature complete NextJS hosting including _middleware and image optimization.
- Non-http function app bindings support with in built integration with NextJS (blob bindings, event hub, etc.)
- Eventually support AWS
- Eventually support hybrid cloud with cloudflare

### Bugs:
- Open an issue. I'll get back to you as soon as I can

### NextJS Advice and Support
- Just reach out


