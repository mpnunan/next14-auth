### Template with Next.js 14, TypeScript, and Firebase authentication

to use:
run 'npm install'
update env
start server with 'npm run dev'

'/app'  routes do not use authentication. you can customize the root layout in '/app/layout.tsx'

'/app/user' routes do use authentication. you can customize the authenticated page layout in '/app/user/layout.tsx'

if you want the entire app to be authenticated, copy the contents of '/app/user/layout.tsx' into '/app/layout.tsx' and then delete the '/app/user' folder


if you want to use axios, I made a custom config in '/utils/axiosConfig.ts'. you can add auth headers to that config, or add:

``` data.defaults.headers.common.Authorization = uid; ``` to the first line of any function you are passing a uid as an auth header

this template is a work in progress. specifically, '/utils/context/AuthContext.jsx' is still a JavaScript file instead of a TypeScript file because I still haven't figured out how to resolve the type errors
