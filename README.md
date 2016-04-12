### Meteor + Bootstrap 4 (alpha) from Npm

You can clone this repo and run:

```
$ npm install
$ meteor
```

or you can configure Meteor + Bootstrap 4 from Npm from the start like that:

```
$ meteor create --release 1.3-rc.5 bootstrap-from-npm
$ cd bootstrap-from-npm
$ npm install
$ npm install --save 4.0.0-alpha.2
$ npm install --save-dev autoprefixer
$ meteor add fourseven:scss
$ meteor remove standard-minifier-css
$ meteor add juliancwirko:postcss
```

in the package.json you need to configure autoprefixer, example:
```
{
  "name": "test-npm-scss",
  "private": true,
  "scripts": {
    "start": "meteor run"
  },
  "dependencies": {
    "bootstrap": "^4.0.0-alpha.2",
    "meteor-node-stubs": "~0.2.0"
  },
  "devDependencies": {
    "autoprefixer": "^6.3.6"
  },
  "postcss": {
    "plugins": {
        "autoprefixer": {
            "browsers": ["last 2 versions", "ie >= 9", "and_chr >= 2.3"]
        }
    }
  }
}
```

Bootstrap 4 (alpha) Docs: [http://v4-alpha.getbootstrap.com/](http://v4-alpha.getbootstrap.com/)
