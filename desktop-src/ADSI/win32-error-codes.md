---
title: Win32-Fehlercodes
description: In der folgenden Tabelle sind die LDAP-Fehlermeldungen für ADSI aufgeführt.
ms.assetid: b609bd56-770a-4546-8640-26ad6e108d54
ms.tgt_platform: multiple
keywords:
- Win32-Fehlercodes ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d1986b0de2e4afeed0fccdcce62851acfaf104c3f360b7ea462410f4484f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118689890"
---
# <a name="win32-error-codes"></a>Win32-Fehlercodes

In der folgenden Tabelle sind die LDAP-Fehlermeldungen für ADSI aufgeführt.



| ADSI-Fehlerwert | LDAP-Nachricht                           | Win32-Nachricht                               | Beschreibung                                      |
|------------------|----------------------------------------|---------------------------------------------|--------------------------------------------------|
| 0L               | **LDAP \_ ERFOLGREICH**                      | **NO \_ ERROR**                               | Vorgang erfolgreich.                             |
| 0x80070005L      | **UNZUREICHENDE \_ \_ LDAP-RECHTE**         | **FEHLER \_ BEIM \_ ZUGRIFF VERWEIGERT**                   | Der Benutzer verfügt über unzureichende Zugriffsrechte.             |
| 0x80070008L      | **LDAP: \_ KEIN \_ ARBEITSSPEICHER**                   | **FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**              | System ist nicht genügend Arbeitsspeicher verfügbar.                         |
| 0x8007001fL      | **LDAP \_ OTHER**                        | **FEHLER \_ BEIM FEHLER \_ "GEN"**                     | Unbekannter Fehler.                                   |
| 0x800700eaL      | **\_ \_ LDAP-TEILERGEBNISSE**             | **FEHLER: \_ WEITERE \_ DATEN**                       | Empfangene Teilergebnisse und Empfehlungen.          |
| 0x800700eaL      | **LDAP: \_ \_ WEITERE \_ ERGEBNISSE, DIE ZURÜCKGEBEN WERDEN \_ MÜSSEN**    | **FEHLER: \_ WEITERE \_ DATEN**                       | Es sollen weitere Ergebnisse zurückgegeben werden.                 |
| 0x800704c7L      | **\_LDAP-BENUTZER \_ ABGEBROCHEN**              | **FEHLER \_ ABGEBROCHEN**                        | Der Benutzer hat den Vorgang abgebrochen.                     |
| 0x800704c9L      | **LDAP \_ CONNECT ERROR (LDAP-VERBINDUNGSFEHLER) \_**               | **FEHLER: \_ VERBINDUNG \_ ABGELEHNT**              | Die Verbindung kann nicht hergestellt werden.                 |
| 0x8007052eL      | **UNGÜLTIGE \_ \_ LDAP-ANMELDEINFORMATIONEN**         | **FEHLER \_ BEI DER \_ ANMELDUNG**                   | Die angegebenen Anmeldeinformationen sind ungültig.                |
| 0x800705b4L      | **\_LDAP-TIMEOUT**                      | **\_FEHLERZEITÜBERSCHREITUNG**                          | Time out bei der Suche.                                |
| 0x80071392L      | **LDAP \_ IST BEREITS \_ VORHANDEN**              | **FEHLEROBJEKT \_ \_ IST BEREITS \_ VORHANDEN**          | Das Objekt ist bereits vorhanden.                           |
| 0x8007200aL      | **LDAP \_ KEIN \_ SOLCHES \_ ATTRIBUT**          | **FEHLER \_ DS \_ KEIN ATTRIBUT ODER \_ \_ \_ WERT**     | Das angeforderte Attribut ist nicht vorhanden.              |
| 0x8007200bL      | **UNGÜLTIGE \_ \_ LDAP-SYNTAX**              | **FEHLER \_ DS \_ UNGÜLTIGE \_ ATTRIBUTSYNTAX \_**   | Die Syntax ist ungültig.                             |
| 0x8007200cL      | **NICHT \_ DEFINIERTER \_ LDAP-TYP**              | **FEHLER \_ \_ DS-ATTRIBUTTYP \_ \_ NICHT DEFINIERT**   | Typ nicht definiert.                                |
| 0x8007200dL      | **\_LDAP-ATTRIBUT \_ ODER \_ -WERT \_ VORHANDEN** | **FEHLER \_ \_ DS-ATTRIBUT \_ ODER \_ -WERT \_ VORHANDEN** | Das Attribut ist vorhanden, oder der Wert wurde zugewiesen. |
| 0x8007200eL      | **LDAP \_ AUSGELASTET**                         | **FEHLER \_ DS \_ AUSGELASTET**                         | Der Server ist ausgelastet.                                  |
| 0x8007200fL      | **LDAP \_ NICHT VERFÜGBAR**                  | **FEHLER \_ DS \_ NICHT VERFÜGBAR**                  | Der Server ist nicht verfügbar.                         |
| 0x80072014L      | **\_ \_ LDAP-OBJEKTKLASSENVERLETZUNG \_**     | **FEHLER: \_ DS \_ OBJ-KLASSENVERLETZUNG \_ \_**        | Objektklassenverletzung.                          |
| 0x80072015L      | **LDAP \_ NICHT \_ AUF \_ \_ NONLEAF ZULÄSSIG**    | **FEHLER \_ "DS \_ \_ CANT" AUF NICHT \_ BLATT \_**          | Der Vorgang ist für ein Nichtblattobjekt nicht zulässig.  |
| 0x80072016L      | **LDAP \_ IM \_ \_ \_ RDN NICHT ZULÄSSIG**        | **FEHLER \_ DS \_ CANT \_ ON \_ RDN**                | Der Vorgang ist für ein RDN nicht zulässig.              |
| 0x80072017L      | **LDAP \_ NO \_ OBJECT \_ CLASS \_ MODS**      | **FEHLER \_ DS \_ CANT \_ MOD \_ OBJ-KLASSE \_**        | Die Objektklasse kann nicht geändert werden.                      |
| 0x80072020L      | **FEHLER BEI \_ \_ LDAP-VORGÄNGEN**            | **FEHLER \_ BEI \_ DS-VORGÄNGEN \_**            | Vorgangsfehler.                        |
| 0x80072021L      | **\_ \_ LDAP-PROTOKOLLFEHLER**              | **FEHLER \_ BEIM \_ DS-PROTOKOLL \_**              | Protokollfehler.                         |
| 0x80072022L      | **\_LDAP-ZEITLIMIT \_ ÜBERSCHRITTEN**          | **FEHLER \_ DS \_ TIMELIMIT \_ ÜBERSCHRITTEN**          | Das Zeitlimit wurde überschritten.                             |
| 0x80072023L      | **LDAP \_ SIZELIMIT EXCEEDED (LDAP-GRÖßENLIMIT \_ ÜBERSCHRITTEN)**          | **FEHLER \_ DS \_ SIZELIMIT \_ ÜBERSCHRITTEN**          | Das Größenlimit wurde überschritten.                             |
| 0x80072024L      | **\_LDAP-ADMINISTRATORLIMIT \_ \_ ÜBERSCHRITTEN**       | **\_FEHLER: \_ DS-ADMINISTRATORLIMIT \_ \_ ÜBERSCHRITTEN**       | Das Verwaltungslimit auf dem Server wurde überschritten.     |
| 0x80072025L      | **\_LDAP-VERGLEICH \_ FALSE**               | **FEHLER \_ DS \_ COMPARE \_ FALSE**               | Compare yielded **FALSE**.                       |
| 0x80072026L      | **\_LDAP–VERGLEICH \_ TRUE**                | **FEHLER \_ DS \_ COMPARE \_ TRUE**                | Vergleichen Sie den ergibten **TRUE-**.                        |
| 0x80072027L      | **\_LDAP-AUTHENTIFIZIERUNGSMETHODE \_ \_ WIRD NICHT \_ UNTERSTÜTZT** | **\_FEHLER: \_ DS-AUTHENTIFIZIERUNGSMETHODE \_ WIRD NICHT \_ \_ UNTERSTÜTZT** | Die Authentifizierungsmethode wird nicht unterstützt.      |
| 0x80072028L      | **\_SICHERE \_ LDAP-AUTHENTIFIZIERUNG \_ ERFORDERLICH**       | **FEHLER \_ DS \_ STRONG \_ AUTH \_ ERFORDERLICH**       | Eine sichere Authentifizierung ist erforderlich.               |
| 0x80072029L      | **\_UNGEEIGNETE \_ LDAP-AUTHENTIFIZIERUNG**          | **FEHLER \_ \_ DS: UNGEEIGNETE \_ AUTHENTIFIZIERUNG**          | Die Authentifizierung ist ungeeignet.                 |
| 0x8007202aL      | **\_LDAP-AUTHENTIFIZIERUNG \_ UNBEKANNT**                | **FEHLER \_ DS \_ AUTH \_ UNKNOWN**                | Unbekannter Authentifizierungsfehler.           |
| 0x8007202bL      | **\_LDAP-EMPFEHLUNG**                     | **FEHLER \_ BEI DER \_ DS-EMPFEHLUNG**                     | Die Empfehlung kann nicht aufgelöst werden.                         |
| 0x8007202cL      | **UNAVAILABLE \_ CRIT EXTENSION (UNAVAILABLE \_ CRIT-ERWEITERUNG FÜR LDAP) \_** | **ERROR \_ DS \_ UNAVAILABLE \_ CRIT \_ EXTENSION** | Die kritische Erweiterung ist nicht verfügbar.               |
| 0x8007202dL      | **\_LDAP-VERTRAULICHKEIT \_ ERFORDERLICH**    | **FEHLER \_ DS \_ VERTRAULICHKEIT \_ ERFORDERLICH**    | Vertraulichkeit ist erforderlich.                     |
| 0x8007202eL      | **\_UNPASSENDER \_ LDAP-ABGLEICH**      | **FEHLER \_ \_ DS– UNGEEIGNETER \_ ABGLEICH**      | Es gab einen ungeeigneten Abgleich.             |
| 0x8007202fL      | **\_ \_ LDAP-EINSCHRÄNKUNGSVERLETZUNG**        | **\_FEHLER: \_ \_ DS-EINSCHRÄNKUNGSVERLETZUNG**        | Es gab einen Einschränkensverstoß.                 |
| 0x80072030L      | **LDAP: \_ KEIN \_ SOLCHES \_ OBJEKT**             | **FEHLER \_ DS \_ NO SUCH \_ \_ OBJECT**             | Das Objekt ist nicht vorhanden.                           |
| 0x80072031L      | **\_ \_ LDAP-ALIASPROBLEM**               | **FEHLER \_ BEIM \_ DS-ALIASPROBLEM \_**               | Der Alias ist ungültig.                              |
| 0x80072032L      | **\_LDAP– UNGÜLTIGE \_ DN-SYNTAX \_**          | **FEHLER \_ DS \_ UNGÜLTIGE \_ \_ DN-SYNTAX**          | Distinguished Name verfügt über eine ungültige Syntax. |
| 0x80072033L      | **LDAP \_ IST \_ BLATT**                     | **FEHLER \_ DS \_ IS \_ LEAF**                     | Das -Objekt ist ein Blatt.                            |
| 0x80072034L      | **\_ \_ LDAP-ALIAS-DEREF-PROBLEM \_**        | **\_FEHLER: \_ DS-ALIAS \_ \_ DEREF-PROBLEM**        | Der Alias kann nicht dereferenzieren.                    |
| 0x80072035L      | **\_LDAP-ABTWILLING \_ FÜR \_ DIE AUSFÜHRUNG**       | **FEHLER \_ \_ DS, DER AUSGEFÜHRT \_ WERDEN SOLL \_**       | Der Server kann den Vorgang nicht ausführen.                 |
| 0x80072036L      | **\_ \_ LDAP-SCHLEIFENERKENNUNG**                 | **FEHLER \_ BEI \_ DS-SCHLEIFE \_ ERKANNT**                 | Es wurde eine Schleife erkannt.                               |
| 0x80072037L      | **\_ \_ LDAP-BENENNUNGSVERLETZUNG**            | **\_FEHLER: \_ DS-BENENNUNGSVERLETZUNG \_**            | Es gab eine Namensverletzung.                    |
| 0x80072038L      | **\_ \_ LDAP-ERGEBNISSE ZU \_ GROß**          | **FEHLER \_ BEI \_ DS-OBJEKTERGEBNISSEN \_ \_ ZU \_ GROß**  | Das Resultset ist zu groß.                        |
| 0x80072039L      | **LDAP \_ WIRKT SICH AUF MEHRERE \_ \_ DSAS AUS**      | **FEHLER \_ DS \_ WIRKT SICH AUF \_ MEHRERE \_ DSAS AUS**      | Es sind mehrere Verzeichnisdienstagenten betroffen.  |
| 0x8007203aL      | **\_ \_ LDAP-SERVER HERUNTER**                 | **FEHLER \_ DS \_ SERVER \_ DOWN**                 | Der LDAP-Server kann nicht kontaktiert werden.                  |
| 0x8007203bL      | **LOKALER \_ \_ LDAP-FEHLER**                 | **FEHLER \_ BEIM LOKALEN \_ DS-FEHLER \_**                 | Lokaler Fehler.                            |
| 0x8007203cL      | **\_LDAP-CODIERUNGSFEHLER \_**              | **\_FEHLER: \_ DS-CODIERUNGSFEHLER \_**              | Codierungsfehler.                         |
| 0x8007203dL      | **\_LDAP-DECODIERUNGSFEHLER \_**              | **FEHLER \_ BEI DER \_ DS-DECODIERUNG \_**              | Decodierungsfehler.                         |
| 0x8007203eL      | **\_ \_ LDAP-FILTERFEHLER**                | **FEHLER \_ DS \_ FILTER \_ UNKNOWN**              | Der Suchfilter ist schlecht.                        |
| 0x8007203fL      | **\_ \_ LDAP-PARAM-FEHLER**                 | **FEHLER \_ BEIM \_ DS-PARAM \_**                 | Ein fehlerhafter Parameter wurde an eine Funktion übergeben.        |
| 0x80072040L      | **LDAP \_ WIRD NICHT \_ UNTERSTÜTZT**               | **FEHLER \_ DS \_ NICHT \_ UNTERSTÜTZT**               | Das Feature wird nicht unterstützt.                           |
| 0x80072041L      | **LDAP: \_ \_ KEINE ERGEBNISSE \_ ZURÜCKGEGEBEN**        | **FEHLER \_ DS \_ KEINE ERGEBNISSE \_ \_ ZURÜCKGEGEBEN**        | Ergebnisse werden nicht zurückgegeben.                        |
| 0x80072042L      | **\_LDAP-STEUERELEMENT \_ NICHT \_ GEFUNDEN**          | **FEHLER \_ \_ DS-STEUERELEMENT \_ NICHT \_ GEFUNDEN**          | Das Steuerelement wurde nicht gefunden.                           |
| 0x80072043L      | **\_ \_ LDAP-CLIENTSCHLEIFE**                 | **FEHLER \_ BEI DS-CLIENTSCHLEIFE \_ \_**                 | Clientschleife wurde erkannt.                        |
| 0x80072044L      | **\_ \_ LDAP-EMPFEHLUNGSLIMIT \_ ÜBERSCHRITTEN**    | **\_FEHLER: \_ DS-EMPFEHLUNGSLIMIT \_ \_ ÜBERSCHRITTEN**    | Die Empfehlungsgrenze wurde überschritten.                         |



 

 

 




