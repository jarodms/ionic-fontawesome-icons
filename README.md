Example Ionic app which uses FontAwesome icons

1) Uses the ionic starter template `tabs`
2) Uses FontAwesome 4.7.0; Ionic 3.9.2
3) Added a simple spinning cog on the Home screen
4) Tab icons are using custom icons, which extend FontAwesome icons. Property is set in tabs.html as `tabIcon="custom-home"`



To get started:
1) `npm i`
2) Copy `node_modules/font-awesome/fonts` folder and paste it under `src/assets`
3) Copy `node_modules/font-awesome/scss` folder and paste it under `src/theme`

`src` folder structure:

```
src
  |
  assets
       |
       fonts
  |
  theme
      |
      scss

```
4) define your custom icons in `theme/variables.scss`
5) Tab Icons (from what I can tell so far), need to be a custom icon which extends FA

```
tabIcon="custom-contacts"
```

and then in `theme/variables.scss`, there is a custom class

```
&[class*="contacts"] {
    @include iconize(true); 
    @extend .fa-users; 
  }
```

6) Using other icons throughout your app can be as simple as 

```
<fa name="cog" animation="spin"></fa>
```

Here's the gallery: https://fontawesome.com/icons?d=gallery


## Final result with icons


![Ionic with Font Awesome Icons](https://github.com/jarodms/ionic-fontawesome-icons/blob/master/Font%20Awesome%20Icons-Ionic%20App.png)

* The _gear_ icon in the text is actually a spinning cog
* Icons in the tab bar are similar in nature to Ionicons but are all Font Awesome Icons