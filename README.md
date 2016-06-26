# Web Components

Web Components are a concept used in modern web development to break a web application into small, more-easily manageable parts. A Web Component is a small, visual template created with the intention of re-using it. This will be a repository for maintaining all web components that I create.

This README.md will be updated with various notes and resources over time.

## Vendor Prefixes

```
/* Android, Chrome, iOS, Safari */
-webkit-
-webkit-transition: all 0.30s ease-in-out;

/* Firefox */
-moz-
-moz-transition: all 0.30s ease-in-out;

Internet Explorer */
-ms-
-ms-transition: all 0.30s ease-in-out;

/* Opera */
-o-
-o-transition: all 0.30s ease-in-out;
```

## Accessibility

Of interesting note is that keyboard accessibility can be improved/added through the addition of the `tabindex` attribute to an element that would otherwise not show the accessibility outline when receiving focus as do most form elements.

>First and foremost, if we want to capture input from the keyboard, we’ll need to use elements that can accept the focus: primarily links (&lt;a>) and form controls (&lt;input>, &lt;select>, &lt;textarea> and &lt;button>). [[18]][ref18]

But suppose we need to have **other** elements capture input/show focus from the keyboard - like a &lt;div&gt;?

>I quickly thought about simply adding the tabindex attribute to an element and after some preliminary tests in FF2/Win and IE7/Win it seems that's all that is necessary to make an element focusable.

>The tabindex value can allow for some interesting behaviour.

>* If given a value of "-1", the element can't be tabbed to but focus can be given to the element programmatically (using element.focus()).
* If given a value of 0, the element can be focused via the keyboard and falls into the tabbing flow of the document.
* Values greater than 0 create a priority level with 1 being the most important.

>I tend to shy away from trying to declare any tabindex as the regular document flow should be predictive enough but if creating a JavaScript-enabled interface, there may be times where tying something to a link actually doesn't make the most sense and having an element be able to receive focus via the keyboard as well as from the mouse can only be a good thing. \- [ACCESSIBILIY! - Making Elements Focusable with Tabindex](http://snook.ca/archives/accessibility_and_usability/elements_focusable_with_tabindex)

<table>
    <tr>
        <th>References - Accessibility</th>
    </tr>
    <tr>
        <th>Resource Title</th>
    </tr>
        <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/Accessibility" target="_blank">Accessibility - on developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-describedby_attribute" target="_blank">Using the aria-describedby attribute - on developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://www.w3.org/TR/WCAG20-TECHS/ARIA1.html" target="_blank">ARIA1: Using the aria-describedby property to provide a descriptive label for user interface controls - w3.org</a></td>
    </tr>
    <tr>
        <td><a href="http://www.powermapper.com/tests/screen-readers/elements/" target="_blank">HTML elements - Screen reader compatibility</a></td>
    </tr>
    <tr>
        <td><a href="https://css-tricks.com/accessiblility-basics-turn-your-css-off/" target="_blank">Accessibility Basics: How Does Your Page Look To A Screen Reader?</a></td>
    </tr>
    <tr>
        <td><a href="http://webaim.org/techniques/screenreader/" target="_blank">Designing for Screen Reader Compatibility</a></td>
    </tr>
    <tr>
        <td><a href="http://accessibleculture.org/research-files/ozewai2011/basic-html5-aria-screenreaders-presentation.html#(1)" target="_blank">HTML5 and ARIA: Accessibility Benefits and Support</a></td>
    </tr>
    <tr>
        <td><a href="https://www.w3.org/TR/html401/interact/forms.html#adef-tabindex" target="_blank">Tabbing navigation - w3.org</a></td>
    </tr>
    <tr>
        <td><a href="http://snook.ca/archives/accessibility_and_usability/elements_focusable_with_tabindex" target="_blank">ACCESSIBILIY! - Making Elements Focusable with Tabindex</a></td>
    </tr>
        <tr>
        <td><a href="http://www.sitepoint.com/accessible-javascript/" target="_blank">Accessible JavaScript: Beyond the Mouse</a></td>
    </tr>
        <tr>
        <td><a href="http://cssgallery.info/testing-the-accessibility-of-the-css-generated-content/" target="_blank">Testing the Accessibility of the CSS Generated Content</a></td>
    </tr>
    <tr>
        <td><a href="http://accessible-colors.com/" target="_blank">Accessible Colors - foreground color vs. background color test</a></td>
    </tr>
</table>

<table>
    <tr>
        <th>References - Other</th>
    </tr>
    <tr>
        <th>Resource Title</th>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/" target="_blank">Mozilla Developer Network - most broad topic index page</a></td>
    </tr>
    <tr>
        <td><a href="http://www.w3schools.com/" target="_blank">W3 Schools</a></td>
    </tr>
    <tr>
        <td><a href="http://css-tricks.com/">CSS Tricks - CSS tricks and tips</a></td>
    </tr>
    <tr>
        <td><a href="http://tympanus.net/codrops/css_reference" target="_blank">Codrops - tips, tricks, inspirational websites and more</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/HTML" target="_blank">HTML - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="http://caniuse.com/" target="_blank">caniuse.com - check if certain features are supported in major browsers</a></td>
    </tr>
    <tr>
        <td><a href="http://learn.shayhowe.com/">learn.shayhowe.com - good tutorial source</a> </td>
    </tr>
    <tr>
        <td><a href="http://www.html5rocks.com/en/">HTML5 Rocks - great tutorial source</td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML" target="_blank">HTML Developer Guide - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/CSS" target="_blank">CSS - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/Guide/CSS" target="_blank">CSS Developer Guide - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Writing_efficient_CSS" target="_blank">Writing efficient CSS - develper.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://www.w3.org/TR/selectors/" target="_blank">[CSS] Selectors Level 3 - w3.org</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/pseudo-classes#Index_of_standard_pseudo-classes" target="_blank">Index of standard pseudo-classes - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/pseudo-elements" target="_blank">Pseudo-elements - developer.mozilla.org</a></td>
    </tr>    
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Positioning" target="_blank">CSS Positioning - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://www.w3.org/TR/CSS21/visuren.html">Visual formatting model - w3.org (nicely indexed)</a></td>
    </tr>
    <tr>
        <td><a href="https://www.w3.org/TR/2013/WD-components-intro-20130606/" target="_blank">Introduction to Web Components - w3.org</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/Web_Components" target="_blank">Web Components - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://component.kitchen/tutorial" target="_blank">Web components tutorial</a></td>
    </tr>
    <tr>
        <td><a href="http://www.bbvaopen4u.com/en/actualidad/web-components-present-and-future-web-development" target="_blank">Web components: present and future in web development</a></td>
    </tr>
    <tr>
        <td><a href="https://www.w3.org/TR/html51/" target="_blank">HTML 5.1 W3C Working Draft</a></td>
    </tr>
    <tr>
        <td><a href="http://materializecss.com/buttons.html" target="_blank">Materializecss.com - buttons</a></td>
    </tr>
    <tr>
        <td><a href="http://www.google.com/design/spec/material-design/introduction.html#" target="_blank">Material Design - google.com</a></td>
    </tr>
    <tr>
        <td><a href="http://materializecss.com/" target="_blank">Materializecss.com - A modern responsive front-end framework based on Material Design</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_variables" target="_blank">Using CSS Variables - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="http://www.w3schools.com/colors/colors_converter.asp" target="_blank">Color Converter - convert name, hex, rgb, hsl, hwb, cmyk, ncol, to any other]</a></td>
    </tr>
    <tr>
        <td><a href="http://www.w3schools.com/colors/colors_picker.asp" target="_blank">Color Picker - use to get shades along with above</a></td>
    </tr>
    <tr>
        <td><a href="http://webdesign.about.com/od/css/a/css-vendor-prefixes.htm" target="_blank">CSS Vendor Prefixes</a></td>
    </tr>
    <tr>
        <td><a href="http://www.sitepoint.com/its-time-to-rethink-vendor-prefixes-in-css/" target="_blank">It’s Time to Rethink Vendor Prefixes in CSS</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes" target="_blank">Pseudo-classes - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="http://www.w3schools.com/cssref/css_selectors.asp" target="_blank">CSS Selector Reference - w3schools.com</a></td>
    </tr>
    <tr>
        <td><a href="https://design.google.com/resources/" target="_blank">Google Design Resources</a></td>
    </tr>
    <tr>
        <td><a href="http://www.javascriptkit.com/javatutors/touchevents.shtml" target="_blank">Introduction to Touch events in JavaScript</a></td>
    </tr>
    <tr>
        <td><a href="https://mobiforge.com/design-development/html5-mobile-web-touch-events" target="_blank">HTML5 for the Mobile Web: Touch Events</a></td>
    </tr>
    <tr>
        <td><a href="https://www.w3.org/Style/CSS/specs.en.html" target="_blank">CSS Specifications - w3.org</a></td>
    </tr>
    <tr>
        <td><a href="https://www.w3.org/TR/css3-layout/" target="_blank">CSS Template Layout Module - w3.org</a></td>
    </tr>
        <tr>
        <td><a href="http://alistapart.com/article/css-floats-101" target="_blank">CSS Floats 101</a></td>
    </tr>
    </tr>
        <tr>
        <td><a href="http://alistapart.com/article/css-shapes-101" target="_blank">CSS Shapes 101</a></td>
    </tr>
    </tr>
    <tr>
        <td><a href="https://www.w3.org/wiki/Styling_lists_and_links" target="_blank">Styling lists and links - w3.org</a></td>
    </tr>
    </tr>
    <tr>
        <td><a href="http://learn.shayhowe.com/html-css/creating-lists/" target="_blank">Creating Lists - learn.shayhowe.com</a></td>
    </tr>
        <tr>
        <td><a href="http://www.webdesignerdepot.com/2012/11/how-to-create-a-simple-css3-tooltip/" target="_blank">How to create a simple CSS3 tooltip</a></td>
    </tr>
        <tr>
        <td><a href="http://www.amp-what.com/unicode/search/" target="_blank">Interactive reference of 14,500 HTML character entities</a></td>
    </tr>
    <tr>
        <td><a href="http://www.sitepoint.com/media-queries-width-vs-device-width/" target="_blank">Media Queries: Width vs. Device Width - sitepoint.com</a></td>
    </tr>
    <tr>
        <td><a href="https://developers.google.com/web/fundamentals/design-and-ui/responsive/fundamentals/use-media-queries?hl=en" target="_blank">Use CSS media queries for responsiveness - developers.google.com</a></td>
    </tr>
    <tr>
        <td><a href="https://responsivedesign.is/strategy/page-layout/defining-breakpoints" target="_blank">Defining Breakpoints - responsivedesign.is</a></td>
    </tr>
        <tr>
        <td><a href="http://foundation.zurb.com/sites/docs/v/5.5.3/media-queries.html" target="_blank">Media Queries - foundation.zurb.com</a></td>
    </tr>
    <tr>
        <td><a href="http://www.sitepoint.com/understanding-css-grid-systems/" target="_blank">Understanding CSS Grid Systems from the Ground Up - sitepoint.com</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_data_attributes" target="_blank">Using data attributes - developer.mozilla.org</a></td>
    </tr>
    </tr>
        <tr>
        <td><a href="https://www.google.com/design/spec/style/color.html#" target="_blank">Material Design - Style - Color on Google</a></td>
    </tr>
    </tr>
        <tr>
        <td><a href="http://stackoverflow.com/questions/1817792/is-there-a-previous-sibling-css-selector/36118012#36118012" target="_blank">Is there a “previous sibling” CSS selector? - see solution using flex</a></td>
    </tr>
    </tr>
    <tr>
        <td><a href="http://www.csszengarden.com/" target="_blank">CSS Zen Garden</a></td>
    </tr>
    </tr>
        <tr>
        <td><a href="https://www.youtube.com/watch?v=s7JwxPnYoOw" target="_blank">Create DIV Boxes with Arrows and Pointers, using CSS</a></td>
    </tr>
    </tr>
        <tr>
        <td><a href="https://css-tricks.com/snippets/css/css-triangle/" target="_blank">CSS Triangle - css-tricks.com</a></td>
    </tr>
    <tr>
        <td><a href="http://lea.verou.me/css3patterns/#" target="_blank">CSS3 Patterns Gallery - Lea Verou</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Using_CSS_flexible_boxes" target="_blank">Using CSS flexible boxes - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://css-tricks.com/snippets/css/a-guide-to-flexbox/" target="_blank">A Complete Guide to Flexbox</a></td>
    </tr>
    <tr>
        <td><a href="https://css-tricks.com/using-flexbox/" target="_blank">Using Flexbox: Mixing Old and New for the Best Browser Support</a></td>
    </tr>
    <tr>
        <td><a href="http://responsivedesignchecker.com/" target="_blank">Responsive Design Checker</a></td>
    </tr>
    <tr>
        <td><a href="https://mothereff.in/unquoted-attributes" target="_blank">Unquoted attribute value validator</a></td>
    </tr>
    <tr>
        <td><a href="http://www.crockford.com/wrrrld/color.html" target="_blank">Standard 140 CSS color names</a></td>
    </tr>
</table>

<table>
    <tr>
        <th>References - Forms</th>
    </tr>
    <tr>
        <th>Resource Title</th>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms" target="_blank">HTML forms guide - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms/Styling_HTML_forms" target="_blank">Styling HTML forms - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="http://alistapart.com/article/flat-ui-and-forms" target="_blank">Flat UI and Forms</a></td>
    </tr>
    <tr>
        <td><a href="https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Forms/Data_form_validation" target="_blank">Data form validation - developer.mozilla.org</a></td>
    </tr>
    <tr>
        <td><a href="https://www.w3.org/TR/html5/forms.html" target="_blank">Forms - HTML5 - w3.org</a></td>
    </tr>
        <tr>
        <td><a href="" target="_blank"></a></td>
    </tr>
        <tr>
        <td><a href="" target="_blank"></a></td>
    </tr>
</table>

