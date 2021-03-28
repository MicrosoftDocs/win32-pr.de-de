---
description: Diese Klasse ist die übergeordnete Klasse für Leistungs Ereignis Ereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 2606fea3-0651-4f7f-83a6-63021039eb95
title: Perfinfo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PerfInfo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 93f12242fef86e5eab81bb702b783eb1f4c1915c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977705"
---
# <a name="perfinfo-class"></a><span data-ttu-id="a36d0-104">Perfinfo-Klasse</span><span class="sxs-lookup"><span data-stu-id="a36d0-104">PerfInfo class</span></span>

<span data-ttu-id="a36d0-105">Diese Klasse ist die übergeordnete Klasse für Leistungs Ereignis Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="a36d0-105">This class is the parent class for performance counter events.</span></span>

<span data-ttu-id="a36d0-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="a36d0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a36d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a36d0-107">Syntax</span></span>

``` syntax
[Guid("{ce1dbfb4-137e-4da6-87b0-3f59aa102cbc}"), EventVersion(2)]
class PerfInfo : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="a36d0-108">Member</span><span class="sxs-lookup"><span data-stu-id="a36d0-108">Members</span></span>

<span data-ttu-id="a36d0-109">Die **perfinfo** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="a36d0-109">The **PerfInfo** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="a36d0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a36d0-110">Remarks</span></span>

<span data-ttu-id="a36d0-111">Um DPC-Ereignisse in einer NT-Kernel Protokollierungs Sitzung zu aktivieren, geben Sie das **ereignisablaufverfolgungsflag \_ \_ \_ DPC** -Flag im **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="a36d0-111">To enable deferred procedure call (DPC) events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_DPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="a36d0-112">Sie können auch eines oder mehrere der folgenden Flags angeben:</span><span class="sxs-lookup"><span data-stu-id="a36d0-112">You can also specify one or more of the following flags:</span></span>

-   <span data-ttu-id="a36d0-113">**Flag für Ereignis Ablauf \_ Verfolgung \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a36d0-113">**EVENT\_TRACE\_FLAG\_INTERRUPT**</span></span>
-   <span data-ttu-id="a36d0-114">**Ereignis Ablauf \_ Verfolgungs \_ Flag- \_ Profil**</span><span class="sxs-lookup"><span data-stu-id="a36d0-114">**EVENT\_TRACE\_FLAG\_PROFILE**</span></span>
-   <span data-ttu-id="a36d0-115">**Ereignis \_ Ablaufverfolgungsflag \_ \_ systemrückruf**</span><span class="sxs-lookup"><span data-stu-id="a36d0-115">**EVENT\_TRACE\_FLAG\_SYSTEMCALL**</span></span>

<span data-ttu-id="a36d0-116">Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für DPC-Ereignisse implementieren, indem Sie die [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) -Funktion aufrufen und [**perfinfoguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="a36d0-116">Event trace consumers can implement special processing for DPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PerfInfoGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="a36d0-117">Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Ereignis beim Verarbeiten von Ereignissen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a36d0-117">Use the following event types to identify the actual event when consuming events.</span></span>



| <span data-ttu-id="a36d0-118">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="a36d0-118">Event type</span></span>           | <span data-ttu-id="a36d0-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a36d0-119">Description</span></span>                                                                                                          |
|----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a36d0-120">Ereignistyp Wert, 46</span><span class="sxs-lookup"><span data-stu-id="a36d0-120">Event type value, 46</span></span> | <span data-ttu-id="a36d0-121">Samplingprofilereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-121">Sampled profile event.</span></span> <span data-ttu-id="a36d0-122">Die [**sampledprofile**](sampledprofile.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-122">The [**SampledProfile**](sampledprofile.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="a36d0-123">Ereignistyp Wert, 51</span><span class="sxs-lookup"><span data-stu-id="a36d0-123">Event type value, 51</span></span> | <span data-ttu-id="a36d0-124">System Rückruf: Ereignis eingeben.</span><span class="sxs-lookup"><span data-stu-id="a36d0-124">System call enter event.</span></span> <span data-ttu-id="a36d0-125">Die " [**syscallenter**](syscallenter.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-125">The [**SysCallEnter**](syscallenter.md) MOF class defines the event data for this event.</span></span>   |
| <span data-ttu-id="a36d0-126">Ereignistyp Wert, 52</span><span class="sxs-lookup"><span data-stu-id="a36d0-126">Event type value, 52</span></span> | <span data-ttu-id="a36d0-127">Exit-Ereignis für System Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="a36d0-127">System call exit event.</span></span> <span data-ttu-id="a36d0-128">Die " [**syscallexit**](syscallexit.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-128">The [**SysCallExit**](syscallexit.md) MOF class defines the event data for this event.</span></span>      |
| <span data-ttu-id="a36d0-129">Ereignistyp Wert, 66</span><span class="sxs-lookup"><span data-stu-id="a36d0-129">Event type value, 66</span></span> | <span data-ttu-id="a36d0-130">Thread-DPC-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-130">Threaded DPC event.</span></span> <span data-ttu-id="a36d0-131">Die [**DPC**](dpc.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-131">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                          |
| <span data-ttu-id="a36d0-132">Ereignistyp Wert, 67</span><span class="sxs-lookup"><span data-stu-id="a36d0-132">Event type value, 67</span></span> | <span data-ttu-id="a36d0-133">ISR-Ereignis (Interrupt Service Routine).</span><span class="sxs-lookup"><span data-stu-id="a36d0-133">Interrupt service routine (ISR) event.</span></span> <span data-ttu-id="a36d0-134">Die [**ISR**](isr.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-134">The [**ISR**](isr.md) MOF class defines the event data for this event.</span></span>       |
| <span data-ttu-id="a36d0-135">Ereignistyp Wert, 68</span><span class="sxs-lookup"><span data-stu-id="a36d0-135">Event type value, 68</span></span> | <span data-ttu-id="a36d0-136">DPC-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-136">DPC event.</span></span> <span data-ttu-id="a36d0-137">Die [**DPC**](dpc.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-137">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                                   |
| <span data-ttu-id="a36d0-138">Ereignistyp Wert, 69</span><span class="sxs-lookup"><span data-stu-id="a36d0-138">Event type value, 69</span></span> | <span data-ttu-id="a36d0-139">DPC-Zeit Geber Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-139">DPC timer event.</span></span> <span data-ttu-id="a36d0-140">Die [**DPC**](dpc.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a36d0-140">The [**DPC**](dpc.md) MOF class defines the event data for this event.</span></span>                             |



 

## <a name="requirements"></a><span data-ttu-id="a36d0-141">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a36d0-141">Requirements</span></span>



| <span data-ttu-id="a36d0-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a36d0-142">Requirement</span></span> | <span data-ttu-id="a36d0-143">Wert</span><span class="sxs-lookup"><span data-stu-id="a36d0-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a36d0-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a36d0-144">Minimum supported client</span></span><br/> | <span data-ttu-id="a36d0-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a36d0-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a36d0-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a36d0-146">Minimum supported server</span></span><br/> | <span data-ttu-id="a36d0-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a36d0-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
