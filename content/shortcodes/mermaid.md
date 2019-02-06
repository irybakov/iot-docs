+++
title = "mermaid"
description = ""
+++

## Flowchart example
{{%expand "Show code ..."%}}
	{{</*mermaid align="left"*/>}}
	graph LR;
		A[Hard edge] -->|Link text| B(Round edge)
    	B --> C{Decision}
    	C -->|One| D[Result one]
    	C -->|Two| E[Result two]
    {{</* /mermaid */>}}
{{%/expand%}}

{{<mermaid align="left">}}
graph LR;
	A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
{{< /mermaid >}}

## Sequence example
{{%expand "Show code ..."%}}
	{{</*mermaid*/>}}
	sequenceDiagram
	    participant Alice
	    participant Bob
	    Alice->>John: Hello John, how are you?
	    loop Healthcheck
	        John->John: Fight against hypochondria
	    end
	    Note right of John: Rational thoughts <br/>prevail...
	    John-->Alice: Great!
	    John->Bob: How about you?
	    Bob-->John: Jolly good!
	{{</* /mermaid */>}}
{{%/expand%}}

{{<mermaid>}}
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
{{< /mermaid >}}



## GANTT Example
{{%expand "Show code ..."%}}
	{{</*mermaid*/>}}
	gantt
	        dateFormat  YYYY-MM-DD
	        title Adding GANTT diagram functionality to mermaid
	        section A section
	        Completed task            :done,    des1, 2014-01-06,2014-01-08
	        Active task               :active,  des2, 2014-01-09, 3d
	        Future task               :         des3, after des2, 5d
	        Future task2               :         des4, after des3, 5d
	        section Critical tasks
	        Completed task in the critical line :crit, done, 2014-01-06,24h
	        Implement parser and jison          :crit, done, after des1, 2d
	        Create tests for parser             :crit, active, 3d
	        Future task in critical line        :crit, 5d
	        Create tests for renderer           :2d
	        Add to mermaid                      :1d
	{{</* /mermaid */>}}
{{%/expand%}}

{{<mermaid>}}
gantt
        dateFormat  YYYY-MM-DD
        title Adding GANTT diagram functionality to mermaid
        section A section
        Completed task            :done,    des1, 2014-01-06,2014-01-08
        Active task               :active,  des2, 2014-01-09, 3d
        Future task               :         des3, after des2, 5d
        Future task2               :         des4, after des3, 5d
        section Critical tasks
        Completed task in the critical line :crit, done, 2014-01-06,24h
        Implement parser and jison          :crit, done, after des1, 2d
        Create tests for parser             :crit, active, 3d
        Future task in critical line        :crit, 5d
        Create tests for renderer           :2d
        Add to mermaid                      :1d
{{</mermaid>}}

# Class diagram
{{<mermaid>}}
classDiagram
	Class01 <|-- AveryLongClass : Cool
	Class03 *-- Class04
	Class05 o-- Class06
	Class07 .. Class08
	Class09 --> C2 : Where am i?
	Class09 --* C3
	Class09 --|> Class07
	Class07 : equals()
	Class07 : Object[] elementData
	Class01 : size()
	Class01 : int chimp
	Class01 : int gorilla
	Class08 <--> C2: Cool label
{{</mermaid>}}


```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```


```scala
implicit val trackerShard: ActorRef = ClusterSharding(system).start(
    typeName = trackerShardName,
    entityProps = TagTrackerSupervisor.props(singletonRef),
    settings = ClusterShardingSettings(system).withRole("core"),
    extractEntityId = extractEntityId,
    extractShardId = extractShardId
  )
```

<div class="mermaid">
classDiagram
	Class01 <|-- AveryLongClass : Cool
	Class03 *-- Class04
	Class05 o-- Class06
	Class07 .. Class08
	Class09 --> C2 : Where am i?
	Class09 --* C3
	Class09 --|> Class07
	Class07 : equals()
	Class07 : Object[] elementData
	Class01 : size()
	Class01 : int chimp
	Class01 : int gorilla
	Class08 <--> C2: Cool label
</div>
