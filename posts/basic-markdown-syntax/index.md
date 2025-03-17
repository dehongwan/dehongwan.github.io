# Basic Markdown Syntax


This article offers a sample of basic Markdown syntax that can be used in Hugo content files.

&lt;!--more--&gt;

{{&lt; admonition &gt;}}
This article is a shameful copy of the great [Grav original page](https://learn.getgrav.org/content/markdown).

If you want to know about the extended Markdown syntax of **LoveIt** theme, please read [extended Markdown syntax page](../theme-documentation-content#extended-markdown-syntax).
{{&lt; /admonition &gt;}}

Let&#39;s face it: Writing content for the Web is tiresome. WYSIWYG editors help alleviate this task, but they generally result in horrible code, or worse yet, ugly web pages.

**Markdown** is a better way to write **HTML**, without all the complexities and ugliness that usually accompanies it.

Some of the key benefits are:

1. Markdown is simple to learn, with minimal extra characters, so it&#39;s also quicker to write content.
2. Less chance of errors when writing in Markdown.
3. Produces valid XHTML output.
4. Keeps the content and the visual display separate, so you cannot mess up the look of your site.
5. Write in any text editor or Markdown application you like.
6. Markdown is a joy to use!

John Gruber, the author of Markdown, puts it like this:

&gt; The overriding design goal for Markdown’s formatting syntax is to make it as readable as possible.
&gt; The idea is that a Markdown-formatted document should be publishable as-is, as plain text,
&gt; without looking like it’s been marked up with tags or formatting instructions.
&gt; While Markdown’s syntax has been influenced by several existing text-to-HTML filters,
&gt; the single biggest source of inspiration for Markdown’s syntax is the format of plain text email.
&gt;
&gt; {{&lt; style &#34;text-align: right;&#34; &gt;}}-- _John Gruber_{{&lt; /style &gt;}}

Without further delay, let us go over the main elements of Markdown and what the resulting HTML looks like!

{{&lt; admonition tip &gt;}}
:(far fa-bookmark fa-fw): Bookmark this page for easy future reference!
{{&lt; /admonition &gt;}}

## 1 Headings

Headings from `h2` through `h6` are constructed with a `#` for each level:

```markdown
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading
```

The HTML looks like this:

```html
&lt;h2&gt;h2 Heading&lt;/h2&gt;
&lt;h3&gt;h3 Heading&lt;/h3&gt;
&lt;h4&gt;h4 Heading&lt;/h4&gt;
&lt;h5&gt;h5 Heading&lt;/h5&gt;
&lt;h6&gt;h6 Heading&lt;/h6&gt;
```

{{&lt; admonition note &#34;Heading IDs&#34; &gt;}}
To add a custom heading ID, enclose the custom ID in curly braces on the same line as the heading:

```markdown
### A Great Heading {#custom-id}
```

The HTML looks like this:

```html
&lt;h3 id=&#34;custom-id&#34;&gt;A Great Heading&lt;/h3&gt;
```
{{&lt; /admonition &gt;}}

## 2 Comments

Comments should be HTML compatible.

```html
&lt;!--
This is a comment
--&gt;
```

Comment below should **NOT** be seen:

&lt;!--
This is a comment
--&gt;

## 3 Horizontal Rules

The HTML `&lt;hr&gt;` element is for creating a &#34;thematic break&#34; between paragraph-level elements.
In Markdown, you can create a `&lt;hr&gt;` with any of the following:

* `___`: three consecutive underscores
* `---`: three consecutive dashes
* `***`: three consecutive asterisks

The rendered output looks like this:

___
---
***

## 4 Body Copy

Body copy written as normal, plain text will be wrapped with `&lt;p&gt;&lt;/p&gt;` tags in the rendered HTML.

So this body copy:

```markdown
Lorem ipsum dolor sit amet, graecis denique ei vel, at duo primis mandamus. Et legere ocurreret pri,
animal tacimates complectitur ad cum. Cu eum inermis inimicus efficiendi. Labore officiis his ex,
soluta officiis concludaturque ei qui, vide sensibus vim ad.
```

The HTML looks like this:

```html
&lt;p&gt;Lorem ipsum dolor sit amet, graecis denique ei vel, at duo primis mandamus. Et legere ocurreret pri, animal tacimates complectitur ad cum. Cu eum inermis inimicus efficiendi. Labore officiis his ex, soluta officiis concludaturque ei qui, vide sensibus vim ad.&lt;/p&gt;
```

A **line break** can be done with one blank line.

## 5 Inline HTML

If you need a certain HTML tag (with a class) you can simply use HTML:

```html
Paragraph in Markdown.

&lt;div class=&#34;class&#34;&gt;
    This is &lt;b&gt;HTML&lt;/b&gt;
&lt;/div&gt;

Paragraph in Markdown.
```

## 6 Emphasis

### Bold

For emphasizing a snippet of text with a heavier font-weight.

The following snippet of text is **rendered as bold text**.

```markdown
**rendered as bold text**
__rendered as bold text__
```

The HTML looks like this:

```html
&lt;strong&gt;rendered as bold text&lt;/strong&gt;
```

### Italics

For emphasizing a snippet of text with italics.

The following snippet of text is _rendered as italicized text_.

```markdown
*rendered as italicized text*
_rendered as italicized text_
```

The HTML looks like this:

```html
&lt;em&gt;rendered as italicized text&lt;/em&gt;
```

### Strikethrough

In [[GFM]^(GitHub flavored Markdown)](https://github.github.com/gfm/) you can do strikethroughs.

```markdown
~~Strike through this text.~~
```

The rendered output looks like this:

~~Strike through this text.~~

The HTML looks like this:

```html
&lt;del&gt;Strike through this text.&lt;/del&gt;
```

### Combination

Bold, italics, and strikethrough can be used in combination.

```markdown
***bold and italics***
~~**strikethrough and bold**~~
~~*strikethrough and italics*~~
~~***bold, italics and strikethrough***~~
```

The rendered output looks like this:

***bold and italics***

~~**strikethrough and bold**~~

~~*strikethrough and italics*~~

~~***bold, italics and strikethrough***~~

The HTML looks like this:

```html
&lt;em&gt;&lt;strong&gt;bold and italics&lt;/strong&gt;&lt;/em&gt;
&lt;del&gt;&lt;strong&gt;strikethrough and bold&lt;/strong&gt;&lt;/del&gt;
&lt;del&gt;&lt;em&gt;strikethrough and italics&lt;/em&gt;&lt;/del&gt;
&lt;del&gt;&lt;em&gt;&lt;strong&gt;bold, italics and strikethrough&lt;/strong&gt;&lt;/em&gt;&lt;/del&gt;
```

## 7 Blockquotes

For quoting blocks of content from another source within your document.

Add `&gt;` before any text you want to quote:

```markdown
&gt; **Fusion Drive** combines a hard drive with a flash storage (solid-state drive) and presents it as a single logical volume with the space of both drives combined.
```

The rendered output looks like this:

&gt; **Fusion Drive** combines a hard drive with a flash storage (solid-state drive) and presents it as a single logical volume with the space of both drives combined.

The HTML looks like this:

```html
&lt;blockquote&gt;
  &lt;p&gt;
    &lt;strong&gt;Fusion Drive&lt;/strong&gt; combines a hard drive with a flash storage (solid-state drive) and presents it as a single logical volume with the space of both drives combined.
  &lt;/p&gt;
&lt;/blockquote&gt;
```

Blockquotes can also be nested:

```markdown
&gt; Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue.
Nunc augue augue, aliquam non hendrerit ac, commodo vel nisi.
&gt;&gt; Sed adipiscing elit vitae augue consectetur a gravida nunc vehicula. Donec auctor
odio non est accumsan facilisis. Aliquam id turpis in dolor tincidunt mollis ac eu diam.
```

The rendered output looks like this:

&gt; Donec massa lacus, ultricies a ullamcorper in, fermentum sed augue.
Nunc augue augue, aliquam non hendrerit ac, commodo vel nisi.
&gt;&gt; Sed adipiscing elit vitae augue consectetur a gravida nunc vehicula. Donec auctor
odio non est accumsan facilisis. Aliquam id turpis in dolor tincidunt mollis ac eu diam.

## 8 Lists

### Unordered

A list of items in which the order of the items does not explicitly matter.

You may use any of the following symbols to denote bullets for each list item:

```markdown
* valid bullet
- valid bullet
&#43; valid bullet
```

For example:

```markdown
* Lorem ipsum dolor sit amet
* Consectetur adipiscing elit
* Integer molestie lorem at massa
* Facilisis in pretium nisl aliquet
* Nulla volutpat aliquam velit
  * Phasellus iaculis neque
  * Purus sodales ultricies
  * Vestibulum laoreet porttitor sem
  * Ac tristique libero volutpat at
* Faucibus porta lacus fringilla vel
* Aenean sit amet erat nunc
* Eget porttitor lorem
```

The rendered output looks like this:

* Lorem ipsum dolor sit amet
* Consectetur adipiscing elit
* Integer molestie lorem at massa
* Facilisis in pretium nisl aliquet
* Nulla volutpat aliquam velit
  * Phasellus iaculis neque
  * Purus sodales ultricies
  * Vestibulum laoreet porttitor sem
  * Ac tristique libero volutpat at
* Faucibus porta lacus fringilla vel
* Aenean sit amet erat nunc
* Eget porttitor lorem

The HTML looks like this:

```html
&lt;ul&gt;
  &lt;li&gt;Lorem ipsum dolor sit amet&lt;/li&gt;
  &lt;li&gt;Consectetur adipiscing elit&lt;/li&gt;
  &lt;li&gt;Integer molestie lorem at massa&lt;/li&gt;
  &lt;li&gt;Facilisis in pretium nisl aliquet&lt;/li&gt;
  &lt;li&gt;Nulla volutpat aliquam velit
    &lt;ul&gt;
      &lt;li&gt;Phasellus iaculis neque&lt;/li&gt;
      &lt;li&gt;Purus sodales ultricies&lt;/li&gt;
      &lt;li&gt;Vestibulum laoreet porttitor sem&lt;/li&gt;
      &lt;li&gt;Ac tristique libero volutpat at&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Faucibus porta lacus fringilla vel&lt;/li&gt;
  &lt;li&gt;Aenean sit amet erat nunc&lt;/li&gt;
  &lt;li&gt;Eget porttitor lorem&lt;/li&gt;
&lt;/ul&gt;
```

### Ordered

A list of items in which the order of items does explicitly matter.

```markdown
1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
4. Facilisis in pretium nisl aliquet
5. Nulla volutpat aliquam velit
6. Faucibus porta lacus fringilla vel
7. Aenean sit amet erat nunc
8. Eget porttitor lorem
```

The rendered output looks like this:

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
4. Facilisis in pretium nisl aliquet
5. Nulla volutpat aliquam velit
6. Faucibus porta lacus fringilla vel
7. Aenean sit amet erat nunc
8. Eget porttitor lorem

The HTML looks like this:

```html
&lt;ol&gt;
  &lt;li&gt;Lorem ipsum dolor sit amet&lt;/li&gt;
  &lt;li&gt;Consectetur adipiscing elit&lt;/li&gt;
  &lt;li&gt;Integer molestie lorem at massa&lt;/li&gt;
  &lt;li&gt;Facilisis in pretium nisl aliquet&lt;/li&gt;
  &lt;li&gt;Nulla volutpat aliquam velit&lt;/li&gt;
  &lt;li&gt;Faucibus porta lacus fringilla vel&lt;/li&gt;
  &lt;li&gt;Aenean sit amet erat nunc&lt;/li&gt;
  &lt;li&gt;Eget porttitor lorem&lt;/li&gt;
&lt;/ol&gt;
```

{{&lt; admonition tip &gt;}}
If you just use `1.` for each number, Markdown will automatically number each item. For example:

```markdown
1. Lorem ipsum dolor sit amet
1. Consectetur adipiscing elit
1. Integer molestie lorem at massa
1. Facilisis in pretium nisl aliquet
1. Nulla volutpat aliquam velit
1. Faucibus porta lacus fringilla vel
1. Aenean sit amet erat nunc
1. Eget porttitor lorem
```

The rendered output looks like this:

1. Lorem ipsum dolor sit amet
1. Consectetur adipiscing elit
1. Integer molestie lorem at massa
1. Facilisis in pretium nisl aliquet
1. Nulla volutpat aliquam velit
1. Faucibus porta lacus fringilla vel
1. Aenean sit amet erat nunc
1. Eget porttitor lorem
{{&lt; /admonition &gt;}}

### Task Lists

Task lists allow you to create a list of items with checkboxes. To create a task list, add dashes (`-`) and brackets with a space (`[ ]`) before task list items. To select a checkbox, add an x in between the brackets (`[x]`).

```markdown
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```

The rendered output looks like this:

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

## 9 Code

### Inline Code

Wrap inline snippets of code with &lt;code&gt;`&lt;/code&gt;.

```markdown
In this example, `&lt;section&gt;&lt;/section&gt;` should be wrapped as **code**.
```

The rendered output looks like this:

In this example, `&lt;section&gt;&lt;/section&gt;` should be wrapped as **code**.

The HTML looks like this:

```html
&lt;p&gt;
  In this example, &lt;code&gt;&amp;lt;section&amp;gt;&amp;lt;/section&amp;gt;&lt;/code&gt; should be wrapped with &lt;strong&gt;code&lt;/strong&gt;.
&lt;/p&gt;
```

### Indented Code

Or indent several lines of code by at least four spaces, as in:

```markdown
    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
```

The rendered output looks like this:

    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code

The HTML looks like this:

```html
&lt;pre&gt;
  &lt;code&gt;
    // Some comments
    line 1 of code
    line 2 of code
    line 3 of code
  &lt;/code&gt;
&lt;/pre&gt;
```

### Block Fenced Code

Use &#34;fences&#34; &lt;code&gt;```&lt;/code&gt; to block in multiple lines of code with a language attribute.

{{&lt; highlight markdown &gt;}}
```markdown
Sample text here...
```
{{&lt; / highlight &gt;}}

The HTML looks like this:

```html
&lt;pre language-html&gt;
  &lt;code&gt;Sample text here...&lt;/code&gt;
&lt;/pre&gt;
```

### Syntax Highlighting

[GFM]^(GitHub Flavored Markdown) also supports syntax highlighting.

To activate it, simply add the file extension of the language you want to use directly after the first code &#34;fence&#34;,
&lt;code&gt;```js&lt;/code&gt;, and syntax highlighting will automatically be applied in the rendered HTML.

For example, to apply syntax highlighting to JavaScript code:

{{&lt; highlight markdown &gt;}}
```js
grunt.initConfig({
  assemble: {
    options: {
      assets: &#39;docs/assets&#39;,
      data: &#39;src/data/*.{json,yml}&#39;,
      helpers: &#39;src/custom-helpers.js&#39;,
      partials: [&#39;src/partials/**/*.{hbs,md}&#39;]
    },
    pages: {
      options: {
        layout: &#39;default.hbs&#39;
      },
      files: {
        &#39;./&#39;: [&#39;src/templates/pages/index.hbs&#39;]
      }
    }
  }
};
```
{{&lt; / highlight &gt;}}

The rendered output looks like this:

```js
grunt.initConfig({
  assemble: {
    options: {
      assets: &#39;docs/assets&#39;,
      data: &#39;src/data/*.{json,yml}&#39;,
      helpers: &#39;src/custom-helpers.js&#39;,
      partials: [&#39;src/partials/**/*.{hbs,md}&#39;]
    },
    pages: {
      options: {
        layout: &#39;default.hbs&#39;
      },
      files: {
        &#39;./&#39;: [&#39;src/templates/pages/index.hbs&#39;]
      }
    }
  }
};
```

{{&lt; admonition &gt;}}
[Syntax highlighting page](https://gohugo.io/content-management/syntax-highlighting/) in **Hugo** Docs introduces more about syntax highlighting, including highlight shortcode.
{{&lt; /admonition &gt;}}

## 10 Tables

Tables are created by adding pipes as dividers between each cell, and by adding a line of dashes (also separated by bars) beneath the header. Note that the pipes do not need to be vertically aligned.

```markdown
| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

The rendered output looks like this:

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

The HTML looks like this:

```html
&lt;table&gt;
  &lt;thead&gt;
    &lt;tr&gt;
      &lt;th&gt;Option&lt;/th&gt;
      &lt;th&gt;Description&lt;/th&gt;
    &lt;/tr&gt;
  &lt;/thead&gt;
  &lt;tbody&gt;
    &lt;tr&gt;
      &lt;td&gt;data&lt;/td&gt;
      &lt;td&gt;path to data files to supply the data that will be passed into templates.&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
      &lt;td&gt;engine&lt;/td&gt;
      &lt;td&gt;engine to be used for processing templates. Handlebars is the default.&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
      &lt;td&gt;ext&lt;/td&gt;
      &lt;td&gt;extension to be used for dest files.&lt;/td&gt;
    &lt;/tr&gt;
  &lt;/tbody&gt;
&lt;/table&gt;
```

{{&lt; admonition note &#34;Right or center aligned text&#34; &gt;}}
Adding a colon on the right side of the dashes below any heading will right align text for that column.

Adding colons on both sides of the dashes below any heading will center align text for that column.

```markdown
| Option | Description |
|:------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

The rendered output looks like this:

| Option | Description |
|:------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
{{&lt; /admonition &gt;}}

## 11 Links {#links}

### Basic Link

```markdown
&lt;https://assemble.io&gt;
&lt;contact@revolunet.com&gt;
[Assemble](https://assemble.io)
```

The rendered output looks like this (hover over the link, there is no tooltip):

&lt;https://assemble.io&gt;

&lt;contact@revolunet.com&gt;

[Assemble](https://assemble.io)

The HTML looks like this:

```html
&lt;a href=&#34;https://assemble.io&#34;&gt;https://assemble.io&lt;/a&gt;
&lt;a href=&#34;mailto:contact@revolunet.com&#34;&gt;contact@revolunet.com&lt;/a&gt;
&lt;a href=&#34;https://assemble.io&#34;&gt;Assemble&lt;/a&gt;
```

### Add a Title

```markdown
[Upstage](https://github.com/upstage/ &#34;Visit Upstage!&#34;)
```

The rendered output looks like this (hover over the link, there should be a tooltip):

[Upstage](https://github.com/upstage/ &#34;Visit Upstage!&#34;)

The HTML looks like this:

```html
&lt;a href=&#34;https://github.com/upstage/&#34; title=&#34;Visit Upstage!&#34;&gt;Upstage&lt;/a&gt;
```

### Named Anchors

Named anchors enable you to jump to the specified anchor point on the same page. For example, each of these chapters:

```markdown
## Table of Contents
  * [Chapter 1](#chapter-1)
  * [Chapter 2](#chapter-2)
  * [Chapter 3](#chapter-3)
```

will jump to these sections:

```markdown
## Chapter 1 &lt;a id=&#34;chapter-1&#34;&gt;&lt;/a&gt;
Content for chapter one.

## Chapter 2 &lt;a id=&#34;chapter-2&#34;&gt;&lt;/a&gt;
Content for chapter one.

## Chapter 3 &lt;a id=&#34;chapter-3&#34;&gt;&lt;/a&gt;
Content for chapter one.
```

{{&lt; admonition &gt;}}
The specific placement of the anchor tag seems to be arbitrary. They are placed inline here since it seems to be unobtrusive, and it works.
{{&lt; /admonition &gt;}}

## 12 Footnotes

Footnotes allow you to add notes and references without cluttering the body of the document. When you create a footnote, a superscript number with a link appears where you added the footnote reference. Readers can click the link to jump to the content of the footnote at the bottom of the page.

To create a footnote reference, add a caret and an identifier inside brackets (`[^1]`). Identifiers can be numbers or words, but they can’t contain spaces or tabs. Identifiers only correlate the footnote reference with the footnote itself — in the output, footnotes are numbered sequentially.

Add the footnote using another caret and number inside brackets with a colon and text (`[^1]: My footnote.`). You don’t have to put footnotes at the end of the document. You can put them anywhere except inside other elements like lists, block quotes, and tables.

```markdown
This is a digital footnote[^1].
This is a footnote with &#34;label&#34;[^label]

[^1]: This is a digital footnote
[^label]: This is a footnote with &#34;label&#34;
```

This is a digital footnote[^1].

This is a footnote with &#34;label&#34;[^label]

[^1]: This is a digital footnote
[^label]: This is a footnote with &#34;label&#34;

## 13 Images

Images have a similar syntax to links but include a preceding exclamation point.

```markdown
![Minion](https://octodex.github.com/images/minion.png)
```

![Minion](https://octodex.github.com/images/minion.png)

or:

```markdown
![Alt text](https://octodex.github.com/images/stormtroopocat.jpg &#34;The Stormtroopocat&#34;)
```

![Alt text](https://octodex.github.com/images/stormtroopocat.jpg &#34;The Stormtroopocat&#34;)

Like links, images also have a footnote style syntax:

```markdown
![Alt text][id]
```

![Alt text][id]

With a reference later in the document defining the URL location:

```markdown
[id]: https://octodex.github.com/images/dojocat.jpg  &#34;The Dojocat&#34;
```

[id]: https://octodex.github.com/images/dojocat.jpg  &#34;The Dojocat&#34;

{{&lt; admonition tip &gt;}}
**LoveIt** theme has [special shortcode for image](../theme-documentation-extended-shortcodes#image), which provides more features.
{{&lt; /admonition &gt;}}


---

> Author: Dillon  
> URL: https://dehongwan.github.io/posts/basic-markdown-syntax/  

