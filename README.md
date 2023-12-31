# hollowmountain2

In 2023, we are finally rebooting this to puiblication... 

This repo is synced with Overleaf, so first push from there to avoid getting out to sync. Ask Ben if you want access but don't have it already.

Use this repo for searches, large changes or other things that are just easier to not do in Overleaf. Be sure to pull the changes into Overleaf afterwards. 

## Organisation

Currently the editors are: Jarvist... {{ your name here, pretty please }}

Trello board for organisation: https://trello.com/b/k97lugrL/the-hollow-mountain-ii-2007-2012

Google Doc's Story 'Hit list': https://docs.google.com/spreadsheet/pub?key=0AnIVS9y2g3bAdGo2eHgzVWNUN3cxeGx5THNMdkkycnc&single=true&gid=0&output=html

## Editing / Contributing

As we are in version control with git, don't worry about breaking things by
editing text! We (the editorial team) can always undo. 

# Formatting

(Most of this is the 2014 info with Jarv's original Markdown version, but some is probably still current.)

### Author attribution

Author attribution done with the `\attrib` magic
i.e.

```
\attrib{Jarvist Moore Frost}
```

### Cave names

Encase cave names as `*Cave Name*` capitalised correctly, and it will be rendered in SMALLCAPS. 
[ Tech note: This is overriding the built-in 'emphasis' (itallic) in markdown, via a redeclaration of the TeX Macro in the header.]

### Unusual personal names

`\izi` is a macro which will expand to Izi's full name with correctly rendered Caron on top of Z.

### Footnotes

Footnotes are added with the `\footnote{}` code; in the Tuft form they appear
as numbered small text in the column. This is good for adding editorial 
future-observations / corrections without disrupting the narritative flow (i.e.
lead renamed, or lead noticed which is followed up in the future etc.)

### Pictures

Currently we are including pictures by using the Latex-fall-through mode of
Markdown, which is rather complicated:-
```
\begin{figure*}
\includegraphics[width=0.85\columnwidth]{2010/2010_deep_vrtnarija_colour_coded_inverted_labelled}
\caption{Colour coded diagram of new cave discovered \& surveyed in 2010 in
Vrtnarija.}
\end{figure*}
```

## Technical Details

The individual chapter files are stored in subdirectories (2011,2012 etc.)
along with the media (i.e. pictures) used within those chapters. The file
format is Markdown. This is compiled to Latex with Pandoc, and is then rendered
with Xelatex.

The Makefile first produces the TeX file with all the content
('HollowMountainII-2007to2012_content.tex') which is then combined with the
style/header file ('HollowMountainII-2007to2012.tex') to produce a PDF.
Currently we are rendering with the 'tufte-book' class to get a fairly
pleasantly readable single-column A4 format.
