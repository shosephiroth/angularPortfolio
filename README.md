# AngularPortfolio

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.2.2.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).


---------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Notes: 

## 11/8/21

initial commit took some time, it's been a couple months since using Angular. The commands I followed were:\
cd\
mkdir\
ng new\
ng serve\

I was then hit with an error that would not allow me to build:

"The serve command requires to be run in an Angular project, but a project definition could not be found"

This led me to https://stackoverflow.com/questions/53096996/angular-cli-error-the-serve-command-requires-to-be-run-in-an-angular-project-b

I learned to try:

ng update @angular/cli

Still no dice. I had a new error message: "Error "Your cache folder contains root-owned files, due to a bug in previous versions of npm" while "npx create-react-app example_app""

Next I found this: https://www.c-sharpcorner.com/article/solution-of-angular-npm-error-npm-error-package-install-failed-see-above/

and tried:

npm cache verify  
npm cache clear -- force  

Next I ran:

npm install -g @angular/cli@8.2.2

Then:

npm install --legacy-peer-deps

and lastly:

ng serve

And now I can see this:\
![Screen Shot 2021-11-08 at 4 35 07 PM](https://user-images.githubusercontent.com/44537080/140824271-ea77e417-9b78-4138-8a9a-13aeba9183f2.png)

Next I decided to add Bootstrap. I found this in my search for how to do accomplish this since I'm using Angular 8.2.2. Here's what did not work:\
https://stackoverflow.com/questions/37649164/how-to-add-bootstrap-to-an-angular-cli-project

I realized the particular version would come into play so I kept searching and found this source. This did work:\
https://www.itsolutionstuff.com/post/how-to-add-bootstrap-in-angular-8-install-bootstrap-4-in-angular-8example.html

And now my page looks like this!:\
![Screen Shot 2021-11-10 at 3 05 03 PM](https://user-images.githubusercontent.com/44537080/141185960-ae4afeb7-198e-40aa-aefd-4c026a0ad5e4.png)

Took me some time to figure out how to replace the Angular icon with my face. Now you can see my big head at its regular size (depending on your screen size lol)\
Ultimately what worked is that I had to change the name of the image to favicon.ico and update the file path urls in place. I learned some browsers look for the icon differently so you need to change the file name and update the paths, not just 1 or the other:

https://stackoverflow.com/questions/40817280/how-to-change-angular-cli-favicon
https://reactgo.com/angular-change-favicon/
https://www.w3.org/2005/10/howto-favicon

![Screen Shot 2021-11-10 at 4 17 33 PM](https://user-images.githubusercontent.com/44537080/141195582-ada7d7d5-6bf5-42bd-b323-e5fb111ef1d6.png)
