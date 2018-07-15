## Sprint 1 - 6/2018

## Sprint 2 - 7/2018
This week I am setting up a basic production server so that we can have REST calls for database connectivity.
The plan is to use Express as an app server and to proxy calls to the database. Step by step:
* Split the root of the project into a client and a server directory
* Add a package.json to the root directory for shared dependencies and scripts that I want 
to be able to run from the root. For example, it will be nice to have `build`, `start:dev` and `start:prod`
at the root. **NOTE:** For now I am using bash in the top-level yarn scripts, so they won't
work on windows. I will keep the README platform agnostic.
* Update .gitignore to ignore node_modules everywhere.
* Add `concurrently` to the root to run two server procs at once. This is because in dev
we want to run the dev server proxying to the api server.
* Add a yarn scipt to start the servers.
* Add dev server proxying to webpack config in `client/package.json`

I used a couple blog posts about how to set up Express and the webpack dev server:
* https://medium.freecodecamp.org/how-to-make-create-react-app-work-with-a-node-backend-api-7c5c48acb1b0
* https://www.fullstackreact.com/articles/using-create-react-app-with-a-server/

### Open Issues
* Top-level yarn scripts use bash so they won't work on Windows. Eventually these should
become node scripts