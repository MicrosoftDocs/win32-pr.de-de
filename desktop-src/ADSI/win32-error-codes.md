---
title: Win32-Fehler Codes
description: In der folgenden Tabelle sind die LDAP-Fehlermeldungen für ADSI aufgeführt.
ms.assetid: b609bd56-770a-4546-8640-26ad6e108d54
ms.tgt_platform: multiple
keywords:
- Win32-Fehler Codes ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d8151c07fb6470d395f15e088ae5e50f3e43bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947320"
---
# <a name="win32-error-codes"></a>Win32-Fehler Codes

In der folgenden Tabelle sind die LDAP-Fehlermeldungen für ADSI aufgeführt.



| ADSI-Fehlerwert | LDAP-Nachricht                           | Win32-Nachricht                               | BESCHREIBUNG                                      |
|------------------|----------------------------------------|---------------------------------------------|--------------------------------------------------|
| 0L               | **LDAP- \_ Erfolg**                      | **kein \_ Fehler**                               | Vorgang erfolgreich.                             |
| 0x80070005l      | **unzureichende LDAP- \_ \_ Rechte**         | **Fehler \_ Zugriff \_ verweigert**                   | Der Benutzer verfügt nicht über ausreichende Zugriffsrechte.             |
| 0x80070008l      | **LDAP \_ ohne Arbeits \_ Speicher**                   | **Fehler \_ nicht \_ genügend Arbeits \_ Speicher**              | Das System verfügt nicht über genügend Arbeitsspeicher.                         |
| 0x8007001fl      | **\_anderes LDAP**                        | **Fehler \_ gen \_ fehlgeschlagen**                     | Unbekannter Fehler.                                   |
| 0x800700eal      | **LDAP- \_ partielle \_ Ergebnisse**             | **Fehler \_ Weitere \_ Daten**                       | Partielle Ergebnisse und Verweise wurden empfangen.          |
| 0x800700eal      | **zurück zugebende LDAP- \_ \_ Ergebnisse \_ \_**    | **Fehler \_ Weitere \_ Daten**                       | Weitere Ergebnisse werden zurückgegeben.                 |
| 0x800704c7l      | **LDAP- \_ Benutzer \_ abgebrochen**              | **Fehler \_ abgebrochen**                        | Der Vorgang wurde vom Benutzer abgebrochen.                     |
| 0x800704c9l      | **LDAP- \_ Verbindungs \_ Fehler**               | **Fehler \_ Verbindung \_ verweigert**              | Die Verbindung kann nicht hergestellt werden.                 |
| 0x8007052el      | **LDAP \_ - \_ Anmelde Informationen ungültig**         | **Fehler beim \_ anmelden. \_**                   | Die angegebenen Anmelde Informationen sind ungültig.                |
| 0x800705b4l      | **LDAP- \_ Timeout**                      | **Fehler \_ Timeout**                          | Timeout bei der Suche.                                |
| 0x80071392l      | **LDAP ist \_ bereits \_ vorhanden.**              | **das Fehler \_ Objekt ist \_ bereits \_ vorhanden.**          | Das Objekt ist bereits vorhanden.                           |
| 0x8007200al      | **LDAP \_ - \_ \_ Attribut nicht**          | **Fehler- \_ DS \_ kein \_ Attribut \_ oder \_ Wert**     | Das angeforderte Attribut ist nicht vorhanden.              |
| 0x8007200bl      | **\_ungültige LDAP- \_ Syntax**              | **Fehler- \_ DS \_ ungültige \_ Attribut \_ Syntax.**   | Die Syntax ist ungültig.                             |
| 0x8007200cl      | **nicht \_ definierter LDAP- \_ Typ**              | **Fehler \_ DS \_ - \_ Attributtyp nicht \_ definiert**   | Der Typ ist nicht definiert.                                |
| 0x8007200dl      | **LDAP- \_ Attribut \_ oder- \_ Wert \_ vorhanden** | **Fehler- \_ DS- \_ Attribut oder- \_ \_ Wert \_ vorhanden** | Das Attribut ist vorhanden, oder der Wert wurde zugewiesen. |
| 0x8007200el      | **LDAP \_ ausgelastet**                         | **Fehler- \_ DS \_ ausgelastet**                         | Der Server ist ausgelastet.                                  |
| 0x8007200fl      | **LDAP nicht \_ verfügbar**                  | **Fehler- \_ DS nicht \_ verfügbar**                  | Der Server ist nicht verfügbar.                         |
| 0x80072014l      | **Verletzung der LDAP- \_ Objekt \_ Klasse \_**     | **Fehler- \_ DS- \_ obj- \_ Klassen \_ Verletzung**        | Objektklassen Verletzung.                          |
| 0x80072015l      | **LDAP \_ ist \_ \_ für nicht \_ Blatt nicht zulässig.**    | **Fehler " \_ DS" \_ auf " \_ \_ nicht \_ Blatt"**          | Der Vorgang ist für ein nicht-Blatt Objekt nicht zulässig.  |
| 0x80072016l      | **LDAP \_ ist \_ \_ für \_ RDN nicht zulässig.**        | **Fehler " \_ DS" \_ \_ bei \_ RDN**                | Der Vorgang ist in einem RDN nicht zulässig.              |
| 0x80072017l      | **LDAP \_ - \_ Objekt \_ Klassen- \_ Mods**      | **Error \_ DS \_ cant \_ mod \_ obj- \_ Klasse**        | Objektklasse kann nicht geändert werden.                      |
| 0x80072020l      | **LDAP- \_ Vorgangs \_ Fehler**            | **Fehler \_ DS- \_ Vorgangs \_ Fehler**            | Vorgangs Fehler.                        |
| 0x80072021l      | **LDAP- \_ Protokoll \_ Fehler**              | **Fehler- \_ DS- \_ Protokoll \_ Fehler**              | Protokollfehler.                         |
| 0x80072022l      | **LDAP \_ timelimit \_ überschritten**          | **Fehler bei ' \_ \_ timelimit ' \_ überschritten.**          | Das Zeitlimit wurde überschritten.                             |
| 0x80072023l      | **LDAP- \_ SizeLimit \_ überschritten**          | **Fehler " \_ DS \_ SizeLimit" \_ überschritten.**          | Das Größenlimit wurde überschritten.                             |
| 0x80072024l      | **LDAP- \_ Administrator \_ Limit \_ überschritten**       | **Fehler- \_ DS- \_ Administrator \_ Limit \_ überschritten**       | Die Verwaltungs Beschränkung auf dem Server wurde überschritten.     |
| 0x80072025l      | **LDAP- \_ Vergleich \_ false**               | **Fehler- \_ DS- \_ Vergleich \_ false**               | Compare hat **false** zurückgegeben.                       |
| 0x80072026l      | **LDAP- \_ Vergleich \_ true**                | **Fehler- \_ DS mit \_ \_ true vergleichen**                | Compare hat **true** ergeben.                        |
| 0x80072027l      | **die LDAP-Authentifizierungs \_ \_ Methode \_ \_ wird nicht unterstützt.** | **Fehler-DS-Authentifizierungs \_ \_ \_ Methode \_ \_ wird nicht unterstützt.** | Die Authentifizierungsmethode wird nicht unterstützt.      |
| 0x80072028l      | **Hohe LDAP-Authentifizierung \_ \_ \_ erforderlich.**       | **Fehler \_ DS \_ starke Authentifizierung \_ \_ erforderlich.**       | Eine strenge Authentifizierung ist erforderlich.               |
| 0x80072029l      | **nicht geeignete LDAP-Authentifizierung \_ \_**          | **Fehler- \_ DS- \_ ungeeignete Authentifizierung \_**          | Die Authentifizierung ist ungeeignet.                 |
| 0x8007202al      | **die LDAP-Authentifizierung ist \_ \_ unbekannt.**                | **Fehler \_ DS-Authentifizierung \_ \_ unbekannt**                | Unbekannter Authentifizierungsfehler.           |
| 0x8007202bl      | **LDAP- \_ Referenz**                     | **Fehler- \_ DS- \_ Referenz**                     | Der Verweis kann nicht aufgelöst werden.                         |
| 0x8007202cl      | **LDAP \_ - \_ Crit-Erweiterung nicht verfügbar \_** | **Fehler- \_ DS nicht \_ Verfügbare \_ Crit- \_ Erweiterung** | Kritische Erweiterung ist nicht verfügbar.               |
| 0x8007202dl      | **LDAP- \_ Vertraulichkeit \_ erforderlich**    | **Fehler- \_ DS- \_ Vertraulichkeit \_ erforderlich**    | Vertraulichkeit ist erforderlich.                     |
| 0x8007202el      | **unerwünschte LDAP- \_ \_ Übereinstimmung**      | **Fehler- \_ DS- \_ ungeeignet \_**      | Es ist eine ungeeignete Übereinstimmung vorhanden.             |
| 0x8007202fl      | **Verletzung der LDAP- \_ Einschränkung \_**        | **Fehler-DS-Einschränkungs \_ \_ \_ Verletzung**        | Eine Einschränkungs Verletzung ist aufgetreten.                 |
| 0x80072030l      | **LDAP \_ - \_ Objekt nicht solches \_ Objekt**             | **Fehler- \_ DS ist \_ kein \_ solches \_ Objekt**             | Das Objekt ist nicht vorhanden.                           |
| 0x80072031l      | **LDAP- \_ Alias \_ Problem**               | **Fehler- \_ DS- \_ Alias \_ Problem**               | Der Alias ist ungültig.                              |
| 0x80072032l      | **\_ungültige \_ DN- \_ Syntax von LDAP**          | **Fehler- \_ DS \_ ungültige \_ DN- \_ Syntax**          | Der Distinguished Name weist eine ungültige Syntax auf. |
| 0x80072033l      | **LDAP \_ ist ein \_ Blatt.**                     | **Fehler- \_ DS \_ ist \_ Blatt**                     | Das-Objekt ist ein Blatt.                            |
| 0x80072034l      | **\_ \_ Deref- \_ Problem mit LDAP-Alias**        | **Fehler- \_ DS- \_ Alias- \_ Deref- \_ Problem**        | Der Alias kann nicht dereferenziert werden.                    |
| 0x80072035l      | **LDAP ist \_ nicht \_ zur \_ Ausführung bereit.**       | **Fehler- \_ DS ist \_ nicht \_ zur \_ Ausführung bereit**       | Der Server kann den Vorgang nicht ausführen.                 |
| 0x80072036l      | **LDAP- \_ Schleifen \_ Erkennung**                 | **Fehler- \_ DS- \_ Schleifen \_ Erkennung**                 | Die Schleife wurde erkannt.                               |
| 0x80072037l      | **Verletzung der LDAP- \_ Benennung \_**            | **Fehler- \_ DS- \_ Benennungs \_ Verletzung**            | Eine Benennungs Verletzung ist aufgetreten.                    |
| 0x80072038l      | **LDAP- \_ Ergebnisse \_ zu \_ groß**          | **Fehler- \_ DS- \_ Objekt \_ Ergebnisse \_ zu \_ groß**  | Der Resultset ist zu groß.                        |
| 0x80072039l      | **LDAP \_ wirkt sich auf \_ mehrere \_ DSAs aus**      | **Fehler- \_ DS wirkt sich auf \_ \_ mehrere \_ DSAs aus**      | Es sind mehrere Verzeichnisdienstagenten betroffen.  |
| 0x8007203al      | **LDAP- \_ Server \_ nach unten**                 | **Fehler \_ DS- \_ Server \_ nach unten**                 | Der LDAP-Server kann nicht kontaktiert werden.                  |
| 0x8007203bl      | **lokaler LDAP- \_ \_ Fehler**                 | **Fehler- \_ DS \_ local- \_ Fehler**                 | Lokaler Fehler.                            |
| 0x8007203cl      | **LDAP- \_ Codierungs \_ Fehler**              | **Fehler- \_ DS- \_ Codierungs \_ Fehler**              | Codierungsfehler.                         |
| 0x8007203dl      | **LDAP- \_ Decodierung \_ Fehler**              | **Fehler \_ DS- \_ Decodierungs \_ Fehler**              | Decodierungs Fehler.                         |
| 0x8007203el      | **LDAP- \_ Filter \_ Fehler**                | **Fehler- \_ DS- \_ Filter \_ unbekannt**              | Der Suchfilter ist falsch.                        |
| 0x8007203fl      | **LDAP- \_ param- \_ Fehler**                 | **Fehler \_ DS- \_ param- \_ Fehler**                 | Ein ungültiger Parameter wurde an eine Funktion übergeben.        |
| 0x80072040l      | **LDAP \_ nicht \_ unterstützt**               | **Fehler- \_ DS \_ nicht \_ unterstützt**               | Das Feature wird nicht unterstützt.                           |
| 0x80072041l      | **LDAP \_ keine \_ Ergebnisse \_ zurückgegeben**        | **Fehler " \_ DS \_ keine \_ Ergebnisse \_ zurückgegeben"**        | Die Ergebnisse werden nicht zurückgegeben.                        |
| 0x80072042l      | **LDAP- \_ Steuerelement \_ nicht \_ gefunden.**          | **Fehler- \_ DS- \_ Steuerelement \_ nicht \_ gefunden**          | Das Steuerelement wurde nicht gefunden.                           |
| 0x80072043l      | **LDAP- \_ Client \_ Schleife**                 | **Fehler- \_ DS- \_ Client \_ Schleife**                 | Client Schleife wurde erkannt.                        |
| 0x80072044l      | **LDAP- \_ Verweis \_ Limit \_ überschritten**    | **Fehler- \_ DS- \_ Verweis \_ Limit \_ überschritten**    | Das Verweis Limit wurde überschritten.                         |



 

 

 




