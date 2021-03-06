---
id: 58965611f9fc0f352b528e6c
title: Logging a User Out
challengeType: 2
---

## Description
<section id='description'>
As a reminder, this project is being built upon the following starter project on <a href='https://glitch.com/#!/import/github/freeCodeCamp/boilerplate-advancednode/'>Glitch</a>, or cloned from <a href='https://github.com/freeCodeCamp/boilerplate-advancednode/'>GitHub</a>.
Creating the logout logic is easy. The route should just unauthenticate the user and redirect to the home page instead of rendering any view.
In passport, unauthenticating a user is as easy as just calling <code>req.logout();</code> before redirecting.
<blockquote>
app.route('/logout')<br>
  .get((req, res) => {<br>
      req.logout();<br>
      res.redirect('/');<br>
  });
</blockquote>
You may have noticed that we're not handling missing pages (404), the common way to handle this in Node is with the following middleware. Go ahead and add this in after all your other routes:
<blockquote>app.use((req, res, next) => {<br>
  res.status(404)<br>
    .type('text')<br>
    .send('Not Found');<br>
});
</blockquote>
Submit your page when you think you've got it right.
</section>

## Instructions
<section id='instructions'>

</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Logout route
    testString: getUserInput => $.get(getUserInput('url')+ '/_api/server.js') .then(data => { assert.match(data, /req.logout/gi, 'You should be call req.logout() in youre /logout route'); }, xhr => { throw new Error(xhr.statusText); })
  - text: Logout should redirect to the home page /
    testString: getUserInput => $.get(getUserInput('url')+ '/logout') .then(data => { assert.match(data, /Home page/gi, 'When a user logs out they should be redirected to the homepage'); }, xhr => { throw new Error(xhr.statusText); })

```

</section>

## Challenge Seed
<section id='challengeSeed'>

</section>

## Solution
<section id='solution'>

```js
// solution required
```
</section>
