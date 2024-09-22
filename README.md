# 20books_mastodon
Metadaten, die aus dem #20books / Mastodon per scraping der Bilder und Identifikation mit GenAI erzeugt wurden

## Ablauf der Datenerzeigung

1) Download der Preview-Bilder des Hashtags #20books per Mastodon API
2) Komprimierung der Bilder auf 10 kb zur Reduktion der benötigten Input-Token für GenKI Abfrage
3) Ermittlung von Autor, Titel, Erscheingsjahr, Genre und Sub-Genre per OpenAI API an GPT4o
Promt:
4) Bereinigung der Daten
   Entfernung von No Value Einträgen
   Manuelle Bereinigung von flascher Reihenfolge von Autor und Titel
   Fehler im csv-Format
   Flasche Anzahl an Werte zurückgeliefert (z.B. 2 Sub-Genres)
5) Zählen von identischen Titeln

## Dateien
raw.csv sind die Rückgabe von GPT4o
Die übrigen Dateien sind bereinigt, gezählt und sortierte Werte des im Dateinamen enthaltenen Parameters
