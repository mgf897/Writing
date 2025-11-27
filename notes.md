# Test

Fiction or nonfiction? 
Writing books that sell

Reasons to write 
Fiction
- storytelling
- share ideas 

Non-fiction 
- solve a problem for the reader 
- share knowledge 

If every book is a startup, which is more likely to succeed? 

## Pandoc
Pandoc can combine multiple Markdown files and create various output including EPUB

EPUB file can be uploaded to Amazon KDP to become Kindle titles 

Book metadata (like title, author, cover image) is defined in a YAML block 

```

---
title:  'This is the title: it contains a colon'
author:
- Author One
- Author Two
keywords: [nothing, nothingness]
cover-image: ./filename.png
date: YYYY-MM-DD (Only the year is necessary.)
...
```

Markdown files are concatenated together sorted by filename. Using numerical filenames makes this easy. E.g. `0001_frontMatter.md` and `9999_backMatter.md`

Python can be used to generate Markdown files based on generated content.

All files can be comined using
`pandoc -o book.epub --toc --strip-comments *.md`

Page breaks can be enforced by including inline HTML in the Markdown files
`<div style="page-break-after: always;"></div>`
