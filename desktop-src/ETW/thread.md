---
description: 'Threadklasse: Diese Klasse ist die übergeordnete Klasse für Threadereignisse. Die folgende Syntax wird durch MOF-Code vereinfacht.'
ms.assetid: 0bf14240-3b8d-4eb5-b751-7b2e23b55762
title: Thread-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread
api_type:
- NA
api_location: ''
ms.openlocfilehash: 121a8d4aa04017011648d80329ee02396582987a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105528"
---
# <a name="thread-class"></a><span data-ttu-id="69f48-104">Thread-Klasse</span><span class="sxs-lookup"><span data-stu-id="69f48-104">Thread class</span></span>

<span data-ttu-id="69f48-105">Diese Klasse ist die übergeordnete Klasse für Threadereignisse.</span><span class="sxs-lookup"><span data-stu-id="69f48-105">This class is the parent class for thread events.</span></span>

<span data-ttu-id="69f48-106">Die folgende Syntax wird durch MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="69f48-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f48-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="69f48-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(3)]
class Thread : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="69f48-108">Member</span><span class="sxs-lookup"><span data-stu-id="69f48-108">Members</span></span>

<span data-ttu-id="69f48-109">Die **Thread-Klasse** definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="69f48-109">The **Thread** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="69f48-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69f48-110">Remarks</span></span>

<span data-ttu-id="69f48-111">Um Threadereignisse in einer NT-Kernelprotokollierungssitzung zu aktivieren, geben Sie beim Aufrufen der [**StartTrace-Funktion**](/windows/win32/api/evntrace/nf-evntrace-starttracea) das **FLAG EVENT TRACE FLAG \_ \_ \_ THREAD** im **EnableFlags-Member** einer [**EVENT TRACE \_ \_ PROPERTIES-Struktur**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) an.</span><span class="sxs-lookup"><span data-stu-id="69f48-111">To enable thread events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_THREAD** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="69f48-112">Ereignisverfolgungsverbraucher können eine spezielle Verarbeitung für Threadereignisse implementieren, indem sie die [**SetTraceCallback-Funktion**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**ThreadGuid**](nt-kernel-logger-constants.md) als *pGuid-Parameter* angeben.</span><span class="sxs-lookup"><span data-stu-id="69f48-112">Event trace consumers can implement special processing for thread events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ThreadGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="69f48-113">Verwenden Sie die folgenden Ereignistypen, um das tatsächliche Threadereignis beim Verwenden von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="69f48-113">Use the following event types to identify the actual thread event when consuming events.</span></span>



| <span data-ttu-id="69f48-114">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="69f48-114">Event type</span></span>                                                      | <span data-ttu-id="69f48-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69f48-115">Description</span></span>                                                                                                                                                                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69f48-116">**EVENT \_ TRACE \_ TYPE \_ END**(Ereignistypwert ist 2)</span><span class="sxs-lookup"><span data-stu-id="69f48-116">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="69f48-117">Endthreadereignis.</span><span class="sxs-lookup"><span data-stu-id="69f48-117">End thread event.</span></span> <span data-ttu-id="69f48-118">Die [**\_ MOF-Klasse Thread TypeGroup1**](thread-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="69f48-118">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="69f48-119">**EVENT \_ TRACE \_ TYPE \_ START**(Ereignistypwert ist 1)</span><span class="sxs-lookup"><span data-stu-id="69f48-119">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="69f48-120">Threadereignis starten.</span><span class="sxs-lookup"><span data-stu-id="69f48-120">Start thread event.</span></span> <span data-ttu-id="69f48-121">Die [**\_ MOF-Klasse Thread TypeGroup1**](thread-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="69f48-121">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |
| <span data-ttu-id="69f48-122">Ereignistypwert, 3</span><span class="sxs-lookup"><span data-stu-id="69f48-122">Event type value, 3</span></span>                                             | <span data-ttu-id="69f48-123">Starten des Datensammlungsthread-Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="69f48-123">Start data collection thread event.</span></span> <span data-ttu-id="69f48-124">Aufzählen von Threads, die derzeit zum Zeitpunkt des Starts der Kernelsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="69f48-124">Enumerates threads that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="69f48-125">Die [**\_ MOF-Klasse Thread TypeGroup1**](thread-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="69f48-125">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="69f48-126">Ereignistypwert, 4</span><span class="sxs-lookup"><span data-stu-id="69f48-126">Event type value, 4</span></span>                                             | <span data-ttu-id="69f48-127">Enddatensammlungsthreadereignis.</span><span class="sxs-lookup"><span data-stu-id="69f48-127">End data collection thread event.</span></span> <span data-ttu-id="69f48-128">Listet Threads auf, die derzeit zum Zeitpunkt des Beendens der Kernelsitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="69f48-128">Enumerates threads that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="69f48-129">Die [**MOF-Klasse Thread \_ TypeGroup1**](thread-typegroup1.md) definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="69f48-129">The [**Thread\_TypeGroup1**](thread-typegroup1.md) MOF class defines the event data for this event.</span></span>     |



 

<span data-ttu-id="69f48-130">Prozess- und Threadstartereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="69f48-130">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="69f48-131">Daher entsprechen die **ProcessId-** und **ThreadId-Member** von [**EVENT TRACE \_ \_ HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und Thread, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="69f48-131">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="69f48-132">Aus diesem Grund enthalten diese Ereignisse die Prozess- und Threadbezeichner in den Ereignisdaten (zusätzlich zu denen im Ereignisheader).</span><span class="sxs-lookup"><span data-stu-id="69f48-132">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="69f48-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69f48-133">Requirements</span></span>



| <span data-ttu-id="69f48-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69f48-134">Requirement</span></span> | <span data-ttu-id="69f48-135">Wert</span><span class="sxs-lookup"><span data-stu-id="69f48-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="69f48-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69f48-136">Minimum supported client</span></span><br/> | <span data-ttu-id="69f48-137">Nur Windows \[ Vista-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69f48-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="69f48-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69f48-138">Minimum supported server</span></span><br/> | <span data-ttu-id="69f48-139">Nur Windows Server \[ 2008-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69f48-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="69f48-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="69f48-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f48-141">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="69f48-141">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="69f48-142">**\_ThreadtypGruppe1**</span><span class="sxs-lookup"><span data-stu-id="69f48-142">**Thread\_TypeGroup1**</span></span>](thread-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="69f48-143">**Thread \_ V0**</span><span class="sxs-lookup"><span data-stu-id="69f48-143">**Thread\_V0**</span></span>](thread-v0.md)
</dt> <dt>

[<span data-ttu-id="69f48-144">**Thread \_ V1**</span><span class="sxs-lookup"><span data-stu-id="69f48-144">**Thread\_V1**</span></span>](thread-v1.md)
</dt> <dt>

[<span data-ttu-id="69f48-145">**Thread \_ V2**</span><span class="sxs-lookup"><span data-stu-id="69f48-145">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 
