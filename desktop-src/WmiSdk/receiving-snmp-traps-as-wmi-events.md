---
description: WMI ordnet SNMP-Traps automatisch WMI-Ereignissen zu. Das System platziert die im Trap enthaltenen Daten in den entsprechenden Eigenschaften einer WMI-Ereignis Instanz für den Zugriff durch den WMI-Host Computer.
ms.assetid: 549f58a9-9d3b-41b9-a374-ab83877f63a7
ms.tgt_platform: multiple
title: Empfangen von SNMP-Traps als WMI-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da24be8ea9a4882af0b961b1d0f6f0c3d442c70c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528508"
---
# <a name="receiving-snmp-traps-as-wmi-events"></a><span data-ttu-id="91f03-104">Empfangen von SNMP-Traps als WMI-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="91f03-104">Receiving SNMP Traps as WMI Events</span></span>

<span data-ttu-id="91f03-105">WMI ordnet SNMP-Traps automatisch WMI-Ereignissen zu.</span><span class="sxs-lookup"><span data-stu-id="91f03-105">WMI automatically maps SNMP traps to WMI events.</span></span> <span data-ttu-id="91f03-106">Das System platziert die im Trap enthaltenen Daten in den entsprechenden Eigenschaften einer WMI-Ereignis Instanz für den Zugriff durch den WMI-Host Computer.</span><span class="sxs-lookup"><span data-stu-id="91f03-106">The system places the data contained in the trap in the corresponding properties of a WMI event instance for access by the WMI host machine.</span></span>

> [!Note]  
> <span data-ttu-id="91f03-107">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="91f03-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="91f03-108">Das Empfangen eines SNMP-Traps ist nahezu identisch mit dem Empfang von Ereignissen von einem beliebigen anderen WMI-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="91f03-108">Receiving an SNMP trap is nearly identical to receiving events from any other WMI provider.</span></span> <span data-ttu-id="91f03-109">Der SNMP-Ereignis Filter hat jedoch mehrere eindeutige Klassen, die Sie beachten sollten, bevor Sie sich für Ereignisse registrieren.</span><span class="sxs-lookup"><span data-stu-id="91f03-109">However, the SNMP event filter has several unique classes to be aware of before registering for events.</span></span> <span data-ttu-id="91f03-110">Außerdem erfordert der Ereignis Anbieter ausschließlich die Verwendung des \\ SMIR-Namespace.</span><span class="sxs-lookup"><span data-stu-id="91f03-110">Also, the event provider requires the use of the \\smir namespace exclusively.</span></span>

<span data-ttu-id="91f03-111">Die gängigsten Klassen für die Registrierung bei sind [SnmpNotification](snmpnotification.md) und [snmpextendednotification](snmpextendednotification.md).</span><span class="sxs-lookup"><span data-stu-id="91f03-111">The most common classes to register with are [SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md).</span></span> <span data-ttu-id="91f03-112">Consumer, die Ereignis Benachrichtigungen verwenden, um Werte in überwachten SNMP-Geräten zu aktualisieren, müssen sich für snmpextendednotification-Ereignisse registrieren.</span><span class="sxs-lookup"><span data-stu-id="91f03-112">Consumers intent on using event notifications to update values in monitored SNMP devices must register for SnmpExtendedNotification events.</span></span> <span data-ttu-id="91f03-113">Die Informationen aus SnmpNotification-Ereignissen sind nicht wiederverwendbar.</span><span class="sxs-lookup"><span data-stu-id="91f03-113">The information from SnmpNotification events is not reusable.</span></span>

<span data-ttu-id="91f03-114">In der folgenden Tabelle sind Informationen zum Einrichten des Computers zum Empfangen von SNMP-Traps als WMI-Ereignisse aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="91f03-114">The following table lists information about setting up your computer to receive SNMP traps as WMI events.</span></span>



| <span data-ttu-id="91f03-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="91f03-115">Task</span></span>                                                                               | <span data-ttu-id="91f03-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91f03-116">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="91f03-117">Auswählen zwischen SNMP-Ereignis Anbietern</span><span class="sxs-lookup"><span data-stu-id="91f03-117">Choosing Between SNMP Event Providers</span></span>](choosing-between-snmp-event-providers.md) | <span data-ttu-id="91f03-118">WMI umfasst zwei SNMP-Ereignis Anbieter.</span><span class="sxs-lookup"><span data-stu-id="91f03-118">WMI includes two SNMP event providers.</span></span>                                             |
| [<span data-ttu-id="91f03-119">Empfangen von SNMP-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="91f03-119">Receiving SNMP Events</span></span>](receiving-snmp-events.md)                                 | <span data-ttu-id="91f03-120">SNMP-Ereignis Anbieter unterstützen drei Arten von SNMPv1 Traps und SNMPv2-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="91f03-120">SNMP event providers support three types of SNMPv1 traps and SNMPv2 notifications.</span></span> |



 

<span data-ttu-id="91f03-121">Im folgenden Beispiel wird ein Computer festgelegt, der für das **snmplinkupnotification** -Ereignis von einem verwalteten Hub überwacht werden soll.</span><span class="sxs-lookup"><span data-stu-id="91f03-121">The following example sets up a computer to monitor for the **SnmpLinkUpNotification** event from a managed hub.</span></span>


```VB
Set objLocator = CreateObject("wbemscripting.swbemlocator")
Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")

set objwbemEventsource = _ 
    objServices.ExecNotificationQuery _
   ("SELECT * FROM SnmpLinkUpNotification")

set objWbemObject = objwbemEventsource.NextEvent()

wscript.echo "Received " & objWbemObject.path_.class

for each prop in objWbemObject.properties_
    wscript.echo prop.name & " -- " & prop.value
next
```



 

 



