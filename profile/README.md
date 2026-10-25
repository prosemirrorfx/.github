# prosemirrorfx

ProseMirror-style rich text editing for JavaFX applications, kept in one place: the shared base modules and the generic components built on them.

This organisation is new and has no published code yet.

## How it is organised

Applications keep their own editor components. What turns out to be useful to more than one application is promoted here as a generic module or component, so that applications can use it as it is, or customise it, and so that the patterns can be refactored and improved in one place. An application with a completely different need builds its own component on whatever base modules are useful, and anything it builds that proves generic can later be brought here.

## Planned modules

These are plans, not releases.

- core: the document model, schema, transforms, commands and input rules, with no JavaFX dependency.
- view: the JavaFX view of a document.
- markdown: markdown import and export.
- format: a light, block-addressed document format for people and AI to edit together.
- demo: a small application showing the editor on its own.

Java packages and Maven coordinates use `io.github.prosemirrorfx`.

## Built on

- [ProseMirror](https://prosemirror.net) by Marijn Haverbeke, MIT licence, whose document model and editing design this follows.
- [prosemirror-kotlin](https://github.com/atlassian-labs/prosemirror-kotlin) by Atlassian, Apache License 2.0, the JVM port of the ProseMirror model that the base modules depend on.

This is an independent project. It is not affiliated with, endorsed by or sponsored by ProseMirror or Atlassian.
