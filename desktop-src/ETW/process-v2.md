---
description: Diese Klasse ist die übergeordnete Klasse für Prozess Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: c055dc1f78da13c0dfa29bea948a8f0c94363ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960489"
---
# <a name="process_v2-class"></a><span data-ttu-id="f5953-104">Process \_ v2-Klasse</span><span class="sxs-lookup"><span data-stu-id="f5953-104">Process\_V2 class</span></span>

<span data-ttu-id="f5953-105">Diese Klasse ist die übergeordnete Klasse für Prozess Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f5953-105">This class is the parent class for process events.</span></span>

<span data-ttu-id="f5953-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="f5953-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5953-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5953-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class Process_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="f5953-108">Member</span><span class="sxs-lookup"><span data-stu-id="f5953-108">Members</span></span>

<span data-ttu-id="f5953-109">Die **Process** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="f5953-109">The **Process** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5953-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5953-110">Remarks</span></span>

<span data-ttu-id="f5953-111">Um Prozess Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das Ablaufverfolgungsflag für die **Ereignis \_ \_ \_ Ablauf Verfolgung** im **enableflags** -Member einer Eigenschaften Struktur der [**Ereignis Ablauf \_ Verfolgung \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="f5953-111">To enable process events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_PROCESS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="f5953-112">Sie können auch das folgende Flag angeben:</span><span class="sxs-lookup"><span data-stu-id="f5953-112">You can also specify the following flag:</span></span>

-   <span data-ttu-id="f5953-113">**Prozessindikatoren für die Ereignis \_ \_ \_ Ablauf Verfolgung \_**</span><span class="sxs-lookup"><span data-stu-id="f5953-113">**EVENT\_TRACE\_FLAG\_PROCESS\_COUNTERS**</span></span>

<span data-ttu-id="f5953-114">Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für Prozess Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**ProcessGuid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="f5953-114">Event trace consumers can implement special processing for process events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ProcessGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="f5953-115">Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Prozess Ereignis beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f5953-115">Use the following event types to identify the actual process event when consuming events.</span></span>



| <span data-ttu-id="f5953-116">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="f5953-116">Event type</span></span>                                                      | <span data-ttu-id="f5953-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5953-117">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5953-118">**Ereignis \_ Ablaufverfolgungstyp \_ \_ Ende**(Ereignistyp Wert ist 2)</span><span class="sxs-lookup"><span data-stu-id="f5953-118">**EVENT\_TRACE\_TYPE\_END**(Event type value is 2)</span></span><br/>   | <span data-ttu-id="f5953-119">Prozess Ereignis beenden.</span><span class="sxs-lookup"><span data-stu-id="f5953-119">End process event.</span></span> <span data-ttu-id="f5953-120">Die " [**Process \_ TypeGroup1**](process-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5953-120">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="f5953-121">**Ereignis \_ \_ \_ Start** Ablaufverfolgungstyp (Ereignistyp Wert ist 1)</span><span class="sxs-lookup"><span data-stu-id="f5953-121">**EVENT\_TRACE\_TYPE\_START**(Event type value is 1)</span></span><br/> | <span data-ttu-id="f5953-122">Prozess Ereignis starten.</span><span class="sxs-lookup"><span data-stu-id="f5953-122">Start process event.</span></span> <span data-ttu-id="f5953-123">Die " [**Process \_ TypeGroup1**](process-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5953-123">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                        |
| <span data-ttu-id="f5953-124">Ereignistyp Wert, 3</span><span class="sxs-lookup"><span data-stu-id="f5953-124">Event type value, 3</span></span>                                             | <span data-ttu-id="f5953-125">Ereignis zum Starten der Daten Sammlungs Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="f5953-125">Start data collection process event.</span></span> <span data-ttu-id="f5953-126">Listet die Prozesse auf, die derzeit zum Zeitpunkt des Starts der Kernel Sitzung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f5953-126">Enumerates processes that are currently running at the time the kernel session starts.</span></span> <span data-ttu-id="f5953-127">Die " [**Process \_ TypeGroup1**](process-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5953-127">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="f5953-128">Wert für Ereignistyp, 4</span><span class="sxs-lookup"><span data-stu-id="f5953-128">Event type value, 4</span></span>                                             | <span data-ttu-id="f5953-129">Ereignis für Daten Sammlungs Prozess beenden.</span><span class="sxs-lookup"><span data-stu-id="f5953-129">End data collection process event.</span></span> <span data-ttu-id="f5953-130">Listet Prozesse auf, die zurzeit ausgeführt werden, wenn die Kernel Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f5953-130">Enumerates processes that are currently running at the time the kernel session ends.</span></span> <span data-ttu-id="f5953-131">Die " [**Process \_ TypeGroup1**](process-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5953-131">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>     |
| <span data-ttu-id="f5953-132">Ereignistyp Wert, 32</span><span class="sxs-lookup"><span data-stu-id="f5953-132">Event type value, 32</span></span>                                            | <span data-ttu-id="f5953-133">Leistungsindikator Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5953-133">Performance counters event.</span></span> <span data-ttu-id="f5953-134">Die [**Process \_ v2 \_ TypeGroup2**](process-v2-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5953-134">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                                                          |
| <span data-ttu-id="f5953-135">Ereignistyp Wert, 33</span><span class="sxs-lookup"><span data-stu-id="f5953-135">Event type value, 33</span></span>                                            | <span data-ttu-id="f5953-136">Rundown der Leistungsindikatoren zu Beginn der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f5953-136">Rundown of the performance counters at the start of the session.</span></span> <span data-ttu-id="f5953-137">Die [**Process \_ v2 \_ TypeGroup2**](process-v2-typegroup2.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5953-137">The [**Process\_V2\_TypeGroup2**](process-v2-typegroup2.md) MOF class defines the event data for this event.</span></span>                                                     |
| <span data-ttu-id="f5953-138">Ereignistyp Wert, 39</span><span class="sxs-lookup"><span data-stu-id="f5953-138">Event type value, 39</span></span>                                            | <span data-ttu-id="f5953-139">Defunct-Prozess Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5953-139">Defunct process event.</span></span> <span data-ttu-id="f5953-140">Die " [**Process \_ TypeGroup1**](process-typegroup1.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5953-140">The [**Process\_TypeGroup1**](process-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                      |



 

<span data-ttu-id="f5953-141">Prozess-und Thread Start Ereignisse können im Kontext des übergeordneten Prozesses oder Threads protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="f5953-141">Process and thread start events may be logged in the context of the parent process or thread.</span></span> <span data-ttu-id="f5953-142">Folglich entsprechen die **ProcessID** -und **ThreadId** -Member des [**Ereignis Ablauf \_ Verfolgungs \_ Headers**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) möglicherweise nicht dem Prozess und dem Thread, der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f5953-142">As a result, the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) may not correspond to the process and thread being created.</span></span> <span data-ttu-id="f5953-143">Aus diesem Grund enthalten diese Ereignisse die Prozess-und Thread Bezeichner in den Ereignisdaten (zusätzlich zu den in der Ereignis Kopfzeile).</span><span class="sxs-lookup"><span data-stu-id="f5953-143">This is why these events contain the process and thread identifiers in the event data (in addition to those in the event header).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5953-144">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f5953-144">Requirements</span></span>



| <span data-ttu-id="f5953-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5953-145">Requirement</span></span> | <span data-ttu-id="f5953-146">Wert</span><span class="sxs-lookup"><span data-stu-id="f5953-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f5953-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5953-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f5953-148">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f5953-148">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>       |
| <span data-ttu-id="f5953-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5953-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f5953-150">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="f5953-150">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5953-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f5953-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5953-152">**MSNT \_ systemtrace**</span><span class="sxs-lookup"><span data-stu-id="f5953-152">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="f5953-153">**Prozess**</span><span class="sxs-lookup"><span data-stu-id="f5953-153">**Process**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="f5953-154">**Prozess \_ TypeGroup1**</span><span class="sxs-lookup"><span data-stu-id="f5953-154">**Process\_TypeGroup1**</span></span>](process-typegroup1.md)
</dt> <dt>

[<span data-ttu-id="f5953-155">**Prozess \_ v0**</span><span class="sxs-lookup"><span data-stu-id="f5953-155">**Process\_V0**</span></span>](process-v0.md)
</dt> <dt>

[<span data-ttu-id="f5953-156">**Prozess \_ v1**</span><span class="sxs-lookup"><span data-stu-id="f5953-156">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 
