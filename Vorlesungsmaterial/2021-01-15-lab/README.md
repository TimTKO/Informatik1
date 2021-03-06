# Labor 15.01.21

**Aufgabe 1:**
- Vergleich der Performanz und Memory Nutzung von pass-by-reference vs. pass-by-value

**Aufgabe 2:**
- Programm zum Einlesen eines Integers (0-100) und dessen Ausgabe als String:
  - `25` --> `Fünfundzwanzig`
  - Unterschiedliche Schwierigkeitsgerade:
    - Zahlensystem auf Englisch ist einfacher.
    - Schwieriger mit Zahlen bis 1000 und auf Deutsch

## Hilfen zu Aufgabe 1:

- Benutzung der [`ctime` Bibliothek](https://www.cplusplus.com/reference/ctime/clock/) zum messen der Zeit/CPU-Zyklen (`#include <ctime>`)

- Funktion zum Ausgeben der Memory Nutzung von Prozessen auf Linux Systemen
``` C++
#include <cstdlib>

void print_mem(std::string str="") {
  std::cout << str << std::endl;
  system("ps -o pid,user,%mem,command | sort -b -k3 | grep ./main.out");
}
```

## Lösungen

- [Link zum Repl.it](https://repl.it/join/ucowvexi-toj11001)
- Zwei Beispiele für die Zweite Aufgabe mit dem Ausgeben des Integers:
  - Eine Lösung mit Nutzung von Switch Case
  - Eine Lösung über Vektoren und Modulo (ähnlich wie beim tictactoe board)