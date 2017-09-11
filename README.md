# ionic-environment-variables
Demonstration on how to easily setup environment variables in Ionic.

Sets environment variables based on if Ionic >= 3 is running with the --prod flag.  Adds just a single line to Ionic's default Webpack configuration.

If you need more than dev and prod (all that Ionic supports), you can use your Node environment (NODE_ENV) instead. For this demo both are used, but in a real app choose one, using both isn't intuitive.

After changing the Webpack config, all the logic is encapsulated in the environment-variables module, so it's easy to copy and paste this solution into any Webpack configured Angular 4 app.

### Use 'dev' environment variables
`ionic serve`

### Use 'prod' environment variables 
`npm run ionic:serve:prod` as ionic serve does ignore the --prod option.
Or simply set NODE_ENV to 'prod' before running serve, which is what that npm script does.

### Do 'prod' builds for a platform
When building for a platform you can use e.g. `ionic cordova build ios --prod` or `ionic cordova emulate ios --prod` as a shorthand for using the 'prod' environment variables in your build.

### Use 'qa' environment variables 
`npm run ionic:serve:qa`
Or simply set NODE_ENV to 'qa' before running serve, which is what that npm script does.

Companion to [roblouie's](https://github.com/roblouie) tutorial here, upgraded to Ionic 3 with Angular 4 http://www.roblouie.com/article/296/ionic-2-environment-variables-the-best-way/
