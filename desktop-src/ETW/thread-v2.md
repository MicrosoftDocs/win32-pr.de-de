---
description: Diese Klasse ist die übergeordnete Klasse für Thread Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 63e52cba-42a5-44f0-8eb6-e1bac8414a83
title: Thread_V2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: f28b68a2aac5f2d5293f94ed2bab366d238ae662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866124"
---
# <a name="thread_v2-class"></a><span data-ttu-id="0a613-104">Thread \_ v2-Klasse</span><span class="sxs-lookup"><span data-stu-id="0a613-104">Thread\_V2 class</span></span>

<span data-ttu-id="0a613-105">Diese Klasse ist die übergeordnete Klasse für Thread Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="0a613-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="0a613-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="0a613-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a613-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a613-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="0a613-108">Member</span><span class="sxs-lookup"><span data-stu-id="0a613-108">Members</span></span>

<span data-ttu-id="0a613-109">Die **Thread \_ v2** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="0a613-109">The **Thread\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a613-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a613-110">Remarks</span></span>

<span data-ttu-id="0a613-111">Um Thread Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das **ereignisablaufverfolgungsflag \_ \_ \_ Thread** -Flag im **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="0a613-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="0a613-112">Sie können auch die folgenden Flags angeben:</span><span class="sxs-lookup"><span data-stu-id="0a613-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="0a613-113">**Ereignis \_ Ablaufverfolgungsflag \_ \_ cswitch**</span><span class="sxs-lookup"><span data-stu-id="0a613-113">**EVENT\_TRACE\_FLAG\_CSWITCH**</span></span>
-   <span data-ttu-id="0a613-114">**Ablaufverfolgungsflag-Verteiler \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a613-114">**EVENT\_TRACE\_FLAG\_DISPATCHER**</span></span>

<span data-ttu-id="0a613-115">Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Thread Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**threadguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="0a613-115">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="0a613-116">Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Thread Ereignis zu identifizieren, wenn Ereignisse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a613-116">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="0a613-117">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="0a613-117">Event type</span></span>                                                      | <span data-ttu-id="0a613-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0a613-118">Description</span></span>                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a613-119">**Ereignis \_ Ablaufverfolgungstyp \_ \_ Ende**(Ereignistyp Wert ist 2)</span><span class="sxs-lookup"><span data-stu-id="0a613-119">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="0a613-120">End Thread Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a613-120">End thread event.</span></span> <span data-ttu-id="0a613-121">Die [**Thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a613-121">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="0a613-122">**Ereignis \_ \_ \_ Start** Ablaufverfolgungstyp (Ereignistyp Wert ist 1)</span><span class="sxs-lookup"><span data-stu-id="0a613-122">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="0a613-123">Starten Sie das Thread Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a613-123">Start thread event.</span></span> <span data-ttu-id="0a613-124">Die [**Thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a613-124">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="0a613-125">Ereignistyp Wert, 3</span><span class="sxs-lookup"><span data-stu-id="0a613-125">Event type value, 3</span></span>                                             | <span data-ttu-id="0a613-126">Ereignis für Daten Sammlungs Thread starten.</span><span class="sxs-lookup"><span data-stu-id="0a613-126">Start data collection thread event.</span></span> <span data-ttu-id="0a613-127">Listet Threads auf, die derzeit zum Zeitpunkt des Starts der Kernel Sitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0a613-127">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="0a613-128">Die [**Thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a613-128">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="0a613-129">Wert für Ereignistyp, 4</span><span class="sxs-lookup"><span data-stu-id="0a613-129">Event type value, 4</span></span>                                             | <span data-ttu-id="0a613-130">Ereignis zum Beenden der Daten Sammlungs Thread.</span><span class="sxs-lookup"><span data-stu-id="0a613-130">End data collection thread event.</span></span> <span data-ttu-id="0a613-131">Listet Threads auf, die zurzeit ausgeführt werden, wenn die Kernel Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0a613-131">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="0a613-132">Die [**Thread \_ v2 \_ TypeGroup1**](thread-v2-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a613-132">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="0a613-133">Ereignistyp Wert, 36</span><span class="sxs-lookup"><span data-stu-id="0a613-133">Event type value, 36</span></span>                                            | <span data-ttu-id="0a613-134">Kontextwechsel Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a613-134">Context switch event.</span></span> <span data-ttu-id="0a613-135">Die [**cswitch**](cswitch.md) -MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a613-135">The [**CSwitch**](cswitch.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="0a613-136">Ereignistyp Wert, 50</span><span class="sxs-lookup"><span data-stu-id="0a613-136">Event type value, 50</span></span>                                            | <span data-ttu-id="0a613-137">Fertiges Thread Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a613-137">Ready thread event.</span></span> <span data-ttu-id="0a613-138">Die " [**leserythread**](readythread.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0a613-138">The [**ReadyThread**](readythread.md) MOF class defines the event data for this event.</span></span>                                                                                                                          |



 

<span data-ttu-id="0a613-139">Prozess-und Thread Start Ereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="0a613-139">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="0a613-140">Folglich entsprechen die **ProcessID** -und **ThreadId** -Member des [**Ereignis Ablauf \_ Verfolgungs \_ Headers**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und dem Thread, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0a613-140">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="0a613-141">Aus diesem Grund enthalten diese Ereignisse die Prozess-und Thread Bezeichner in den Ereignisdaten (zusätzlich zu den in der Ereignis Kopfzeile).</span><span class="sxs-lookup"><span data-stu-id="0a613-141">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a613-142">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0a613-142">Requirements</span></span>



| <span data-ttu-id="0a613-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a613-143">Requirement</span></span> | <span data-ttu-id="0a613-144">Wert</span><span class="sxs-lookup"><span data-stu-id="0a613-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0a613-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a613-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0a613-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a613-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0a613-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a613-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0a613-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a613-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a613-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0a613-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a613-150">**MSNT \_ systemtrace**</span><span class="sxs-lookup"><span data-stu-id="0a613-150">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="0a613-151">**Cswitch**</span><span class="sxs-lookup"><span data-stu-id="0a613-151">**CSwitch**</span></span>](cswitch.md)
</dt> <dt>

[<span data-ttu-id="0a613-152">**Aden**</span><span class="sxs-lookup"><span data-stu-id="0a613-152">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="0a613-153">**Thread \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="0a613-153">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="0a613-154">**Thread \_ v0**</span><span class="sxs-lookup"><span data-stu-id="0a613-154">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="0a613-155">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="0a613-155">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 
