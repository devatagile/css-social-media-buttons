Round Social Media Buttons
==========================

A set of Retina-proof round (or rounded) social media buttons, that can be added with just one HTML element. The buttons are 32px in diameter and are (for the most part) made with just CSS.

![](https://raw.github.com/timhuisman/round-social-media-buttons/master/screenshot-1.png)

**Browser compatibility**

The buttons have been tested in the following browsers:

- Opera	12
- Chrome 24
- Safari 5
- Firefox 8
- Internet Explorer 9*
- Chrome for iPhone 23
- Safari for iPhone iOS 6

*The buttons rely heavily on CSS3 and are therefor not shown properly in Internet Explorer 8: meaning no rounded corners and shadows. Lower versions of Internet Explorer than IE8 aren't supported at all.



## Installation ##

Simply put the CSS file in your project CSS folder and link to it in your `<head>` or copy/paste the content of the `social-buttons.css` into your own CSS file:

Not using all the buttons? You can make your own CSS file that suits your needs with LESS/SASS. Open `social-buttons.less` or `social-buttons.scss` and comment out the `@imports` you don't need at the bottom of the file. Compile it and add the CSS to your project.



## How to use ##

Add an HTML element with the class `social-btn` and without any content:

	<a href="#" class="social-btn"></a>
	<span class="social-btn"></span>

Add a class of a (social) network, like for example `github` (see 'Lists of available classes' below for all the possibilities):

	<a href="#" class="social-btn github"></a>
	<span class="social-btn github"></span>

And that's it!


**Alternative buttons**

Some buttons have an alternative version, that use another icon (`github`) and/or different color button (`youtube`).
Want to use one of these alternative buttons instead? Add `alt` or in case of more than one alternative `alt#` (# is number) as class:

  <a href="#" class="social-btn github alt2"></a>
  <span class="social-btn github alt2"></span>

If the alternative version also has a different color button (like `youtube`) it is slightly different: this type uses the old (pre 1.3.1) notation with button name and 'alt' as one class:

  <a href="#" class="social-btn youtube-alt"></a>
  <span class="social-btn youtube-alt"></span>


**Rounded buttons**

Don't want fully rounded buttons? Add the class `rounded` for a button with just slightly rounded corners:

	<a href="#" class="social-btn github rounded"></a>
	<span class="social-btn github rounded"></span>


**Lists of available classes**

- `facebook` [`alt` **!new**]
- `flickr`
- `foursquare` [`alt` **!new**]
- `github` [`alt` | `alt2` **!new**]
- `gplus`
- `icheckmovies`
- `lastfm`
- `linkedin`
- `mail`
- `path`
- `rss`
- `skype` [`alt`]
- `tumblr`
- `twitter` [`alt`]
- `vimeo`
- `youtube` [`alt` **!new**] | `youtube-alt`



## Changelog ##

**v.1.3.1**

- [**!important] Changed the way how alternative buttons are used: instead of `github-alt` it is now `github alt` (read more under the **Alternative buttons** section). | This has resulted in a decrease in code with 13 lines and 564 charachters, and filesize with 0.564 bytes of the compiled CSS file.
- [**!important] Switched Github icons: the favicon version is now the primary icon, the Octocat has become `github alt2`.

**v.1.3.0**

- [**!important] Added four alternative buttons: `facebook-alt`, `foursquare-alt`, `github-alt2` and `youtube-alt2`.

**v.1.2.5**

- Fixed background-position for `youtube-alt` icon in SCSS file
- Removed inline-block mixin: is only needed for lower than IE8 browsers.
- Removed double background-size attribute in LESS file.

**v.1.2.4**

- Added browser prefix versions of the Retina media query & background-size, so that all browser use the Retina sprite if possible. 

**v.1.2.3**

- Added `content: ''` on `social-btn` to remove any content added to the button: resolves bug causing the button to break ([Issue #10](https://github.com/timhuisman/round-social-media-buttons/issues/10))
- Added `social-buttons.min.less` and `social-buttons.min.scss` for easier compiling of style into a minified and unminified version.

**v.1.2.2**

- [**!important] Updated `foursquare` button: changed background-color and replaced the icon with its official (fav)icon: the green ball with white trail.

**v.1.2.1**

- Alphabetical order restored / Remove Trailing Whitespace (thanks [@cafferata](https://github.com/cafferata))
- Optimized images: Saved 2,6 KB of 11,1KB (thanks [@cafferata](https://github.com/cafferata))
- Added an alternative button: `skype-alt`.
- Repositioned both Skype icons to the right column in the sprites.
- [**!important] Switched Skype icons: the favicon version is now the primary icon.
- [**!important] Switched Github icons: the Octocat is now the primary icon.
- [**!important] Switched Twitter icons: the Twitter bird is now the primary icon.
- Changed color of _"White"_ (actually `#F1F2F2`) icons to `#fff`;
- Improved YouTube icons: the word 'Tube' has been made fully transparent.

**v.1.2.0**

- [**!important] Added two new buttons: `skype` (thanks [@AMeijerNL](https://github.com/AMeijerNL)) and `icheckmovies`.
- Converted sprite from horizontally to vertically orientated (thanks [@AMeijerNL](https://github.com/AMeijerNL)), for smaller file size and load time.
- Added pointer cursor to button, so that non-anchor elements have the same visual button behaviour as anchor elements.
- Added source files for both normal and Retina sprites as Adobe Illustrator files.

**v.1.1.0**

- Added a SASS version (using the .scss notation) of the files

**v.1.0.1**

- Optimized sprites: removed 1px and 2px (Retina) empty space between icons and compressed the files to decrease filesize by almost 50%.
- Changed order of alternative icons in sprite: first the normal icon and then the alternative icon instead of vice versa.