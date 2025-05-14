1-Zweck der Anwendung

Die Anwendung simuliert das strategische Brettspiel "Dame" in einer digitalen 
Umgebung.
Ziele der Anwendung sind:
• Lernzweck: Spieler können die Regeln und Strategien des Spiels erlernen.
• Unterhaltung: Menschliche Spieler und eine KI können gegeneinander antreten.
• Technische Demonstration: Das Projekt zeigt die Anwendung von objektorientierter 
Programmierung (OOP) in Java und demonstriert die Integration von Spiellogik, Live 
View Programming und KI.

2-Programmiertechnische Herausforderungen, Ihr Lösungsansatz?
   
• Spiellogik und Regeln umsetzen: Die Spiellogik umfasst das Bewegen von Steinen, 
Schlagen von Gegnern, Dame-Umwandlung und Alle Regeln müssen klar definiert und 
validiert werden.
Lösungsansatz: Implementierung von Klassen und Methoden, die es steuern

• KI-Entwicklung: Implementierung einer künstlichen Intelligenz, die in der Lage ist, 
gültige und strategische Züge zu machen.
Lösungsansatz: Minimax Algorithmus

• Benutzeroberfläche: Die visuelle Darstellung des Spiels und keine Interaktion mit 
dem Benutzer 
Lösungsansatz: Live View Programming

• Zugvalidierung: Sicherstellen, dass nur gültige Züge durchgeführt werden, ohne die 
Regeln zu verletzen.
Lösungsansatz: Implementierung eines Regelprüfung, das vor jedem Zug alle 
Bedingungen evaluiert und die Rückmeldung an den Spieler bei ungültigen Zügen.

• Bestscore tracken: Beim Schlagen eines Steins werden Punkte hinzufügen
Lösungsansatz: Verwende eine Datei (z. B. scores.txt …), um die Punktzahlen 
persistent zu speichern.

• Zugmöglichkeit anzeigen:
Lösungsansatz: Wenn ein Spieler ein Feld auswählt, wird eine Methode 
implementiert, die alle möglichen Züge der darauf befindlichen Spielfigur zurückgibt.

4. Szenarien
   
3.1. Szenario 1 – Grundlegender Spielzug
Zweck:

Ein Spieler führt einen einfachen, gültigen Zug mit einem normalen Stein aus.
 Beschreibung:
 
• Der Spieler zieht diagonal vorwärts auf ein freies Feld.

• Das Spielfeld wird aktualisiert.

 Erwartetes Ergebnis:
• Der Stein bewegt sich korrekt auf das neue Feld.

• Das vorherige Feld ist leer.

3.2. Szenario 2 – Normalen und mehrfachen Schlagen eines gegnerischen Steins
Zweck:
Ein Spieler schlägt einen gegnerischen Stein durch Überspringen und entfernt diesen vom 
Spielfeld.
 
 Beschreibung:
• Der Spieler springt mit seinem Stein diagonal über einen gegnerischen Stein, auf ein 
freies Feld dahinter.
 Erwartetes Ergebnis:
• Der gegnerische Stein wird entfernt.
• Der Spielerstein landet auf dem Zielfeld.

3.3. Szenario 3 – Umwandlung in eine Dame
Zweck:
Ein Spieler erreicht mit einem normalen Stein die gegnerische Grundlinie, wodurch der 
Stein zur Dame wird.
 Beschreibung:
• Ein normaler Stein bewegt sich diagonal auf ein Feld der Grundlinie des Gegners.
• Der Stein wird zur Dame umgewandelt und erhält erweiterte Zugmöglichkeiten 
(vorwärts und rückwärts).
 
 Erwartetes Ergebnis:
• Der Stein wird als Dame markiert (z. B. durch ein Symbol oder eine visuelle 
Änderung).
• Der Spieler kann mit der Dame in zukünftigen Zügen vorwärts und rückwärts diagonal 
ziehen

3.4. Szenario 4 – Ungültiger Zug
Zweck:
Das Spiel erkennt und blockiert einen ungültigen Zug, der die Spielregeln verletzt.
 Beschreibung:
• Ein Spieler versucht, auf ein besetztes Feld zu ziehen, rückwärts zu ziehen (bei einem 
normalen Stein) oder sein Teammitglied zu schlagen.
 Erwartetes Ergebnis:
• Der Zug wird nicht ausgeführt.
• Eine Fehlermeldung oder ein Hinweis wird angezeigt (z. B. "Ungültiger Zug …").

3.5. Szenario 5 – Spielende
Zweck:
Das Spiel erkennt das Ende, wenn ein Spieler keine Steine oder keine gültigen Züge mehr 
hat.
 Beschreibung:
• Nach jedem Zug wird überprüft, ob ein Spieler entweder keine Steine mehr besitzt 
oder keine Züge mehr ausführen kann.
• Das Spiel gibt den Gewinner aus.
 Erwartetes Ergebnis:
• Wenn ein Spieler alle gegnerischen Steine geschlagen hat, wird er zum Sieger erklärt.
• Falls beide Spieler keine Züge mehr haben, wird das beste Score angezeigt.
