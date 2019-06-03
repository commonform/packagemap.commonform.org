Common Form is built out of JavaScript, stored and versioned in several npm packages.

The [core packages](#core) define and enforce the schema for Common Forms, handle serializing and hashing those data for [content addressing](https://en.wikipedia.org/wiki/Content-addressable_storage), and provide a few oft-used utility modules.

[Annotators](#annotators) analyze Common Forms and return annotations to their content identifying structural and stylistic issues.

[Renderers](#renderers) transform Common Form data into other formats, like Microsoft Word, HTML, and CommonMark.

# Core

## Schemas

- The most important package is [commonform-validate](https://www.npmjs.com/package/commonform-validate), which defines the schema rules for bits of legal text expressed as Common Forms.

- [signature-page-schema](https://www.npmjs.com/package/signature-page-schema) defines a schema for data about signature pages.

- [commonform-validate-directions](https://www.npmjs.com/package/commonform-validate-directions) defines a schema for directions for filling in Common Forms' blanks.

## Content Addressing

- [commonform-serialize](https://www.npmjs.com/package/commonform-serialize) serializes JSON with keys sorted, so the same JSON always serializes the same way.

- [commonform-hash](https://www.npmjs.com/package/commonform-hash) hashes Common Forms with SHA256.

## Utilities

- [commonform-analyze](https://www.npmjs.com/package/commonform-analyze) takes a Common Form and returns a report about the terms, headings, and other structural elements it uses.

- [commonform-predicate](https://www.npmjs.com/package/commonform-predicate) provides a number of predicate functions for identifying the types of Common Form content elements.

# Annotators

Annotators take Common Forms and return arrays of notes, called annotations, about their content.

## General Annotators

- [commonform-critique](https://www.npmjs.com/package/commonform-critique) criticizes style and word choice

- [commonform-lint](https://www.npmjs.com/package/commonform-lint) notes structural issues, like undefined terms

## Specific Annotators

- [commonform-alex](https://www.npmjs.com/package/commonform-alex) annotates potentially insensitive language.

- [commonform-archaic](https://www.npmjs.com/package/commonform-archaic) annotates archaic terms.

- [commonform-mscd](https://www.npmjs.com/package/commonform-mscd) annotates usages covered by Ken Adam's Manual of Style for Contract Drafting.

- [commonform-unmarked-uses](https://www.npmjs.com/package/commonform-unmarked-uses) annotates uses of defined terms that aren't marked as uses.

- [doubleplus-numbers](https://www.npmjs.com/package/doubleplus-numbers) annotates repetitions like "ten (10)".

- [passive-aggressor](https://www.npmjs.com/package/passive-aggressor) annotates passive constructions.

## Data Packages

A number of [specific annotators](#specific-annotators) in turn depend on data packages.

- [american-legal-archaisms](https://www.npmjs.com/package/american-legal-archaisms) lists archaisms that lawyers can't seem to get enough of.

- [mscd](https://www.npmjs.com/package/mscd) lists usages discouraged in Ken Adams' Manual of Style for Contract Drafting.

- [wordy-words](https://www.npmjs.com/package/wordy-words) lists short, plain alternatives to common long words and phrases.

## Metaprogramming

- [commonform-regexp-annotator](https://www.npmjs.com/package/commonform-regexp-annotator) builds annotators based on regular expressions.

- [commonform-phrase-annotator](https://www.npmjs.com/package/commonform-phrase-annotator) builds annotators based on fixed words or phrases.

# Renderers

Renderers take Common Form data and output them into different formats.

## Specific Formats

- [commonform-docx](https://www.npmjs.com/package/commonform-docx) renders Microsoft Word `.docx` files.

- [commonform-commonmark](https://www.npmjs.com/package/commonform-commonmark) translates to and from a subset of [CommonMark](https://commonmark.org/).  See also [type.commonform.org](https://type.commonform.org).

- [commonform-html](https://www.npmjs.com/package/commonform-html) renders HTML.

- [ooxml-signature-pages](https://www.npmjs.com/package/ooxml-signature-pages) renders signature pages to Microsoft Word format.

## Helpers

- [commonform-group-series](https://www.npmjs.com/package/commonform-group-series) groups content elements into paragraphs and series of children.

- [commonform-number](https://www.npmjs.com/package/commonform-number) adds numbering metadata to Common Forms.

- [commonform-resolve](https://www.npmjs.com/package/commonform-resolve) adds metadata about blank values and referenced section numbers.

## Numberings

Numberings turn numbering metadata from commonform-number into numbers like "1(a)(iii)".

- [abstract-numbering](https://www.npmjs.com/package/abstract-numbering) defines the interface for numberings.

- [agreement-schedule-exhibits-numbering](https://www.npmjs.com/package/agreement-schedule-exhibits-numbering) renders an agreement followed by a schedule and exhibits.

- [decimal-numbering](https://www.npmjs.com/package/decimal-numbering) creates numbers like "1.2.3".

- [outline-numbering](https://www.npmjs.com/package/outline-numbering) creates numbers like "1(b)(iii)".

- [plan-addenda-exhibits-numbering](https://www.npmjs.com/package/plan-addenda-exhibits-numbering) numbers a plan followed by addenda and exhibits.

- [resolutions-schedules-exhibits-numbering](https://www.npmjs.com/package/resolutions-schedules-exhibits-numbering) renders resolutions followed by schedules and exhibits.
