# Amadeus PlantUML Theme

## What is it?

This is a plantUML theme for my employer, [Amadeus](https://amadeus.com). It
draws from the official brand colors and makes other adjustments to make nicer
diagrams.

## Why?

I firmly believe that communicating effectively requires removing as many
barriers to understanding as possible. A key barrier to consider is *cognitive
load*, which can be summarized as the amount of ideas, jargon, and notation that
must be understood before one can begin to understand the actual message or idea
being conveyed.

Diagrams are often used to provide visual aids to understanding of systems,
including software and business systems. But diagrams produced by plantuml,
the leading diagramming software in Amadeus (and many other organizations), the
default visuals produced are noisy and ugly. Noise occurs when diagrams fail
to hierarchically apply color, emphasis, and transparency to draw focus to the
essential concepts, while retaining the supplemental information required when
reviewing the diagram deeply. Ugliness, while often considered unimportant,
distracts the mind from the message and subconciously generates negative
emotional response. Elimination of noise and ugliness are some of the key jobs
of design in marketing and communications, but are applicable even to internal
stakeholders. In other words, taking care to make a clean, readable theme makes
this essential tool more effective.

## Status

This theme does not yet cover all elements supported by plantuml. Contributions
are welcome. Elements for the following are mostly complete:

- component diagrams
- sequence diagrams
- use case diagrams

## Usage

In your plantuml diagram files, declare the theme like so:

```puml
@startuml

!theme amadeus from https://raw.githubusercontent.com/EpocSquadron/plantuml-theme-amadeus/main/

' The rest of your diagram here...

@enduml
```

If you are modifying the theme locally (please consider contributing!) you can clone
this repository or download just the `puml-theme-amadeus.puml` file locally, then
point to it in your theme declaration:

```puml
@startuml

' Assuming you cloned into a sibling directory relative to the diagram
!theme amadeus from ../plantuml-theme-amadeus/

' The rest of your diagram here...

@enduml
```

### Amadeus Colors

The theme defines a number of colors following the pattern `<VARIANT><COLOR><Optional:ALPHA>`.
Example colors are `DARKSKY`, `LIGHTVIOLETALPHA`, and `VIVIDCANARY`. Here are the complete
options:

- VARIANT: Amadeus brand guidelines define three variants of each core color, termed
  `LIGHT`, `DARK`, and `VIVID`.
- COLOR: The core colors, with names derived from travel themed scenes. They are `SKY`,
  `FOREST`, `CANARY`, `CRIMSON`, `FUCHSIA`, or `VIOLET`.
- ALPHA: Each color is defined with a 35% opaque (65% transparent) version. These are not
  part of the brand guidelines per se, but are convenient in designing readable diagrams.
  Simply append `ALPHA` to apply it.

There is also one outlier color `CLOUDWHITE` which does not have variants as
defined above, and is actually equivalent to plantuml's `#white`. The theme does
however provide the `CLOUDWHITEALPHA` variant for convenience.

An example of overriding the theme defaults for specific elements:

```puml
@startuml

!theme amadeus from https://raw.githubusercontent.com/EpocSquadron/plantuml-theme-amadeus/main/

' Override any theme bits or add diagram specific styles you want after including
' the theme. 
<style>
note {
  MaxMessageSize 100
}
.exampleStereotype {
  BackgroundColor LIGHTCANARY
  FontColor DARKCANARY
  BorderColor DARKCANARY
}
</style>

' The rest of your diagram here...

@enduml
```

Here is a visual reference of all available colors:

| Variable | Color |
|--|--|
|`CLOUDWHITE` | ![#FFFFFF](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FFFFFF) `#FFFFFF` |
|`CLOUDWHITEALPHA` | ![#FFFFFF35](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FFFFFF35) `#FFFFFF35` |
|`DARKSKY` | ![#000835](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23000835) `#000835` |
|`DARKSKYALPHA` | ![#00083535](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%2300083535) `#00083535` |
|`VIVIDSKY` | ![#3A8BFF](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%233A8BFF) `#3A8BFF` |
|`VIVIDSKYALPHA` | ![#3A8BFF35](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%233A8BFF35) `#3A8BFF35` |
|`LIGHTSKY` | ![#C5D5F9](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23C5D5F9) `#C5D5F9` |
|`LIGHTSKYALPHA` | ![#C5D5F935](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23C5D5F935) `#C5D5F935` |
|`DARKFOREST` | ![#023A00](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23023A00) `#023A00` |
|`DARKFORESTALPHA` | ![#023A0035](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23023A0035) `#023A0035` |
|`VIVIDFOREST` | ![#92FF73](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%2392FF73) `#92FF73` |
|`VIVIDFORESTALPHA` | ![#92FF7335](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%2392FF7335) `#92FF7335` |
|`LIGHTFOREST` | ![#C8FFC0](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23C8FFC0) `#C8FFC0` |
|`LIGHTFORESTALPHA` | ![#C8FFC035](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23C8FFC035) `#C8FFC035` |
|`DARKCANARY` | ![#564A00](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23564A00) `#564A00` |
|`DARKCANARYALPHA` | ![#564A0035](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23564A0035) `#564A0035` |
|`VIVIDCANARY` | ![#FCE649](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FCE649) `#FCE649` |
|`VIVIDCANARYALPHA` | ![#FCE64935](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FCE64935) `#FCE64935` |
|`LIGHTCANARY` | ![#FFFEB0](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FFFEB0) `#FFFEB0` |
|`LIGHTCANARYALPHA` | ![#FFFEB035](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FFFEB035) `#FFFEB035` |
|`DARKCRIMSON` | ![#560900](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23560900) `#560900` |
|`DARKCRIMSONALPHA` | ![#56090035](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%2356090035) `#56090035` |
|`VIVIDCRIMSON` | ![#FF514D](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FF514D) `#FF514D` |
|`VIVIDCRIMSONALPHA` | ![#FF514D35](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FF514D35) `#FF514D35` |
|`LIGHTCRIMSON` | ![#FFD7D7](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FFD7D7) `#FFD7D7` |
|`LIGHTCRIMSONALPHA` | ![#FFD7D735](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FFD7D735) `#FFD7D735` |
|`DARKFUCHSIA` | ![#4F0230](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%234F0230) `#4F0230` |
|`DARKFUCHSIAALPHA` | ![#4F023035](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%234F023035) `#4F023035` |
|`VIVIDFUCHSIA` | ![#FF58AC](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FF58AC) `#FF58AC` |
|`VIVIDFUCHSIAALPHA` | ![#FF58AC35](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FF58AC35) `#FF58AC35` |
|`LIGHTFUCHSIA` | ![#FFC5F9](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FFC5F9) `#FFC5F9` |
|`LIGHTFUCHSIAALPHA` | ![#FFC5F935](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23FFC5F935) `#FFC5F935` |
|`DARKVIOLET` | ![#26005A](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%2326005A) `#26005A` |
|`DARKVIOLETALPHA` | ![#26005A35](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%2326005A35) `#26005A35` |
|`VIVIDVIOLET` | ![#B650FF](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23B650FF) `#B650FF` |
|`VIVIDVIOLETALPHA` | ![#B650FF35](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23B650FF35) `#B650FF35` |
|`LIGHTVIOLET` | ![#E4C7FF](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23E4C7FF) `#E4C7FF` |
|`LIGHTVIOLETALPHA` | ![#E4C7FF35](https://images.placeholders.dev/?width=250&height=25&text=%22%20%22&bgColor=%23E4C7FF35) `#E4C7FF35` |



### Sequence Diagrams

To best work with the theme, make sure your return messages are formatted
correctly. This will ensure that the message for the response shows below the
response arrow, which helps a lot with clarity.

```puml
' Correct
a -> b: request
a <-- b: response

' Incorrect
a -> b: request
b --> a: response
```

For boxes, the theme defaults to `VIOLET` colors, in order to be distinct from
groups but not so distinct as to seem to carry obvious meaning. It may make
sense to change the colors to something that makes sense for each box in your
diagram, which can be accomplished by overriding with stereotype styles:

```puml
<style>
.box1 {
  BackgroundColor LIGHTCRIMSONALPHA
  BodyBackgroundColor LIGHTCRIMSONALPHA
  BorderColor LIGHTCRIMSON
  FontColor DARKCRIMSON
}
.box2 {
  BackgroundColor LIGHTCANARYALPHA
  BodyBackgroundColor LIGHTCANARYALPHA
  BorderColor LIGHTCANARY
  FontColor DARKCANARY
}
</style>
hide <<box1>> stereotype
hide <<box2>> stereotype

box "box1" <<box1>>
  participant a
  participant b
endbox
box "box2" <<box2>>
  participant c
  participant d
endbox
```

### Amadeus Font

Amadeus' official font Amadeus Neue is preinstalled on all workstations,
and could theoretically be used to further the brand guideline adherence of
diagrams. However, in practice the font is not available or functional in the
following contexts:

- SVG Export: Even if declared correctly and present on your system, an SVG
  export of the diagram will not be displayed with the correct font.
- Confluence Macro: Most diagrams are embedded in confluence via the macro,
  which produces diagrams with a limited set of available fonts, and outputs
  SVG format.

For this reason, the theme defaults to `DejaVu Sans`, which is available in all
practical scenarios. If you wish to make use of Amadeus Neue for other contexts
such as in presentations, you may choose to declare the font in your diagram and
then export as PNG.

In your diagram:

```puml
@startuml

!theme amadeus from https://raw.githubusercontent.com/EpocSquadron/plantuml-theme-amadeus/main/

skinparam DefaultFontName "Amadeus Neue"

' The rest of your diagram here...
  
@enduml
```

Then ensure the environment from which you are exporting has the font available.
While workstations will have this installed by default, if you are using Windows
Subsystem for Linux, you will need to install the font in the linux context
as well. Verify you have done so correctly with:

```sh
plantuml -printfonts | grep 'Amadeus'
```

If it prints `Amadeus Neue`, then you can export with the plantuml CLI:

```sh
plantuml -tpng path/to/diagram.puml
```

