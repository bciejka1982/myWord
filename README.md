# myWord

<i>An easy open source way to create nice-looking web pages for essays.</i>



I have a new writing tool I'm working on and wanted it to be able to create beautiful essay pages like Medium. But Medium doesn't have an API. So I made an essay-viewer that does. ;-)

<a href="http://myword.io/">http://myword.io/</a>

Now, I'm not a great CSS hacker. That's obvious. But all that's needed is a framework to get started. That's the idea.

I'm going to keep iterating. :-)

#### Blog post

The Scripting News <a href="http://scripting.com/2015/02/12/somethingFunIWhippedUp.html">blog post</a> announcing myword.io,  a good place to post a comment.

#### MyWord Editor

There's a <a href="https://github.com/scripting/myWordEditor">new project</a> that picks up where this one left off, that turns the MyWord renderer into a full blog editing system. 

#### Updates

##### v0.48 2/16/15 by DW

1. The two main sections are both positioned <i>absolute,</i> so the text will always begin at the same vertical place no matter how much descriptive text there is.

2. There's a transparent dark rectangle around the byline-title-description section, which makes the text jump out a bit more over the picture. 

3. There's a footer section at the bottom, but I haven't done any CSS for it yet, and there's no way to set it via the JSON.

##### v0.46 2/14/15 by DW -- Happy Valentine's Day!

1. Added dropshadows to the byline and description.

2. Added styles to make it look reasonable on a phone. 

##### v0.45 2/13/15 by DW

1. Made the description fixed height, so the body text always begins at the same vertical position. 

2. Made the body text a little narrower and added to the line-height.

3. Show the version number in the upper-right corner of the page, in white.

##### v0.44 2/13/15 by DW

Thanks to an excellent <a href="http://scripting.com/2015/02/12/somethingFunIWhippedUp.html#comment-1851937171">suggestion</a> by Paulo Querido, myword.io now supports Markdown. 

Here's a <a href="http://myword.io/?url=http://myword.io/examples/markdown.json">demo page</a>, and the <a href="http://myword.io/examples/markdown.json">JSON source file</a> is renders.

Here's how it works. 

1. Markdown is off by default, you can turn it on by including "flMarkdown": "true". 

2. Markdown only applies to the subs. The title, description, byline, etc are not processed.

3. When we generate the Markdown text from the JSON, we add two linefeeds at the end of every line. So every line is effectively a paragraph. Unless it has markup that makes Markdown think it's something else.

4. The CSS for Markdown needs work. I added one fix for &lt;h4> but a lot more is probably needed to make it look great. Please, if you're good with Markdown, Bootstrap Toolkit (which is part of the environment) and CSS, take a look and see if you can improve. 

##### v0.43 2/13/15 by DW

A bunch of small changes, loose-end fixes.

1. If there's an error in the JSON, we put up a dialog saying so, along with a suggestion that you use the excellent <a href="http://jsonlint.com/">JSONLINT</a> site to find the error.

2. If it's been more than a day since an article was posted, instead of saying "By Mary Jones <b>at</b> Wednesday", we say "<b>on</b> Wednesday".

3. Before using any of the values in the JSON, be sure it exists. 

4. You can change the title font and the body font. See the <a href="http://myword.io/essay.json">example JSON file</a> for a clue.

