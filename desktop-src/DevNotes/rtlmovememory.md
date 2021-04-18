---
description: Kopiert den Inhalt eines Quell Speicherblocks in einen Zielspeicher Block und unterstützt überlappende Quell-und Zielspeicher Blöcke.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Rtlmuvememory-Funktion (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340112"
---
# <a name="rtlmovememory-function"></a><span data-ttu-id="81b03-103">Rtlmuvememory-Funktion</span><span class="sxs-lookup"><span data-stu-id="81b03-103">RtlMoveMemory function</span></span>

<span data-ttu-id="81b03-104">Kopiert den Inhalt eines Quell Speicherblocks in einen Zielspeicher Block und unterstützt überlappende Quell-und Zielspeicher Blöcke.</span><span class="sxs-lookup"><span data-stu-id="81b03-104">Copies the contents of a source memory block to a destination memory block, and supports overlapping source and destination memory blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b03-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="81b03-105">Syntax</span></span>


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a><span data-ttu-id="81b03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="81b03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81b03-107">*Ziel* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="81b03-107">*Destination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81b03-108">Ein Zeiger auf den Zielspeicher Block, in den die Bytes kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81b03-108">A pointer to the destination memory block to copy the bytes to.</span></span>

</dd> <dt>

<span data-ttu-id="81b03-109">*Quelle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81b03-109">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81b03-110">Ein Zeiger auf den Quell Speicherblock, aus dem die Bytes kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81b03-110">A pointer to the source memory block to copy the bytes from.</span></span>

</dd> <dt>

<span data-ttu-id="81b03-111">*Länge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81b03-111">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81b03-112">Die Anzahl der Bytes, die aus der Quelle in das Ziel kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="81b03-112">The number of bytes to copy from the source to the destination.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81b03-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81b03-113">Return value</span></span>

<span data-ttu-id="81b03-114">Keine</span><span class="sxs-lookup"><span data-stu-id="81b03-114">None</span></span>

## <a name="remarks"></a><span data-ttu-id="81b03-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81b03-115">Remarks</span></span>

<span data-ttu-id="81b03-116">Der Quell Speicherblock, der durch *Quelle* und *Länge* definiert wird, kann den Zielspeicher Block überlappen, der durch das *Ziel* und die *Länge* definiert wird.</span><span class="sxs-lookup"><span data-stu-id="81b03-116">The source memory block, which is defined by *Source* and *Length*, can overlap the destination memory block, which is defined by *Destination* and *Length*.</span></span>

<span data-ttu-id="81b03-117">Die [**rtlcopymemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) -Routine läuft schneller als **rtlmuvememory**, aber **rtlcopymemory** erfordert, dass sich die Quell-und Zielspeicher Blöcke nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="81b03-117">The [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) routine runs faster than **RtlMoveMemory**, but **RtlCopyMemory** requires that the source and destination memory blocks do not overlap.</span></span>

<span data-ttu-id="81b03-118">Aufrufer von **rtlmuvememory** können in beliebiger unql ausgeführt werden, wenn sich die Quell-und Zielspeicher Blöcke im nicht auslagerenden System Arbeitsspeicher befinden.</span><span class="sxs-lookup"><span data-stu-id="81b03-118">Callers of **RtlMoveMemory** can be running at any IRQL if the source and destination memory blocks are in nonpaged system memory.</span></span> <span data-ttu-id="81b03-119">Andernfalls muss der Aufrufer auf der Ebene "iriql <= APC" ausgeführt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="81b03-119">Otherwise, the caller must be running at IRQL <= APC\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="81b03-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81b03-120">Requirements</span></span>



| <span data-ttu-id="81b03-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81b03-121">Requirement</span></span> | <span data-ttu-id="81b03-122">Wert</span><span class="sxs-lookup"><span data-stu-id="81b03-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b03-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81b03-123">Minimum supported client</span></span><br/> | <span data-ttu-id="81b03-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81b03-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="81b03-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81b03-125">Minimum supported server</span></span><br/> | <span data-ttu-id="81b03-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81b03-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="81b03-127">Zielplattform</span><span class="sxs-lookup"><span data-stu-id="81b03-127">Target platform</span></span><br/>          | <dl> <span data-ttu-id="81b03-128"><dt>[Universell](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="81b03-128"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="81b03-129">Header</span><span class="sxs-lookup"><span data-stu-id="81b03-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="81b03-130"><dt>WDM. h (Include WDM. h, ntddk. h oder ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81b03-130"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="81b03-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="81b03-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="81b03-132"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="81b03-132"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="81b03-133">DLL</span><span class="sxs-lookup"><span data-stu-id="81b03-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81b03-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81b03-134"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="81b03-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81b03-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b03-136">**Rtlcopymemory**</span><span class="sxs-lookup"><span data-stu-id="81b03-136">**RtlCopyMemory**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
