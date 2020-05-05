# examplemarkdown

# Betillo
## Betillo
### Betillo
### Betillo

_Betillo_
**Betillo**

~~Betillo~~
**999**
#Images
![Betillo](https://avatars2.githubusercontent.com/u/22943822?s=460&v=4 )


#Images
![image](images/a.jpg)

# PlantUML markdown support seems not enabled on gitlab.com

As per https://docs.gitlab.com/ce/administration/integration/plantuml.html, this [PlantUML sequence diagram](http://plantuml.com/sequence-diagram) should work:

```plantuml
Bob -> Alice : hello
Alice -> Bob : Go Away
```

# PlantUML file rendering seems not enabled on gitlab.com

It would be nice if this linked [plantuml-diagram.plantuml](plantuml-diagram.plantuml) file would render by itself.


```plantuml
@startuml
' hide the spot
hide circle

' avoid problems with angled crows feet
skinparam linetype ortho

entity "Entity01" as e01 {
  *e1_id : number <<generated>>
  --
  *name : text
  description : text
}

entity "Entity02" as e02 {
  *e2_id : number <<generated>>
  --
  *e1_id : number <<FK>>
  other_details : text
}

entity "Entity03" as e03 {
  *e3_id : number <<generated>>
  --
  e1_id : number <<FK>>
  other_details : text
}

e01 ||..o{ e02
e01 |o..o{ e03
@enduml
```
