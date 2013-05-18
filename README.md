# Notizen aus der Firmware

## Build Prozess

### OpenWRT feeds 
OpenWRT-Komponenten werden über "feeds" zum Build hinzugefügt.
Die Definitionen für die Quellen steht in der Datei "feeds.conf.default" und wird über

    scripts/feeds update -a
    scripts/feeds install -a

hinzugefügt.

Bei KBU wird die Datei "feeds.conf.pushable" verwendet, welche auch schreibenden Zugriff auf die Quellen
der Komponenten erlaubt.

*Frage: Wozu ist schreibender Zugriff notwendig?*

### build.sh

Wir (FFM) haben die notwendigen Build-Schritte in einem Script zusammengefaßt, welches lokal oder von
Jenkins (Buildserver) aufgerufen werden kann/wird.
