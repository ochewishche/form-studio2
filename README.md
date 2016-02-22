# Introduction

Sample application based upon [mgechev](https://github.com/mgechev)/ [angular2-seed](https://github.com/mgechev/angular2-seed).

[![Join the chat at https://gitter.im/mgechev/angular2-seed](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mgechev/angular2-seed?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Dependency Status](https://david-dm.org/mgechev/angular2-seed.svg)](https://david-dm.org/mgechev/angular2-seed)
[![devDependency Status](https://david-dm.org/mgechev/angular2-seed/dev-status.svg)](https://david-dm.org/mgechev/angular2-seed#info=devDependencies)

**Note:** Angular 2.0 is not production ready yet! This project is perfect for playing around with the latest versions but do not start new projects with it since a lot of new changes are going to be introduced until the framework is officially released.

# Features

* Component styling
* Custom Directive
* Router module (implementing child routes*)
* Http module
* Form module (using template driven form approach)

# How to start

**Note** that this seed project requires node v0.12.x or higher and npm 3.x.x.

```bash
npm install
# dev
npm run serve.dev
```
_Does not rely on any global dependencies._

# Directory Structure

```
.
├── app
│   ├── components
│   │   ├── about
│   │   │   ├── about.html
│   │   │   ├── about.ts
│   │   │   └── about_spec.ts
│   │   └── home
│   │       ├── home.css
│   │       ├── home.html
│   │       ├── home.ts
│   │       └── home_spec.ts
│   ├── services
│   │   ├── name_list.ts
│   │   └── name_list_spec.ts
│   ├── typings
│   ├── app.css
│   ├── app.html
│   ├── app.ts
│   ├── index.html
│   └── init.ts
├── dist
│   ├── dev
│   └── prod
├── tools
│   ├── tasks
│   ├── utils.js
│   └── workflow.config.js
├── tsd_typings
├── gulpfile.js
├── karma.conf.js
├── package.json
├── test-main.js
├── tsconfig.json
└── tsd.json
```

# Configuration

Default application server configuration

```javascript
var PORT             = 5555;
var LIVE_RELOAD_PORT = 4002;
var APP_BASE         = '/';
```

Configure at runtime

```bash
npm run serve.dev -- --port 8080 --reload-port 4000 --base /my-app/
```

# Now to extend?

If you want to use your custom libraries:

```bash
npm install my-library --save
vim gulpfile.js
```
Add reference to the installed library in `PATH.src.lib` into `./tools/workflow.config.js`.

# Running test

```bash
# In a single bash window
npm run test

# Debug - In two bash windows
npm run karma      # 1st window
npm run test.dev   # 2nd window
```