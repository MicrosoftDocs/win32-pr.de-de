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
# <a name="winsnmp-programming-tasks"></a><span data-ttu-id="9ec61-103">WinSNMP-Programmieraufgaben</span><span class="sxs-lookup"><span data-stu-id="9ec61-103">WinSNMP Programming Tasks</span></span>

<span data-ttu-id="9ec61-104">In der folgenden Tabelle werden die grundlegenden Programmier Prozeduren zusammengefasst, die Sie zum Codieren einer WinSNMP-Anwendung ausführen müssen, sowie die Themen mit Informationen zu diesen Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="9ec61-104">The following table summarizes the basic programming procedures that you must perform to code a WinSNMP application, and the topics that provide information about these tasks.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ec61-105">Programmieraufgabe</span><span class="sxs-lookup"><span data-stu-id="9ec61-105">Programming task</span></span></th>
<th><span data-ttu-id="9ec61-106">Aufgabenbezogene Funktion und Themen</span><span class="sxs-lookup"><span data-stu-id="9ec61-106">Task-related function and topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ec61-107">Öffnen Sie die WinSNMP-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9ec61-107">Open the WinSNMP application.</span></span></td>
<td><span data-ttu-id="9ec61-108">Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-108">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>.</span></span> <span data-ttu-id="9ec61-109">Weitere Informationen finden Sie unter <a href="opening-and-closing-a-winsnmp-application.md">Öffnen und Schließen einer WinSNMP-Anwendung</a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-109">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ec61-110">Öffnen Sie mindestens eine WinSNMP-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9ec61-110">Open one or more WinSNMP sessions.</span></span></td>
<td><span data-ttu-id="9ec61-111">Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>snmpkreatesession</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-111">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>.</span></span> <span data-ttu-id="9ec61-112">Weitere Informationen finden Sie unter <a href="opening-and-closing-a-winsnmp-session.md">Öffnen und Schließen einer WinSNMP-Sitzung</a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-112">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ec61-113">Registrieren Sie sich, um Traps oder Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="9ec61-113">Register to receive traps or notifications.</span></span></td>
<td><span data-ttu-id="9ec61-114">Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>snmpregiester</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-114">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>.</span></span> <span data-ttu-id="9ec61-115">Siehe <a href="managing-traps-and-notifications.md">Verwalten von Traps und Benachrichtigungen</a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-115">See <a href="managing-traps-and-notifications.md">Managing Traps and Notifications</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ec61-116">Erstellen Sie mindestens eine Variablen Bindungs Liste für die Einbindung in ein PDU.</span><span class="sxs-lookup"><span data-stu-id="9ec61-116">Create one or more variable binding lists for incorporation in a PDU.</span></span></td>
<td><span data-ttu-id="9ec61-117">Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>snmpkreatevbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>snmpduplialisievbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>snmpsetvb</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-117">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>.</span></span> <span data-ttu-id="9ec61-118">Weitere Informationen finden Sie <a href="working-with-variable-binding-lists.md">unter Arbeiten mit Variablen Bindungs Listen</a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-118">See <a href="working-with-variable-binding-lists.md">Working with Variable Binding Lists</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9ec61-119">Die Anwendung muss möglicherweise andere <a href="winsnmp-functions.md">Variablen Bindungsfunktionen</a> zum Erstellen der Variablen Bindungs Liste aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9ec61-119">The application may need to call other <a href="winsnmp-functions.md">variable binding functions</a> to create the variable binding list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ec61-120">Erstellen Sie einen oder mehrere PDUs für die Übertragung und Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="9ec61-120">Create one or more PDUs for transmission and processing.</span></span></td>
<td><span data-ttu-id="9ec61-121">Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>snmpkreatepdu</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>snmpsetpdudata</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>snmpduplierepdu</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-121">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>.</span></span> <span data-ttu-id="9ec61-122">Weitere Informationen finden Sie <a href="working-with-protocol-data-units.md">unter Arbeiten mit Protokolldaten Einheiten</a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-122">See <a href="working-with-protocol-data-units.md">Working with Protocol Data Units</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9ec61-123">Die Anwendung muss möglicherweise andere <a href="winsnmp-functions.md">PDU-Funktionen</a> und WinSNMP- <a href="winsnmp-functions.md">Hilfsprogrammfunktionen</a> zum Erstellen des PDU-Programms aufruft.</span><span class="sxs-lookup"><span data-stu-id="9ec61-123">The application may need to call other <a href="winsnmp-functions.md">PDU functions</a> and WinSNMP <a href="winsnmp-functions.md">utility functions</a> to create the PDU.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ec61-124">Senden Sie eine oder mehrere SNMP-Vorgangs Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="9ec61-124">Submit one or more SNMP operation requests.</span></span></td>
<td><span data-ttu-id="9ec61-125">Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>snmpsendmsg</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-125">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>.</span></span> <span data-ttu-id="9ec61-126">Siehe <a href="sending-snmp-messages.md">Senden von SNMP-Nachrichten</a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-126">See <a href="sending-snmp-messages.md">Sending SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ec61-127">Rufen Sie die Antwort auf die SNMP-Vorgangs Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="9ec61-127">Retrieve the response to the SNMP operation request.</span></span></td>
<td><span data-ttu-id="9ec61-128">Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>snmprecvmsg</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-128">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>.</span></span> <span data-ttu-id="9ec61-129">Siehe <a href="receiving-snmp-messages.md">empfangen von SNMP-Nachrichten</a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-129">See <a href="receiving-snmp-messages.md">Receiving SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ec61-130">Verarbeiten der Anforderungs Antwort.</span><span class="sxs-lookup"><span data-stu-id="9ec61-130">Process the request response.</span></span></td>
<td><span data-ttu-id="9ec61-131">Anwendungsspezifische Logik verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ec61-131">Use application-specific logic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ec61-132">Schließen Sie jede WinSNMP-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="9ec61-132">Close each WinSNMP session.</span></span></td>
<td><span data-ttu-id="9ec61-133">Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>snmpclose</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-133">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>.</span></span> <span data-ttu-id="9ec61-134">Weitere Informationen finden Sie unter <a href="opening-and-closing-a-winsnmp-session.md">Öffnen und Schließen einer WinSNMP-Sitzung</a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-134">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ec61-135">Schließen Sie die WinSNMP-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="9ec61-135">Close the WinSNMP application.</span></span></td>
<td><span data-ttu-id="9ec61-136">Verwenden Sie <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>snmpcleanup</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-136">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>.</span></span> <span data-ttu-id="9ec61-137">Weitere Informationen finden Sie unter <a href="opening-and-closing-a-winsnmp-application.md">Öffnen und Schließen einer WinSNMP-Anwendung</a>.</span><span class="sxs-lookup"><span data-stu-id="9ec61-137">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9ec61-138">Die folgenden Themen enthalten zusätzliche Informationen zu anderen allgemeinen Programmier Konzepten, die für die WinSNMP-Umgebung spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="9ec61-138">The following topics contain additional information about other general programming concepts specific to the WinSNMP environment.</span></span>



|                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ec61-139">Allgemeine Programmieraufgaben</span><span class="sxs-lookup"><span data-stu-id="9ec61-139">General programming tasks</span></span>](general-winsnmp-programming-tasks.md) | <span data-ttu-id="9ec61-140">[Verwalten von Objekt](managing-object-identifiers.md)Bezeichners, die[WinSNMP-Deskriptoren freigeben](freeing-winsnmp-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="9ec61-140">[Managing Object Identifiers](managing-object-identifiers.md)[Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md)</span></span><br/> [<span data-ttu-id="9ec61-141">Festlegen des Entitäts-und Kontext Übersetzungsmodus</span><span class="sxs-lookup"><span data-stu-id="9ec61-141">Setting the Entity and Context Translation Mode</span></span>](setting-the-entity-and-context-translation-mode.md)<br/> [<span data-ttu-id="9ec61-142">Verwalten der Richtlinie für Neuübertragungen</span><span class="sxs-lookup"><span data-stu-id="9ec61-142">Managing the Retransmission Policy</span></span>](managing-the-retransmission-policy.md)<br/> [<span data-ttu-id="9ec61-143">Schreiben von WinSNMP-Anwendungen mit mehreren Threads</span><span class="sxs-lookup"><span data-stu-id="9ec61-143">Writing WinSNMP Applications with Multiple Threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)<br/> [<span data-ttu-id="9ec61-144">Registrieren einer SNMP-Agent-Anwendung</span><span class="sxs-lookup"><span data-stu-id="9ec61-144">Registering an SNMP Agent Application</span></span>](registering-an-snmp-agent-application.md)<br/> |



 

<span data-ttu-id="9ec61-145">Außerdem muss die WinSNMP-Anwendung möglicherweise Aufrufe der folgenden WinSNMP-Funktionen einbinden: [**snmpfreevbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**snmpfreeentity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**snmpfreedescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**snmpfreecontext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)und [**snmpfreepdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span><span class="sxs-lookup"><span data-stu-id="9ec61-145">In addition, the WinSNMP application may need to incorporate calls to the following WinSNMP functions: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span></span> <span data-ttu-id="9ec61-146">Dadurch kann die Microsoft WinSNMP-Implementierung WinSNMP-Speicher Objekte freigeben.</span><span class="sxs-lookup"><span data-stu-id="9ec61-146">This enables the Microsoft WinSNMP implementation to free WinSNMP memory objects.</span></span> <span data-ttu-id="9ec61-147">Als allgemeine Regel gilt: die WinSNMP-Anwendung sollte alle Ressourcen freigeben, die als Ergebnis eines Aufrufes einer WinSNMP-Funktion zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9ec61-147">As a general rule, the WinSNMP application should free all resources allocated as the result of a call to a WinSNMP function.</span></span> <span data-ttu-id="9ec61-148">Weitere Informationen zum Aufheben der Zuordnung von Ressourcen finden Sie unter [Zuordnen von WinSNMP-Speicher Objekten](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9ec61-148">For additional information about deallocating resources, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 





