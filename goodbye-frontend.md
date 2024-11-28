---
title: Goodbye Frontend
createdAt: 2024/11/28
---

# Goodbye Frontend

I’ve been working in the react ecosystem for some time now.
I will soon transition into a new role so it’s a good time to look back on my experiences and learnings as a frontend developer.

Overall I had an amazing experience. Great coworkers, tough challenges, close to the user. Let’s dive into the details.

## HTML

As a frontend web developer the outcome of your work is HTML, CSS and JavaScript.
CSS and JS will be minified and transformed for optimization reasons while HTML is easily human readable.
You can just open the file and read it.
You _should_ be able to read it and understand what is going on.
If not, your code probably needs to improve.

If your HTML is semantic and readable, you are on track to achieve digital accessibility and have nice selectors while testing.
Learning about proper ARIA and following WCAG standards took my understanding and expectation of good HTML to another level.

## React

React embraces composition.
Components are built of smaller components and hooks.
Hooks are composed of hooks.

There is not much you can do fatally wrong which results in a colorful palette of solutions.
Within a team, you need to establish a common style to enable consistency.
Consistency is important as it makes navigation in your repository a smooth experience.

React’s Dan Abramov said: [UI=f(data)(state)](https://overreacted.io/the-two-reacts/).
The user interface is the result of your component f being applied to data and state.
There are two ways to consume your dependencies: component properties and context.
Properties are explicit so you need to supply them every time you want to use the component.
To improve readability and ergonomics, the properties should simple.
More complex dependencies can be passed to the component by context.

Be careful with custom context.
It will come back to you!

## JavaScript

You can do anything in JS in any way you want.
As mentioned beforehand, be consistent.
Use eslint. Configure it to your needs.
Every npm dependency should have an eslint plugin.
It will save you a lot of hassle in the long run.
TypeScript good.

## Testing

I did not practice test driven development by the book.
I can see its benefits.
If you write your test first, your component will definitely be testable.
Untestable code really is the worst.
You need to refactor it before you can test it.
Unfortunately, refactoring untested code is dangerous.

Write frontend tests that are easy to read.
If your application is accessible, writing tests is really easy.
I recommend mock service worker and testing library.

Frontend web development is nice and a place I can return to. It’s not goodbye forever.
