Unix Shell – Aufgabe 4:

1. # ISSN- und Dates-Spalten ausschneiden:
cut -f 5,12 Datei1.tsv > Datei2.tsv

2. # Spalten-Header löschen:
sed -i ’1d’ Datei2.tsv

3. # Unnötige Zeilen ausschneiden:
sed -i ’/eng/d’ Datei2.tsv

4. # ISSN-Beschriftung ausschneiden:
tr -d ’[IiSsNn: ]’ < Datei2.tsv > Datei3.tsv

5.  # Duplikate entfernen und sortieren (dadurch verschwinden auch die Leerzeichen bis auf die 1. Zeile):
sort Datei3.tsv | uniq Datei4.tsv

6. # Erste Leerzeile entfernen:
grep  ’’\S’’ Datei4.tsv > Datei5.tsv
