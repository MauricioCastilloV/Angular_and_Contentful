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



## Angular DOCS
``This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 18.1.0.``
### Development server
* Run `npx ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.
* Run `npx ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.
* Run `npx ng build` to build the project. The build artifacts will be stored in the `dist/` directory.
* Run `npx ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).
* Run `npx ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.
