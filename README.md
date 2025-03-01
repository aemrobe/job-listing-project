# Frontend Mentor - Job listings with filtering solution

This is a solution to the [Job listings with filtering challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/job-listings-with-filtering-ivstIPCt). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [Run The App](#run-the-app)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page
- Filter job listings based on the categories

### Screenshot

![](<./screenshot/mobile-view.png)

![](<./screenshot/desktop-view.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- [React](https://reactjs.org/) - JS library

### Run The App

After running `npm install` on the terminal, Run this command : `npm start`
Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### What I learned

I worked on this project in collaboration with my friends and my task was to create the companyProfile component and to filter the jobs based on the active filters which the user has selected from the templates. The major learning here was the filtering part.
I used the every method on activeFilters array(an array which contains all the filters selected by the user) to check if the all filters selected are meet by the jobs posted there. since it is every() method, it will return true if all of the filters are meet by the jobs which are posted so that the jobs which meets this criteria will be stored inside the filterJobs array and it returns false if one of the filters doesn't found on the job so that job won't be stored inside filterJobs array. A thing which to be noted here is that if any filters aren't selected from the template,the filtering won't take a place and it will simply display all the jobs which are found in the json.

```js
const filteredJobs =
  activeFilters.length === 0
    ? data
    : data.filter((job) => {
        return activeFilters.every((filter) => {
          if (job.role === filter) return true;
          if (job.level === filter) return true;
          if (job.languages.includes(filter)) return true;
          if (job.tools.includes(filter)) return true;

          return false;
        });
      });
```

### Continued development

I will continue to learn and practice react and I also started learning tailwind css so i will include tailwind css in my future projects.

## Author

- Frontend Mentor - [@aemrobe](https://www.frontendmentor.io/profile/aemrobe)
- Twitter - [@Aemro112](https://www.twitter.com/Aemro112)

## Acknowledgments

I worked on this project in a team so I want to say thanks to my team members for working together with me. The team work spirit which we had was amazing and I gained new knowledge from them and we will continue to do together.
