---
title: WinSNMP-Programmieraufgaben
description: In der folgenden Tabelle sind die grundlegenden Programmierverfahren zusammengefasst, die Sie ausführen müssen, um eine WinSNMP-Anwendung zu codieren, sowie die Themen, die Informationen zu diesen Aufgaben bereitstellen.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007ed1a50688ceff7cdd3bfd9916c1726773cf5ecb2e175af99880950c5c3db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142793"
---
# <a name="winsnmp-programming-tasks"></a>WinSNMP-Programmieraufgaben

In der folgenden Tabelle sind die grundlegenden Programmierverfahren zusammengefasst, die Sie ausführen müssen, um eine WinSNMP-Anwendung zu codieren, sowie die Themen, die Informationen zu diesen Aufgaben bereitstellen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Programmieraufgabe</th>
<th>Aufgabenbezogene Funktionen und Themen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Öffnen Sie die WinSNMP-Anwendung.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup.</strong></a> Siehe <a href="opening-and-closing-a-winsnmp-application.md">Öffnen und Schließen einer WinSNMP-Anwendung.</a><br/></td>
</tr>
<tr class="even">
<td>Öffnen Sie mindestens eine WinSNMP-Sitzung.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>. Weitere Informationen finden Sie unter <a href="opening-and-closing-a-winsnmp-session.md">Öffnen und Schließen einer WinSNMP-Sitzung.</a><br/></td>
</tr>
<tr class="odd">
<td>Registrieren Sie sich, um Traps oder Benachrichtigungen zu empfangen.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister.</strong></a> Weitere Informationen finden Sie unter <a href="managing-traps-and-notifications.md">Verwalten von Traps und Benachrichtigungen.</a><br/></td>
</tr>
<tr class="even">
<td>Erstellen Sie eine oder mehrere Variablenbindungslisten für die Aufnahme in eine PDU.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>. Weitere Informationen finden Sie unter <a href="working-with-variable-binding-lists.md">Arbeiten mit Variablenbindungslisten.</a><br/>
<blockquote>
[!Note]<br />
Die Anwendung muss möglicherweise andere <a href="winsnmp-functions.md">Variablenbindungsfunktionen</a> aufrufen, um die Variablenbindungsliste zu erstellen.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Erstellen Sie eine oder mehrere PDUs für die Übertragung und Verarbeitung.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData,</strong></a> <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU.</strong></a> Weitere Informationen finden Sie unter <a href="working-with-protocol-data-units.md">Arbeiten mit Protokolldateneinheiten.</a><br/>
<blockquote>
[!Note]<br />
Die Anwendung muss möglicherweise andere <a href="winsnmp-functions.md">PDU-Funktionen</a> und WinSNMP-Hilfsfunktionen aufrufen, um die PDU zu erstellen. <a href="winsnmp-functions.md"></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Übermitteln Sie eine oder mehrere SNMP-Vorgangsanforderungen.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg.</strong></a> Weitere Informationen finden Sie <a href="sending-snmp-messages.md">unter Senden von SNMP-Nachrichten.</a><br/></td>
</tr>
<tr class="odd">
<td>Rufen Sie die Antwort auf die SNMP-Vorgangsanforderung ab.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg.</strong></a> Weitere Informationen finden Sie <a href="receiving-snmp-messages.md">unter Empfangen von SNMP-Nachrichten.</a><br/></td>
</tr>
<tr class="even">
<td>Verarbeiten Sie die Anforderungsantwort.</td>
<td>Verwenden Sie anwendungsspezifische Logik.</td>
</tr>
<tr class="odd">
<td>Schließen Sie jede WinSNMP-Sitzung.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>. Weitere Informationen finden Sie unter <a href="opening-and-closing-a-winsnmp-session.md">Öffnen und Schließen einer WinSNMP-Sitzung.</a><br/></td>
</tr>
<tr class="even">
<td>Schließen Sie die WinSNMP-Anwendung.</td>
<td>Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup.</strong></a> Siehe <a href="opening-and-closing-a-winsnmp-application.md">Öffnen und Schließen einer WinSNMP-Anwendung.</a><br/></td>
</tr>
</tbody>
</table>



 

Die folgenden Themen enthalten zusätzliche Informationen zu anderen allgemeinen Programmierkonzepten, die für die WinSNMP-Umgebung spezifisch sind.



| Thema                                                              | Konzepte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Allgemeine Programmieraufgaben](general-winsnmp-programming-tasks.md) | [Verwalten von Objektbezeichnern,](managing-object-identifiers.md)[die WinSNMP-Deskriptoren freigeben](freeing-winsnmp-descriptors.md)<br/> [Festlegen des Entitäts- und Kontextübersetzungsmodus](setting-the-entity-and-context-translation-mode.md)<br/> [Verwalten der Neuübertragungsrichtlinie](managing-the-retransmission-policy.md)<br/> [Schreiben von WinSNMP-Anwendungen mit mehreren Threads](writing-winsnmp-applications-with-multiple-threads.md)<br/> [Registrieren einer SNMP-Agent-Anwendung](registering-an-snmp-agent-application.md)<br/> |



 

Darüber hinaus muss die WinSNMP-Anwendung möglicherweise Aufrufe der folgenden WinSNMP-Funktionen integrieren: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)und [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu). Dadurch kann die Microsoft WinSNMP-Implementierung WinSNMP-Speicherobjekte freigeben. In der Regel sollte die WinSNMP-Anwendung alle Ressourcen freigeben, die als Ergebnis eines Aufrufs einer WinSNMP-Funktion zugeordnet wurden. Weitere Informationen zur Zuordnung von Ressourcen finden Sie unter [Zuordnen von WinSNMP-Speicherobjekten.](allocating-winsnmp-memory-objects.md)

 

 





