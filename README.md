# Amadeus PlantUML Theme

This is a plantUML theme for my employer, [Amadeus](https://amadeus.com).
It essentially draws from the official brand colors and makes some other
adjustments to make nicer diagrams for internal use.

## Usage

In your plantuml diagram files, declare the theme like so:

```puml
@startuml

!theme amadeus from https://raw.githubusercontent.com/EpocSquadron/plantuml-theme-amadeus/main/

' Override any theme bits or add diagram specific styles you want after including
' the theme. You can use any of the defined brand colors. They exist in VIVID,
' LIGHT, and DARK variants, with sufficient contrast between DARK and LIGHT for
' background/foreground. Suffix the variant with the color name, one of SKY,
' FOREST, CANARY, CRIMSON, FUCHSIA, or VIOLET. CLOUDWHITE is an available outlier
' as well, although equivalent to #white.
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
