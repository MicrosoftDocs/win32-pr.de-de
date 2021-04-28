---
description: 'Process_V2-Klasse: Diese Klasse ist die übergeordnete Klasse für Prozessereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
ms.assetid: 75596278-43cc-4040-a43d-6958d0935b68
title: Process_V2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process
api_type:
- NA
api_location: ''
ms.openlocfilehash: 77d700e7847d0ad19a019985a4e19343ce8f383d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106298"
---
# <a name="process_v2-class"></a><span data-ttu-id="0277c-104">Process \_ V2-Klasse</span><span class="sxs-lookup"><span data-stu-id="0277c-104">Process\_V2 class</span></span>

<span data-ttu-id="0277c-105">Diese Klasse ist die übergeordnete Klasse für Prozessereignisse.</span><span class="sxs-lookup"><span data-stu-id="0277c-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="0277c-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="0277c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0277c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0277c-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="0277c-108">Member</span><span class="sxs-lookup"><span data-stu-id="0277c-108">Members</span></span>

<span data-ttu-id="0277c-109">Die **Process-Klasse** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="0277c-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="0277c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0277c-110">Remarks</span></span>

<span data-ttu-id="0277c-111">Um Prozessereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **EVENT TRACE FLAG \_ \_ \_ PROCESS-Flag** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.</span><span class="sxs-lookup"><span data-stu-id="0277c-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="0277c-112">Sie können auch das folgende Flag angeben:</span><span class="sxs-lookup"><span data-stu-id="0277c-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="0277c-113">**\_ \_ \_ \_ EREIGNISABLAUFVERFOLGUNGSFLAG-PROZESSINDIKATOREN**</span><span class="sxs-lookup"><span data-stu-id="0277c-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="0277c-114">Consumer der Ereignisablaufverfolgung können eine spezielle Verarbeitung für Prozessereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**ProcessGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="0277c-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="0277c-115">Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Prozessereignis beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0277c-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="0277c-116">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="0277c-116">Event type</span></span>                                                      | <span data-ttu-id="0277c-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0277c-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0277c-118">**EVENT \_ TRACE \_ TYPE \_ END**(Ereignistypwert ist 2)</span><span class="sxs-lookup"><span data-stu-id="0277c-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="0277c-119">Endprozessereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-119">End process event.</span></span> <span data-ttu-id="0277c-120">Die [**Process \_ TypeGroup1**](process-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="0277c-121">**EVENT \_ TRACE \_ TYPE \_ START**(Ereignistypwert ist 1)</span><span class="sxs-lookup"><span data-stu-id="0277c-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="0277c-122">Startprozessereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-122">Start process event.</span></span> <span data-ttu-id="0277c-123">Die [**Process \_ TypeGroup1**](process-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="0277c-124">Ereignistypwert, 3</span><span class="sxs-lookup"><span data-stu-id="0277c-124">Event type value, 3</span></span>                                             | <span data-ttu-id="0277c-125">Starten sie das Datensammlungsprozessereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-125">Start data collection process event.</span></span> <span data-ttu-id="0277c-126">Aufzählen von Prozessen, die derzeit zum Zeitpunkt des Starts der Kernelsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0277c-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="0277c-127">Die [**\_ MOF-Klasse Process TypeGroup1**](process-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="0277c-128">Ereignistypwert, 4</span><span class="sxs-lookup"><span data-stu-id="0277c-128">Event type value, 4</span></span>                                             | <span data-ttu-id="0277c-129">Beenden des Datensammlungsprozess-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="0277c-129">End data collection process event.</span></span> <span data-ttu-id="0277c-130">Aufzählen von Prozessen, die derzeit zum Zeitpunkt des Beendens der Kernelsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0277c-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="0277c-131">Die [**\_ MOF-Klasse Process TypeGroup1**](process-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="0277c-132">Ereignistypwert, 32</span><span class="sxs-lookup"><span data-stu-id="0277c-132">Event type value, 32</span></span>                                            | <span data-ttu-id="0277c-133">Leistungsindikatorereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-133">Performance counters event.</span></span> <span data-ttu-id="0277c-134">Die [**\_ MOF-Klasse \_ Process V2 TypeGroup2**](process-v2-typegroup2.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-134">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                                                          |
| <span data-ttu-id="0277c-135">Ereignistypwert, 33</span><span class="sxs-lookup"><span data-stu-id="0277c-135">Event type value, 33</span></span>                                            | <span data-ttu-id="0277c-136">Rundown der Leistungsindikatoren zu Beginn der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0277c-136">Rundown of the performance counters at the start of the session.</span></span> <span data-ttu-id="0277c-137">Die [**\_ MOF-Klasse \_ Process V2 TypeGroup2**](process-v2-typegroup2.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-137">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                     |
| <span data-ttu-id="0277c-138">Ereignistypwert, 39</span><span class="sxs-lookup"><span data-stu-id="0277c-138">Event type value, 39</span></span>                                            | <span data-ttu-id="0277c-139">Ereignis für den ablaufenden Prozess.</span><span class="sxs-lookup"><span data-stu-id="0277c-139">Defunct process event.</span></span> <span data-ttu-id="0277c-140">Die [**\_ MOF-Klasse Process TypeGroup1**](process-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0277c-140">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |



 

<span data-ttu-id="0277c-141">Prozess- und Threadstartereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="0277c-141">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="0277c-142">Daher entsprechen die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und Thread, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0277c-142">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="0277c-143">Aus diesem Grund enthalten diese Ereignisse die Prozess- und Threadbezeichner in den Ereignisdaten (zusätzlich zu den im Ereignisheader).</span><span class="sxs-lookup"><span data-stu-id="0277c-143">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="0277c-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0277c-144">Requirements</span></span>



| <span data-ttu-id="0277c-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0277c-145">Requirement</span></span> | <span data-ttu-id="0277c-146">Wert</span><span class="sxs-lookup"><span data-stu-id="0277c-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="0277c-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0277c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0277c-148">Windows \[ Vista-Desktop-Apps \| UWP-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0277c-148">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="0277c-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0277c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0277c-150">UWP-Apps für Windows Server \[ 2008-Desktop-Apps \|\]</span><span class="sxs-lookup"><span data-stu-id="0277c-150">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0277c-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0277c-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0277c-152">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="0277c-152">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="0277c-153">**Prozess**</span><span class="sxs-lookup"><span data-stu-id="0277c-153">**Process**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="0277c-154">**Process \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="0277c-154">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="0277c-155">**Verarbeiten \_ von V0**</span><span class="sxs-lookup"><span data-stu-id="0277c-155">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="0277c-156">**Prozess \_ V1**</span><span class="sxs-lookup"><span data-stu-id="0277c-156">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 
