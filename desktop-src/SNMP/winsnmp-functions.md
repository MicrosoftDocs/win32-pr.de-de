---
title: WinSNMP-Funktionen
description: Die mit WinSNMP verwendeten Funktionen fallen in die folgenden Funktionsgruppierungen. Es folgt eine alphabetische Liste.
ms.assetid: ae95ac47-81ff-4715-b3e9-e19c07223712
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29169e8cf86b7f21ebbc40ced2ac37a46668c727183a9b2970eb368c7e81d85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142803"
---
# <a name="winsnmp-functions"></a>WinSNMP-Funktionen

\[SNMP ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen [Windows Remoteverwaltung](/windows/desktop/WinRM/portal), bei dem es sich um die Microsoft-Implementierung von WS-Man handelt.\]

Die mit WinSNMP verwendeten Funktionen fallen in die folgenden Funktionsgruppierungen. Es folgt eine alphabetische Liste.

-   [Kommunikationsfunktionen](#winsnmp-communications-functions)
-   [Entitäts- und Kontextfunktionen](#winsnmp-entity-and-context-functions)
-   [Datenbankfunktionen](#winsnmp-database-functions)
-   [PDU-Funktionen](#winsnmp-pdu-functions)
-   [Hilfsfunktionen](#winsnmp-utility-functions)
-   [Variablenbindungsfunktionen](#winsnmp-variable-binding-functions)
-   [Alphabetische Liste der WinSNMP-Funktionen](/windows)

## <a name="winsnmp-communications-functions"></a>WinSNMP-Kommunikationsfunktionen

Die WinSNMP-Kommunikationsfunktionen stellen eine Schnittstelle zwischen der aufrufenden WinSNMP-Anwendung und der Microsoft WinSNMP-Implementierung bereit. Die Implementierung übernimmt die Kommunikation zwischen der Anwendung und anderen Verwaltungsentitäten.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>SnmpCancelMsg</strong></a></td>
<td>Fordert an, dass die Microsoft WinSNMP-Implementierung Neuübertragungsversuche und Time out-Benachrichtigungen für eine SNMP-Anforderungsnachricht abbricht.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a></td>
<td>Informiert die Implementierung, dass eine Anwendung die Verbindung trennt und keine zugeordneten Ressourcen mehr benötigt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>SnmpCleanupEx</strong></a></td>
<td>Führt eine Bereinigung aus, wenn in einer WinSNMP-Anwendung keine ausstehenden erfolgreichen Aufrufe von <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> oder <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> vorhanden sind.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a></td>
<td>Ermöglicht der Implementierung das Zuordnen von Ressourcen, die einer Sitzung zugeordnet sind, und das Schließen von Kommunikationsmechanismen.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a></td>
<td>Fordert die Implementierung auf, eine WinSNMP-Sitzung zu öffnen und Ressourcen und Kommunikationsmechanismen zuzuordnen. Beim Entwickeln neuer WinSNMP-Anwendungen wird empfohlen, die <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession-Funktion</strong></a> aufzurufen, um eine WinSNMP-Sitzung zu öffnen, anstatt die <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen-Funktion</strong></a> aufzurufen.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>SnmpListen</strong></a></td>
<td>Registriert oder entfernt die Registrierung einer WinSNMP-Anwendung als SNMP-Agent.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a></td>
<td>Fordert die Implementierung auf, eine WinSNMP-Sitzung zu öffnen und Ressourcen und Kommunikationsmechanismen zuzuordnen. Beim Entwickeln neuer WinSNMP-Anwendungen wird empfohlen, die <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession-Funktion</strong></a> aufzurufen, um eine WinSNMP-Sitzung zu öffnen, anstatt die <strong>SnmpOpen-Funktion</strong> aufzurufen.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a></td>
<td>Gibt SNMP-Nachrichten und ausstehende Trapdaten und Benachrichtigungen zurück.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a></td>
<td>Informiert die Implementierung darüber, dass die Anwendung die Registrierung für Traps und Benachrichtigungen aufheben muss.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a></td>
<td>Fordert an, dass die Implementierung eine Protokolldateneinheit überträgt.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a></td>
<td>Benachrichtigt die Implementierung, Initialisierungsverfahren für die Anwendung auszuführen. Eine Anwendung muss die <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup-Funktion</strong></a> erfolgreich aufrufen, bevor sie eine andere WinSNMP-Funktion aufruft.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a></td>
<td>Benachrichtigt die Microsoft WinSNMP-Implementierung, dass die WinSNMP-Anwendung die Dienste der Implementierung erfordert. <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> ermöglicht die Unterstützung mehrerer unabhängiger Softwaremodule, die WinSNMP innerhalb derselben Anwendung verwenden.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a></td>
<td>Benachrichtigt eine WinSNMP-Sitzung, dass eine SNMP-Nachricht oder ein asynchrones Ereignis verfügbar ist.
<blockquote>
[!Note]<br />
Diese Rückruffunktion gilt nur für Sitzungen, die als Ergebnis eines Aufrufs der <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession-Funktion</strong></a> geöffnet wurden.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="winsnmp-entity-and-context-functions"></a>WinSNMP-Entitäts- und Kontextfunktionen

Die WinSNMP-Entitäts- und Kontextfunktionen ermöglichen es einer WinSNMP-Anwendung, benutzerfreundliche Namen für SNMP-Entitäten und -Kontexte anzugeben. Die Microsoft WinSNMP-Implementierung übersetzt den Namen mithilfe der Datenbank der Implementierung in die SNMPv1- oder SNMPv2C-Komponenten.



| Funktion                                     | Beschreibung                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) | Gibt eine Zeichenfolge zurück, die einen SNMP-Kontext (einen Satz verwalteter Objektressourcen) identifiziert.                                  |
| [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)   | Gibt eine Zeichenfolge zurück, die eine SNMP-Verwaltungsentität identifiziert.                                                            |
| [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)   | Gibt Ressourcen frei, die von der [**SnmpStrToContext-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) für einen SNMP-Kontext zugeordnet werden.         |
| [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)     | Gibt Ressourcen frei, die von der [**SnmpStrToEntity-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) für eine SNMP-Verwaltungsentität zugeordnet werden. |
| [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)           | Ändert den Port, der einer SNMP-Zielentität zugewiesen ist.                                                               |
| [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) | Gibt ein Handle für SNMP-Kontextinformationen zurück, das für die Implementierung spezifisch ist.                                   |
| [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)   | Gibt ein Handle für SNMP-Verwaltungsentitätsinformationen zurück, die für die Implementierung spezifisch sind.                         |



 

## <a name="winsnmp-database-functions"></a>WinSNMP-Datenbankfunktionen

Die WinSNMP-Datenbankfunktionen bieten einer WinSNMP-Anwendung Zugriff auf die aktuellen Einstellungen im Speicher administrativer Informationen der Microsoft WinSNMP-Implementierung. Diese Funktionen ermöglichen das Ändern des Neuübertragungsmodus und des Entitäts- und Kontextübersetzungsmodus. Die Datenbankfunktionen bieten der Anwendung auch die Möglichkeit, time-out- und retry count-Werte zu bearbeiten.



| Funktion                                               | Beschreibung                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) | Gibt die aktuelle Einstellung des Neuübertragungsmodus zurück.                                               |
| [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)                   | Gibt den Wert für die Wiederholungsanzahl in Einheiten für die erneute Übertragung von SNMP-Nachrichtenanforderungen zurück.             |
| [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)               | Gibt den Time out-Wert in Hundertstel einer Sekunde für die Übertragung von SNMP-Nachrichtenanforderungen zurück. |
| [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)   | Gibt die aktuelle Einstellung des Entitäts- und Kontextübersetzungsmodus zurück.                               |
| [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)         | Ruft Informationen ab, die den WinSNMP-Anbieter identifizieren.                                             |
| [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) | Ändert den Neuübertragungsmodus.                                                                      |
| [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)                   | Ändert den Wert der Wiederholungsanzahl für die erneute Übertragung von SNMP-Nachrichtenanforderungen.                        |
| [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)               | Ändert den Time out-Wert für die Übertragung von SNMP-Nachrichtenanforderungen.                             |
| [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)   | Ändert den Entitäts- und Kontextübersetzungsmodus.                                                      |



 

## <a name="winsnmp-pdu-functions"></a>WinSNMP-PDU-Funktionen

Die WinSNMP-PDU-Funktionen ermöglichen WinSNMP-Anwendungen das Extrahieren und Aktualisieren der Datenelemente (oder Felder) einer PDU. Dies schließt PDUs ein, die durch einen Aufruf der [**SnmpRecvMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) oder der [**SnmpDecodeMsg-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) zurückgegeben werden. Die PDU-Funktionen erstellen auch PDUs für die Verwendung in den Funktionen [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) und [**SnmpEncodeMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)



| Funktion                                     | Beschreibung                                                                                                                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)       | Erstellt und initialisiert eine SNMP-Protokolldateneinheit.                                                                                                                               |
| [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) | Dupliziert eine SNMP-Protokolldateneinheit.                                                                                                                                            |
| [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)           | Gibt Ressourcen frei, die einer SNMP-Protokolldateneinheit zugeordnet sind, die von der [**SnmpCreatePdu-**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) oder [**der SnmpDuplicatePdu-Funktion**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) erstellt wurde. |
| [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)     | Gibt ausgewählte Datenelemente aus einer angegebenen SNMP-Protokolldateneinheit zurück.                                                                                                          |
| [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)     | Aktualisiert ausgewählte Datenelemente in einer angegebenen SNMP-Protokolldateneinheit.                                                                                                            |



 

## <a name="winsnmp-utility-functions"></a>WinSNMP-Hilfsprogrammfunktionen

Die WinSNMP-Hilfsfunktionen ermöglichen einer WinSNMP-Anwendung die Verwaltung von Objekten und SNMP-Nachrichten über die WinSNMP-Schnittstelle.



| Funktion                                         | Beschreibung                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)           | Decodiert eine codierte oder serialisierte SNMP-Nachricht in die zugehörigen Komponenten.                                      |
| [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)           | Erstellt eine codierte SNMP-Nachricht.                                                                                    |
| [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) | Signalisiert der Microsoft WinSNMP-Implementierung, dass der für einen bestimmten Deskriptor belegte Arbeitsspeicher freigegeben werden soll. |
| [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)     | Gibt den Codewert für den letzten Fehler für den letzten SNMP-Vorgang zurück.                                                      |
| [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)         | Vergleicht zwei SNMP-Objektbezeichner.                                                                               |
| [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)               | Kopiert einen SNMP-Objektbezeichner.                                                                                   |
| [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)             | Konvertiert die interne binäre Darstellung eines SNMP-Objektbezeichners in das gepunktete numerische Zeichenfolgenformat.       |
| [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)             | Konvertiert das gepunktete numerische Zeichenfolgenformat eines SNMP-Objektbezeichners in seine interne binäre Darstellung.       |



 

## <a name="winsnmp-variable-binding-functions"></a>WinSNMP-Variablenbindungsfunktionen

Mit den WinSNMP-Variablenbindungsfunktionen können WinSNMP-Anwendungen Variablenbindungslisten erstellen und bearbeiten und in PDUs einschließen.



| Funktion                                     | Beschreibung                                                                                                                                                                     |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)         | Listet die Variablenbindungseinträge in einer angegebenen Variablenbindungsliste auf.                                                                                                   |
| [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)       | Erstellt eine neue Variablenbindungsliste.                                                                                                                                            |
| [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)         | Entfernt einen Variablenbindungseintrag aus einer Variablenbindungsliste.                                                                                                                  |
| [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) | Kopiert eine Variablenbindungsliste.                                                                                                                                                 |
| [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)           | Gibt Ressourcen für eine Variablenbindungsliste frei, die zuvor von der [**Funktion SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) oder [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) zugeordnet wurde. |
| [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)               | Ruft Informationen aus einem angegebenen Variablenbindungseintrag ab.                                                                                                                  |
| [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)               | Ändert Variablenbindungseinträge in einer Variablenbindungsliste. fügt neue Variablenbindungseinträge an eine vorhandene Variablenbindungsliste an.                                         |



 

## <a name="winsnmp-functions---alphabetic-list"></a>Alphabetische Liste der WinSNMP-Funktionen

-   [**\_SNMPAPI-RÜCKRUF**](/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback)
-   [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)
-   [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)
-   [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)
-   [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)
-   [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)
-   [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)
-   [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)
-   [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)
-   [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)
-   [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)
-   [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu)
-   [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)
-   [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)
-   [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)
-   [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)
-   [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)
-   [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)
-   [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)
-   [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)
-   [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)
-   [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)
-   [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode)
-   [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)
-   [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)
-   [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)
-   [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)
-   [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)
-   [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten)
-   [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)
-   [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)
-   [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)
-   [**SnmpOpen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen)
-   [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)
-   [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)
-   [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)
-   [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)
-   [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)
-   [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode)
-   [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)
-   [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)
-   [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)
-   [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)
-   [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)
-   [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext)
-   [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)
-   [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

 

