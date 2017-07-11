# Web App Manifest

***

**Articles**

- [The Web App Manifest (Google Web Fundamentals)](https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/)


***

**Tools**

Web App Manifest generator \([link](https://app-manifest.firebaseapp.com/)\)

***

**Best Practices**

- Track how the app is launched. Add a query to the `start_url` parameter then use an analytics suite to track the query string. If you use this method, remember to update the list of files cached by the App Shell to ensure that the file with the query string is cached.

- Place the manifest link on all your site's pages, so it will be retrieved by Chrome right when the user first visits, no matter what page they land on.

- The `short_name` is preferred on Chrome and will be used if present over the name field.

- Define icon sets for different density screens. Chrome will attempt to use the icon closet to 48dp, for example, 96px on a 2x device or 144px for a 3x device.

- Remember to include an icon with a size that is sensible for a splash screen and don't forget to set the `background_color`.

***

**Further Reading**

***

**Basic Configuration**


```

{

  "name": "Notes",

  "short_name": "Notes",

  "scope": "./",

  "start_url": "index.html",

  "display": "standalone",

  "orientation": "any",

  "theme_color": "#9C27B0",

  "background_color": "#9C27B0"

}
```



**name**: The name of your app. Pick any name you want! I called my app "Notes", because it's going to be a note-taking app. I have the best names.

**scope**: The scope of your app is the directory that should be considered the root of your app. The value you see in my example is the value you should use.

**start\_url**: The URL that should be opened when your app starts. Since we only have one entry point, this should just be index.html.

**display**: How the app should be presented to the user when launched from the home screen. Using the value standalone will make your Web App look like a native app \(without any browser chrome\) when launched.

**orientation**: The preferred display orientation of the app. We use "any" to suggest that our app can be displayed at any orientation.

**theme\_color**: The primary theme color of your app. This will be used to adjust the highlight color of native OS chrome \(where applicable\) when your app launches.

**background\_color**: The color that will be used for the splash screen as the app is launching from a mobile device's home screen.

***

**Icon Configuration**

```
"icons": [{

  "src": "bower_components/note-app/common/images/icon-0-75x.png",

  "sizes": "36x36",

  "type": "image/png"

}, {...}]
```



**src**: The path to the icon for a given scale.

**sizes**: The size of the icon you are pointing at.

**type**: The mime-type for the icon source image.


