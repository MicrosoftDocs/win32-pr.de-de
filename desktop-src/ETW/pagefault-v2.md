---
description: Diese Klasse ist die übergeordnete Klasse für Seiten Fehlerereignisse. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: cc349e75-fe81-427e-8cf9-15c76e8e4dad
title: PageFault_V2-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PageFault_V2
api_type:
- NA
api_location: ''
ms.openlocfilehash: a545e8ae7c5afb000c26d89d9359f620fa7a653d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977640"
---
# <a name="pagefault_v2-class"></a><span data-ttu-id="fd12e-104">Pagefault \_ v2-Klasse</span><span class="sxs-lookup"><span data-stu-id="fd12e-104">PageFault\_V2 class</span></span>

<span data-ttu-id="fd12e-105">Diese Klasse ist die übergeordnete Klasse für Seiten Fehlerereignisse.</span><span class="sxs-lookup"><span data-stu-id="fd12e-105">This class is the parent class for page fault events.</span></span>

<span data-ttu-id="fd12e-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="fd12e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd12e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd12e-107">Syntax</span></span>

``` syntax
[Guid("{3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c}"), EventVersion(2)]
class PageFault_V2 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="fd12e-108">Member</span><span class="sxs-lookup"><span data-stu-id="fd12e-108">Members</span></span>

<span data-ttu-id="fd12e-109">Die **Pagefault \_ v2** -Klasse definiert keine Member.</span><span class="sxs-lookup"><span data-stu-id="fd12e-109">The **PageFault\_V2** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd12e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd12e-110">Remarks</span></span>

<span data-ttu-id="fd12e-111">Wenn Sie alle Seiten Fehlerereignisse in einer NT-Kernel Protokollierungs Sitzung aktivieren möchten, geben Sie das Flag für das **Ereignis Ablaufverfolgungsflag \_ \_ \_ Speicher \_ Seiten \_ Fehler** im **enableflags** -Member einer [**Ereignis Ablauf \_ Verfolgungs \_ Eigenschaften**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) -Struktur beim Aufrufen der [**starttrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="fd12e-111">To enable all page fault events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_MEMORY\_PAGE\_FAULTS** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span> <span data-ttu-id="fd12e-112">Sie können auch die folgenden Flags angeben:</span><span class="sxs-lookup"><span data-stu-id="fd12e-112">You can also specify the following flags:</span></span>

-   <span data-ttu-id="fd12e-113">**Ereignis Ablauf \_ Verfolgung Flag für Arbeits \_ \_ Speicher \_ \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="fd12e-113">**EVENT\_TRACE\_FLAG\_MEMORY\_HARD\_FAULTS**</span></span>
-   <span data-ttu-id="fd12e-114">**Ereignis \_ Ablaufverfolgungs- \_ Flag \_ virtuelle \_ Zuweisung**</span><span class="sxs-lookup"><span data-stu-id="fd12e-114">**EVENT\_TRACE\_FLAG\_VIRTUAL\_ALLOC**</span></span>

<span data-ttu-id="fd12e-115">Ereignisablaufverfolgungs-Consumer können eine spezielle Verarbeitung für alle Seiten Fehlerereignisse implementieren, indem Sie die Funktion [**settracecallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) aufrufen und [**pagefehlerguid**](nt-kernel-logger-constants.md) als *pguid* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="fd12e-115">Event trace consumers can implement special processing for all page fault events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**PageFaultGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="fd12e-116">Verwenden Sie die folgenden Ereignis Typen, um das tatsächliche Speicher Ereignis zu identifizieren, wenn Ereignisse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd12e-116">Use the following event types to identify the actual memory event when consuming events.</span></span>



| <span data-ttu-id="fd12e-117">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="fd12e-117">Event type</span></span>                                                     | <span data-ttu-id="fd12e-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd12e-118">Description</span></span>                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd12e-119">Ereignis \_ Ablaufverfolgungstyp \_ \_ mm \_ Kuh (Ereignistyp Wert ist 12)</span><span class="sxs-lookup"><span data-stu-id="fd12e-119">EVENT\_TRACE\_TYPE\_MM\_COW(Event type value is 12)</span></span><br/> | <span data-ttu-id="fd12e-120">Copy-on-Write-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-120">Copy-on-write event.</span></span> <span data-ttu-id="fd12e-121">Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-121">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="fd12e-122">Vor Windows Vista definiert die [**Pagefault \_ transitionfault**](pagefault-transitionfault.md) -MOF-Klasse das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-122">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>     |
| <span data-ttu-id="fd12e-123">Ereignis \_ Ablaufverfolgungstyp \_ \_ mm \_ DZF (Ereignistyp Wert ist 11)</span><span class="sxs-lookup"><span data-stu-id="fd12e-123">EVENT\_TRACE\_TYPE\_MM\_DZF(Event type value is 11)</span></span><br/> | <span data-ttu-id="fd12e-124">Fehler Ereignis nach Bedarf NULL.</span><span class="sxs-lookup"><span data-stu-id="fd12e-124">Demand zero fault event.</span></span> <span data-ttu-id="fd12e-125">Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-125">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="fd12e-126">Vor Windows Vista definiert die [**Pagefault \_ transitionfault**](pagefault-transitionfault.md) -MOF-Klasse das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-126">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span> |
| <span data-ttu-id="fd12e-127">Ereignis \_ Ablaufverfolgungstyp \_ \_ mm \_ GPF (Ereignistyp Wert ist 13)</span><span class="sxs-lookup"><span data-stu-id="fd12e-127">EVENT\_TRACE\_TYPE\_MM\_GPF(Event type value is 13)</span></span><br/> | <span data-ttu-id="fd12e-128">Fehler Ereignis der Guard-Seite.</span><span class="sxs-lookup"><span data-stu-id="fd12e-128">Guard page fault event.</span></span> <span data-ttu-id="fd12e-129">Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-129">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="fd12e-130">Vor Windows Vista definiert die [**Pagefault \_ transitionfault**](pagefault-transitionfault.md) -MOF-Klasse das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-130">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="fd12e-131">Ereignis \_ Ablaufverfolgungstyp \_ \_ mm \_ HPF (Ereignistyp Wert ist 14)</span><span class="sxs-lookup"><span data-stu-id="fd12e-131">EVENT\_TRACE\_TYPE\_MM\_HPF(Event type value is 14)</span></span><br/> | <span data-ttu-id="fd12e-132">Hartes Seiten Fehler Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-132">Hard page fault event.</span></span> <span data-ttu-id="fd12e-133">Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-133">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="fd12e-134">Vor Windows Vista definiert die [**Pagefault \_ transitionfault**](pagefault-transitionfault.md) -MOF-Klasse das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-134">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>   |
| <span data-ttu-id="fd12e-135">Ereignis Ablauf \_ Verfolgungs \_ Typ \_ mm \_ tf (Ereignistyp Wert ist 10)</span><span class="sxs-lookup"><span data-stu-id="fd12e-135">EVENT\_TRACE\_TYPE\_MM\_TF(Event type value is 10)</span></span><br/>  | <span data-ttu-id="fd12e-136">Übergangs Fehler Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-136">Transition fault event.</span></span> <span data-ttu-id="fd12e-137">Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-137">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span> <span data-ttu-id="fd12e-138">Vor Windows Vista definiert die [**Pagefault \_ transitionfault**](pagefault-transitionfault.md) -MOF-Klasse das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-138">Prior to Windows Vista, the [**PageFault\_TransitionFault**](pagefault-transitionfault.md) MOF class defines the event.</span></span>  |
| <span data-ttu-id="fd12e-139">Ereignis Ablauf \_ Verfolgungs \_ Typ \_ mm \_ AV (Ereignistyp Wert ist 15)</span><span class="sxs-lookup"><span data-stu-id="fd12e-139">EVENT\_TRACE\_TYPE\_MM\_AV(Event type value is 15)</span></span><br/>  | <span data-ttu-id="fd12e-140">Zugriffs Verletzungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-140">Access violation event.</span></span> <span data-ttu-id="fd12e-141">Die [**Pagefault \_ TypeGroup1**](pagefault-typegroup1.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-141">The [**PageFault\_TypeGroup1**](pagefault-typegroup1.md) MOF class defines the event data for this event.</span></span>                                                                                                                           |
| <span data-ttu-id="fd12e-142">Ereignistyp Wert, 32</span><span class="sxs-lookup"><span data-stu-id="fd12e-142">Event type value, 32</span></span>                                           | <span data-ttu-id="fd12e-143">Hartes Seiten Fehler Ereignis. Die " [**Pagefault \_ Hardfault**](pagefault-hardfault.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-143">Hard page fault event.The [**PageFault\_HardFault**](pagefault-hardfault.md) MOF class defines the event data for this event.</span></span>                                                                                                                               |
| <span data-ttu-id="fd12e-144">Ereignistyp Wert, 105</span><span class="sxs-lookup"><span data-stu-id="fd12e-144">Event type value, 105</span></span>                                          | <span data-ttu-id="fd12e-145">Bild Ladevorgang in Auslagerungs Datei Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-145">Image load in page file event.</span></span> <span data-ttu-id="fd12e-146">Die [**Pagefault \_ imageloadbacked**](pagefault-imageloadbacked.md) MOF-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-146">The [**PageFault\_ImageLoadBacked**](pagefault-imageloadbacked.md) MOF class defines the event data for this event.</span></span>                                                                                                          |
| <span data-ttu-id="fd12e-147">Ereignistyp Wert, 98</span><span class="sxs-lookup"><span data-stu-id="fd12e-147">Event type value, 98</span></span>                                           | <span data-ttu-id="fd12e-148">Virtuelles Zuordnungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-148">Virtual allocation event.</span></span> <span data-ttu-id="fd12e-149">Die " [**virtualzuweisung**](pagefault-virtualalloc.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-149">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                |
| <span data-ttu-id="fd12e-150">Ereignistyp Wert, 99</span><span class="sxs-lookup"><span data-stu-id="fd12e-150">Event type value, 99</span></span>                                           | <span data-ttu-id="fd12e-151">Virtuelles kostenloses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-151">Virtual free event.</span></span> <span data-ttu-id="fd12e-152">Die " [**virtualzuweisung**](pagefault-virtualalloc.md) MOF"-Klasse definiert die Ereignisdaten für dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="fd12e-152">The [**VirtualAlloc**](pagefault-virtualalloc.md) MOF class defines the event data for this event.</span></span>                                                                                                                                      |



 

<span data-ttu-id="fd12e-153">Sie können den **ProcessID** -und den **ThreadId** -Member des [**Ereignis Ablauf \_ Verfolgungs \_ Headers**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) verwenden, um den fehlerhaften Prozess oder Thread zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fd12e-153">You can use the **ProcessId** and **ThreadId** members of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) to identify the faulting process or thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd12e-154">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fd12e-154">Requirements</span></span>



| <span data-ttu-id="fd12e-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd12e-155">Requirement</span></span> | <span data-ttu-id="fd12e-156">Wert</span><span class="sxs-lookup"><span data-stu-id="fd12e-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fd12e-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd12e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="fd12e-158">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd12e-158">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fd12e-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd12e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="fd12e-160">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd12e-160">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
