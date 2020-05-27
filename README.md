# harmonium-doc-improve

#### Suggestions on how to improve [Harmonium documentation](https://harmonium.revelry.co/)

## 1. Installation and Setup section

### current issues: 

 1. For less experienced developers, it’s unclear how to import sass files and replicate the examples locally.
 2. The link for downloading the starter settings in the middle of the document does not work.
 3. No direct navigation to the installation and setup page on side navbar.

### Potential improvement

####  1. suggestions on issue 1:

* On installation section, add `npm install --save node-sass` instruction  and/or 
link tutorials on how to import sass stylesheets into react app. (https://www.w3schools.com/react/react_sass.asp)
* Remind users to create a sass file in the directory if they haven't already done so.
* Add more detail on the sass file instruction.

current:
```scss
/* myapp.scss */
@import 'wherever-your-styles-live/color-palette';
@import 'wherever-your-styles-live/harmonium-settings';
@import 'wherever-your-styles-live/harmonium-component-settings';
@import '~/harmonium/scss/app';
/* your styles here; */
```
to:
```scss
/* myapp.scss */
@import 'wherever-your-styles-live/color-palette'; // For example: @import './styles/color-palette'
@import 'wherever-your-styles-live/harmonium-settings';  // @import './styles/harmonium-settings'
@import 'wherever-your-styles-live/harmonium-component-settings'; // @import './styles/harmonium-component-settings'
@import '~/harmonium/scss/app';
/* your styles here; */
```
###### Personal experience with the issue: I got stuck with `wherever-your-styles-live` for a while. Might just be my own problem. Could help someone like me to follow the instruction more easily by adding an example
* Remind them to import the scss file in their react app like they would with css files. Presumably in index.js.

####  2. suggestions on issue 2:
current: 
```
Harmonium includes !default values for color-palette and harmonium-settings vars. You can download the starter settings here (which include color-palette.scss and harmonium-settings.scss) and easily view/edit variables to fit your project
```
The hypelink on `here` directs users to page not found.

Fix: replace the link with the one on side Nav that's working properly.


