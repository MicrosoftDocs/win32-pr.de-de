---
title: WinSNMP-Funktionen
description: Die mit WinSNMP verwendeten Funktionen sind in die folgenden funktionalen Gruppierungen unterteilt. Eine alphabetische Liste folgt.
ms.assetid: ae95ac47-81ff-4715-b3e9-e19c07223712
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c5ebb49e8ec56c0d0b1174fd667d847c09d3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101942"
---
# <a name="winsnmp-functions"></a>WinSNMP-Funktionen

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-man handelt.\]

Die mit WinSNMP verwendeten Funktionen sind in die folgenden funktionalen Gruppierungen unterteilt. Eine alphabetische Liste folgt.

-   [Kommunikationsfunktionen](#winsnmp-communications-functions)
-   [Entitäts-und Kontextfunktionen](#winsnmp-entity-and-context-functions)
-   [Datenbankfunktionen](#winsnmp-database-functions)
-   [PDU-Funktionen](#winsnmp-pdu-functions)
-   [Hilfsfunktionen](#winsnmp-utility-functions)
-   [Variablen Bindungsfunktionen](#winsnmp-variable-binding-functions)
-   [Alphabetische Liste der WinSNMP-Funktionen](/windows)

## <a name="winsnmp-communications-functions"></a>WinSNMP-Kommunikationsfunktionen

Die WinSNMP-Kommunikationsfunktionen stellen eine Schnittstelle zwischen der aufrufenden WinSNMP-Anwendung und der Microsoft WinSNMP-Implementierung bereit. Die-Implementierung übernimmt die Kommunikation zwischen der Anwendung und anderen Verwaltungs Entitäten.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>Snmpcancelmsg</strong></a></td>
<td>Fordert an, dass von der Microsoft WinSNMP-Implementierung Neuübertragungs Versuche und Timeout Benachrichtigungen für eine SNMP-Anforderungs Nachricht abgebrochen werden.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>Snmpcleanup</strong></a></td>
<td>Informiert die Implementierung, dass eine Anwendung die Verbindung trennt und keine zugeordneten Ressourcen mehr erfordert.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>Snmpcleanupex</strong></a></td>
<td>Führt eine Bereinigung durch, wenn keine ausstehenden erfolgreichen Aufrufe von <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> oder <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>snmpstartupex</strong></a> innerhalb einer WinSNMP-Anwendung vorhanden sind.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>Snmpclose</strong></a></td>
<td>Ermöglicht der Implementierung, die Zuordnung von Ressourcen, die einer Sitzung zugeordnet sind, und das Schließen der Kommunikationsmechanismen zu trennen.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>Snmpkreatesession</strong></a></td>
<td>Fordert die-Implementierung auf, eine WinSNMP-Sitzung zu öffnen und Ressourcen und Kommunikationsmechanismen zuzuordnen. Beim Entwickeln neuer WinSNMP-Anwendungen wird empfohlen, dass Sie die <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>snmpcreatesession</strong></a> -Funktion aufrufen, um eine WinSNMP-Sitzung zu öffnen, anstatt die <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>snmpopen</strong></a> -Funktion aufzurufen.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>Snmplauschen</strong></a></td>
<td>Registriert oder hebt die Registrierung einer WinSNMP-Anwendung als SNMP-Agent auf.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>Snmpopen</strong></a></td>
<td>Fordert die-Implementierung auf, eine WinSNMP-Sitzung zu öffnen und Ressourcen und Kommunikationsmechanismen zuzuordnen. Beim Entwickeln neuer WinSNMP-Anwendungen wird empfohlen, dass Sie die <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>snmpcreatesession</strong></a> -Funktion aufrufen, um eine WinSNMP-Sitzung zu öffnen, anstatt die <strong>snmpopen</strong> -Funktion aufzurufen.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>Snmprecvmsg</strong></a></td>
<td>Gibt SNMP-Nachrichten und ausstehende Trap Daten und Benachrichtigungen zurück.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>Snmpregiester</strong></a></td>
<td>Informiert die-Implementierung, dass sich die Anwendung für Traps und Benachrichtigungen registrieren oder deren Registrierung aufheben muss.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>Snmpsendmsg</strong></a></td>
<td>Fordert an, dass die-Implementierung eine Protokolldaten Einheit überträgt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a></td>
<td>Benachrichtigt die-Implementierung, Initialisierungs Prozeduren für die Anwendung auszuführen. Eine Anwendung muss die <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> -Funktion erfolgreich aufrufen, bevor Sie eine andere WinSNMP-Funktion aufruft.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>Snmpstartupex</strong></a></td>
<td>Benachrichtigt die Microsoft WinSNMP-Implementierung, dass die WinSNMP-Anwendung die Dienste der Implementierung erfordert. <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>Snmpstartupex</strong></a> ermöglicht die Unterstützung für mehrere unabhängige Softwaremodule, die WinSNMP innerhalb derselben Anwendung verwenden.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a></td>
<td>Benachrichtigt eine WinSNMP-Sitzung, dass eine SNMP-Nachricht oder ein asynchrones Ereignis verfügbar ist.
<blockquote>
[!Note]<br />
Diese Rückruffunktion gilt nur für Sitzungen, die als Ergebnis eines Aufrufs der <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>snmpkreatesession</strong></a> -Funktion geöffnet wurden.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="winsnmp-entity-and-context-functions"></a>WinSNMP-Entitäts-und Kontextfunktionen

Mit den WinSNMP-Entitäts-und Kontextfunktionen kann eine WinSNMP-Anwendung benutzerfreundliche Namen für SNMP-Entitäten und-Kontexte angeben. Die Microsoft WinSNMP-Implementierung übersetzt den Namen mithilfe der-Implementierungs Datenbank in seine SNMPv1-oder SNMPv2C-Komponenten.



| Funktion                                     | BESCHREIBUNG                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**Snmpcontexttstr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) | Gibt eine Zeichenfolge zurück, die einen SNMP-Kontext (eine Gruppe von verwalteten Objektressourcen) identifiziert.                                  |
| [**Snmpentitytstr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)   | Gibt eine Zeichenfolge zurück, die eine SNMP-Verwaltungs Entität identifiziert.                                                            |
| [**Snmpfreecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)   | Gibt die von der [**snmpstraudecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) -Funktion zugeordneten Ressourcen für einen SNMP-kontextfrei.         |
| [**Snmpfreentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)     | Gibt Ressourcen frei, die von der [**snmpstraudeentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) -Funktion für eine SNMP-Verwaltungs Entität zugeordnet sind. |
| [**Snmpsetport**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)           | Ändert den Port, der einer SNMP-Ziel Entität zugewiesen ist.                                                               |
| [**Snmpstraudecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) | Gibt ein Handle für SNMP-Kontextinformationen zurück, die für die-Implementierung spezifisch sind.                                   |
| [**Snmpstrauch-Entität**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)   | Gibt ein Handle für die SNMP-Verwaltungs Entitäts Informationen zurück, die für die-Implementierung spezifisch sind.                         |



 

## <a name="winsnmp-database-functions"></a>WinSNMP-Datenbankfunktionen

Die WinSNMP-Datenbankfunktionen stellen eine WinSNMP-Anwendung mit Zugriff auf die aktuellen Einstellungen im Speicher der Microsoft WinSNMP-Implementierung der administrativen Informationen bereit. Diese Funktionen ermöglichen das Ändern des Neuübertragungs Modus und des Entitäts-und Kontext Übersetzungsmodus. Die Datenbankfunktionen bieten der Anwendung außerdem die Möglichkeit, die Werte für Timeout und Wiederholungs Anzahl zu ändern.



| Funktion                                               | BESCHREIBUNG                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Snmpgetretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) | Gibt die aktuelle Einstellung des Neuübertragungs Modus zurück.                                               |
| [**Snmpgetretry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)                   | Gibt den Wert für die Wiederholungs Anzahl in Einheiten für die erneute Übertragung von SNMP-Nachrichten Anforderungen zurück.             |
| [**Snmpgettimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)               | Gibt den Timeout Wert (in Hundertstel Sekunden) für die Übertragung von SNMP-Nachrichten Anforderungen zurück. |
| [**Snmpgettranslatemode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)   | Gibt die aktuelle Einstellung des Entitäts-und Kontext Übersetzungsmodus zurück.                               |
| [**Snmpgetvendorinfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)         | Ruft Informationen ab, die den WinSNMP-Anbieter identifizieren.                                             |
| [**Snmpstretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) | Ändert den Modus für Neuübertragungen.                                                                      |
| [**Snmpabtretry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)                   | Ändert den Wert für die Wiederholungs Anzahl für die erneute Übertragung von SNMP-Nachrichten Anforderungen.                        |
| [**Snmpsettimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)               | Ändert den Timeout Wert für die Übertragung von SNMP-Nachrichten Anforderungen.                             |
| [**Snmpsettranslatemode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)   | Ändert den Entitäts-und Kontext Übersetzungsmodus.                                                      |



 

## <a name="winsnmp-pdu-functions"></a>WinSNMP PDU-Funktionen

Mit den WinSNMP PDU-Funktionen können WinSNMP-Anwendungen die Datenelemente (oder Felder) eines PDU extrahieren und aktualisieren. Dies schließt PDUs ein, die von einem Rückruf der [**snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) -Funktion oder der [**snmpdecodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) -Funktion zurückgegeben werden. Die PDU-Funktionen konstruieren auch PDUs zur Verwendung in den Funktionen [**snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) und [**snmpencodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .



| Funktion                                     | BESCHREIBUNG                                                                                                                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)       | Erstellt und Initialisiert eine SNMP-Protokolldaten Einheit.                                                                                                                               |
| [**Snmpduplialisiepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) | Dupliziert eine SNMP-Protokolldaten Einheit.                                                                                                                                            |
| [**Snmpfreepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)           | Gibt Ressourcen frei, die mit einer SNMP-Protokolldaten Einheit verknüpft sind, die von der [**snmpcreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) -Funktion oder der [**snmpdupliaseepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) -Funktion erstellt wurde |
| [**Snmpgetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)     | Gibt ausgewählte Datenelemente aus einer angegebenen SNMP-Protokolldaten Einheit zurück.                                                                                                          |
| [**Snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)     | Aktualisiert die ausgewählten Datenelemente in einer angegebenen SNMP-Protokolldaten Einheit.                                                                                                            |



 

## <a name="winsnmp-utility-functions"></a>WinSNMP-Dienstprogramm Funktionen

Mit den Hilfsprogrammfunktionen von WinSNMP kann eine WinSNMP-Anwendung Objekte und SNMP-Nachrichten über die WinSNMP-Schnittstelle verwalten.



| Funktion                                         | BESCHREIBUNG                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Snmpdecodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)           | Decodiert eine codierte oder serialisierte SNMP-Nachricht in ihre Bestandteile.                                      |
| [**Snmpencodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)           | Erstellt eine verschlüsselte SNMP-Nachricht.                                                                                    |
| [**Snmpfredescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) | Signalisiert der Microsoft WinSNMP-Implementierung, dass der für einen bestimmten Deskriptor zugewiesene Arbeitsspeicher freigegeben werden soll. |
| [**Snmpgetlasterror**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)     | Gibt den letzten Fehlercode für den letzten SNMP-Vorgang zurück.                                                      |
| [**Snmpoidcompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)         | Vergleicht zwei SNMP-Objekt Bezeichner.                                                                               |
| [**Snmpoidcopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)               | Kopiert einen SNMP-Objekt Bezeichner.                                                                                   |
| [**Snmpoidin**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)             | Konvertiert die interne binäre Darstellung eines SNMP-Objekt Bezeichners in das gepunktete numerische Zeichen folgen Format.       |
| [**Snmpstrau| OID**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)             | Konvertiert das punktierte numerische Zeichen folgen Format eines SNMP-Objekt Bezeichners in seine interne binäre Darstellung.       |



 

## <a name="winsnmp-variable-binding-functions"></a>WinSNMP-Variablen Bindungsfunktionen

Mit den WinSNMP-Variablen Bindungsfunktionen können WinSNMP-Anwendungen Variablen Bindungs Listen erstellen und bearbeiten und Sie in PDUs einschließen.



| Funktion                                     | BESCHREIBUNG                                                                                                                                                                     |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Snmpzähltvbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)         | Listet die Variablen Bindungs Einträge in einer angegebenen Variablen Bindungs Liste auf.                                                                                                   |
| [**Snmpkreatevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)       | Erstellt eine neue Variablen Bindungs Liste.                                                                                                                                            |
| [**Snmpdeletevb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)         | Entfernt einen Variablen Bindungs Eintrag aus einer Variablen Bindungs Liste.                                                                                                                  |
| [**Snmpduplimpevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) | Kopiert eine Variablen Bindungs Liste.                                                                                                                                                 |
| [**Snmpfreevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)           | Gibt Ressourcen für eine Variablen Bindungs Liste frei, die zuvor von der [**snmpcreatevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) oder der [**snmpdupliaseevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) -Funktion zugeordnet wurde. |
| [**Snmpgetvb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)               | Ruft Informationen aus einem angegebenen Variablen Bindungs Eintrag ab.                                                                                                                  |
| [**Snmpsetvb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)               | Ändert Variablen Bindungs Einträge in einer Variablen Bindungs Liste. Fügt neue Variablen Bindungs Einträge an eine vorhandene Variablen Bindungs Liste an.                                         |



 

## <a name="winsnmp-functions---alphabetic-list"></a>Alphabetische Liste der WinSNMP-Funktionen

-   [**Snmpapi- \_ Rückruf**](/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback)
-   [**Snmpcancelmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)
-   [**Snmpcleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)
-   [**Snmpclose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)
-   [**Snmpcontexttstr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)
-   [**Snmpzähltvbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)
-   [**Snmpkreatepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)
-   [**Snmpkreatesession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)
-   [**Snmpkreatevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)
-   [**Snmpdecodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)
-   [**Snmpdeletevb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)
-   [**Snmpduplialisiepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu)
-   [**Snmpduplimpevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)
-   [**Snmpencodemsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)
-   [**Snmpentitytstr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)
-   [**Snmpfreecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)
-   [**Snmpfredescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)
-   [**Snmpfreentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)
-   [**Snmpfreepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)
-   [**Snmpfreevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)
-   [**Snmpgetlasterror**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)
-   [**Snmpgetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)
-   [**Snmpgetretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode)
-   [**Snmpgetretry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)
-   [**Snmpgettimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)
-   [**Snmpgettranslatemode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)
-   [**Snmpgetvb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)
-   [**Snmpgetvendorinfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)
-   [**Snmplauschen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten)
-   [**Snmpoidcompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)
-   [**Snmpoidcopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)
-   [**Snmpoidin**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)
-   [**Snmpopen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen)
-   [**Snmprecvmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)
-   [**Snmpregiester**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)
-   [**Snmpsendmsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)
-   [**Snmpsetpdudata**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)
-   [**Snmpsetport**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)
-   [**Snmpstretransmitmode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode)
-   [**Snmpabtretry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)
-   [**Snmpsettimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)
-   [**Snmpsettranslatemode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)
-   [**Snmpsetvb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)
-   [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)
-   [**Snmpstraudecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext)
-   [**Snmpstrauch-Entität**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)
-   [**Snmpstrau| OID**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

 

