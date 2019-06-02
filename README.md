Common Form is built out of JavaScript, stored and versioned in several npm packages.

The [core packages](#core) define and enforce the schema for Common Forms, handle serializing and hashing those data for [content addressing](https://en.wikipedia.org/wiki/Content-addressable_storage), and provide a few oft-used utility modules.

[Annotators](#annotators) analyze Common Forms and return annotations to their content identifying structural and stylistic issues.

[Renderers](#renders) transform Common Form data into other formats, like Microsoft Word, HTML, and CommonMark.

# Core

## Schema

The most important package is [commonform-validate](https://www.npmjs.com/package/commonform-validate), which defines the schema rules for bits of legal text expressed as Common Forms.

## Content Addressing

- [commonform-serialize](https://www.npmjs.com/package/commonform-serialize)
- [commonform-hash](https://www.npmjs.com/package/commonform-hash)

## Utilities

- [commonform-analyze](https://www.npmjs.com/package/commonform-analyze)
- [commonform-predicate](https://www.npmjs.com/package/commonform-predicate)

# Annotators

Annotators take Common Forms and return arrays of notes, called annotations, about their content.

## General Annotators

- [commonform-critique](https://www.npmjs.com/package/commonform-critique) criticizes style and word choice
- [commonform-lint](https://www.npmjs.com/package/commonform-lint) notes structural issues, like undefined terms

## Specific Annotators

- [commonform-alex](https://www.npmjs.com/package/commonform-alex)
- [commonform-archaic](https://www.npmjs.com/package/commonform-archaic)
- [commonform-mscd](https://www.npmjs.com/package/commonform-mscd)
- [commonform-unmarked-uses](https://www.npmjs.com/package/commonform-unmarked-uses)
- [doubleplus-numbers](https://www.npmjs.com/package/doubleplus-numbers)
- [passive-aggressor](https://www.npmjs.com/package/passive-aggressor)

## Data Packages

A number of [specific annotators](#specific-annotators) in turn depend on data packages.

- [american-legal-archaisms](https://www.npmjs.com/package/american-legal-archaisms)
- [mscd](https://www.npmjs.com/package/mscd)
- [wordy-words](https://www.npmjs.com/package/wordy-words)

## Metaprogramming

- [commonform-regexp-annotator](https://www.npmjs.com/package/commonform-regexp-annotator)
- [commonform-phrase-annotator](https://www.npmjs.com/package/commonform-phrase-annotator)

# Renderers

## Specific Formats

- [commonform-docx](https://www.npmjs.com/package/commonform-docx)
- [commonform-commonmark](https://www.npmjs.com/package/commonform-commonmark)
- [commonform-html](https://www.npmjs.com/package/commonform-html)
- [ooxml-signature-pages](https://www.npmjs.com/package/ooxml-signature-pages)

## Helpers

- [commonform-group-series](https://www.npmjs.com/package/commonform-group-series)
- [commonform-number](https://www.npmjs.com/package/commonform-number)
- [commonform-resolve](https://www.npmjs.com/package/commonform-resolve)

## Numberings

- [abstract-numbering](https://www.npmjs.com/package/abstract-numbering)
- [agreement-schedule-exhibits-numbering](https://www.npmjs.com/package/agreement-schedule-exhibits-numbering)
- [decimal-numbering](https://www.npmjs.com/package/decimal-numbering)
- [outline-numbering](https://www.npmjs.com/package/outline-numbering)
- [plan-addenda-exhibits-numbering](https://www.npmjs.com/package/plan-addenda-exhibits-numbering)
- [resolutions-schedules-exhibits-numbering](https://www.npmjs.com/package/resolutions-schedules-exhibits-numbering)
