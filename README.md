# [WebGurus HTML Devkit](https://gurulabs.io/html-devkit/)

WG-HTML-Devkit is a starter pack for front-end development using HTML5 Boilerplate, gulp, Bower, and Bootstrap Sass, that will help you make better sites.

* Source: [https://github.com/webgurus/webgurus-html-devkit](https://github.com/webgurus/webgurus-html-devkit)
* Homepage: [https://gurulabs.io/html-devkit/](https://gurulabs.io/html-devkit/)
* Twitter: [@webgurus](https://twitter.com/webgurus)

## Requirements

| Prerequisite       | How to check | How to install
| ------------------ | ------------ | ------------- |
| PHP >= 5.4.x       | `php -v`     | [php.net](http://php.net/manual/en/install.php) |
| Node.js >= 6.9     | `node -v`    | [nodejs.org](http://nodejs.org/) |
| gulp-cli >= 2.0.0  | `gulp -v`    | `npm install -g gulp-cli` |
| Bower >= 1.3.12    | `bower -v`   | `npm install -g bower` |

For more installation notes, refer to the [Install gulp and Bower](#install-gulp-and-bower) section in this document.

## Features

* [gulp](http://gulpjs.com/) build script that compiles both Sass and Less, checks for JavaScript errors, optimizes images, and concatenates and minifies files
* [BrowserSync](http://www.browsersync.io/) for keeping multiple browsers and devices synchronized while testing, along with injecting updated CSS and JS into your browser while you're developing
* [Bower](http://bower.io/) for front-end package management
* [asset-builder](https://github.com/austinpray/asset-builder) for the JSON file based asset pipeline
* [Bootstrap](http://getbootstrap.com/)

## Development

WG-HTML-Devkit uses [gulp](http://gulpjs.com/) as its build system and [Bower](http://bower.io/) to manage front-end packages.

### Clone / Download this devkit and rename it

You can download this devkit in zip format [here](https://github.com/webgurus/webgurus-html-devkit/archive/master.zip).

1. Open the downloaded Archive
2. Rename the extracted folder to your new project's name
3. Version control your new project using Git.

### Version control

If you don't know how to start version controlling your project, follow the next couple of steps to get you started:

1. Navigate to your new project's folder `cd project_folder`.
2. Initialize an empty repository with `git init`
3. Stage your initial files to the repository `git add .`
4. Commit your initial staged files with `git commit -am 'Initial commit'`

### Remote repository

You might want to create a Github or Bitbucket repository to have your project pushed to a remote git repo. You can create an empty repository on [github.com](https://github.com) for your new project.

After creating the empty repository you will have to add this remote repository as a `remote` to your local repository so you have an external service to push your code to and keep it safe.

To add your repository to your local project you can follow these steps:

1. Add the new repository as a remote to your local project by using `git remote add origin https://github.com/yourusername/your-new-repo.git`
2. Push the staged/commited changes to your remote repository with the following `git push -u origin master` this is useful if you collaborate on the project with others, they can easily see your changes and contribute too.

### Install gulp and Bower

Building the theme requires [node.js](http://nodejs.org/download/). We recommend you update to the latest version of npm: `npm install -g npm@latest`.

From the command line:

1. Install [gulp-cli](http://gulpjs.com) and [Bower](http://bower.io/) globally with `npm install -g gulp-cli bower`
2. Navigate to the theme directory, then run `npm install`
3. Run `bower install`

You now have all the necessary dependencies to run the build process.

### Available gulp commands

* `gulp` — Compile and optimize the files in your assets directory
* `gulp watch` — Compile assets when file changes are made
* `gulp --production` — Compile assets for production (no source maps).

### Using BrowserSync

To use BrowserSync during `gulp watch` you need to update `devUrl` at the bottom of `assets/manifest.json` to reflect your local development hostname.

For example, if your local development URL is `http://project-name.test` you would update the file to read:
```json
...
  "config": {
    "devUrl": "http://project-name.test"
  }
...
```
If your local development URL looks like `http://localhost:8888/project-name/` you would update the file to read:
```json
...
  "config": {
    "devUrl": "http://localhost:8888/project-name/"
  }
...
```

## Dont' forget to commit and push your work!

* Commit often, so you can revert back to your earlier commits if something goes south.
* Push to the remote repository every couple of hours so collaborators can see your changes.

**That's all folks!**
