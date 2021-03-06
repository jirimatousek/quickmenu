# Quick Menu
The new forward-thinking standard of mobile navigation for the web, providing an unparalleled user experience. Everything is in thumb's reach. No need to stretch or use a second hand to open a hamburger menu.

<p align="center">
    <img src="readme-demo.gif" alt="Demo illustrating the Quick Menu in action." width="300px" height="auto">
</p>

<p align="center">
    Live demo at <a href="https://quickmenu.org">QuickMenu.org</a>. (Ensure you're on mobile.)
</p>

## Key Features
* Themeable with support for both light and dark mode based on user's device preference.
* Mobile landscape orientation supported and tested up to Apple iPhone 12 Pro Max and Samsung Galaxy S20 Ultra.
* Compatible with mobile devices with non-rectangular screens, i.e. notches and gesture areas.
* Menu wording and content all customisable in HTML.
* Responsive for mobile, tablet and desktop. Desktop will render a basic inline navigation.
* SEO friendly. No need to duplicate navigation items for each device type and content display controlled purely via CSS.
* No development dependencies, libraries or prerequisites required.

## Installation
### Quick Start via CDN
For a quick and simple way to implement the Quick Menu into your project, we can use the free open source jsDelivr CDN.

The customisation capabilities are reduced by using a CDN, however you should still be able to make modifications by overwriting the Quick Menu styling properties in your own custom CSS.

```html
<!-- Latest compiled CSS. To be placed in the <head>. -->
<link href="https://cdn.jsdelivr.net/npm/quickmenu@1.2.0/dist/css/quickmenu.min.css" rel="stylesheet" integrity="sha384-1Alh/TQ242wwdeRkNYXqDxDUEHD+BPtfrrmEdEypmRxRBnPFNWN6+iQMNfdXybWr" crossorigin="anonymous">

<!-- Latest compiled JS. To be placed before the closing <body> tag. -->
<script src="https://cdn.jsdelivr.net/npm/quickmenu@1.2.0/dist/js/quickmenu.min.js" integrity="sha384-J+7UVhxvYUPTb1N2qLj0dvniUcy8M1Ssxsic1xFI31naqNI4KlXP+r4D5eLVxhgg" crossorigin="anonymous"></script>
```

We recommend placing the stylesheet before any of your own custom stylesheets, which will ensure your customisations take precedence where possible. Similarly, it's required to place the script before any of your own custom scripts too.

### NPM
The Quick Menu can be installed as a Node.js module into your project using NPM with the following command:

    npm install quickmenu

Using a module bundler such as Webpack, import Quick Menu's JavaScript into your JS file (e.g. usually `main.js` or `app.js`):

```javascript
import QuickMenu from "quickmenu";
```

Then for complete customisation, import Quick Menu's pre-compiled Sass into your `.scss` file: (Depending on your project file structure, you may need to prepend `../` appropriately to the import rule.)

```scss
@import "node_modules/quickmenu/src/scss/quickmenu";
```

Or alternatively you may import the ready-to-use compiled css (via a bundler, e.g. Webpack):

```javascript
import "quickmenu/dist/css/quickmenu.min.css";
```

## Usage
### JavaScript
```javascript
new QuickMenu(); // To initialise the Quick Menu.
```

### HTML Examples
When in responsive mode for mobiles and tablets, the menu is fixed at the bottom of the screen within thumb reach. For desktops a regular inline menu is displayed, therefore you should place the HTML code where you want the navigation to be positioned for desktop visitors.

#### Utmost Minimal
```html
<!-- Utmost Minimal -->
<nav class="quick-menu navigation">
    <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/work">Work</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>
```

#### Minimal: Renaming Quick Menu Button
```html
<!-- Minimal: Renaming Quick Menu Button -->
<div class="quick-menu navigation">
    <div class="button">My Menu</div>
    <nav>
        <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/about">About</a></li>
            <li><a href="/work">Work</a></li>
            <li><a href="/contact">Contact</a></li>
        </ul>
    </nav>
</div>
```

#### Minimal: Renaming Close Button
```html
<!-- Minimal: Renaming Close Button -->
<div class="quick-menu navigation">
    <div class="menu">
        <nav>
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/about">About</a></li>
                <li><a href="/work">Work</a></li>
                <li><a href="/contact">Contact</a></li>
            </ul>
        </nav>
        <div class="menu-close">Dismiss</div>
    </div>
</div>
```

#### Full Fledged
```html
<!-- Full Fledged: including FontAwesome icons, menu heading content, customised wording on open and close buttons. -->
<div class="quick-menu navigation">
    <div class="button"><i class="fas fa-bars"></i> My Menu</div>
    <div class="menu">
        <div class="menu-heading">
            <i class="far fa-compass"></i>
            <span>My Menu</span>
            <p>Explore the contents of this site by jumping around using the following handy menu.</p>
        </div>
        <hr>
        <nav>
            <ul>
                <li><a href="/"><i class="fas fa-home"></i>Home</a></li>
                <li><a href="/about"><i class="far fa-user-circle"></i>About</a></li>
                <li><a href="/work"><i class="fas fa-briefcase"></i>Work</a></li>
                <li><a href="/contact"><i class="far fa-paper-plane"></i>Contact</a></li>
            </ul>
        </nav>
        <div class="menu-close">Dismiss</div>
    </div>
</div>
```

## To-Do / Future Plans
* Remove FontAwesome specific styling and ensure compatibility with any iconography.
* Provide the ability to toggle themes manually.
* Implement the ability to have sub-menus for both desktop and mobile devices.

## Credits / References
* Inspired by "iPhone X Web Navigation Concept" by [Daniel Korpai via Medium](https://medium.muz.li/iphone-x-web-navigation-concept-c06efc0e0c50) and [Dribble](https://dribbble.com/shots/3851367-iPhone-X-Web-Navigation-Idea).
* Research on "The Thumb Zone: Designing For Mobile Users" by [Samantha Ingram via Smashing Magazine](https://www.smashingmagazine.com/2016/09/the-thumb-zone-designing-for-mobile-users/).
* Module development and documentation standards adopted from [Alex MacArthur via TypeIt](https://github.com/alexmacarthur/typeit) and [Bootstrap](https://github.com/twbs/bootstrap).
* Mobile and tablet device viewports obtained from [The Ultimate Guide To iPhone Resolutions](https://www.paintcodeapp.com/news/ultimate-guide-to-iphone-resolutions), ["iPhone 12 vs Designers" by Michal Malewicz via Medium](https://uxdesign.cc/iphone-12-vs-designers-ca8bac776dad) and [Viewport Sizer Tool](https://viewportsizer.com/devices/).
