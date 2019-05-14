# Thesis LaTeX Template

Fork this repository to customize the template.

## Document Options

- `swedish, english`, english main language
- `english,swedish`, swedish main language
- `twoside`, creates a two-sided document (for printing)
- `leftblank`, adds a message to all blank left pages
- `frontmattersintoc`, add all front matter headings to the table of contents
- `abstractintoc`, add the abstract to the table of contents
- `acknowledgementsintoc`, add the acknowledgement to the table of contents
- `listsintoc`, add all the lists to the table of contents
- `tocintoc`, add the the table of content to the table of content

## `main.tex`

At the beginning of `main.tex` you find storing commands (`\title`, `\subtitle`, `\author`, `\supervisor`) to be set by the student.

```
%\title{}      % Your Title/Din titel
%\subtitle{}   % Your Subtitle/Din undertitel
%\author{}     % Your Name/Ditt namn
%\supervisor{} % Your Supervisor/Din handledare
```

## Watermark

The command `\watermark` puts the transparent text `DRAFT` in the foreground on every page. It's possible the customize the watermark text passing a string `\watermark{Approved}`.

## `settings.sty` (for the course coordinator)

In `settings.sty` you find storing commands (`\documenttype`, `\semester`, `\subject`, `\level`, `\credits`) common for a course round and to be set by the course coordinator.

```
\NeedsTeXFormat{LaTeX2e}
\ProvidesPackage{settings}[2019-05-13]

\addto{\captionsenglish}{%
    \renewcommand*\documenttypename{}
    \renewcommand*\semestername{}
    \renewcommand*\subjectname{}
    \renewcommand*\levelname{}
    \renewcommand*\creditsname{}}
\addto{\captionsswedish}{%
    \renewcommand*\documenttypename{}
    \renewcommand*\semestername{}
    \renewcommand*\subjectname{}
    \renewcommand*\levelname{}
    \renewcommand*\creditsname{}}

\examiner{}
\coursecode{} 
```
