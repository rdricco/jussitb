# vtexlegacytb

![npm](https://img.shields.io/npm/dt/vtexlegacytb.svg)

[![NPM](https://nodei.co/npm/vtexlegacytb.png)](https://nodei.co/npm/vtexlegacytb/)

CLI Utils for:

 - Deploy files and templates on VTEX CMS
 - Create a vtex local environment/project architecture
 - Helpers to create static pages, controller and modules



## Installation

```bash

$ npm install -g vtexlegacytb

```

## vtexlegacytb global usage



```bash

$ vtexlegacytb deploy

```



Provide your email and account name to login, after wait the upload processes.



## vtexlegacytb.lock.json

The process will generate a vtexlegacytb.lock.json file in root path of your project.

This file is used to cache files and prevent upload files with same content, we recomend to not delete or ignore this file.

## vtexlegacytb.auth.json

The process will generate a vtexlegacytb.auth.json file in root path of your project.

This file is used to cache your auth login cookie, we recomend to ignore this file in .gitignore.


## Extra

Other utils commands:



*Help*

```bash

$ vtexlegacytb -h

```
___

*Deploy auto provide account and email*

```bash

$ vtexlegacytb deploy --account <accountName> --email <email>

```
___
*Force update all files ignoring lockfile*

```bash

$ vtexlegacytb deploy --force

```
___
*Deploy Template Files*

```bash

$ vtexlegacytb html

```
___
*Deploy SubTemplate Files*

```bash

$ vtexlegacytb sub

```
___
*Deploy ShelvesTemplate Files*

```bash

$ vtexlegacytb shelf

```
___
*Deploy Assets Files*

```bash

$ vtexlegacytb assets

```


## vtexlegacytb project workflow

Run ``vtexlegacytb createProject`` to create a new project folder.
![Create Project](https://github.com/rdricco/vtexlegacytb/blob/master/templates/demo/createProject.gif?raw=true)

Provide a project name, vtex-account and if you want to sync the vtex registered templates,

___

After a long winter (installing de dependencies) you will be able to run de project with gulp:
![Live Reload](https://github.com/rdricco/vtexlegacytb/blob/master/templates/demo/liveReload.gif?raw=true)

With gulp we run a reverse proxy server to css and js local files, so you can edit and see the changes with live reload.
And you can work with: ES6, ES6 Modules, SCSS, *Nitro* controllers and modules.
We highly recommend to make this project a github (private or public) repository

___

After all work done, you can deploy your store:
![Deploy Project](https://github.com/rdricco/vtexlegacytb/blob/master/templates/demo/deploy.gif?raw=true)

With ``npm run deploy`` the project will be compiled and deployed in the specific vtex account.

___

Another npm scripts in your project:


Deploy the project after compile the project with all static pages
```bash

$ npm run deploy-pages

```
___

Create a new Nitro.controller() after provide a controller name
```bash

$ npm run create-controller

```
___

Create a new Nitro.module() after provide a module name
```bash

$ npm run create-module

```
___

Create a new static page folder after provide a controller name
```bash

$ npm run create-page

```