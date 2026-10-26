# prosemirrorfx

ProseMirror-style rich text editing for JavaFX applications, kept in one place: the shared base modules and the generic components built on them.

The first modules are here, early and unreleased: they are published as `0.1.0-SNAPSHOT` builds only, with no release on Maven Central yet.

## How it is organised

Applications keep their own editor components. What turns out to be useful to more than one application is promoted here as a generic module or component, so that applications can use it as it is, or customise it, and so that the patterns can be refactored and improved in one place. An application with a completely different need builds its own component on whatever base modules are useful, and anything it builds that proves generic can later be brought here.

## Modules

- [core](https://github.com/prosemirrorfx/core): the document model, schema, commands and input rules, with no JavaFX dependency.
- [markdown](https://github.com/prosemirrorfx/markdown): markdown and clipboard HTML in and out, with a round trip that writes an unedited file back byte for byte.
- [view](https://github.com/prosemirrorfx/view): the JavaFX view of a document, drawn natively with no WebView, and an embedding class for markdown notes.
- [demo](https://github.com/prosemirrorfx/demo): a small application showing the editor on its own.

Planned, not started: format, a light, block-addressed document format for people and AI to edit together.

Maven coordinates are `io.github.prosemirrorfx:prosemirrorfx-<module>`, and Java packages are `prosemirrorfx.<module>`. Snapshots come from Central's snapshot repository, `https://central.sonatype.com/repository/maven-snapshots/`.

## Built on

- [ProseMirror](https://prosemirror.net) by Marijn Haverbeke, MIT licence, whose document model and editing design this follows.
- [prosemirror-kotlin](https://github.com/atlassian-labs/prosemirror-kotlin) by Atlassian, Apache License 2.0, the JVM port of the ProseMirror model that the base modules depend on.

This is an independent project. It is not affiliated with, endorsed by or sponsored by ProseMirror or Atlassian.
