## PHPUnit 10
- erforderlich für PHP 8.1

### Annotations / Attributes
- Coverage über DocBlocks
- Attribute genutzt werden -> Compiler kann Attributes interpretieren
- `Cover` & `Uses`
- es wird erst nach Attributes gesucht und anschließend der Fallback auf die Annotations

### Eventsystem
- Listener in PHPUnit eingefügt
- jedes Assertion etc. ist ein Event, worauf man reagieren kann
- Events von Kinderprozessen werden an Elternprozesse zurückgegeben, wenn Tests processed sind
