# Melanie Richards - Honouring visual preferences
Slides: https://github.com/melanierichards/talks/tree/master/2019/color-contrast-view-source
Users bring with them highly personalised color and contrast needs, and these can change per day or even per hour. How are we supposed to manage all these needs and preferences with just one color scheme, while also maintaining a design point of view? 
* Media queries: `prefers-color-scheme`(allows web developer to respond to hints from the user as to what color scheme they use), `prefers-contrast`,`forced-colors `(hint that the content is rendered in user’s system colours, can occur when Windows high contrast is active).
* CSS Custom properties can be hugely helpful here, instead of static colours all over your stylesheets, we can set variables on the root node and then use these throughout our stylesheets.
* Use of `currentColor`in fills and strokes of SVGs is recommended
* CSS filter properties are great for adjusting brightness and contrast on photography without changing the actual images
* We can pair this with `color-scheme-meta`, these are hints to the rendering engine how a document can be rendered, _before_ any CSS loads. This can help prevent a flash of white.
* Additional considerations: site-level user overrides.
* We can also query for contrast by using `prefers-contrast` - this can be set to no preference, high and low. These are still under discussion and may change still. 
* How do browsers apply forced colors to web content? The rendering engine reverts some properties, mostly related to color, but also box-shadow and text-shadow. After the reverting, the rendering engine applies the user’s colors. SVGs are for the most part not modified. Only `text` and `foreignObject` are color shifted.
* Web developers know their content best and can apply that knowledge to tailor the forced-colors experience.
* Consider transparency instead of removing styling (e..g don’t remove a border, replace it with `1px solid transparent`.
* Resources:
	* [forced-colors - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/forced-colors)
	* [-ms-high-contrast - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/-ms-high-contrast)
	* [prefers-color-scheme - CSS: Cascading Style Sheets | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-color-scheme)


# Jory Burson - Standardizing JavaScript
TC39  operates in a proposal process through which they take ideas and then craft proposals around them. Anyone can comment on existing proposals or submit a new one. The processes can be quite opaque.

Resources: 
	[TC39 – Specifying JavaScript.](https://tc39.es/)

# Hui Jing Chen - Demystify Modern CSS Layouts with DevTools 
Content based sizing: how much space should content take up? New specification: CSS extrinsic and intrinsic, allowing us to assign automatic widths to the page. By default, browsers don’t break words.
	* max-content
	* min-content
	* fix-content() — still a work in progress


