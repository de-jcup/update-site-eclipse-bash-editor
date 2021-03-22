# P2 update site
This is just a eclipse p2 plugin update site and not a "real" web site.

## Content structure
The p2 update site has following structure:

```
features/
    *.jar
plugins/
    *.jar
content.jar
artifacts.jar
site.xml

```

## Usage in eclipse
### Marketplace
Just search for the plugin in eclipse marketplace client of your eclipse installation and trigger the install there. Then there is **no manual setup necessary** !

The eclipse markeplace client will automatically 
- add the update-site location
- check for plugin updates
- handle update-location changes (e.g. update-site has been moved to another URL/provider)

### Other ways
The eclipse marketplace is normally "the way to go", because it is central, convenient, update-site changes - even location changes - are automatically distributed and much more benefits. 
But if you really need another way to install the plugin you can use the update-site directly or create your own local site:

#### Add update-site manually
- Open `Window -> Preferences` 
- Enter `site` in search field
- Select `Available Software Sites`
- Press `Add...`, follow instructions and use this update site location URL

#### Provide as local update sites
If you want to provide the plugin by a local update site - e.g. when no internet connection to eclipse maretplace is possible/allowed - you can simply copy 
the complete content structure to your local disk. After this you have to do same steps described before to add the update-site manually, but instead of the URL
of this site you simple use your local update site path.
