---
description: Das Objekt "slibemeventsource" ruft Ereignisse aus einer Ereignis Abfrage in Verbindung mit SWbemServices.Execnotificationquery ab.
ms.assetid: 7efd5e6a-4311-4d20-8b05-e9208eec098a
ms.tgt_platform: multiple
title: Errbemeventsource-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 09/25/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource
- ISWbemEventSource
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8da55a7b6722c263fe9a3fb0af7a8db07d672e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348886"
---
# <a name="swbemeventsource-object"></a><span data-ttu-id="195f6-103">"Errbemeventsource"-Objekt</span><span class="sxs-lookup"><span data-stu-id="195f6-103">SWbemEventSource object</span></span>

<span data-ttu-id="195f6-104">Das Objekt " **slibemeventsource** " ruft Ereignisse aus einer Ereignis Abfrage in Verbindung mit [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md)ab.</span><span class="sxs-lookup"><span data-stu-id="195f6-104">The **SWbemEventSource** object retrieves events from an event query in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="195f6-105">Sie erhalten ein " **slibemeventsource** "-Objekt, wenn Sie **SWbemServices.Execnotificationquery** aufrufen, um eine Ereignis Abfrage durchführen.</span><span class="sxs-lookup"><span data-stu-id="195f6-105">You get an **SWbemEventSource** object if you make a call to **SWbemServices.ExecNotificationQuery** to make an event query.</span></span> <span data-ttu-id="195f6-106">Sie können dann die [**NextEvent**](swbemeventsource-nextevent.md) -Methode verwenden, um Ereignisse abzurufen, sobald sie eintreffen.</span><span class="sxs-lookup"><span data-stu-id="195f6-106">You can then use the [**NextEvent**](swbemeventsource-nextevent.md) method to retrieve events as they arrive.</span></span> <span data-ttu-id="195f6-107">Dieses Objekt kann nicht durch den VBScript-Befehl "up- [Object](/previous-versions//xzysf6hc(v=vs.85)) " erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="195f6-107">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

## <a name="members"></a><span data-ttu-id="195f6-108">Member</span><span class="sxs-lookup"><span data-stu-id="195f6-108">Members</span></span>

<span data-ttu-id="195f6-109">Das Objekt " **errbemeventsource** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="195f6-109">The **SWbemEventSource** object has these types of members:</span></span>

-   [<span data-ttu-id="195f6-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="195f6-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="195f6-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="195f6-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="195f6-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="195f6-112">Methods</span></span>

<span data-ttu-id="195f6-113">Das Objekt " **errbemeventsource** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="195f6-113">The **SWbemEventSource** object has these methods.</span></span>



| <span data-ttu-id="195f6-114">Methode</span><span class="sxs-lookup"><span data-stu-id="195f6-114">Method</span></span>                                          | <span data-ttu-id="195f6-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="195f6-115">Description</span></span>                                                                                                                                  |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="195f6-116">**NextEvent**</span><span class="sxs-lookup"><span data-stu-id="195f6-116">**NextEvent**</span></span>](swbemeventsource-nextevent.md) | <span data-ttu-id="195f6-117">Wird zum Abrufen eines Ereignisses in Verbindung mit [**SWbemServices.Execnotificationquery**](swbemservices-execnotificationquery.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="195f6-117">Used to retrieve an event in conjunction with [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="195f6-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="195f6-118">Properties</span></span>

<span data-ttu-id="195f6-119">Das Objekt " **errbemeventsource** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="195f6-119">The **SWbemEventSource** object has these properties.</span></span>



| <span data-ttu-id="195f6-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="195f6-120">Property</span></span>                                                    | <span data-ttu-id="195f6-121">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="195f6-121">Access type</span></span>          | <span data-ttu-id="195f6-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="195f6-122">Description</span></span>                                              |
|:------------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="195f6-123">**Sicherheit\_**</span><span class="sxs-lookup"><span data-stu-id="195f6-123">**Security\_**</span></span>](swbemeventsource-security-.md)<br/> | <span data-ttu-id="195f6-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="195f6-124">Read-only</span></span><br/> | <span data-ttu-id="195f6-125">Wird verwendet, um die Sicherheitseinstellungen zu lesen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="195f6-125">Used to read or change the security settings.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="195f6-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="195f6-126">Examples</span></span>

<span data-ttu-id="195f6-127">Dieses Skript verwendet die Methoden der Klasse " **errbemeventsource** " und die Klasse " [**Swap Services**](swbemservices.md) " in Verbindung mit einer WQL-Abfrage für Anwendungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="195f6-127">This script uses the methods of the **SWbemEventSource** class and the [**SWbemServices**](swbemservices.md) class in conjunction with a WQL query for application events.</span></span> <span data-ttu-id="195f6-128">Weitere Informationen zur WMI-Ereignis Benachrichtigung und zu Abfragen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md), [Ausführen eines Skripts auf der Grundlage eines Ereignisses](running-a-script-based-on-an-event.md)und [empfangen von asynchronen Ereignis Benachrichtigungen](receiving-asynchronous-event-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="195f6-128">For more information about WMI event notification and queries see [Monitoring Events](monitoring-events.md), [Running a Script Based on an Event](running-a-script-based-on-an-event.md), and [Receiving Asynchronous Event Notifications](receiving-asynchronous-event-notifications.md).</span></span>


```VB
' Connect to WMI, obtaining an SWbemServices object
set svc = _
CreateObject("Wbemscripting.SWbemLocator")._
   ConnectServer(,"root\cimv2")

' Obtain an SWbemEventSource object from the 
' SWbemServices.ExecNotificationQuery method to specify the 
' event source as "Application" events in a Win32_NTLogEvent
set evtsrc = svc.ExecNotificationQuery("SELECT * " _
   & "FROM __InstanceCreationEvent " _
   & "WHERE TargetInstance ISA 'Win32_NTLogEvent'" _
   & "AND TargetInstance.Logfile ='Application'")

' Wait for an event by executing the NextEvent method on the 
' SWbemEventSource object.
while (num < 5)
    set inst = evtsrc.NextEvent(-1)
    Wscript.echo inst.TargetInstance.Logfile
    num = num + 1
wend
```



## <a name="requirements"></a><span data-ttu-id="195f6-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="195f6-129">Requirements</span></span>



| <span data-ttu-id="195f6-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="195f6-130">Requirement</span></span> | <span data-ttu-id="195f6-131">Wert</span><span class="sxs-lookup"><span data-stu-id="195f6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="195f6-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="195f6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="195f6-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="195f6-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="195f6-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="195f6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="195f6-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="195f6-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="195f6-136">Header</span><span class="sxs-lookup"><span data-stu-id="195f6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="195f6-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="195f6-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="195f6-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="195f6-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="195f6-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="195f6-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="195f6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="195f6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="195f6-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="195f6-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="195f6-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="195f6-142">CLSID</span></span><br/>                    | <span data-ttu-id="195f6-143">CLSID-austauschen von " \_ errbemeventsource"</span><span class="sxs-lookup"><span data-stu-id="195f6-143">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="195f6-144">IID</span><span class="sxs-lookup"><span data-stu-id="195f6-144">IID</span></span><br/>                      | <span data-ttu-id="195f6-145">IID \_ iswbemeventsource</span><span class="sxs-lookup"><span data-stu-id="195f6-145">IID\_ISWbemEventSource</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="195f6-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="195f6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="195f6-147">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="195f6-147">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

