# Stundenbuch

Arbeitsstunden auf dem Handy eintragen: Datum, Beginn, Ende, Pause und Notiz.
Die App zeigt die Stunden pro Tag, die Summe der Woche (Montag bis Sonntag) und des Monats.

- Tagesarten: Arbeit, Frei, Urlaub, Krank, Stundenabbau
- Urlaub, Krank und Stundenabbau zählen 8 Std für den Monat, Stundenabbau nimmt zusätzlich 8 Std vom Überstundenkonto
- Monats-Soll 169 Std (einzelne Monate anpassbar), Über- und Minusstunden laufen in ein Überstundenkonto
- Auszahlungen von Überstunden lassen sich eintragen
- Urlaubsanspruch pro Jahr mit genommenen und übrigen Tagen

Die Einträge bleiben nur auf dem Handy gespeichert. Nichts davon landet hier im Repository.

## Zwei Varianten, gleiche App

**Android-App (APK)**
Wird bei jeder Änderung automatisch gebaut. Download unter [Releases](../../releases/tag/app) → `Stundenbuch.apk`.
Beim ersten Installieren muss Android einmal erlauben, Apps aus dieser Quelle zu installieren.
Neue Versionen lassen sich einfach drüber installieren, die Einträge bleiben erhalten.

**Web-App**
Läuft über GitHub Pages: https://inkyspoon.github.io/stundenbuch/
In Chrome auf Android über das Menü "App installieren" bzw. "Zum Startbildschirm hinzufügen" aufs Handy holen.
Funktioniert danach auch offline.

Achtung: Die beiden Varianten haben getrennte Speicher. Er sollte sich für eine entscheiden.
Umziehen geht über "Sicherung speichern" und in der anderen Variante "Sicherung wiederherstellen".

## Aufbau

- `docs/` die App selbst (eine HTML-Seite), wird auch von GitHub Pages ausgeliefert
- `android/` kleine Android-Hülle, die `docs/` anzeigt
- `.github/workflows/android.yml` baut die APK und legt sie unter Releases ab

Der Signierschlüssel `android/app/stundenbuch.keystore` liegt bewusst im Repo, damit jede neue APK
als Update über die alte passt. Für eine private App ist das in Ordnung.

Schriften: Barlow und Barlow Semi Condensed (SIL Open Font License, siehe `docs/fonts/OFL.txt`).
