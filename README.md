# VK-miniapps-deploy

Deploy straight to VK MiniApps hosting with one simple command.

## Usage

```
# install it from npm and symlink it into your PATH
npm install @vkontakte/vk-miniapps-deploy -g

# now run it!
vk-miniapps-deploy
```

You can also use `npm run` to package it with your app without installing it globally.

First add this to your scripts section of `package.json`:

```JSON
  "scripts": {
    "deploy": "vk-miniapps-deploy",
    "clean-source": "rimraf README.md src webroot package.json"
  },
```

And then install `vk-miniapps-deploy` as a devDependency:

```
npm install @vkontakte/vk-miniapps-deploy --save-dev
```

And now you can run `npm run deploy` to run the `vk-miniapps-deploy` installed in the local `node_modules` folder (even if you have never done `npm install vk-miniapps-deploy -g`).

## Options

To configure `vk-miniapps-deploy` all you need to do is specify a couple of things in your `vk-hosting-config.json` 

``` JSON
{
  "staticpath": "build",
  "app_id": "...",
}
```

## How to use:
* Make sure that in package.json the key value «homepage» is «./»
* Copy the example config to the root folder of your application vk-hosting-config.json.example
  and remove the suffix «.example»
* Run yarn deploy

For your CI, you can use

```bash
$ env MINI_APPS_ACCESS_TOKEN=fcbc78243e0e993969d478df4eb11376bcec6d806bb6dbaad80e8c7b32d59b9e9a52d5296b53fd00bdf7d yarn deploy
```