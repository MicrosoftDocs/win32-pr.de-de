---
title: Win32-Fehlercodes für ADSI 2.0
description: In der folgenden Tabelle sind die LDAP-Fehlermeldungen für ADSI 2.0 aufgeführt.
ms.assetid: 99d97ea8-1dcc-49f4-a2bf-36ff8076e83a
ms.tgt_platform: multiple
keywords:
- Win32-Fehlercodes für ADSI 2.0 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea81b4d277ad43cb2278d23549e370df1d11b3058be1e9c8b0f8b9329eabe26e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589750"
---
# <a name="win32-error-codes-for-adsi-20"></a>Win32-Fehlercodes für ADSI 2.0

In der folgenden Tabelle sind die LDAP-Fehlermeldungen für ADSI 2.0 aufgeführt.



| ADSI-Fehlerwert | LDAP-Nachricht                           | Win32-Nachricht                        | Beschreibung                                          |
|------------------|----------------------------------------|--------------------------------------|------------------------------------------------------|
| 0                | **LDAP \_ ERFOLGREICH**                      | **NO \_ ERROR**                        | Vorgang erfolgreich.                                 |
| 0x80070002       | **LDAP \_ KEIN \_ SOLCHES \_ OBJEKT**             | **FEHLERDATEI \_ \_ NICHT \_ GEFUNDEN**          | Das Objekt ist nicht vorhanden.                               |
| 0x80070005       | **\_ \_ LDAP-AUTHENTIFIZIERUNGSMETHODE \_ WIRD NICHT \_ UNTERSTÜTZT** | **FEHLER \_ BEIM \_ ZUGRIFF VERWEIGERT**            | Die Authentifizierungsmethode wird nicht unterstützt.                 |
| 0x80070005       | **STARKE \_ \_ LDAP-AUTHENTIFIZIERUNG \_ ERFORDERLICH**       | **FEHLER \_ BEIM \_ ZUGRIFF VERWEIGERT**            | Erfordert eine starke Authentifizierung.                      |
| 0x80070005       | **UNGEEIGNETE \_ \_ LDAP-AUTHENTIFIZIERUNG**          | **FEHLER \_ BEIM \_ ZUGRIFF VERWEIGERT**            | Ungeeignete Authentifizierung.                        |
| 0x80070005       | **UNZUREICHENDE \_ \_ LDAP-RECHTE**         | **FEHLER \_ BEIM \_ ZUGRIFF VERWEIGERT**            | Der Benutzer verfügt über unzureichende Zugriffsrechte.                 |
| 0x80070005       | **\_LDAP-AUTHENTIFIZIERUNG \_ UNBEKANNT**                | **FEHLER \_ BEIM \_ ZUGRIFF VERWEIGERT**            | Unbekannter Authentifizierungsfehler.               |
| 0x80070008       | **LDAP \_ KEIN \_ ARBEITSSPEICHER**                   | **FEHLER: \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**       | System ist nicht genügend Arbeitsspeicher verfügbar.                             |
| 0x8007001F       | **LDAP \_ OTHER**                        | **FEHLER \_ BEIM FEHLER \_ "GEN"**              | Unbekannter Fehler.                              |
| 0x8007001F       | **LOKALER \_ \_ LDAP-FEHLER**                 | **FEHLER \_ BEIM FEHLER \_ "GEN"**              | Lokaler Fehler.                                |
| 0x80070037       | **LDAP \_ NICHT VERFÜGBAR**                  | **FEHLER \_ DEV \_ NICHT \_ VORHANDEN**           | Der Server ist nicht verfügbar.                             |
| 0x8007003A       | **\_LDAP-SERVER \_ NICHT VERFÜGBAR**                 | **FEHLER \_ " BAD NET \_ \_ RESP"**            | Der LDAP-Server kann nicht kontaktiert werden.                      |
| 0x8007003B       | **\_LDAP-CODIERUNGSFEHLER \_**              | **FEHLER \_ UNEXP \_ NET \_ ERR**           | Codierungsfehler.                             |
| 0x8007003B       | **\_LDAP-DECODIERUNGSFEHLER \_**              | **FEHLER \_ UNEXP \_ NET \_ ERR**           | Decodierungsfehler.                             |
| 0x80070044       | **\_LDAP-ADMINISTRATORLIMIT \_ \_ ÜBERSCHRITTEN**       | **FEHLER: \_ \_ ZU VIELE \_ NAMEN**          | Die Verwaltungsgrenze auf dem Server wurde überschritten.         |
| 0x80070056       | **UNGÜLTIGE \_ \_ LDAP-ANMELDEINFORMATIONEN**         | **FEHLER: \_ UNGÜLTIGES \_ KENNWORT**         | Die Anmeldeinformationen sind ungültig.                                |
| 0x80070057       | **UNGÜLTIGE \_ \_ LDAP-DN-SYNTAX \_**          | **FEHLER \_ UNGÜLTIGER \_ PARAMETER**        | Distinguished Name verfügt über ungültige Syntax.     |
| 0x80070057       | **\_ \_ LDAP-NAMENSVERLETZUNG**            | **FEHLER \_ UNGÜLTIGER \_ PARAMETER**        | Namensverletzung.                                    |
| 0x80070057       | **\_ \_ LDAP-OBJEKTKLASSENVERLETZUNG \_**     | **FEHLER \_ UNGÜLTIGER \_ PARAMETER**        | Objektklassenverletzung.                              |
| 0x80070057       | **\_ \_ LDAP-FILTERFEHLER**                | **FEHLER \_ UNGÜLTIGER \_ PARAMETER**        | Der Suchfilter ist schlecht.                                |
| 0x80070057       | **\_ \_ LDAP-PARAM-FEHLER**                 | **FEHLER \_ UNGÜLTIGER \_ PARAMETER**        | Ein fehlerhafter Parameter wurde an eine Routine übergeben.               |
| 0X8007006E       | **FEHLER BEI \_ \_ LDAP-VORGÄNGEN**            | **FEHLER \_ BEIM ÖFFNEN \_**              | Vorgangsfehler.                            |
| 0x8007007A       | **\_LDAP-ERGEBNISSE \_ ZU \_ GROß**          | **FEHLER: \_ NICHT GENÜGEND \_ PUFFER**      | Das Resultseset ist zu groß.                            |
| 0x8007007B       | **UNGÜLTIGE \_ \_ LDAP-SYNTAX**              | **FEHLER \_ UNGÜLTIGER \_ NAME**             | Syntax ungültig.                                    |
| 0x8007007C       | **\_ \_ LDAP-PROTOKOLLFEHLER**              | **FEHLER \_ \_ UNGÜLTIGER WERT**            | Protokollfehler.                                      |
| 0x800700B7       | **LDAP \_ IST BEREITS \_ VORHANDEN**              | **FEHLER \_ IST BEREITS \_ VORHANDEN**           | Das Objekt ist bereits vorhanden.                               |
| 0x800700EA       | **\_ \_ LDAP-TEILERGEBNISSE**             | **FEHLER: \_ WEITERE \_ DATEN**                | Empfangene Teilergebnisse und Empfehlungen.              |
| 0x800700EA       | **LDAP \_ AUSGELASTET**                         | **FEHLER \_ AUSGELASTET**                      | Der Server ist ausgelastet.                                      |
| 0x800703EB       | **DURCHZUFÜHRENDE \_ \_ LDAP-2012-LDAP-FUNKTIONEN \_**       | **FEHLER \_ KANN NICHT ABGESCHLOSSEN \_ \_ WERDEN**        | Der Server kann den Vorgang nicht ausführen.                     |
| 0x8007041D       | **\_LDAP-TIMEOUT**                      | **TIMEOUT \_ FÜR \_ \_ FEHLERDIENSTANFORDERUNG** | Time out bei der Suche.                                    |
| 0x800704B8       | **LDAP \_ COMPARE \_ FALSE**               | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Vergleichen Sie den zurückgegebenen **WERT FALSE.**                           |
| 0x800704B8       | **LDAP \_ COMPARE \_ TRUE**                | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Vergleichen Sie die ergebene **TRUE-.**                            |
| 0x800704B8       | **\_LDAP-EMPFEHLUNG**                     | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Die Empfehlung kann nicht behoben werden.                             |
| 0x800704B8       | **\_CRIT-ERWEITERUNG "LDAP NICHT \_ \_ VERFÜGBAR"** | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Kritische Erweiterung ist nicht verfügbar.                   |
| 0x800704B8       | **LDAP \_ KEIN \_ SOLCHES \_ ATTRIBUT**          | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Das angeforderte Attribut ist nicht vorhanden.                  |
| 0x800704B8       | **NICHT \_ DEFINIERTER \_ LDAP-TYP**              | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Der Typ ist nicht definiert.                                 |
| 0x800704B8       | **FALSCHER \_ \_ LDAP-ABGLEICH**      | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Es gab einen ungeeigneten Abgleich.                 |
| 0x800704B8       | **\_LDAP-EINSCHRÄNKUNGSVERLETZUNG \_**        | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Es gab eine Einschränkungsverletzung.                     |
| 0x800704B8       | **\_LDAP-ATTRIBUT \_ ODER \_ -WERT \_ VORHANDEN** | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Das Attribut ist vorhanden, oder der Wert wurde zugewiesen. |
| 0x800704B8       | **\_ \_ LDAP-ALIASPROBLEM**               | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Alias ist ungültig.                                  |
| 0x800704B8       | **LDAP \_ IS \_ LEAF**                     | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Das Objekt ist ein Blatt.                                    |
| 0x800704B8       | **\_LDAP-ALIAS \_ \_ DEREF-PROBLEM**        | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Der Alias kann nicht dereferenziert werden.                        |
| 0x800704B8       | **\_ \_ LDAP-SCHLEIFEN-ERKENNUNG**                 | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Die Schleife wurde erkannt.                                   |
| 0x800704B8       | **LDAP \_ NICHT \_ AUF \_ \_ NONLEAF ZULÄSSIG**    | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Der Vorgang ist für ein Nichtblattobjekt nicht zulässig.       |
| 0x800704B8       | **LDAP \_ IM \_ \_ \_ RDN NICHT ZULÄSSIG**        | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Der Vorgang ist im RDN nicht zulässig.                     |
| 0x800704B8       | **LDAP \_ NO \_ OBJECT \_ CLASS \_ MODS**      | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Die Objektklasse kann nicht geändert werden.                          |
| 0x800704B8       | **LDAP \_ WIRKT SICH AUF MEHRERE \_ \_ DSAS AUS**      | **FEHLER \_ \_ ERWEITERTER FEHLER**           | Es sind mehrere Verzeichnisdienstagenten betroffen.      |
| 0x800704C7       | **\_LDAP-BENUTZER \_ ABGEBROCHEN**              | **FEHLER \_ ABGEBROCHEN**                 | Der Benutzer hat den Vorgang abgebrochen.                     |
| 0x80070718       | **\_LDAP-ZEITLIMIT \_ ÜBERSCHRITTEN**          | **FEHLER: \_ NICHT \_ GENÜGEND \_ KONTINGENT**        | Das Zeitlimit wurde überschritten.                                 |
| 0x80070718       | **LDAP \_ SIZELIMIT EXCEEDED (LDAP-GRÖßENLIMIT \_ ÜBERSCHRITTEN)**          | **FEHLER: \_ NICHT \_ GENÜGEND \_ KONTINGENT**        | Das Größenlimit wurde überschritten.                                 |



 

In ADSI 2.0 werden mehrere LDAP-Fehlermeldungen einem Win32-Fehlercode als **FEHLER \_ \_ ERWEITERTER FEHLER** zugeordnet. Rufen Sie [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) auf, um die vom Server zurückgegebene Fehlerzeichenfolge abzurufen. Weitere Informationen finden Sie weiter unten unter [Adsi Extended Error Messages (Erweiterte ADSI-Fehlermeldungen).](adsi-extended-error-messages.md)

 

 




