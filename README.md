# Metadaten als flexible Objekteigenschaften
In Anwendungen mit einigermaßen umfangreichen Datenstrukturen 
möchte man möglichst flexibel Objekteigenschaften speichern.
Außerdem möchte man über Anwendungsgrenzen hinweg Daten 
austauschen, ohne stets Beschreibungsdaten mitliefern zu
müssen. 

Das IQB verwendet Metadatenkataloge, in denen die
Metadaten definiert sind. Verschiedene Anwendungen greifen 
darauf zu und erzeugen auf dieser Grundlage Eingabeformulare
und Datenlisten usw. Jede Anwendung, die in importierten Daten
Verweise auf diese Kataloge entdeckt, kann die Daten korrekt
interpretieren.  

In diesem Repository sind die grundsätzlichen Definitionen zu
finden:
- mdc.xsd: Eine XML-Schemadatei, die die Syntax eines Katalogs
beschreibt
- mdc-core.xml: Ein Katalog, der Metadaten definiert, die selbst
in Katalogen oder Metadatendefinitionen verwendet werden. Zu 
beachten hier ist der Verweis auf mdc.xsd, wodurch XML-Editoren
in der Lage sind, den Katalog zu validieren.  
- mdc-example.xml: Ein Katalog, der beispielhaft das Einbinden 
sowohl der mdc.xsd als auch die Nutzung des Katalogs mdc-core.xml
zeigt. Es ist demonstriert, wie Metadaten in einem XML-Kontext
gespeichert werden. 

# Begriffe
- Ein Metadatenkatalog MDC ist eine Sammlung von 
Metadatendefinitionen MDD. 
- Eine Metadatendefinition beschreibt den Typ und damit 
mögliche Werte für eine Information. Sie legt die Bedeutung der Werte in Bezug auf ein Datenobjekt fest und sichert so die Übertragbarkeit der Information über Systemgrenzen hinweg.
- Der Metadatenkatalog hat eine eindeutige ID.
- Metadatendefinitionen haben eine ID, die innerhalb des Katalogs eindeutig ist.
- Ein Metadatenkatalog kann selbst Metadaten enthalten, die über einen anderen Metadatenkatalog definiert sind.
- Eine Metadatendefinition kann selbst Metadaten enthalten, die über einen anderen Metadatenkatalog definiert sind.
# Versionierung
- Ein Metadatenkatalog wird nach dem SemVer-System MAJOR.MINOR.PATCH versioniert. Weder einzelne Metadatendefinitionen noch zulässige Werte innerhalb von Metadatendefinitionen werden versioniert.
- Sobald sich Inhalte des Metadatenkatalogs derart ändern, dass Dateninkompatibilität anzunehmen ist, wird die MAJOR -Versionsnummer erhöht. Es wird im Katalog eine Information „changelog“ hinterlegt, welche Metadatendefinition(en) betroffen sind/ist und welche Art die Änderung war (kurzer Text).
- Sobald neue Metadatendefinitionen zu einem Metadatenkatalog hinzugefügt wurden, wird die MINOR-Version erhöht.
- Die PATCH-Version wird erhöht, wenn kleinere Änderungen ohne Auswirkungen auf die existierenden Daten vorgenommen wurden.
# Repräsentation
- Ein MDC liegt öffentlich verfügbar auf GitHub.com. Hier sind Dokumentationen hinterlegt. Die Version eines MDC entspricht der auf GitHub.com hinterlegten Versionierung (Tag).
- Ein MDC ist eine XML-Datei. Diese kann gegen eine ebenfalls auf GitHub.com verfügbare Xsd validiert werden.
