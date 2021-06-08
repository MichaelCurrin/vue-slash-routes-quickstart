# Vue Slash Routes Quickstart
> Starter template for a Vue 3 project using Vue Router and slash-based routes

<!-- Badges generated with https://michaelcurrin.github.io/badge-generator/ -->
[![GitHub tag](https://img.shields.io/github/tag/MichaelCurrin/vue-slash-routes-quickstart?include_prereleases=&sort=semver)](https://github.com/MichaelCurrin/vue-slash-routes-quickstart/releases/)
[![License](https://img.shields.io/badge/License-MIT-blue)](#license)

[![Made with Node.js](https://img.shields.io/badge/Node.js->=12-blue?logo=node.js&logoColor=white)](https://nodejs.org)

[![Package - vue](https://img.shields.io/github/package-json/dependency-version/MichaelCurrin/vue-slash-routes-quickstart/vue)](https://www.npmjs.com/package/vue)
[![Package - vue-router](https://img.shields.io/github/package-json/dependency-version/MichaelCurrin/vue-slash-routes-quickstart/vue-router)](https://www.npmjs.com/package/vue-router)


## Preview

<div align="center">
    <a href="https://michaelcurrin.github.io/vue-slash-routes-quickstart/">
        <img src="/sample.png" alt="Sample screenshot" title="Sample screenshot" width="350" />
    </a>
</div>

<br>

<div align="center">

[![Use this template](https://img.shields.io/badge/Generate-Use_this_template-2ea44f?style=for-the-badge&logo=github)](https://github.com/MichaelCurrin/vue-slash-routes-quickstart/generate)

</div>


## About

### Hash paths

Normally all the URLs on a Vue app are on a hash path.

- `/#/`
- `/#/about`

### Slash paths

But this app is configured to use path-based routes that use slash-based routing instead of hash-based.

This is done thanks to the HTML5 History API - Vue is able to to push changes to the URL's history.

This logic is set up in [src/router/index.js](/src/router/index.js) using `createWebHistory` from `vue-router`. It's docstring says:

> Creates an HTML5 history. Most common history for single page applications.

### Error page

Normally a bad path like this would still look like app outline, but with no content.

- `/#/not-a-path`

Now if you use slash-based routing and you send someone to a bad path like this, they'll see an ugly server error.

- `/not-a-path`

So docs recommend you to set up a fallback for bad URLs around 404 error so that you root to page. You need to do this in an Nginx config, or if use use Netlify you can set up some `404.html` page or root if a path is not matched (I don't know how you easily define the good paths in both the app and the Netlify config though).

### Project creation

This project was set up using Vue UI.

```sh
$ vue vui
```

And creating a new project using Vue 3 and Vue Router and the choice to have slash paths. Linting, formatting and Babel were turned off.


## Resources

For a setup using the plain _hash_ routes, see Vue Router Quickstart:

- [![MichaelCurrin - vue-router-quickstart](https://img.shields.io/static/v1?label=MichaelCurrin&message=vue-router-quickstart&color=blue&logo=github)](https://github.com/MichaelCurrin/vue-router-quickstart)

For a setup _without_ Vue Router, see Vue Quickstart:

- [![MichaelCurrin - vue-quickstart](https://img.shields.io/static/v1?label=MichaelCurrin&message=vue-quickstart&color=blue&logo=github)](https://github.com/MichaelCurrin/vue-quickstart)

To learn more about Vue, see [Vue](https://michaelcurrin.github.io/dev-resources/resources/javascript/packages/vue/) resources.


## Installation

```sh
$ yarn install
```

## Usage

```sh
$ yarn start
```

Open the browser at:

- http://localhost:8080/

The second page is at:

- http://localhost:8080/about


## License

Released under [MIT](/LICENSE) by [@MichaelCurrin](https://github.com/MichaelCurrin).
