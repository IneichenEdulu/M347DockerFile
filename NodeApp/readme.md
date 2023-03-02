# Erstellen des Docker Images
Bemerkung: `<username>` kann durch Ihren Nutzernamen der Docker-Registry ersetzt werden oder weggelassen werden.\
Befehl: `docker build -t <username>/express-example .`

# Docker-Container starten

Befehl: `docker run -p 8090:8080 --name=express-example --restart=always -d <username>/express-example`\
Bemerkungen:
* `--name`: Mit diesem Namen wird der Container referenziert.
* `--restart`: (<i>Restart-Policy</i>) Mit always wird der Container immer neu gestartet, unabhängig davon, mit welchem <i>Exit-Code</i> er zuvor beendet wurde.
* `-d`: Startet den Container im Hintergrund. Abbruch des Prozesses mit <b>Cmd + C</b> bzw. <b>Strg + C</b>
* `-p 8090:8080` 8080 ist der Port auf dem Container, 8090 Port auf dem Host
