---
description: 'Process-Klasse: Diese Klasse ist die übergeordnete Klasse für Prozessereignisse. Die folgende Syntax wird aus MOF-Code vereinfacht.'
ms.assetid: a505c693-2169-499b-bd32-42fa9bd69d2f
title: Process-Klasse
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
ms.openlocfilehash: 8085bae0d00ebe830efff420744f6b7e9b4bf23c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106268"
---
# <a name="process-class"></a><span data-ttu-id="013ee-104">Process-Klasse</span><span class="sxs-lookup"><span data-stu-id="013ee-104">Process class</span></span>

<span data-ttu-id="013ee-105">Diese Klasse ist die übergeordnete Klasse für Prozessereignisse.</span><span class="sxs-lookup"><span data-stu-id="013ee-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="013ee-106">Die folgende Syntax wird aus MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="013ee-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="013ee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="013ee-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Process : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="013ee-108">Member</span><span class="sxs-lookup"><span data-stu-id="013ee-108">Members</span></span>

<span data-ttu-id="013ee-109">Die **Process-Klasse** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="013ee-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="013ee-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="013ee-110">Remarks</span></span>

<span data-ttu-id="013ee-111">Um Prozessereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **EVENT TRACE FLAG \_ \_ \_ PROCESS-Flag** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.</span><span class="sxs-lookup"><span data-stu-id="013ee-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="013ee-112">Sie können auch das folgende Flag angeben:</span><span class="sxs-lookup"><span data-stu-id="013ee-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="013ee-113">**\_ \_ \_ \_ EREIGNISABLAUFVERFOLGUNGSFLAG-PROZESSINDIKATOREN**</span><span class="sxs-lookup"><span data-stu-id="013ee-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="013ee-114">Consumer der Ereignisablaufverfolgung können eine spezielle Verarbeitung für Prozessereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**ProcessGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="013ee-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="013ee-115">Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Prozessereignis beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="013ee-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="013ee-116">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="013ee-116">Event type</span></span>                                                      | <span data-ttu-id="013ee-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="013ee-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="013ee-118">**EVENT \_ TRACE \_ TYPE \_ END**(Ereignistypwert ist 2)</span><span class="sxs-lookup"><span data-stu-id="013ee-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="013ee-119">Endprozessereignis.</span><span class="sxs-lookup"><span data-stu-id="013ee-119">End process event.</span></span> <span data-ttu-id="013ee-120">Die [**Process \_ TypeGroup1**](process-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="013ee-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="013ee-121">**EVENT \_ TRACE \_ TYPE \_ START**(Ereignistypwert ist 1)</span><span class="sxs-lookup"><span data-stu-id="013ee-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="013ee-122">Startprozessereignis.</span><span class="sxs-lookup"><span data-stu-id="013ee-122">Start process event.</span></span> <span data-ttu-id="013ee-123">Die [**Process \_ TypeGroup1**](process-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="013ee-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="013ee-124">Ereignistypwert, 3</span><span class="sxs-lookup"><span data-stu-id="013ee-124">Event type value, 3</span></span>                                             | <span data-ttu-id="013ee-125">Starten sie das Datensammlungsprozessereignis.</span><span class="sxs-lookup"><span data-stu-id="013ee-125">Start data collection process event.</span></span> <span data-ttu-id="013ee-126">Aufzählen von Prozessen, die derzeit zum Zeitpunkt des Starts der Kernelsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="013ee-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="013ee-127">Die [**\_ MOF-Klasse Process TypeGroup1**](process-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="013ee-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="013ee-128">Ereignistypwert, 4</span><span class="sxs-lookup"><span data-stu-id="013ee-128">Event type value, 4</span></span>                                             | <span data-ttu-id="013ee-129">Beenden des Datensammlungsprozess-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="013ee-129">End data collection process event.</span></span> <span data-ttu-id="013ee-130">Aufzählen von Prozessen, die derzeit zum Zeitpunkt des Beendens der Kernelsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="013ee-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="013ee-131">Die [**\_ MOF-Klasse Process TypeGroup1**](process-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="013ee-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="013ee-132">Prozess- und Threadstartereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="013ee-132">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="013ee-133">Daher entsprechen die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und Thread, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="013ee-133">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="013ee-134">Aus diesem Grund enthalten diese Ereignisse die Prozess- und Threadbezeichner in den Ereignisdaten (zusätzlich zu den im Ereignisheader).</span><span class="sxs-lookup"><span data-stu-id="013ee-134">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="013ee-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="013ee-135">Requirements</span></span>



| <span data-ttu-id="013ee-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="013ee-136">Requirement</span></span> | <span data-ttu-id="013ee-137">Wert</span><span class="sxs-lookup"><span data-stu-id="013ee-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="013ee-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="013ee-138">Minimum supported client</span></span><br/> | <span data-ttu-id="013ee-139">Windows \[ Vista-Desktop-Apps \| UWP-Apps\]</span><span class="sxs-lookup"><span data-stu-id="013ee-139">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="013ee-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="013ee-140">Minimum supported server</span></span><br/> | <span data-ttu-id="013ee-141">UWP-Apps für Windows Server \[ 2008-Desktop-Apps \|\]</span><span class="sxs-lookup"><span data-stu-id="013ee-141">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="013ee-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="013ee-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="013ee-143">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="013ee-143">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="013ee-144">**Process \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="013ee-144">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="013ee-145">**Verarbeiten \_ von V0**</span><span class="sxs-lookup"><span data-stu-id="013ee-145">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="013ee-146">**Prozess \_ V1**</span><span class="sxs-lookup"><span data-stu-id="013ee-146">**Process\_V1**</span></span>](process-v1.md)
</dt> <dt>

[<span data-ttu-id="013ee-147">**Prozess \_ V2**</span><span class="sxs-lookup"><span data-stu-id="013ee-147">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 
