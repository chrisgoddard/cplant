# cplant
cplant(Color PLANT uml) is theme for the plant UML.

```uml
@startuml
!include themes/azusa-color.pu

title <size:20>Sample Sequence</size>

actor User
participant "First Class" as A
participant "Second Class" as B
participant "Last Class" as C

User -> A: DoWork
activate A

A -> B: Create Request
activate B

B -> C: DoWork
activate C
C --> B: WorkDone
destroy C

B --> A: Request Created
deactivate B

A --> User: Done
deactivate A

@enduml

```

![azusa-color](sample_seq.png)
