---
tags:
  - "#project"
  - orangesalon
type: project
---
I'm currently using [Quartz](https://quartz.jzhao.xyz/) as a static site generator to upload the contents of my obsidian vault as html.  The problem is that I frequently will reference other notes in my Powers of Horror notes, and I need a way to include only those notes that are referenced without using anything else.

### Using Quartz

To build quartz, run
``` 
npx quartz create
```

To run quartz, run 
```
npx quartz build --serve
```

### Parsing
To that end I've been using [obsidianmd-parser](https://codeberg.org/paddyd/obsidianmd-parser) which is a python parser for obsidian files.  On Ubuntu, I've created a folder called webdev in my home directory.  In that folder, I have a pipenv setup `pipenv run python (x.py)` with the obsidian-md parser library installed.  Right now I'm building a program that will recursively go through and create symlinks for each link in the notes.