# ContentfulAngular18

## Commands used
### Before start (if not have created a project, follow these steps)
1. Create a Angular Project using v18 (we don't specify a global cli version and that's why we type "npx")
``npx @angular/cli@18 new *<project_name>*``
    - You must be sure if you want to install "CSS" or options, and "SSR" in your project.

2. Start your project using "npx" to be sure if everything is fine.
``npx ng serve``

### Steps
1. To start fetching data from Contentful, start by creating an Angular service via the CLI. The g is shorthand for the generate command.
``npx ng g service contentful``

2. To make your first requests use the Contentful JavaScript client library and add it as a dependency to your project.
``npm install contentful``
    - https://github.com/contentful/contentful.js

3. Create a "services" folder in the same branch as app.
``mkdir services``

4. Create a "Contentful" service.
``npx ng g s Contentful``

5. Then go to "contentful.service.ts" file inside "services" folder and add the next line, below "import { Injectable } from '@angular/core';"
``import { createClient, Entry } from 'contentful';``

6. Then create a "environments" folder in the same branch as app.
``mkdir environments``

7. Create a "environment.ts" file inside "environments" folder.
``echo $null >> environment.ts``

8. Type the next command lines inside "environment.ts" file.
```
export const environment = {
    production: false,
    spaceId: '',
    accessToken: ''
}
```
    - Go "contentful.com", then enter in a Space, go to "Settings" below of your icon profile, create an API key and obtain your keys.
    - Remember to use 'Space ID' obtained from Contentful Settings for 'spaceId' inside environment.ts.
    - Remember to use 'Content Delivery API - access token' obtained from Contentful Settings for 'accessToken' inside environment.ts.

9. Type the next command lines to update your "environment.ts" file.
```
export const environment = {
    production: false,
    spaceId: environment.spaceId,
    accessToken: environment.accessToken,
}
```
    - If 'environment.ts' is not imported, remember to do it manually by: "import { environment } from '../environments/environment';" 

10. 

## Angular DOCS
``This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 18.1.0.``
### Development server
* Run `npx ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.
* Run `npx ng generate component component-name` to generate a new component. You can also use `npx ng generate directive|pipe|service|class|guard|interface|enum|module`.
* Run `npx ng build` to build the project. The build artifacts will be stored in the `dist/` directory.
* Run `npx ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).
* Run `npx ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.
