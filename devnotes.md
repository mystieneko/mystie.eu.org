# Configuration
## Development
### CSS
file to use: `/css/min/styles.min.css`
html: `<link href="/css/min/styles.min.css" rel="stylesheet">`  
#### Compile CSS
in `css` folder:  
`rm -rf all.css && cat variables.css cont.css general.css links.css mobile.css nav.css socialicons.css dropdown.css dl.css fonts.css >> all.css`  
### JS
*no strict limit.* use what you want  
## Production
### CSS
file to use: `/css/min/all.min.css`  
html: `<link href="/css/min/all.min.css" rel="stylesheet">`  
_do not_ use regular css, it only slows down the speed & you probably don't want that
#### Compile CSS
in `css` folder:  
`rm -rf all.css min/all.min.css && cat variables.css cont.css general.css links.css mobile.css nav.css socialicons.css dropdown.css dl.css fonts.css >> all.css && css-minify -f all.css -o min/`  
*note that [css-minify](https://www.npmjs.com/package/css-minify) must be installed globally to minify css*
### JS
in `scripts` folder:
`uglifyjs -o <FILENAME>.min.js -- <FILENAME>.js`
`<FILENAME>` is the filename of a script without extension (like `dcStatus`)
### Note
if a script is small, there is no need in minifying it