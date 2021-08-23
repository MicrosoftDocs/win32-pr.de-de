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
| 0L               | **\_LDAP-ERFOLG**                      | **KEIN \_ FEHLER**                               | Vorgang erfolgreich.                             |
| 0x80070005L      | **\_LDAP UNZUREICHENDE \_ RECHTE**         | **FEHLERZUGRIFF \_ \_ VERWEIGERT**                   | Der Benutzer verfügt über unzureichende Zugriffsrechte.             |
| 0x80070008L      | **LDAP \_ OHNE \_ ARBEITSSPEICHER**                   | **FEHLER \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**              | Das System verfügt nicht über genügend Arbeitsspeicher.                         |
| 0x8007001fL      | **LDAP \_ OTHER**                        | **FEHLER \_ \_ GEN-FEHLER**                     | Unbekannter Fehler.                                   |
| 0x800700eaL      | **TEILERGEBNISSE VON LDAP \_ \_**             | **\_FEHLER BEI WEITEREN \_ DATEN**                       | Partielle Ergebnisse und empfangene Empfehlungen.          |
| 0x800700eaL      | **\_LDAP– WEITERE \_ \_ \_ ZURÜCKZUGEBENDE ERGEBNISSE**    | **\_FEHLER BEI WEITEREN \_ DATEN**                       | Weitere Ergebnisse sollen zurückgegeben werden.                 |
| 0x800704c7L      | **\_LDAP-BENUTZER \_ ABGEBROCHEN**              | **FEHLER \_ ABGEBROCHEN**                        | Der Benutzer hat den Vorgang abgebrochen.                     |
| 0x800704c9L      | **LDAP \_ \_ CONNECT-FEHLER**               | **FEHLERVERBINDUNG \_ \_ VERWEIGERT**              | Die Verbindung kann nicht hergestellt werden.                 |
| 0x8007052eL      | **\_UNGÜLTIGE \_ LDAP-ANMELDEINFORMATIONEN**         | **FEHLER BEIM \_ \_ ANMELDEFEHLER**                   | Die angegebenen Anmeldeinformationen sind ungültig.                |
| 0x800705b4L      | **\_LDAP-TIMEOUT**                      | **\_FEHLERTIMEOUT**                          | Bei der Suche ist ein Time out (Time out) für die Suche erfolgt.                                |
| 0x80071392L      | **LDAP \_ IST BEREITS \_ VORHANDEN**              | **FEHLEROBJEKT \_ \_ BEREITS \_ VORHANDEN**          | Das Objekt ist bereits vorhanden.                           |
| 0x8007200aL      | **LDAP \_ NO \_ SUCH \_ ATTRIBUTE**          | **FEHLER \_ DS \_ KEIN ATTRIBUT ODER \_ \_ \_ WERT**     | Das angeforderte Attribut ist nicht vorhanden.              |
| 0x8007200bL      | **\_UNGÜLTIGE \_ LDAP-SYNTAX**              | **FEHLER \_ \_ DS: UNGÜLTIGE \_ \_ ATTRIBUTSYNTAX**   | Die Syntax ist ungültig.                             |
| 0x8007200cL      | **\_NICHT DEFINIERTER \_ LDAP-TYP**              | **\_FEHLER: \_ DS-ATTRIBUTTYP \_ \_ UNDEFINED**   | Typ nicht definiert.                                |
| 0x8007200dL      | **\_LDAP-ATTRIBUT \_ ODER \_ -WERT \_ VORHANDEN** | **FEHLER: \_ DS-ATTRIBUT \_ ODER \_ \_ -WERT \_ VORHANDEN** | Das Attribut ist vorhanden, oder der Wert wurde zugewiesen. |
| 0x8007200eL      | **LDAP \_ AUSGELASTET**                         | **FEHLER \_ DS \_ AUSGELASTET**                         | Der Server ist ausgelastet.                                  |
| 0x8007200fL      | **LDAP \_ NICHT VERFÜGBAR**                  | **FEHLER \_ DS \_ NICHT VERFÜGBAR**                  | Der Server ist nicht verfügbar.                         |
| 0x80072014L      | **\_ \_ \_ LDAP-OBJEKTKLASSENVERLETZUNG**     | **FEHLER: \_ \_ \_ \_ DS-OBJ-KLASSENVERLETZUNG**        | Objektklassenverletzung.                          |
| 0x80072015L      | **LDAP \_ AUF \_ \_ \_ NONLEAF NICHT ZULÄSSIG**    | **FEHLER \_ DS \_ CANT \_ ON NON \_ \_ LEAF**          | Der Vorgang ist für ein Nichtblattobjekt nicht zulässig.  |
| 0x80072016L      | **LDAP \_ AUF \_ \_ \_ RDN NICHT ZULÄSSIG**        | **FEHLER \_ DS \_ CANT \_ ON \_ RDN**                | Der Vorgang ist für einen RDN nicht zulässig.              |
| 0x80072017L      | **LDAP \_ NO \_ OBJECT \_ CLASS \_ MODS**      | **ERROR \_ DS \_ CANT \_ MOD \_ OBJ \_ CLASS**        | Die Objektklasse kann nicht geändert werden.                      |
| 0x80072020L      | **\_ \_ LDAP-BETRIEBSFEHLER**            | **FEHLER \_ BEI \_ DS-VORGÄNGEN \_**            | Vorgangsfehler.                        |
| 0x80072021L      | **\_ \_ LDAP-PROTOKOLLFEHLER**              | **FEHLER \_ BEIM \_ DS-PROTOKOLLFEHLER \_**              | Protokollfehler.                         |
| 0x80072022L      | **\_LDAP-ZEITLIMIT \_ ÜBERSCHRITTEN**          | **FEHLER \_ DS \_ TIMELIMIT \_ ÜBERSCHRITTEN**          | Zeitlimit überschritten.                             |
| 0x80072023L      | **LDAP \_ SIZELIMIT \_ ÜBERSCHRITTEN**          | **FEHLER \_ DS \_ SIZELIMIT \_ ÜBERSCHRITTEN**          | Größenbeschränkung überschritten.                             |
| 0x80072024L      | **\_LDAP-ADMINISTRATORLIMIT \_ \_ ÜBERSCHRITTEN**       | **\_FEHLER: \_ DS-ADMINISTRATORLIMIT \_ \_ ÜBERSCHRITTEN**       | Die Verwaltungsgrenze auf dem Server wurde überschritten.     |
| 0x80072025L      | **LDAP \_ COMPARE \_ FALSE**               | **FEHLER \_ "DS \_ COMPARE \_ FALSE"**               | Vergleichen Sie den zurückgegebenen **WERT FALSE.**                       |
| 0x80072026L      | **LDAP \_ COMPARE \_ TRUE**                | **FEHLER \_ "DS \_ COMPARE \_ TRUE"**                | Vergleichen Sie die ergebene **TRUE-.**                        |
| 0x80072027L      | **\_ \_ LDAP-AUTHENTIFIZIERUNGSMETHODE \_ WIRD NICHT \_ UNTERSTÜTZT** | **FEHLER: \_ DIE \_ DS-AUTHENTIFIZIERUNGSMETHODE \_ \_ WIRD NICHT \_ UNTERSTÜTZT.** | Die Authentifizierungsmethode wird nicht unterstützt.      |
| 0x80072028L      | **STARKE \_ \_ LDAP-AUTHENTIFIZIERUNG \_ ERFORDERLICH**       | **FEHLER \_ DS \_ STRONG \_ AUTH \_ ERFORDERLICH**       | Eine starke Authentifizierung ist erforderlich.               |
| 0x80072029L      | **UNGEEIGNETE \_ \_ LDAP-AUTHENTIFIZIERUNG**          | **FEHLER: \_ DS \_ : \_ UNGEEIGNETE AUTHENTIFIZIERUNG**          | Die Authentifizierung ist ungeeignet.                 |
| 0x8007202aL      | **\_LDAP-AUTHENTIFIZIERUNG \_ UNBEKANNT**                | **FEHLER \_ DS \_ AUTH \_ UNKNOWN**                | Unbekannter Authentifizierungsfehler.           |
| 0x8007202bL      | **\_LDAP-EMPFEHLUNG**                     | **FEHLER \_ \_ DS-EMPFEHLUNG**                     | Die Empfehlung kann nicht behoben werden.                         |
| 0x8007202cL      | **\_CRIT-ERWEITERUNG "LDAP NICHT \_ \_ VERFÜGBAR"** | **FEHLER: \_ NICHT \_ VERFÜGBARE \_ CRIT-ERWEITERUNG FÜR DS \_** | Kritische Erweiterung ist nicht verfügbar.               |
| 0x8007202dL      | **\_LDAP-VERTRAULICHKEIT \_ ERFORDERLICH**    | **FEHLER \_ \_ DS-VERTRAULICHKEIT \_ ERFORDERLICH**    | Vertraulichkeit ist erforderlich.                     |
| 0x8007202eL      | **FALSCHER \_ \_ LDAP-ABGLEICH**      | **FEHLER: \_ DS – \_ UNGEEIGNETER \_ ABGLEICH**      | Es gab einen ungeeigneten Abgleich.             |
| 0x8007202fL      | **\_LDAP-EINSCHRÄNKUNGSVERLETZUNG \_**        | **\_FEHLER: \_ DS-EINSCHRÄNKUNGSVERLETZUNG \_**        | Es gab eine Einschränkungsverletzung.                 |
| 0x80072030L      | **LDAP \_ KEIN \_ SOLCHES \_ OBJEKT**             | **FEHLER \_ DS \_ KEIN \_ SOLCHES \_ OBJEKT**             | Das Objekt ist nicht vorhanden.                           |
| 0x80072031L      | **\_ \_ LDAP-ALIASPROBLEM**               | **\_FEHLER: \_ DS-ALIASPROBLEM \_**               | Alias ist ungültig.                              |
| 0x80072032L      | **UNGÜLTIGE \_ \_ LDAP-DN-SYNTAX \_**          | **FEHLER \_ DS \_ \_ UNGÜLTIGE DN-SYNTAX \_**          | Distinguished Name verfügt über ungültige Syntax. |
| 0x80072033L      | **LDAP \_ IS \_ LEAF**                     | **FEHLER \_ DS \_ IS \_ LEAF**                     | Das -Objekt ist ein Blatt.                            |
| 0x80072034L      | **\_LDAP-ALIAS \_ \_ DEREF-PROBLEM**        | **FEHLER \_ DS \_ ALIAS \_ DEREF \_ PROBLEM**        | Der Alias kann nicht dereferenziert werden.                    |
| 0x80072035L      | **DURCHZUFÜHRENDE \_ \_ LDAP-2012-LDAP-FUNKTIONEN \_**       | **FEHLER \_ BEIM AUSFÜHREN VON DS-FEHLERN \_ \_ \_**       | Der Server kann den Vorgang nicht ausführen.                 |
| 0x80072036L      | **\_ \_ LDAP-SCHLEIFEN-ERKENNUNG**                 | **FEHLER \_ BEIM ERKENNEN EINER DS-SCHLEIFE \_ \_**                 | Die Schleife wurde erkannt.                               |
| 0x80072037L      | **\_ \_ LDAP-NAMENSVERLETZUNG**            | **\_FEHLER: \_ DS-BENENNUNGSVERLETZUNG \_**            | Es gab einen Namensverstoß.                    |
| 0x80072038L      | **\_LDAP-ERGEBNISSE \_ ZU \_ GROß**          | **\_FEHLER: \_ DS-OBJEKTERGEBNISSE \_ \_ ZU \_ GROß**  | Das Resultseset ist zu groß.                        |
| 0x80072039L      | **LDAP \_ WIRKT SICH AUF MEHRERE \_ \_ DSAS AUS**      | **FEHLER \_ DS \_ WIRKT SICH AUF \_ MEHRERE \_ DSAS AUS**      | Es sind mehrere Verzeichnisdienstagenten betroffen.  |
| 0x8007203aL      | **\_LDAP-SERVER \_ NICHT VERFÜGBAR**                 | **\_FEHLER: \_ DS-SERVER \_ NICHT VERFÜGBAR**                 | Der LDAP-Server kann nicht kontaktiert werden.                  |
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



 

 

 




