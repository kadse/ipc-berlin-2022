## Memory Leaks
- Garbage Collector kümmert sich seit PHP 5.3.0 darum
- nach 10.000 Ref-Cycles greift der GC und räumt den Memory frei
- Werte in ein Array schreiben kopiert das Array, z.B.
```php
function test(array $array) {
    $array[] = 10000001; // Hier wird das Array kopiert
}
```
- Objekte verwenden ist immer besser als Arrays
- Arrays nutzen mehr Memory als Objekte und legen oft Kopien an
- Bei Iterationen Generators nutzen -> bedarf deutlich weniger Memory als foreach
- https://github.com/BitOne/php-meminfo
- **WeakMap** (ab PHP 8) -> Verbesserung für den Klassencache

Source: https://github.com/kambo-1st/ipc-memory-leaks-talk

Slides: [PDF](../src/php_memory_leaks.pdf)