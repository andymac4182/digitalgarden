---
{"dg-publish":true,"permalink":"/resources/mermaid-diagrams/","dgHomeLink":true,"dgPassFrontmatter":false,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowInlineTitle":true}
---

* Mermaid Homepage https://mermaid-js.github.io/mermaid/#/
* Mermaid live editor https://mermaid.live/
* Mermaid support in Bitbucket .md files https://jira.atlassian.com/browse/BCLOUD-21675
* Mermaid supported in `.mmd` files in Bitbucket
* GitHub support for mermaid
	* https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams
	* https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/
* List of places mermaid is integrated https://github.com/mermaid-js/mermaid/blob/develop/docs/integrations.md



# Examples
## Flow Chart
```mermaid
graph TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]
```

## Class Diagram
```mermaid
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
      +String beakColor
      +swim()
      +quack()
    }
    class Fish{
      -int sizeInFeet
      -canEat()
    }
    class Zebra{
      +bool is_wild
      +run()
    }
```

## State Diagram
```mermaid
stateDiagram-v2
    [*] --> Still
    Still --> [*]
    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

## ER Diagram
```mermaid
erDiagram
          CUSTOMER }|..|{ DELIVERY-ADDRESS : has
          CUSTOMER ||--o{ ORDER : places
          CUSTOMER ||--o{ INVOICE : "liable for"
          DELIVERY-ADDRESS ||--o{ ORDER : receives
          INVOICE ||--|{ ORDER : covers
          ORDER ||--|{ ORDER-ITEM : includes
          PRODUCT-CATEGORY ||--|{ PRODUCT : contains
          PRODUCT ||--o{ ORDER-ITEM : "ordered in"
```




# Alternatives 
* [[Resources/Asciiflow|Asciiflow]]