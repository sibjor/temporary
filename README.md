```mermaid
---
config:
  theme: redux
---
flowchart TD
    A{"Android Mobile Device"} <--> B("Unity App Runtime")

    C("Unity Android Build") --> B
    D{"Unity Game Engine"} --> C
    E("Unity AR PKG") --> D
    F("Unity Android PKG") --> D
    G("Unity Device Profiler") --> D
    H("Unity Firebase Firestore PKG") --> D
    I{"Firebase Firestore DB"} <--> H

    I --> A 

    J("Aseprite/Unity GUI") --> K
    K{"2D Artwork"} --> D
    L("Player Character") --> K
    M("Animation")--> L
    N("Idle") --> M 
    O("Walking") --> M
    P("The World") --> K
    Q("Sky") --> P
    R("Vegetation") --> P
    S("Ground") --> P
    T("Inventory GUI") --> J
    U("Amount of Steps GUI") --> J
    V("Currency Amount GUI") --> J
    X("World Map") --> K
    Y("Home Base") --> K
    Z("House") --> Y
    R --> Y
    S --> Y
    Q --> Y

    Å{"Game Loop"} <--> B
    Å --> Ä("Walk Outside")
    Ä --> Ö("Gain Currency")
    Ö --> ø("Buy Items")
    1 --> æ("Customize HUB")
    æ --> Ä
    ø --> Ä
    1("Visit Home Base") <--> Ä
    Ä <--> 2("Reach Destination?")
    ```
