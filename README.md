# Hugo shortcode to render Kroki diagrams

The `diagram` Hugo shortcode renders [Kroki](https://kroki.io/) supported diagrams from in markdown text. Kroki provides an HTTP API to create diagrams from textual descriptions and  [supports many diagramming formats](https://kroki.io/#support).

## Usage

Include this in your Hugo `config.yaml`:

```
modules:
  imports:
  - path: "github.com/adobe/hugo-spectrum/v1"

```

## Dot Sample

```html
{{<diagram name="diagram1" type="dot">}}
digraph { Hello -> World }
{{</diagram>}}
```

## PlantUML Sample

```html
{{<diagram name="diagram2" type="plantuml">}}
@startuml
cloud helloWorld as "Hello World (PlantUML)"
@enduml
{{</diagram>}}
```



