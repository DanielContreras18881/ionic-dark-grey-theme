Dark Theme for ionic2+ apps
----------------------------

This is a "Work in Progress" Dark Theme implementation for ionic2+ apps.

There are several components that still need styling, but its a start. Feel free to contribute with PRs. I'm also not sure if I did this the right way, so feel free to fix

Screenshots
------------
<img src= "https://github.com/pliablepixels/ionic-dark-grey-theme/blob/master/example/resources/screenshots/s1.PNG" height="400px"/><img src= "https://github.com/pliablepixels/ionic-dark-grey-theme/blob/master/example/resources/screenshots/s2.PNG" height="400px"/><img src= "https://github.com/pliablepixels/ionic-dark-grey-theme/blob/master/example/resources/screenshots/s3.PNG" height="400px"/><img src= "https://github.com/pliablepixels/ionic-dark-grey-theme/blob/master/example/resources/screenshots/s4.PNG" height="400px"/><img src= "https://github.com/pliablepixels/ionic-dark-grey-theme/blob/master/example/resources/screenshots/s5.PNG" height="400px"/><img src= "https://github.com/pliablepixels/ionic-dark-grey-theme/blob/master/example/resources/screenshots/s8.PNG" height="400px"/>


How to run the example
------------------------
* `git clone https://github.com/pliablepixels/ionic-dark-grey-theme`
* `cd ionic-dark-grey-theme/example`
* `npm install`
* `ionic serve`


How to use it in your project
-----------------------------
To use it in your project, simply copy over the `src/themes/dark` files to `src/themes/dark` in your project and copy over `src/themes/variables.scss` to your `src/themes` (or modify your `src/themes/variables.scss` to use the dark theme as in this project (look at the end)



iOS Quirks
-----------
In iOS, you'll see a white background as you rotate the phone. To fix this, you need to use a [plugin](https://github.com/EddyVerbruggen/cordova-plugin-webviewcolor). This plugin unfortunately doesn't work with `wkwebview`.


```
 ionic cordova plugin add cordova-plugin-webviewcolor
 ```

 And then add this code to your app:

```
this.plt.ready().then(() => {
      if (this.plt.is('ios')) {
        // change 000 to whatever you need
         window['plugins'].webviewcolor.change('#000');
      }
```