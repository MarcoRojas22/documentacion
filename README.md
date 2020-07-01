# Documentation generation style guidelines

The following guidelines must be applied to format documentation files, as they're meant to improve guides' uniformity and user experience.

## File naming

All document files must be markdown (.md) files, using lowercase words separated by dashes (-). Their names must start with a letter, and end with a number or a letter.

## Document Meta Data

Each document must have these parameters defined at the beginning of its content. These parameters are needed by the markdown parser, so that each document is created accordingly.

**Mandatory parameters**

* **layout** defines the template that will be used for the html of the document. The value for a document that will be published inside **Guides and Resources** must be `guides`.
* **section** specifies the section's name where this document will be placed: "About this release", "Getting started", "Developer guide" ...
* **title** specifies the page title.

**Example**

~~~yaml
---
layout: guides.html
section: Best Practices
title: Using icons
---
~~~

## Title hierarchy

Titles must start with a numbers of hashes that define their title hierarchy:

* `#` for the **document's main title**.
* `##` for each **document section**
* `###` for each **section subtitle**

Remember to use a blank line **before and after** each title line.

**Example**

~~~markdown

# Introducing Cells

The first release of the Cells Core ...

## Highlights

### Cells Core

* Dynamic integration ...

~~~

## Code text formatting

You can use inline code formatting like `echo some code` within two ` characters, or block code formatting like:

~~~markdown
```js
console.log('hi');
```
~~~

This way you can specify the code's language format.

Remember to use a blank line **before and after** each code block.

## Youtube Videos

You must use the [`google-youtube`](https://elements.polymer-project.org/elements/google-youtube) Polymer component for each video you want to insert. The `video-id` attribute will be the video's id from Youtube.

The `<google-youtube>` must have the `class="yt-embed"` class to inherit the guide's styles.

~~~html
<google-youtube
  class="yt-embed"
  video-id="BF1vhr-GzN8"
  autoplay="0"
  rel="0"
  fluid>
</google-youtube>
~~~

# Contributing to Cells Guides

1. Create a fork or branch from the **master** branch for your contribution.
2. You should modify the .md files: this README.md or the files under docs subfolders in order to contribute to the guides.
3. Make a Pull Request to the **master** branch.
4. The updated information will be deployed at [https://bbva-devplatform.appspot.com/en-us/developers/engines/cells/index.html](https://bbva-devplatform.appspot.com/en-us/developers/engines/cells/index.html)

# Testing

Check links of markdowns:
> npm run test:links
