# Angular Portfolio Project

## Please scroll past these instructions to see my development notes!

## Live site below:
https://mattx2k1.netlify.app/ \
[![Netlify Status](https://api.netlify.com/api/v1/badges/3ec0633c-c4d6-46e9-98f6-672cde573992/deploy-status)](https://app.netlify.com/sites/mattx2k1/deploys)

## Angular notes:

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

# Development Notes: 
Major rough draft here at the moment just to keep track of my thoughts, share my struggles and successes with this project. 

## 11/8/21

initial commit took some time, it's been a couple months since using Angular. The commands I followed were:\

```
cd\
mkdir\
ng new\
ng serve\
```

I was then hit with an error that would not allow me to build:

"The serve command requires to be run in an Angular project, but a project definition could not be found"

This led me to https://stackoverflow.com/questions/53096996/angular-cli-error-the-serve-command-requires-to-be-run-in-an-angular-project-b

I learned to try:
```
ng update @angular/cli
```

Still no dice. I had a new error message: "Error "Your cache folder contains root-owned files, due to a bug in previous versions of npm" while "npx create-react-app example_app""

Next I found this: https://www.c-sharpcorner.com/article/solution-of-angular-npm-error-npm-error-package-install-failed-see-above/

and tried:
```
npm cache verify  
npm cache clear -- force  
```
Next I ran:
```
npm install -g @angular/cli@8.2.2
```
Then:
```
npm install --legacy-peer-deps
```
and lastly:
```
ng serve
```
And now I can see this:\
![Screen Shot 2021-11-08 at 4 35 07 PM](https://user-images.githubusercontent.com/44537080/140824271-ea77e417-9b78-4138-8a9a-13aeba9183f2.png)

## 11/10/21

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

and here's my big head:\
![Screen Shot 2021-11-10 at 4 17 33 PM](https://user-images.githubusercontent.com/44537080/141195582-ada7d7d5-6bf5-42bd-b323-e5fb111ef1d6.png)

## 11/21/21

I didn't get a lot done since I'm busy with work and working on Unit 2 assignments in LC101. I did go through a fun period of breaking my code. In the past when I did this I was able to run these commands, and be back to working as if nothing had happened:
```
sudo npm cache clean --force 
npm cache clear -- force  
```
```
npm install
```
But this time, no dice. Here are the notes I took from that day:

### Something I learned:
1. Totally broke my angular app yesterday. I updated Angular in the middle of a project to get a Bootstrap Angular Navbar working. Instead brought my whole project down. I struggled with it for hours. Went down a stack overflow rabbithole but to no avail. Nothing I tried worked and it felt like it only made things worse. I was very frustrated but came to the realization I never pushed my committed changes to my remote repo/GitHub. This was actually a great learning experience because I know now I need to A). make a new branch for dealing with changes and then merge once I know they are working correctly. B). I need to not update in the middle of development (Instructors and TAs warned me but I was curious lol) unless I know exactly what I'm doing or have a mentor who can help guide me through the process. C). Commit my changes at working stages of development (which I knew but didn't want my job to see that I was working on code while working with them ( ͡° ͜ʖ ͡°) lol)
2. Experts say the best way to learn is to break your code and then try to fix it. Though I wasn't able to find a solution through StackOverflow or another source, recloning the repo, rerunning npm install (for node and and angular files/dependencies) got me back to where I was before I started making breaking changes. I copied over my working changes like resizing my profile image, adding link highlighting on hover, etc. by going into the broken project files and copying the text from the component.ts files. Worked like a charm.
------------------------------------------------------------------------

Here is what the site looks like now after some minor updates:

![Screen Shot 2021-11-21 at 7 36 47 PM](https://user-images.githubusercontent.com/44537080/142786105-c7a4ed05-da48-4f6c-9eec-a5f0080fac8e.png)

And if you hover your mouse over my picture you'll notice it now has a hyperlink and highlights the border of the picture. This going to help make my page look less static:


![Screen Shot 2021-11-21 at 7 36 56 PM](https://user-images.githubusercontent.com/44537080/142786293-8942074a-7089-42ba-8f2c-3aa453ff8462.png)


Next steps I want to do are add a Navbar which is what broke my code; Navbar being an Angular powered Bootstrap tool, Bootstrap was asking me to upgrade ANG CLI. Building one from scratch will be more fun anyways, I just wanted to try a template first to see how it would look/feel. 


