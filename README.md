# Cyan Core - The core Tailwind V4 stylesheets to implement the Cyan interface

## Installing
```
npm install @cyandesign/core
```



To use, import in your main stylesheet:
```css
@import "@cyandesign/core";
```

You can also use the different parts separately:
```css
@import "@cyandesign/core/theme.css";
/*Utility classes require the theme import*/
@import "@cyandesign/core/utilities.css";
```

## Setup
### Custom Variables
Cyan supports 4 themes out of the box:
* Light
* Dark
* Darker
* Black/AMOLED
with light being the default, meaning no extra setup is needed. If your app follows standard CSS `prefers-color-scheme`, dark mode also works out of the box. To make all 3 dark modes work, you need to set custom variants as follows:
```scss
@custom-variant dark (&:where(.theme-dark, .theme-dark *, .theme-dark .theme-light, .theme-dark .theme-light *));
@custom-variant darker (&:where(.theme-darker, .theme-darker *));
@custom-variant black (&:where(.theme-midnight, .theme-midnight *));
```

### Screenshots:
![image](http://www.dablulite.dev/_next/image?url=%2Fcyan3-screenshot-1.png&w=1920&q=100)
![image](http://www.dablulite.dev/_next/image?url=%2Fcyan3-screenshot-2.png&w=1920&q=100)
