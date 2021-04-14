---
description: Gibt einen Speicherblock frei, der von einem Heap von rtlzucateheap zugewiesen wurde.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: RtlFreeHeap-Funktion (ntifs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523587"
---
# <a name="rtlfreeheap-function"></a><span data-ttu-id="c47ad-103">RtlFreeHeap-Funktion</span><span class="sxs-lookup"><span data-stu-id="c47ad-103">RtlFreeHeap function</span></span>

<span data-ttu-id="c47ad-104">Gibt einen Speicherblock frei, der von einem Heap von [**rtlzucateheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="c47ad-104">Frees a memory block that was allocated from a heap by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

## <a name="syntax"></a><span data-ttu-id="c47ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c47ad-105">Syntax</span></span>


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a><span data-ttu-id="c47ad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c47ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c47ad-107">*Heaphandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c47ad-107">*HeapHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c47ad-108">Ein Handle für den Heap, dessen Speicherblock freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c47ad-108">A handle for the heap whose memory block is to be freed.</span></span> <span data-ttu-id="c47ad-109">Dieser Parameter ist ein Handle, das von [**rtlkreateheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c47ad-109">This parameter is a handle returned by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>

</dd> <dt>

<span data-ttu-id="c47ad-110">*Flags* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="c47ad-110">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c47ad-111">Ein Satz von Flags, die Aspekte der Freigabe eines Speicherblocks steuern.</span><span class="sxs-lookup"><span data-stu-id="c47ad-111">A set of flags that controls aspects of freeing a memory block.</span></span> <span data-ttu-id="c47ad-112">Wenn Sie den folgenden Wert angeben, wird der entsprechende Wert überschrieben, der im *Flags* -Parameter angegeben wurde, als der Heap von [**rtlkreateheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c47ad-112">Specifying the following value overrides the corresponding value that was specified in the *Flags* parameter when the heap was created by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>



| <span data-ttu-id="c47ad-113">Flag</span><span class="sxs-lookup"><span data-stu-id="c47ad-113">Flag</span></span>                           | <span data-ttu-id="c47ad-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c47ad-114">Meaning</span></span>                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c47ad-115">Heap ist \_ nicht \_ serialisiert.</span><span class="sxs-lookup"><span data-stu-id="c47ad-115">HEAP\_NO\_SERIALIZE</span></span><br/> | <span data-ttu-id="c47ad-116">Der gegenseitige Ausschluss wird nicht verwendet, wenn **RtlFreeHeap** auf den Heap zugreift.</span><span class="sxs-lookup"><span data-stu-id="c47ad-116">Mutual exclusion will not be used when **RtlFreeHeap** is accessing the heap.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="c47ad-117">*Heapbase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c47ad-117">*HeapBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c47ad-118">Ein Zeiger auf den Speicherblock, der freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c47ad-118">A pointer to the memory block to free.</span></span> <span data-ttu-id="c47ad-119">Dieser Zeiger wird von [**rtldepcateheap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c47ad-119">This pointer is returned by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c47ad-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c47ad-120">Return value</span></span>

<span data-ttu-id="c47ad-121">Gibt " **true** " zurück, wenn der Block erfolgreich freigegeben wurde. Andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="c47ad-121">Returns **TRUE** if the block was freed successfully; **FALSE** otherwise.</span></span>

> [!Note]  
> <span data-ttu-id="c47ad-122">Ab Windows 8 wird der Rückgabewert als **logisch** typisiert, was eine andere Größe aufweist als der **boolesche** Wert.</span><span class="sxs-lookup"><span data-stu-id="c47ad-122">Starting with Windows 8 the return value is typed as **LOGICAL**, which has a different size than **BOOLEAN**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c47ad-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c47ad-123">Requirements</span></span>



| <span data-ttu-id="c47ad-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c47ad-124">Requirement</span></span> | <span data-ttu-id="c47ad-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c47ad-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c47ad-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c47ad-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c47ad-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c47ad-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="c47ad-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c47ad-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c47ad-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c47ad-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="c47ad-130">Zielplattform</span><span class="sxs-lookup"><span data-stu-id="c47ad-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="c47ad-131"><dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="c47ad-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="c47ad-132">Header</span><span class="sxs-lookup"><span data-stu-id="c47ad-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c47ad-133"><dt>Ntifs. h (ntifs. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c47ad-133"><dt>Ntifs.h (include Ntifs.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="c47ad-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c47ad-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="c47ad-135"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c47ad-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c47ad-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c47ad-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c47ad-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c47ad-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="c47ad-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c47ad-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c47ad-139">**Rtldepcateheap**</span><span class="sxs-lookup"><span data-stu-id="c47ad-139">**RtlAllocateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[<span data-ttu-id="c47ad-140">**Rtlkreateheap**</span><span class="sxs-lookup"><span data-stu-id="c47ad-140">**RtlCreateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[<span data-ttu-id="c47ad-141">**Rtldestroyheap**</span><span class="sxs-lookup"><span data-stu-id="c47ad-141">**RtlDestroyHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
