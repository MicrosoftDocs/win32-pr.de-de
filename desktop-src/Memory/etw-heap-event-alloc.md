---
description: Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap Zuordnungs Vorgang.
ms.assetid: 572DEC3B-F909-45E5-849F-707AA62F2F5E
title: ETW_HEAP_EVENT_ALLOC-Ereignis (ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_ALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 57e09ed1785f31b6203c526f2b6d42cc4815a266
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343619"
---
# <a name="etw_heap_event_alloc-event"></a><span data-ttu-id="ec5c6-103">Ereignis für etw- \_ Heap \_ Ereignis \_ Zuweisung</span><span class="sxs-lookup"><span data-stu-id="ec5c6-103">ETW\_HEAP\_EVENT\_ALLOC event</span></span>

<span data-ttu-id="ec5c6-104">Das Ereignis **\_ \_ \_ Zuweisungs Ereignis für das ETW-Heap Ereignis** ist ein Ablauf Verfolgungs Ereignis der Speicherverwaltung für einen Heap Zuordnungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-104">The **ETW\_HEAP\_EVENT\_ALLOC** event is a memory management tracing event for a heap allocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_ALLOC
```



## <a name="parameters"></a><span data-ttu-id="ec5c6-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec5c6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec5c6-106">*Heaphandle*</span><span class="sxs-lookup"><span data-stu-id="ec5c6-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5c6-107">Das Handle des Heaps, dem der Arbeitsspeicher zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="ec5c6-108">Dies ist der Heap, mit dem eine APP an die Funktion " [**zugewiescateheap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) " übermittelt wurde, als der Arbeitsspeicher belegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="ec5c6-109">*Größe*</span><span class="sxs-lookup"><span data-stu-id="ec5c6-109">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5c6-110">Die Größe in Bytes, die vom Heap zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-110">The size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="ec5c6-111">*Adresse*</span><span class="sxs-lookup"><span data-stu-id="ec5c6-111">*Address*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5c6-112">Die Adresse des zugeordneten Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-112">The address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="ec5c6-113">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="ec5c6-113">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5c6-114">Die Quelle des Speichers, der von der Zuweisung für die Heap Zuordnung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-114">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="ec5c6-115">In der folgenden Tabelle sind die möglichen Werte für den *Quell* Parameter aufgeführt, die in der *ntetw. h* -Header Datei definiert sind:</span><span class="sxs-lookup"><span data-stu-id="ec5c6-115">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="ec5c6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ec5c6-116">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="ec5c6-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ec5c6-117">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="ec5c6-118">Arbeits <dt>**Speicher \_ Von \_ Lookaside**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ec5c6-118"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="ec5c6-119">Arbeitsspeicher aus der Lookaside-Liste.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-119">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="ec5c6-120">Arbeits <dt>**Speicher \_ Aus \_ lowfrag**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ec5c6-120"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="ec5c6-121">Arbeitsspeicher vom Heap mit niedriger Fragmentierung.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-121">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="ec5c6-122">Arbeits <dt>**Speicher \_ Aus \_ mainpath**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ec5c6-122"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="ec5c6-123">Arbeitsspeicher vom Hauptcodepfad.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-123">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="ec5c6-124">Arbeits <dt> **Speicher \_ von \_ slowpath**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ec5c6-124"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="ec5c6-125">Der Arbeitsspeicher von einem langsamen Pfad.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-125">Memory from slow path.</span></span><br/>                                            |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="ec5c6-126">Arbeits <dt>**Speicher \_ Aus \_ ungültigem**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ec5c6-126"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="ec5c6-127">Ungültiger Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-127">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="ec5c6-128">Arbeits <dt>**Speicher \_ Aus \_ Segment \_ Heap**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ec5c6-128"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="ec5c6-129">Dieser Wert ist für die zukünftige Verwendung reserviert und wird nie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-129">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec5c6-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec5c6-130">Remarks</span></span>

<span data-ttu-id="ec5c6-131">Das Ereignis Zuordnungs Ereignis für den etw-Heap wird bei allen Heap **\_ \_ \_ Zuordnungen** protokolliert.</span><span class="sxs-lookup"><span data-stu-id="ec5c6-131">The **ETW\_HEAP\_EVENT\_ALLOC** event is logged on all heap allocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec5c6-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec5c6-132">Requirements</span></span>



| <span data-ttu-id="ec5c6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec5c6-133">Requirement</span></span> | <span data-ttu-id="ec5c6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="ec5c6-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec5c6-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ec5c6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ec5c6-136">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec5c6-136">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ec5c6-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ec5c6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ec5c6-138">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ec5c6-138">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ec5c6-139">Header</span><span class="sxs-lookup"><span data-stu-id="ec5c6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec5c6-140"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec5c6-140"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec5c6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec5c6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5c6-142">Ablauf Verfolgungs Ereignisse für die Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="ec5c6-142">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
