# HaulyCSS
is a SCSS-Framework they've set the goal to produce just the things you need and not more.

## How is working?
HaulyCSS allows you to create all classes for each viewport with variable-maps. It's easy to expand.

### Viewports
In this example you see the variable map of the viewports.

```
// ****** 
// * #Map-viewports
// */
$map-viewports: (
	"m"  : "screen and (max-width: 640px)",
	"t"  : "screen and (min-width: 641px) and (max-width: 980px)",
	"d"  : "screen and (min-width: 981px) and (max-width: 1199px)",
	"hd" : "screen and (min-width: 1200px)"
);
```
The names of the viewports will be used for a mixing wrapping, like:

```
@include mediaQuery('m') {
	// just do things for mobile screens
}
```

### Create Helper Classes
For example you want to use with-classes like w-6/12-hd you've expand this map with the new styles and set the desired viewport as 1.

Notice: You see the name "6\/12" in this map? In your HTML you've to write 6/12.

The first value is the property-value, after this comes the viewport names and the last is for all. The last is doesn't wrapped in a mediaQuery-mixin.

```
$map-width : (
    6\/12  : ( percentage( 6 / 12 ), 0, 0, 0, 1, 1 ),
    "100p" : ( 100%                , 1, 1, 1, 0, 1 ),
);
```

#### Attention
All created classes have prefixes like emmet.io for e.g.:

| Class        | CSS-Code                                              |
| -------------|-------------------------------------------------------|
| w-6\/12-hd   | @media screen and (min-width: 1200px) { width: 50%; } |
| mgt-20       | margin-top: 20px;                                     |

### Features
	
* Blockquote
* Fast
* Lightweight
* Easy extendable
* SCSS
* Buttons (btn--primary btn--secondary)
* Forms
* X-Element

© Copyright by HaulyShit
