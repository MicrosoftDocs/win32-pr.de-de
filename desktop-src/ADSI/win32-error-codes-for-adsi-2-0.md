---
title: Win32-Fehler Codes für ADSI 2,0
description: In der folgenden Tabelle werden die LDAP-Fehlermeldungen für ADSI 2,0 aufgelistet.
ms.assetid: 99d97ea8-1dcc-49f4-a2bf-36ff8076e83a
ms.tgt_platform: multiple
keywords:
- Win32-Fehler Codes für ADSI 2,0 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e079fa6a98df28625f6307f774ce194712a52a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855227"
---
# <a name="win32-error-codes-for-adsi-20"></a>Win32-Fehler Codes für ADSI 2,0

In der folgenden Tabelle werden die LDAP-Fehlermeldungen für ADSI 2,0 aufgelistet.



| ADSI-Fehlerwert | LDAP-Nachricht                           | Win32-Nachricht                        | BESCHREIBUNG                                          |
|------------------|----------------------------------------|--------------------------------------|------------------------------------------------------|
| 0                | **LDAP- \_ Erfolg**                      | **kein \_ Fehler**                        | Vorgang erfolgreich.                                 |
| 0x80070002       | **LDAP \_ - \_ Objekt nicht solches \_ Objekt**             | **Fehler \_ Datei \_ nicht \_ gefunden.**          | Das Objekt ist nicht vorhanden.                               |
| 0x80070005       | **die LDAP-Authentifizierungs \_ \_ Methode \_ \_ wird nicht unterstützt.** | **Fehler \_ Zugriff \_ verweigert**            | Die Authentifizierungsmethode wird nicht unterstützt.                 |
| 0x80070005       | **Hohe LDAP-Authentifizierung \_ \_ \_ erforderlich.**       | **Fehler \_ Zugriff \_ verweigert**            | Erfordert eine strenge Authentifizierung.                      |
| 0x80070005       | **nicht geeignete LDAP-Authentifizierung \_ \_**          | **Fehler \_ Zugriff \_ verweigert**            | Nicht geeignete Authentifizierung.                        |
| 0x80070005       | **unzureichende LDAP- \_ \_ Rechte**         | **Fehler \_ Zugriff \_ verweigert**            | Der Benutzer verfügt nicht über ausreichende Zugriffsrechte.                 |
| 0x80070005       | **die LDAP-Authentifizierung ist \_ \_ unbekannt.**                | **Fehler \_ Zugriff \_ verweigert**            | Unbekannter Authentifizierungsfehler.               |
| 0x80070008       | **LDAP \_ ohne Arbeits \_ Speicher**                   | **Fehler \_ nicht \_ genügend Arbeits \_ Speicher**       | Das System verfügt nicht über genügend Arbeitsspeicher.                             |
| 0x8007001f       | **\_anderes LDAP**                        | **Fehler \_ gen \_ fehlgeschlagen**              | Unbekannter Fehler.                              |
| 0x8007001f       | **lokaler LDAP- \_ \_ Fehler**                 | **Fehler \_ gen \_ fehlgeschlagen**              | Lokaler Fehler.                                |
| 0x80070037       | **LDAP nicht \_ verfügbar**                  | **Fehler \_ dev ist \_ nicht \_ vorhanden.**           | Der Server ist nicht verfügbar.                             |
| 0x8007003a       | **LDAP- \_ Server \_ nach unten**                 | **Fehler bei fehlerhafter Netzwerk Zuweisung. \_ \_ \_**            | Der LDAP-Server kann nicht kontaktiert werden.                      |
| 0x8007003b       | **LDAP- \_ Codierungs \_ Fehler**              | **Fehler beim \_ unexp \_ net \_ Err.**           | Codierungsfehler.                             |
| 0x8007003b       | **LDAP- \_ Decodierung \_ Fehler**              | **Fehler beim \_ unexp \_ net \_ Err.**           | Decodierungs Fehler.                             |
| 0x80070044       | **LDAP- \_ Administrator \_ Limit \_ überschritten**       | **Fehler \_ zu \_ viele \_ Namen.**          | Die Verwaltungs Beschränkung auf dem Server wurde überschritten.         |
| 0x80070056       | **LDAP \_ - \_ Anmelde Informationen ungültig**         | **Fehler \_ ungültiges \_ Kennwort**         | Die Anmelde Informationen sind ungültig.                                |
| 0x80070057       | **\_ungültige \_ DN- \_ Syntax von LDAP**          | **Fehler bei \_ ungültigem \_ Parameter**        | Der Distinguished Name weist eine ungültige Syntax auf.     |
| 0x80070057       | **Verletzung der LDAP- \_ Benennung \_**            | **Fehler bei \_ ungültigem \_ Parameter**        | Benennungs Verletzung.                                    |
| 0x80070057       | **Verletzung der LDAP- \_ Objekt \_ Klasse \_**     | **Fehler bei \_ ungültigem \_ Parameter**        | Objektklassen Verletzung.                              |
| 0x80070057       | **LDAP- \_ Filter \_ Fehler**                | **Fehler bei \_ ungültigem \_ Parameter**        | Der Suchfilter ist falsch.                                |
| 0x80070057       | **LDAP- \_ param- \_ Fehler**                 | **Fehler bei \_ ungültigem \_ Parameter**        | Ein ungültiger Parameter wurde an eine Routine übergeben.               |
| 0x8007006e       | **LDAP- \_ Vorgangs \_ Fehler**            | **Fehler beim \_ Öffnen. \_**              | Vorgangs Fehler.                            |
| 0x8007007a       | **LDAP- \_ Ergebnisse \_ zu \_ groß**          | **Fehler \_ beim \_ Puffer.**      | Der Resultset ist zu groß.                            |
| 0x8007007B       | **\_ungültige LDAP- \_ Syntax**              | **\_ungültiger \_ Name.**             | Die Syntax ist ungültig.                                    |
| 0x8007007c       | **LDAP- \_ Protokoll \_ Fehler**              | **\_ungültige \_ Ebene**            | Protokollfehler.                                      |
| 0x800700B7       | **LDAP ist \_ bereits \_ vorhanden.**              | **Fehler ist \_ bereits \_ vorhanden.**           | Das Objekt ist bereits vorhanden.                               |
| 0x800700EA       | **LDAP- \_ partielle \_ Ergebnisse**             | **Fehler \_ Weitere \_ Daten**                | Partielle Ergebnisse und Verweise wurden empfangen.              |
| 0x800700EA       | **LDAP \_ ausgelastet**                         | **Fehler \_ ausgelastet**                      | Der Server ist ausgelastet.                                      |
| 0x800703eb des       | **LDAP ist \_ nicht \_ zur \_ Ausführung bereit.**       | **der Fehler \_ kann \_ nicht \_ vervollständigt werden.**        | Der Server kann den Vorgang nicht ausführen.                     |
| 0x8007041d       | **LDAP- \_ Timeout**                      | **Timeout für Fehler \_ Dienst \_ Anforderung \_** | Timeout bei der Suche.                                    |
| 0x800704b8       | **LDAP- \_ Vergleich \_ false**               | **Fehler beim \_ erweiterten \_ Fehler.**           | Compare hat **false** zurückgegeben.                           |
| 0x800704b8       | **LDAP- \_ Vergleich \_ true**                | **Fehler beim \_ erweiterten \_ Fehler.**           | Compare hat **true** ergeben.                            |
| 0x800704b8       | **LDAP- \_ Referenz**                     | **Fehler beim \_ erweiterten \_ Fehler.**           | Der Verweis kann nicht aufgelöst werden.                             |
| 0x800704b8       | **LDAP \_ - \_ Crit-Erweiterung nicht verfügbar \_** | **Fehler beim \_ erweiterten \_ Fehler.**           | Kritische Erweiterung ist nicht verfügbar.                   |
| 0x800704b8       | **LDAP \_ - \_ \_ Attribut nicht**          | **Fehler beim \_ erweiterten \_ Fehler.**           | Das angeforderte Attribut ist nicht vorhanden.                  |
| 0x800704b8       | **nicht \_ definierter LDAP- \_ Typ**              | **Fehler beim \_ erweiterten \_ Fehler.**           | Der Typ ist nicht definiert.                                 |
| 0x800704b8       | **unerwünschte LDAP- \_ \_ Übereinstimmung**      | **Fehler beim \_ erweiterten \_ Fehler.**           | Es ist eine ungeeignete Übereinstimmung vorhanden.                 |
| 0x800704b8       | **Verletzung der LDAP- \_ Einschränkung \_**        | **Fehler beim \_ erweiterten \_ Fehler.**           | Eine Einschränkungs Verletzung ist aufgetreten.                     |
| 0x800704b8       | **LDAP- \_ Attribut \_ oder- \_ Wert \_ vorhanden** | **Fehler beim \_ erweiterten \_ Fehler.**           | Das Attribut ist vorhanden, oder der Wert wurde zugewiesen. |
| 0x800704b8       | **LDAP- \_ Alias \_ Problem**               | **Fehler beim \_ erweiterten \_ Fehler.**           | Der Alias ist ungültig.                                  |
| 0x800704b8       | **LDAP \_ ist ein \_ Blatt.**                     | **Fehler beim \_ erweiterten \_ Fehler.**           | Das Objekt ist ein Blatt.                                    |
| 0x800704b8       | **\_ \_ Deref- \_ Problem mit LDAP-Alias**        | **Fehler beim \_ erweiterten \_ Fehler.**           | Der Alias kann nicht dereferenziert werden.                        |
| 0x800704b8       | **LDAP- \_ Schleifen \_ Erkennung**                 | **Fehler beim \_ erweiterten \_ Fehler.**           | Die Schleife wurde erkannt.                                   |
| 0x800704b8       | **LDAP \_ ist \_ \_ für nicht \_ Blatt nicht zulässig.**    | **Fehler beim \_ erweiterten \_ Fehler.**           | Der Vorgang ist für ein nicht-Blatt Objekt nicht zulässig.       |
| 0x800704b8       | **LDAP \_ ist \_ \_ für \_ RDN nicht zulässig.**        | **Fehler beim \_ erweiterten \_ Fehler.**           | Der Vorgang ist für RDN nicht zulässig.                     |
| 0x800704b8       | **LDAP \_ - \_ Objekt \_ Klassen- \_ Mods**      | **Fehler beim \_ erweiterten \_ Fehler.**           | Objektklasse kann nicht geändert werden.                          |
| 0x800704b8       | **LDAP \_ wirkt sich auf \_ mehrere \_ DSAs aus**      | **Fehler beim \_ erweiterten \_ Fehler.**           | Es sind mehrere Verzeichnisdienstagenten betroffen.      |
| 0x800704c7       | **LDAP- \_ Benutzer \_ abgebrochen**              | **Fehler \_ abgebrochen**                 | Der Benutzer hat den Vorgang abgebrochen.                     |
| 0x80070718       | **LDAP \_ timelimit \_ überschritten**          | **Fehler bei \_ nicht \_ ausreichendem \_ Kontingent.**        | Das Zeitlimit wurde überschritten.                                 |
| 0x80070718       | **LDAP- \_ SizeLimit \_ überschritten**          | **Fehler bei \_ nicht \_ ausreichendem \_ Kontingent.**        | Das Größenlimit wurde überschritten.                                 |



 

In ADSI 2,0 werden mehrere LDAP-Fehlermeldungen einem Win32-Fehlercode als **Fehler beim \_ erweiterten \_** Fehler zugeordnet. Rufen Sie [**adsgetlasterror**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) auf, um die vom Server zurückgegebene Fehler Zeichenfolge abzurufen. Weitere Informationen finden Sie weiter unten unter [Erweiterte ADSI-Fehlermeldungen](adsi-extended-error-messages.md) .

 

 




