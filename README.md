# Night Land Website

2025-03-12
The next version of the Night Land Website, which is devoted to the weird fiction of William Hope Hodgson. If you like H. P. Lovecraft, you might like Hodgson.

The current Joomla version is deployed at https://nightland.website.

Most of the items on the Night Land Website are copyrighted. On which, more later.

**Not ready to deploy!** Most of it's not here yet.

## Tech Used

So far:

- HTML5
- CSS3
- Sass
- Loading our own free fonts directly, instead of loading them from Google, for user privacy reasons.

There isn't any Javascript now. Maybe eventually there'll be some. The most likely use for it is to let people easily load an alternate stylesheet (a light mode being the obvious candidate). 

Sass is a CSS preprocessor, which I'm using mostly to name colors and keep commonly used values easily accessible. The *.scss are the ones I mark up. Pinegrow (my editor) converts them into the corresponding *.css files. I could've used --var() syntax for the same function, but I found out about Sass first.

## Basic Page Design

1. The design is screen-size responsive.

2. It's light on dark. This is the Night Land.

3. Most items are centered.

4. There are variable-color tiling backgrounds, deep behind everything.

5. There are dark-to-transparent gradients above that. Their function is to mask the tiling backgrounds under the centered text, so the text is legible.

6. I hope the contrast is, for most people, high enough for easy reading while falling short of being uncomfortably glary.

7. Large text can have lower contrast than small text because the bigger letters are more visible.

8. I do not set an absolute text size. Let the user pick that in their browser settings.

9. We have:
	* Text content pages;
	* Index pages;
	* Graphics content pages;
	* Graphics index pages;
	* Unusual pages.
	
	Text content pages have body text. The others usually don't.

10. There are at least 2 basic color schemes, for different sections of the site:
	* The Last Redoubt (background is black, most colors are cool);
	* The Darkening (background is red-black, most colors are warm).

11. No text on any page is intended to be magenta. If you see magenta text, it means I had no instances of that CSS selector on the original page, and so didn't decide on a color for it. Change it to something that is legible and harmonizes with the rest of the page color scheme.


### Basic CSS:
Import the common stuff:

* Font loading;
* Standard dimensions;
* General reset of bad CSS defaults;
* Color variable names.

Styles for individual page elements:
* General page settings;
* Header settings;
* Main settings;
* Footer settings.

It's as simple as I could figure out how to make it while getting the intended effect. The only more complex thing that you need to notice is that the basic construction of a page is layered:
1. tiling background (in html),
2. gradient over tiling background (in body),
3. section formatting in header, nav, main, footer.
4. specific content formatting.

## Krita Graphics Files

Files with the suffix .kra in the image folder are Krita files. They're not the versions we deploy in the website: rather, they're the layered versions I used to make some of the flat webp and png files. They're included because not having the layered versions limits what a future maintainer could do with the images.


