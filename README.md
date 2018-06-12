# md_docs
Template for HTML documentation generated from markdown via pandoc

## Requirements

* GNU Make
* pandoc
* inotify-tools

## How to use

### Edit files

First of all, edit `src/metadata.yaml`: title, author, abstract, etc.

Place your Markdown files into the folder `src`. Their filenames determine their order in the final document.

Images go into the `src/img` folder.

### Compile

Run `make` to compile once.

### Automatically recompile and refresh

Set page refresh timeout in the `00_header.md` to a lower value. Run `make watch` in the terminal. Open the created HTML file with the browser.

Now edit the files. As soon as they are modified the document is recompiled. The browser updates the view asynchronously.

**Pro tip:** you can embed `live.js` into  `00_header.md` and serve the HTML page via a simple web server, i.e. Python `SimpleHTTPServer`. Then the browser updates the page only when it changed, e.g. synchronously.

### Change style

The style of the final webpage is determined by the CSS file `.pandoc_style.css`
