---
{"dg-publish":true,"permalink":"/resources/obsidian-notes-for-1-on-1/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowInlineTitle":true}
---


# Overview
I needed the ability to take actions to raise with someone across all notes to allow for taking feedback items during meetings and in daily notes.

The rough outcome of this is you set up a task that is tagged with `#1on1` or `#question` then link to the persons page. 

# Steps
1. Create below as a markdown file called `People Footer`
2. Remove the `js` from the syntax highlighting making it a `dataviewjs` element

# To chat about
```js dataviewjs
dv.taskList(dv.pages().file.tasks
    .where(t => 
	    !t.completed 
	    && (t.text.includes("#1on1") || t.text.includes("#question"))
	    && t.text.includes("[[" + dv.current().file.name + "]]")
	)
)
```

3. Add the below `dataviewjs` section to each person page you want to display this on

```js dataviewjs
const footer = await dv.io.load(dv.page("People Footer").file.path)
dv.paragraph(footer)
```