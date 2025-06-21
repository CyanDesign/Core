# Cyan Core - The core Tailwind V4 stylesheets to implement the Cyan interface

## Installing
~~npm install @cyandesign/core~~

> [!IMPORTANT]
>
> Intalling as a module is not yet possible, due to some complications with my NPM account, this readme will be updated as soon as the issue is resolved. You should instead add this repo as a git submodule to your project (considering you are using git), or just download the repo source and extract the files into a folder in your repo, then change `@cyandesign/core` with `./<name-of-the-folder>`


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