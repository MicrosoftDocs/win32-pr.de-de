---
description: 'Thread_V2 Klasse: Diese Klasse ist die übergeordnete Klasse für Threadereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
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
ms.openlocfilehash: b00067af61a55e61f70b0c799a1512edf284f11c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105618"
---
# <a name="thread_v2-class"></a><span data-ttu-id="1eb31-104">Thread \_ V2-Klasse</span><span class="sxs-lookup"><span data-stu-id="1eb31-104">Thread\_V2 class</span></span>

<span data-ttu-id="1eb31-105">Diese Klasse ist die übergeordnete Klasse für Threadereignisse.</span><span class="sxs-lookup"><span data-stu-id="1eb31-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="1eb31-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="1eb31-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb31-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1eb31-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Thread_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="1eb31-108">Member</span><span class="sxs-lookup"><span data-stu-id="1eb31-108">Members</span></span>

<span data-ttu-id="1eb31-109">Die **Thread \_ V2-Klasse** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="1eb31-109">The **Thread\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eb31-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1eb31-110">Remarks</span></span>

<span data-ttu-id="1eb31-111">Um Threadereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG \_ \_ \_ THREAD** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.</span><span class="sxs-lookup"><span data-stu-id="1eb31-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="1eb31-112">Sie können auch die folgenden Flags angeben:</span><span class="sxs-lookup"><span data-stu-id="1eb31-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="1eb31-113">**\_ \_ EREIGNIS-ABLAUFVERFOLGUNGSFLAG \_ CSWITCH**</span><span class="sxs-lookup"><span data-stu-id="1eb31-113">**EVENT\_TRACE\_FLAG\_CSWITCH**</span></span>
-   <span data-ttu-id="1eb31-114">**\_ \_ EREIGNISVERFOLGUNGSFLAG \_ DISPATCHER**</span><span class="sxs-lookup"><span data-stu-id="1eb31-114">**EVENT\_TRACE\_FLAG\_DISPATCHER**</span></span>

<span data-ttu-id="1eb31-115">Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Threadereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**ThreadGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="1eb31-115">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="1eb31-116">Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Threadereignis beim Verwenden von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1eb31-116">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="1eb31-117">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="1eb31-117">Event type</span></span>                                                      | <span data-ttu-id="1eb31-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1eb31-118">Description</span></span>                                                                                                                                                                                                                          |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb31-119">**EVENT \_ TRACE \_ TYPE \_ END**(Ereignistypwert ist 2)</span><span class="sxs-lookup"><span data-stu-id="1eb31-119">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="1eb31-120">Endthreadereignis.</span><span class="sxs-lookup"><span data-stu-id="1eb31-120">End thread event.</span></span> <span data-ttu-id="1eb31-121">Die [**\_ MOF-Klasse Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1eb31-121">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="1eb31-122">**EVENT \_ TRACE \_ TYPE \_ START**(Ereignistypwert ist 1)</span><span class="sxs-lookup"><span data-stu-id="1eb31-122">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="1eb31-123">Threadereignis starten.</span><span class="sxs-lookup"><span data-stu-id="1eb31-123">Start thread event.</span></span> <span data-ttu-id="1eb31-124">Die [**\_ MOF-Klasse Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1eb31-124">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="1eb31-125">Ereignistypwert, 3</span><span class="sxs-lookup"><span data-stu-id="1eb31-125">Event type value, 3</span></span>                                             | <span data-ttu-id="1eb31-126">Starten des Datensammlungsthread-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="1eb31-126">Start data collection thread event.</span></span> <span data-ttu-id="1eb31-127">Aufzählen von Threads, die derzeit zum Zeitpunkt des Starts der Kernelsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1eb31-127">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="1eb31-128">Die [**\_ MOF-Klasse Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1eb31-128">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="1eb31-129">Ereignistypwert, 4</span><span class="sxs-lookup"><span data-stu-id="1eb31-129">Event type value, 4</span></span>                                             | <span data-ttu-id="1eb31-130">Enddatensammlungsthreadereignis.</span><span class="sxs-lookup"><span data-stu-id="1eb31-130">End data collection thread event.</span></span> <span data-ttu-id="1eb31-131">Aufzählen von Threads, die derzeit zum Zeitpunkt des Beendens der Kernelsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1eb31-131">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="1eb31-132">Die [**\_ MOF-Klasse Thread V2 \_ TypeGroup1**](thread-v2-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1eb31-132">The [**Thread\_V2\_TypeGroup1**](thread-v2-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="1eb31-133">Ereignistypwert, 36</span><span class="sxs-lookup"><span data-stu-id="1eb31-133">Event type value, 36</span></span>                                            | <span data-ttu-id="1eb31-134">Kontextwechselereignis.</span><span class="sxs-lookup"><span data-stu-id="1eb31-134">Context switch event.</span></span> <span data-ttu-id="1eb31-135">Die [**MOF-Klasse CSwitch**](cswitch.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1eb31-135">The [**CSwitch**](cswitch.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="1eb31-136">Ereignistypwert, 50</span><span class="sxs-lookup"><span data-stu-id="1eb31-136">Event type value, 50</span></span>                                            | <span data-ttu-id="1eb31-137">Ready-Threadereignis.</span><span class="sxs-lookup"><span data-stu-id="1eb31-137">Ready thread event.</span></span> <span data-ttu-id="1eb31-138">Die [](readythread.md) ReadyThread-MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="1eb31-138">The [**ReadyThread**](readythread.md) MOF class defines the event data for this event.</span></span>                                                                                                                          |



 

<span data-ttu-id="1eb31-139">Prozess- und Threadstartereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="1eb31-139">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="1eb31-140">Daher entsprechen die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und Thread, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1eb31-140">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="1eb31-141">Aus diesem Grund enthalten diese Ereignisse die Prozess- und Threadbezeichner in den Ereignisdaten (zusätzlich zu den im Ereignisheader).</span><span class="sxs-lookup"><span data-stu-id="1eb31-141">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb31-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1eb31-142">Requirements</span></span>



| <span data-ttu-id="1eb31-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1eb31-143">Requirement</span></span> | <span data-ttu-id="1eb31-144">Wert</span><span class="sxs-lookup"><span data-stu-id="1eb31-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1eb31-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1eb31-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb31-146">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1eb31-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1eb31-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1eb31-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb31-148">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1eb31-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1eb31-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1eb31-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb31-150">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="1eb31-150">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="1eb31-151">**CSwitch**</span><span class="sxs-lookup"><span data-stu-id="1eb31-151">**CSwitch**</span></span>](cswitch.md)
</dt> <dt>

[<span data-ttu-id="1eb31-152">**Thread**</span><span class="sxs-lookup"><span data-stu-id="1eb31-152">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="1eb31-153">**\_ThreadtypGruppe1**</span><span class="sxs-lookup"><span data-stu-id="1eb31-153">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="1eb31-154">**Thread \_ V0**</span><span class="sxs-lookup"><span data-stu-id="1eb31-154">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="1eb31-155">**Thread \_ V1**</span><span class="sxs-lookup"><span data-stu-id="1eb31-155">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 
