---
title: WinSNMP-Programmieraufgaben
description: In der folgenden Tabelle werden die grundlegenden Programmier Prozeduren zusammengefasst, die Sie zum Codieren einer WinSNMP-Anwendung ausführen müssen, sowie die Themen mit Informationen zu diesen Aufgaben.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75fa8d2ad223fbd8f71eff78c7cd232ddc492a9
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "103857980"
---
# <a name="winsnmp-programming-tasks"></a>WinSNMP-Programmieraufgaben

In der folgenden Tabelle werden die grundlegenden Programmier Prozeduren zusammengefasst, die Sie zum Codieren einer WinSNMP-Anwendung ausführen müssen, sowie die Themen mit Informationen zu diesen Aufgaben.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Programmieraufgabe</th>
<th>Aufgabenbezogene Funktion und Themen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Öffnen Sie die WinSNMP-Anwendung.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>. Weitere Informationen finden Sie unter <a href="opening-and-closing-a-winsnmp-application.md">Öffnen und Schließen einer WinSNMP-Anwendung</a>.<br/></td>
</tr>
<tr class="even">
<td>Öffnen Sie mindestens eine WinSNMP-Sitzung.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>snmpkreatesession</strong></a>. Weitere Informationen finden Sie unter <a href="opening-and-closing-a-winsnmp-session.md">Öffnen und Schließen einer WinSNMP-Sitzung</a>.<br/></td>
</tr>
<tr class="odd">
<td>Registrieren Sie sich, um Traps oder Benachrichtigungen zu empfangen.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>snmpregiester</strong></a>. Siehe <a href="managing-traps-and-notifications.md">Verwalten von Traps und Benachrichtigungen</a>.<br/></td>
</tr>
<tr class="even">
<td>Erstellen Sie mindestens eine Variablen Bindungs Liste für die Einbindung in ein PDU.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>snmpkreatevbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>snmpduplialisievbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>snmpsetvb</strong></a>. Weitere Informationen finden Sie <a href="working-with-variable-binding-lists.md">unter Arbeiten mit Variablen Bindungs Listen</a>.<br/>
<blockquote>
[!Note]<br />
Die Anwendung muss möglicherweise andere <a href="winsnmp-functions.md">Variablen Bindungsfunktionen</a> zum Erstellen der Variablen Bindungs Liste aufzurufen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Erstellen Sie einen oder mehrere PDUs für die Übertragung und Verarbeitung.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>snmpkreatepdu</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>snmpsetpdudata</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>snmpduplierepdu</strong></a>. Weitere Informationen finden Sie <a href="working-with-protocol-data-units.md">unter Arbeiten mit Protokolldaten Einheiten</a>.<br/>
<blockquote>
[!Note]<br />
Die Anwendung muss möglicherweise andere <a href="winsnmp-functions.md">PDU-Funktionen</a> und WinSNMP- <a href="winsnmp-functions.md">Hilfsprogrammfunktionen</a> zum Erstellen des PDU-Programms aufruft.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Senden Sie eine oder mehrere SNMP-Vorgangs Anforderungen.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>snmpsendmsg</strong></a>. Siehe <a href="sending-snmp-messages.md">Senden von SNMP-Nachrichten</a>.<br/></td>
</tr>
<tr class="odd">
<td>Rufen Sie die Antwort auf die SNMP-Vorgangs Anforderung ab.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>snmprecvmsg</strong></a>. Siehe <a href="receiving-snmp-messages.md">empfangen von SNMP-Nachrichten</a>.<br/></td>
</tr>
<tr class="even">
<td>Verarbeiten der Anforderungs Antwort.</td>
<td>Anwendungsspezifische Logik verwenden.</td>
</tr>
<tr class="odd">
<td>Schließen Sie jede WinSNMP-Sitzung.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>snmpclose</strong></a>. Weitere Informationen finden Sie unter <a href="opening-and-closing-a-winsnmp-session.md">Öffnen und Schließen einer WinSNMP-Sitzung</a>.<br/></td>
</tr>
<tr class="even">
<td>Schließen Sie die WinSNMP-Anwendung.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>snmpcleanup</strong></a>. Weitere Informationen finden Sie unter <a href="opening-and-closing-a-winsnmp-application.md">Öffnen und Schließen einer WinSNMP-Anwendung</a>.<br/></td>
</tr>
</tbody>
</table>



 

Die folgenden Themen enthalten zusätzliche Informationen zu anderen allgemeinen Programmier Konzepten, die für die WinSNMP-Umgebung spezifisch sind.



|                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Allgemeine Programmieraufgaben](general-winsnmp-programming-tasks.md) | [Verwalten von Objekt](managing-object-identifiers.md)Bezeichners, die[WinSNMP-Deskriptoren freigeben](freeing-winsnmp-descriptors.md)<br/> [Festlegen des Entitäts-und Kontext Übersetzungsmodus](setting-the-entity-and-context-translation-mode.md)<br/> [Verwalten der Richtlinie für Neuübertragungen](managing-the-retransmission-policy.md)<br/> [Schreiben von WinSNMP-Anwendungen mit mehreren Threads](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registrieren einer SNMP-Agent-Anwendung](registering-an-snmp-agent-application.md)<br/> |



 

Außerdem muss die WinSNMP-Anwendung möglicherweise Aufrufe der folgenden WinSNMP-Funktionen einbinden: [**snmpfreevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**snmpfreeentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**snmpfreedescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**snmpfreecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)und [**snmpfreepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu). Dadurch kann die Microsoft WinSNMP-Implementierung WinSNMP-Speicher Objekte freigeben. Als allgemeine Regel gilt: die WinSNMP-Anwendung sollte alle Ressourcen freigeben, die als Ergebnis eines Aufrufes einer WinSNMP-Funktion zugeordnet sind. Weitere Informationen zum Aufheben der Zuordnung von Ressourcen finden Sie unter [Zuordnen von WinSNMP-Speicher Objekten](allocating-winsnmp-memory-objects.md).

 

 





