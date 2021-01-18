# Hugo shortcode to render Kroki diagrams

The `diagram` Hugo shortcode renders [Kroki](https://kroki.io/) supported diagrams from in markdown text. Kroki provides an HTTP API to create diagrams from textual descriptions and  [supports many diagramming formats](https://kroki.io/#support).

## Usage

Include this in your Hugo `config.yaml`:

```
module:
  imports:
    - path: github.com/netspective-studios/hugo-shortcode-diagram
      mounts:
        - source: shortcodes
          target: layouts/shortcodes

```
If you are using `config.toml` in Hugo

```
[[module.imports]]
path                              = "github.com/netspective-studios/hugo-shortcode-diagram"

[[module.imports.mounts]]
source                            = "shortcodes"
target                            = "layouts/shortcodes"

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



