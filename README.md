# Waller

> Set the desktop wallpaper from Unsplash API

## Requirements

 - Linux System
 - Generate an API token from [Unsplash](https://unsplash.com/documentation#user-authentication)
 - Node installed

## Getting Started 

1. Clone the directory or download the directory as a zip file<br>

```sh
$ git clone https://github.com/skbro/Games-Arena.git
```
2. Install all required Dependencies
```sh
$ npm install
```
3. Go to node_modules/unsplash-js/lib/unsplash.js and add the following line
```js
const fetch = require('node-fetch');
```
4. Run the following command and make sure /usr/bin/gsettings is returned. Go to [stackoverflow](https://askubuntu.com/questions/558446/my-dconf-gsettings-installation-is-broken-how-can-i-fix-it-without-ubuntu-reins) in case of any problem.
```sh
$ which gsettings
```

## Usage

```
Usage: index [options] [command]

Desktop Wallpaper

Options:
  -V, --version              output the version number
  -h, --help                 output usage information

Commands:
  url|u [imgurl]             Add image from url( Wrap in double quotes )
  key|k [options] [keyword]  Get Image with given keyword
  random|r                   Set a Random wallpaper
  config                     Set Unsplash API token. Visit https://unsplash.com/documentation#user-authentication
```

## Problems Faced
 - **Problem**: Anaconda3 package interfered with Gsettings( An API that allows you to access key/value pairs (e.g., persistent application settings) without directly talking to the actual backend that stores that data (config files, gconf, dconf). ).<br/>
 **Solution**: Need to change PATH in .profile file.
 - **Problem**: Unsplash API requires fetch which is a browser API.<br/>
 **Solution**: Used 'node-fetch' and required it in lib folder of unsplash-js.


## Plans

### If user doesn't has Unsplash token
 - [ ] Use backup img from scrape.

### When User has token 
 - [ ] Allow him for follow collections and Users.