
# Publikationsleitlinien für einfach nutzbare Daten (ENTWURF)

## Technische Vorgaben

Für tabellarische Daten verwenden wir standardmässig das Format [CSV](http://opendatahandbook.org/glossary/en/terms/csv/).

> - CSV ist besser als Excel, alle Formate sind besser als Word, PDF oder Fliesstext.
> - Für Daten mit komplexen Strukturen und/oder um Daten einfach zwischen Programmen und Systemen zu übertragen, ist das Format [JSON](http://opendatahandbook.org/glossary/en/terms/json/) sehr gut.

Variabeln und Werte trennen wir mittels Kommas ',' voneinander (nicht mittels Semikolons ';')

> - Ausser es gibt einen guten Grund.
> - Standardeinstellungen eines Programms, wie z.B. Excel, sind kein guter Grund.

CSV-Dateien speichern wir als Unicode (UTF-8) ab.

> - Das geht [so](https://github.com/openZH/mdd-ogd-handbook/blob/main/publikationsleitlinien/UTF-8-kodieren.md).

## Formale Vorgaben

Pro Spalte ein Datentyp.

Spaltenüberschriften (Variabeln):
- beginnen nicht mit einer Zahl,
- haben keine Leerzeichen, sondern sind zusammengeschrieben (Gross- und Kleinbuchsteben sind möglich) oder mittel 'Underline' verbunden (z.B. ',
- haben keine Umlaute, sondern sind ausgeschrieben als 'ae', 'oe', 'ue' und
- haben keine Sonderzeichen, sondern sind ausgeschrieben (z.B. 'prozent' statt '%').

Werte, die Umlaute, Kommata oder Ähnliches enthalten mit rahmen wir mittels Anführungs- und Schlusszeichen ein (z.B. "Französisch, Deutsch").

In Datumsangaben keine Zeichenketten (z.B. '24. Dez. 2021') verwenden, sondern standardmässig das Format 'YYYY-MM-DD' (z.B. '2021-12-24').

Zahlen einheitlich formatieren ohne Hochkommas, Leerzeichen oder andere 1000er-Trennzeichen.

URLs aufrufbar ausschreiben im Format 'https://...'.

Werte, die unbekannt sind, als solche ausweisen (nicht als '0'), sondern als 'NA'.

## Datenstruktur-Standards

Wir bauen Datenstrukturen gemäss der Maxime 'Tidy Data' auf.

> Das heisst: Pro Variable eine Spalte, pro Beobachtung eine Zeile, pro Wert eine Zelle.  
> 
> ``BFS_NR,GEBIET_NAME,INDIKATOR_JAHR,INDIKATOR_VALUE,EINHEIT_KURZ``  
> ``1,Aeugst a.A.,1990,111,Fr./Einw.``  
> ``1,Aeugst a.A.,1991,102,Fr./Einw.``  
> ``1,Aeugst a.A.,1992,85,Fr./Einw.``

Keine Leerzeilen.

Keine Spalten-Hierarchien, also keine miteinander zusammengeführten Zellen (z.B. um Ober- und Unterkategorien zu repräsentieren), sondern Oberkategorien in einer ersten Spalte, Unterkategorien in einer zweiten Spalte.

Wir verzichten auf überflüssige Variablen (z.B. mit denselben Wert über die gesamte Reihe).

Keine Fussnoten und ähnliche Verweise. Hinweise:
- entweder in einer eigenen Spalte aufnehmen oder
- (wenn kurz) in der Metadaten-Beschreibung der entsprechenden Daten-Ressource aufführen oder
- (wenn ausführlicher) als HTML-Page, TXT- oder PDF-Datei in den Metadaten unter "Weitere Informationen" referenzieren.

## Inhaltliche Standards

Wir wählen möglichst aussagekräftige Spaltenüberschriften (Variabeln). Ihre Bedeutung erklären wir:
- (wenn kurz) in der Metadaten-Beschreibung der entsprechenden Daten-Ressource oder
- (wenn ausführlicher) auf einer HTML-Page, in einer TXT- oder PDF-Datei, die wir in den Metadaten unter "Weitere Informationen" referenzieren.

Wir führen keine Variabeln auf, deren Werte sich aus den in der Datei vorhandenen Werten von Variabeln berechnen lassen (z.B. keine Prozentangaben als eigene Spalte, wenn Grundwerte in einer Spalte vorhanden sind).

> - Ausser es gibt einen guten Grund.
