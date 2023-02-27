---
title: 'Golkonda'
date: 2023-02-27
excerpt: 'Egress control and Mitre Att&ck dashboard'
author: ['David Arthur']
coverImage: ''
tags: ['Hackfest', 'ANZ, Japan, ASEAN', 'Big-IP, Telemetry Streaming, iRules, ILX, Elastic Search, Kibana, Log Stash, Virus Total']
team: ['Yukio', 'Ito', 'James Lee', 'Kayvan Farzaneh', 'Cameron Jenkins']
sponsor: []
mentor: ['David Arthur']
---
## Project Description

Solution to help Blue Teams struggling with egress control and identifying malicious activities like C&C (C2) and data exfiltration

## Key Hypothesis

Using the Big-IP full proxy architecture and security modules, it is possible to configure a difficult to bypass, if not impregnable, egress control point from customer environments. Additionally, by understanding Mitre Att&ck techniques to acheive the Command and Control (C&C) and Exfiltration (exfil) tactics, that customer alerts can be generated to give Blue teams high fidelity signals of malicious activity and / or compromised end points.

## How It Works

The solution comprises a Big-IP system(s) with custom configurations for handling common C&C and exfil techniques; e.g.: DNS, HTTP, HTTPS, NTP, ICMP, etc. Profiles, iRules, etc. are then configured to look for specific indicators of Att&ck techniques and generate customer logging, along with the Mitre Att&ck technique and / or Tactic nomenclature, to an extenal ELK system for visualtisation. Additionally, an iRules LX (ILX) module has been written to do a sideband call out to Virus Total (VT) for additional validation and enrichment; this could be expanded to support other external threat intel systems. 

Once sent to the ELK platform, a custom dashboard has been created to surface the alert(s), the Mitre technique and / or tactic identifier, link to relevant Mitre Att&ck page, details on end-point, C&C and / or exfil destination, VT enrichment, etc.

The intent is for this to be able to be configured in three mains ways; visibility only (i.e.: alerting but no blockin), blocking (i.e.: alerting and blocking), and deception (i.e.: alerting and redirect, honey destination, misleading response, etc.)

## Business Value

Blue teams and threat hunters burn valuable cycles tryng to understand where attackers dwell in their environments and how attackers are communicating externally to accomplish their missions. This solution aims to identify malicious activity ealry, as well as provide preventative and / or deceptive controls. This allows an organisation to be selective about how they want to respond and what feedback they want to provide the attackers; using deception will still be preventative but it could buy the responders time to investigate before alerting the adversaries. It is also intended that this provide high fidelity signals to teams for investigation so as to reduce alert fatigue and tick and flick alert investigation; increasing the organisations security posture while reducing the operation burden upon security operations teams.

## Technologies Used

Big-IP, Telemetry Streaming, iRules, ILX, Elastic Search, Kibana, Log Stash, Virus Total

## Presentations

#### VIDEO EXAMPLE:

Update the src link with the embedded link of your video.

<iframe width="560" height="315" src="https://web.microsoftstream.com/embed/video/471816ec-fc92-4488-aab7-6654b4714b2f?autoplay=false&showinfo=true" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### POWERPOINT EXAMPLE:

Update the src link with the embedded link provided by powerpoint under the share option.

<iframe src="https://f5.sharepoint.com/:p:/r/sites/F5HackfestFeb23/Shared%20Documents/Egress%20Control%20Dashboard%20and%20Security%20Operations/2023-02-03_hackfest_Egress_Control.pptx?d=wefd1630a9f9845ef9823ae2580e58979&csf=1&web=1&e=QWfYAV" width="476px" height="288px" frameborder="0">This is an embedded <a target="_blank" href="https://office.com">Microsoft Office</a> presentation, powered by <a target="_blank" href="https://office.com/webapps">Office</a>.</iframe>

## Interested? Come join us!

Reach out to the principal researchers if you are interested in supporting this project.

| Role   | Skills                                                               |
| ------ | ------------------------------------------------------------------------- |
| example role  | example skills |

Note: you are free to add other sections as you'd like.

BELOW ARE EXAMPLES OF HOW TO DISPLAY TEXT ON THE MARKDOWN PAGE

# h1 Heading

## h2 Heading

### h3 Heading

#### h4 Heading

##### h5 Heading

###### h6 Heading

## Horizontal Rules

---

## Typographic replacements

Enable typographer option to see result.

(c) (C) (r) (R) (tm) (TM) (p) (P) +-

test.. test... test..... test?..... test!....

!!!!!! ???? ,, -- ---

"Smartypants, double quotes" and 'single quotes'

## Emphasis

**This is bold text**

**This is bold text**

_This is italic text_

_This is italic text_

~~Strikethrough~~

## Blockquotes

> Blockquotes can also be nested...
>
> > ...by using additional greater-than signs right next to each other...
> >
> > > ...or with spaces between arrows.

## Lists

Unordered

- Create a list by starting a line with `+`, `-`, or `*`
- Sub-lists are made by indenting 2 spaces:
  - Marker character change forces new list start:
    - Ac tristique libero volutpat at
    * Facilisis in pretium nisl aliquet
    - Nulla volutpat aliquam velit
- Very easy!

Ordered

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa

4. You can use sequential numbers...
5. ...or keep all the numbers as `1.`

Start numbering with offset:

57. foo
1. bar

## Code

Inline `code`

Block code "fences"

```
Sample text here...
```

Syntax highlighting

```js:fileName.js
var foo = function (bar) {
  return bar++;
};

console.log(foo(5));
```

## Tables

| Option | Description                                                               |
| ------ | ------------------------------------------------------------------------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default.    |
| ext    | extension to be used for dest files.                                      |

Right aligned columns

| Option |                                                               Description |
| -----: | ------------------------------------------------------------------------: |
|   data | path to data files to supply the data that will be passed into templates. |
| engine |    engine to be used for processing templates. Handlebars is the default. |
|    ext |                                      extension to be used for dest files. |

## Links

[link text](http://dev.nodeca.com)

[link with title](http://nodeca.github.io/pica/demo/ 'title text!')

Autoconverted link https://github.com/nodeca/pica (enable linkify to see)

## Plugins

The killer feature of `markdown-it` is very effective support of
[syntax plugins](https://www.npmjs.org/browse/keyword/markdown-it-plugin).

### [Emojies](https://github.com/markdown-it/markdown-it-emoji)

> Classic markup: :wink: :crush: :cry: :tear: :laughing: :yum:
>
> Shortcuts (emoticons): :-) :-( 8-) ;)

see [how to change output](https://github.com/markdown-it/markdown-it-emoji#change-output) with twemoji.

### [Subscript](https://github.com/markdown-it/markdown-it-sub) / [Superscript](https://github.com/markdown-it/markdown-it-sup)

- 19^th^
- H~2~O

==Marked text==

### [Footnotes](https://github.com/markdown-it/markdown-it-footnote)

Footnote 1 link[^first].

Footnote 2 link[^second].

Inline footnote^[Text of inline footnote] definition.

Duplicated footnote reference[^second].

[^first]: Footnote **can have markup**

    and multiple paragraphs.

[^second]: Footnote text.

### [Abbreviations](https://github.com/markdown-it/markdown-it-abbr)

This is HTML abbreviation example.

It converts "HTML", but keep intact partial entries like "xxxHTMLyyy" and so on.

[HTML]: Hyper Text Markup Language

### [Custom containers](https://github.com/markdown-it/markdown-it-container)

::: warning
_here be dragons_
:::

Fluctuations requires an enormous amount of energy, and there would be a remnant of that energy in that space afterwards if the fluctuations were flushed out, plus an unstable environment (1veritasium). Even on computers, deleted data is not actually tossed away, by rather written over. The fact that there can never be nothingness means the universe, and anything possibly beyond it, is eternal, as something has always been around. Whatever we consider to be before the Big Bang—God.

The fact that there can never be nothingness means the universe, and anything possibly beyond it, is eternal, as something has always been around. Whatever we consider to be before the Big Bang—God, the universe in infinitesimal form, or both—one thing is certain: it was there.

## Custom Components

import Demo from '../../components/Demo';

Here's a **neat** demo, click me:

<Demo />

Here's an avatar component:

<Avatar />

<br />
<Callout emoji="🚀">Callout component to draw attention!</Callout>

<br />
<ListCard
  title="Why this list is great..."
  list={['Because its React', 'it looks great', 'and can be any color']}
/>

<ListCard
  title="All the color options for this list..."
  list={[
    'slate',
    'gray',
    'zinc',
    'neutral',
    'stone',
    'red',
    'orange',
    'amber',
    'yellow',
    'lime',
    'green',
    'emerald',
    'teal',
    'cyan',
    'sky',
    'blue',
    'indigo',
    'violet',
    'purple',
    'fuchsia',
    'pink',
    'rose'
  ]}
  color="cyan"
/>

---

## Images

Markdown syntax example

![](images/InnovateF5/texture.jpg)

HTML img tag component example

<img
  src={`https://images.unsplash.com/photo-1497633762265-9d179a990aa6?crop=entropy&cs=tinysrgb&fm=jpg&ixlib=rb-1.2.1&q=60&raw_url=true&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MXx8Ym9va3N8ZW58MHx8MHx8&auto=format&fit=crop&w=500`}
/>

Image component example

<Image
  alt={`Example`}
  src={`images/InnovateF5/texture.jpg`}
  width={608}
  height={608}
/>

Theme controlled image example

<ImageWithTheme
  alt={`Theme image example`}
  light={`https://images.unsplash.com/photo-1558591710-4b4a1ae0f04d?crop=entropy&cs=tinysrgb&fm=jpg&ixlib=rb-1.2.1&q=80&raw_url=true&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=987`}
  dark={`https://images.unsplash.com/photo-1653038337841-3945ada02f59?crop=entropy&cs=tinysrgb&fm=jpg&ixlib=rb-1.2.1&q=80&raw_url=true&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=927`}
  width={608}
  height={608}
/>
# Golkonda
