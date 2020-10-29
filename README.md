# MQTT producer

Diser Producer verbindet sich mit dem RabittMQ (Broker) der auf dem localhost:1883 erreichbar ist.

Der producer published Nachrichten  an dem Topic home/room1 mit dem clientid der entweder durch argument eingegeben werden kann, oder wird automatisch mit einem timestamp generiert.

# Voraussetzung
RabittMQ ist installiert und laeuft auf dem port 1883

# Build
Das projekt wird mit maven gebaut (**im Powershell**)

```
cd mqttproducer
mvn clean compile assembly:single
```

Nach dem build, es wird eine jar Datei im /target erstellt.
Der producer produziert eine Nachricht pro Sekunde.

Um den Producer mit dem clientid device1 zu starten braucht man den folgenden Befehl im Windows Powershell auszufuehren:
```
 java -jar .\target\mqttpublisher-0.0.1-SNAPSHOT-jar-with-dependencies.jar device1
```
natuerlich kann mann meherer Producers mit unterschiedlichen clientid starten.

wenn kein argument eingegeben wird, ein random clientid mit dem start timestamp generiert wird.
