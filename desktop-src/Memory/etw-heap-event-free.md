---
description: Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap freien Vorgang.
ms.assetid: 0CCC59F1-AB96-4B7A-9A86-19CA4FBA4A8A
title: ETW_HEAP_EVENT_FREE-Ereignis (ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_FREE
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: fd30eccb5848917d752441df79881078dc14d36e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862427"
---
# <a name="etw_heap_event_free-event"></a><span data-ttu-id="04165-103">\_ \_ Ereignis \_ freies Ereignis für etw-Heap</span><span class="sxs-lookup"><span data-stu-id="04165-103">ETW\_HEAP\_EVENT\_FREE event</span></span>

<span data-ttu-id="04165-104">Das Ereignis **\_ \_ \_ freie Ereignis "etw-Heap** " ist ein Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap-Free-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="04165-104">The **ETW\_HEAP\_EVENT\_FREE** event is a memory management tracing event for a heap free operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_FREE
```



## <a name="parameters"></a><span data-ttu-id="04165-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="04165-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04165-106">*Heaphandle*</span><span class="sxs-lookup"><span data-stu-id="04165-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="04165-107">Das Handle des Heaps, dem der Arbeitsspeicher zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="04165-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="04165-108">Dies ist der Heap, mit dem eine APP an die Funktion " [**zugewiescateheap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) " übermittelt wurde, als der Arbeitsspeicher belegt wurde.</span><span class="sxs-lookup"><span data-stu-id="04165-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="04165-109">*Adresse*</span><span class="sxs-lookup"><span data-stu-id="04165-109">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="04165-110">Die Adresse des freigegebenen Speichers.</span><span class="sxs-lookup"><span data-stu-id="04165-110">The address of the memory that was freed.</span></span>

</dd> <dt>

<span data-ttu-id="04165-111">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="04165-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="04165-112">Die Quelle des Speichers, der von der Zuweisung für die Heap Zuordnung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="04165-112">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="04165-113">In der folgenden Tabelle sind die möglichen Werte für den *Quell* Parameter aufgeführt, die in der *ntetw. h* -Header Datei definiert sind:</span><span class="sxs-lookup"><span data-stu-id="04165-113">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="04165-114">Wert</span><span class="sxs-lookup"><span data-stu-id="04165-114">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="04165-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="04165-115">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="04165-116">Arbeits <dt>**Speicher \_ Von \_ Lookaside**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="04165-116"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="04165-117">Arbeitsspeicher aus der Lookaside-Liste.</span><span class="sxs-lookup"><span data-stu-id="04165-117">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="04165-118">Arbeits <dt>**Speicher \_ Aus \_ lowfrag**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="04165-118"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="04165-119">Arbeitsspeicher vom Heap mit niedriger Fragmentierung.</span><span class="sxs-lookup"><span data-stu-id="04165-119">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="04165-120">Arbeits <dt>**Speicher \_ Aus \_ mainpath**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="04165-120"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="04165-121">Arbeitsspeicher vom Hauptcodepfad.</span><span class="sxs-lookup"><span data-stu-id="04165-121">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="04165-122">Arbeits <dt> **Speicher \_ von \_ slowpath**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="04165-122"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="04165-123">Arbeitsspeicher von langsamer c.</span><span class="sxs-lookup"><span data-stu-id="04165-123">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="04165-124">Arbeits <dt>**Speicher \_ Aus \_ ungültigem**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="04165-124"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="04165-125">Ungültiger Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="04165-125">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="04165-126">Arbeits <dt>**Speicher \_ Aus \_ Segment \_ Heap**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="04165-126"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="04165-127">Dieser Wert ist für die zukünftige Verwendung reserviert und wird nie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="04165-127">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04165-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04165-128">Remarks</span></span>

<span data-ttu-id="04165-129">Das Ereignis freie Ereignis " **etw- \_ Heap \_ Ereignis \_** " wird bei allen Heap freien Vorgängen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="04165-129">The **ETW\_HEAP\_EVENT\_FREE** event is logged on all heap free operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="04165-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04165-130">Requirements</span></span>



| <span data-ttu-id="04165-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04165-131">Requirement</span></span> | <span data-ttu-id="04165-132">Wert</span><span class="sxs-lookup"><span data-stu-id="04165-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04165-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04165-133">Minimum supported client</span></span><br/> | <span data-ttu-id="04165-134">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04165-134">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="04165-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04165-135">Minimum supported server</span></span><br/> | <span data-ttu-id="04165-136">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04165-136">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="04165-137">Header</span><span class="sxs-lookup"><span data-stu-id="04165-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="04165-138"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="04165-138"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04165-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04165-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04165-140">Ablauf Verfolgungs Ereignisse für die Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="04165-140">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
