---
description: Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap-neuzuordnungs Vorgang.
ms.assetid: D8080B7B-CECC-40DB-B52A-2C3E4F04ABA9
title: ETW_HEAP_EVENT_REALLOC-Ereignis (ntwmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ETW_HEAP_EVENT_REALLOC
api_type:
- HeaderDef
api_location:
- ntwmi.h
ms.openlocfilehash: 7aec225793967c38b97fecae88d28141e48a3cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351667"
---
# <a name="etw_heap_event_realloc-event"></a><span data-ttu-id="2cbc8-103">Ereignis zur \_ \_ \_ erneuten Zuweisung von etw-Heap Ereignissen</span><span class="sxs-lookup"><span data-stu-id="2cbc8-103">ETW\_HEAP\_EVENT\_REALLOC event</span></span>

<span data-ttu-id="2cbc8-104">Das Ereignis **\_ \_ \_ realloc für das ETW-Heap Ereignis** ist ein Ablauf Verfolgungs Ereignis für die Speicherverwaltung für einen Heap-neuzuordnungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-104">The **ETW\_HEAP\_EVENT\_REALLOC** event is a memory management tracing event for a heap reallocation operation.</span></span>


```C++
typedef struct ETW_HEAP_EVENT_REALLOC
```



## <a name="parameters"></a><span data-ttu-id="2cbc8-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cbc8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cbc8-106">*Heaphandle*</span><span class="sxs-lookup"><span data-stu-id="2cbc8-106">*HeapHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="2cbc8-107">Das Handle des Heaps, dem der Arbeitsspeicher zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-107">The handle of the heap where the memory was allocated.</span></span> <span data-ttu-id="2cbc8-108">Dies ist der Heap, mit dem eine APP an die Funktion " [**zugewiescateheap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) " übermittelt wurde, als der Arbeitsspeicher belegt wurde.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-108">This is the heap handle an app passed to the [**AllocateHeap**](/previous-versions/windows/desktop/legacy/aa374721(v=vs.85)) function when the memory was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="2cbc8-109">*NewAddress*</span><span class="sxs-lookup"><span data-stu-id="2cbc8-109">*NewAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="2cbc8-110">Die neue Adresse des zugewiesenen Speichers.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-110">The new address of the memory that was allocated.</span></span>

</dd> <dt>

<span data-ttu-id="2cbc8-111">*Oldaddress*</span><span class="sxs-lookup"><span data-stu-id="2cbc8-111">*OldAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="2cbc8-112">Die alte Adresse des zuvor zugewiesenen Speichers.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-112">The old address of the memory that was previously allocated.</span></span>

</dd> <dt>

<span data-ttu-id="2cbc8-113">*NewSize*</span><span class="sxs-lookup"><span data-stu-id="2cbc8-113">*NewSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2cbc8-114">Die neue Größe in Bytes, die vom Heap zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-114">The new size in bytes allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="2cbc8-115">*OldSize*</span><span class="sxs-lookup"><span data-stu-id="2cbc8-115">*OldSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2cbc8-116">Die alte Größe in Bytes, die zuvor vom Heap zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-116">The old size in bytes previously allocated from the heap.</span></span>

</dd> <dt>

<span data-ttu-id="2cbc8-117">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="2cbc8-117">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="2cbc8-118">Die Quelle des Speichers, der von der Zuweisung für die Heap Zuordnung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-118">The source of the memory that the allocator used for the heap allocation.</span></span>

<span data-ttu-id="2cbc8-119">In der folgenden Tabelle sind die möglichen Werte für den *Quell* Parameter aufgeführt, die in der *ntetw. h* -Header Datei definiert sind:</span><span class="sxs-lookup"><span data-stu-id="2cbc8-119">The following table lists the possible values for the *Source* parameter as defined in the *ntetw.h* header file:</span></span>



| <span data-ttu-id="2cbc8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2cbc8-120">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="2cbc8-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2cbc8-121">Meaning</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="MEMORY_FROM_LOOKASIDE"></span><span id="memory_from_lookaside"></span><dl> <span data-ttu-id="2cbc8-122">Arbeits <dt>**Speicher \_ Von \_ Lookaside**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc8-122"><dt>**MEMORY\_FROM\_LOOKASIDE**</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="2cbc8-123">Arbeitsspeicher aus der Lookaside-Liste.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-123">Memory from the lookaside list.</span></span><br/>                                   |
| <span id="MEMORY_FROM_LOWFRAG"></span><span id="memory_from_lowfrag"></span><dl> <span data-ttu-id="2cbc8-124">Arbeits <dt>**Speicher \_ Aus \_ lowfrag**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc8-124"><dt>**MEMORY\_FROM\_LOWFRAG**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="2cbc8-125">Arbeitsspeicher vom Heap mit niedriger Fragmentierung.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-125">Memory from the low-fragmentation heap.</span></span><br/>                           |
| <span id="MEMORY_FROM_MAINPATH"></span><span id="memory_from_mainpath"></span><dl> <span data-ttu-id="2cbc8-126">Arbeits <dt>**Speicher \_ Aus \_ mainpath**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc8-126"><dt>**MEMORY\_FROM\_MAINPATH**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="2cbc8-127">Arbeitsspeicher vom Hauptcodepfad.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-127">Memory from main code path.</span></span><br/>                                       |
| <span id="MEMORY_FROM_SLOWPATH____________________"></span><span id="memory_from_slowpath____________________"></span><dl> <span data-ttu-id="2cbc8-128">Arbeits <dt> **Speicher \_ von \_ slowpath**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc8-128"><dt>**MEMORY\_FROM\_SLOWPATH** </dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="2cbc8-129">Arbeitsspeicher von langsamer c.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-129">Memory from slow c.</span></span><br/>                                               |
| <span id="MEMORY_FROM_INVALID"></span><span id="memory_from_invalid"></span><dl> <span data-ttu-id="2cbc8-130">Arbeits <dt>**Speicher \_ Aus \_ ungültigem**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc8-130"><dt>**MEMORY\_FROM\_INVALID**</dt> <dt>5</dt></span></span> </dl>                                             | <span data-ttu-id="2cbc8-131">Ungültiger Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-131">Memory that was not valid.</span></span><br/>                                        |
| <span id="MEMORY_FROM_SEGMENT_HEAP"></span><span id="memory_from_segment_heap"></span><dl> <span data-ttu-id="2cbc8-132">Arbeits <dt>**Speicher \_ Aus \_ Segment \_ Heap**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc8-132"><dt>**MEMORY\_FROM\_SEGMENT\_HEAP**</dt> <dt>6</dt></span></span> </dl>                             | <span data-ttu-id="2cbc8-133">Dieser Wert ist für die zukünftige Verwendung reserviert und wird nie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-133">This value is reserved for future use and will never be returned.</span></span><br/> |



 

</dd> </dl>

<span data-ttu-id="2cbc8-134">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-134">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cbc8-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cbc8-135">Remarks</span></span>

<span data-ttu-id="2cbc8-136">Das Ereignis **\_ \_ \_ realloc für das ETW-Heap Ereignis** wird bei allen Heap Zuordnungen protokolliert.</span><span class="sxs-lookup"><span data-stu-id="2cbc8-136">The **ETW\_HEAP\_EVENT\_REALLOC** event is logged on all heap reallocations.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cbc8-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cbc8-137">Requirements</span></span>



| <span data-ttu-id="2cbc8-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cbc8-138">Requirement</span></span> | <span data-ttu-id="2cbc8-139">Wert</span><span class="sxs-lookup"><span data-stu-id="2cbc8-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2cbc8-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2cbc8-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2cbc8-141">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cbc8-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2cbc8-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2cbc8-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2cbc8-143">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2cbc8-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="2cbc8-144">Header</span><span class="sxs-lookup"><span data-stu-id="2cbc8-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cbc8-145"><dt>Ntwmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cbc8-145"><dt>Ntwmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cbc8-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cbc8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbc8-147">Ablauf Verfolgungs Ereignisse für die Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="2cbc8-147">Memory Management Tracing Events</span></span>](memory-management-tracing-events.md)
</dt> </dl>

 

 
