

The is a simple website, to present the content of a mini-textbook
which tutors how a modern LLM works, for the University of Manchester
EEEN3001 module.

This website is based on Hugo, and uses a theme named Hextra, which in
turn uses dependencies such as KaTeX and FlexSearch.

The theme has been forked and edited, for longevity, and to give
better credit to the dependencies behind the Hextra theme.

To edit via Github Codespaces:

- upon generating the Codespace, run `download_theme.sh` so that the site can be built by Hugo
- during development, decomment `<!-- <meta http-equiv="refresh" content="2"> -->` to prevent automatic refreshes (there was some issue with the Hugo's `livereload.js`, so this is a quickfix)
- run `hugo serve -D`

The website has been mirrored in the following locations thus far:

- https://llm-textbook.pages.dev/docs/
- https://qdosgit3.github.io/llm_textbook/
-


By Thomas Prior


