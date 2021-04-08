---
description: Die ccheaprebelegc-Funktion ordnet den von der ccheapbelegc-Funktion zugewiesenen Arbeitsspeicher neu zu.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: Ccheaprezuweisung-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756451"
---
# <a name="ccheaprealloc-function"></a><span data-ttu-id="3bb1e-103">Ccheaprezuweisung-Funktion</span><span class="sxs-lookup"><span data-stu-id="3bb1e-103">CCHeapReAlloc function</span></span>

<span data-ttu-id="3bb1e-104">Die **ccheaprebelegc** -Funktion ordnet den von der **ccheapbelegc** -Funktion zugewiesenen Arbeitsspeicher neu zu.</span><span class="sxs-lookup"><span data-stu-id="3bb1e-104">The **CCHeapReAlloc** function reallocates memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bb1e-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="3bb1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bb1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb1e-107">*lpmem*</span><span class="sxs-lookup"><span data-stu-id="3bb1e-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb1e-108">Zeiger auf den ursprünglich zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3bb1e-108">Pointer to the original allocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="3bb1e-109">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="3bb1e-109">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb1e-110">Größe des neu belegten Speichers (gemessen in Bytes).</span><span class="sxs-lookup"><span data-stu-id="3bb1e-110">Size of the reallocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3bb1e-111">*bzeroinit*</span><span class="sxs-lookup"><span data-stu-id="3bb1e-111">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="3bb1e-112">Indikator dafür, ob neu zugeordneter Speicher initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3bb1e-112">Indicator of whether reallocated memory was initialized.</span></span> <span data-ttu-id="3bb1e-113">Wenn der Parameterwert **true** ist, wird der neu zugewiesene Speicher mit 0 (null) initialisiert.</span><span class="sxs-lookup"><span data-stu-id="3bb1e-113">If the parameter value is **TRUE**, the newly reallocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb1e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bb1e-114">Return value</span></span>

<span data-ttu-id="3bb1e-115">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den neu zugeordneten Speicher.</span><span class="sxs-lookup"><span data-stu-id="3bb1e-115">If the function is successful, the return value is a pointer to the reallocated memory.</span></span>

<span data-ttu-id="3bb1e-116">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="3bb1e-116">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb1e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bb1e-117">Requirements</span></span>



| <span data-ttu-id="3bb1e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bb1e-118">Requirement</span></span> | <span data-ttu-id="3bb1e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3bb1e-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb1e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3bb1e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb1e-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bb1e-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3bb1e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3bb1e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb1e-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bb1e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3bb1e-124">Header</span><span class="sxs-lookup"><span data-stu-id="3bb1e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bb1e-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bb1e-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="3bb1e-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3bb1e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3bb1e-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bb1e-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3bb1e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3bb1e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bb1e-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bb1e-129"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bb1e-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bb1e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb1e-131">Setccinstptr</span><span class="sxs-lookup"><span data-stu-id="3bb1e-131">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="3bb1e-132">Getccinstptr</span><span class="sxs-lookup"><span data-stu-id="3bb1e-132">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="3bb1e-133">Ccheap-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="3bb1e-133">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="3bb1e-134">Ccheapfree</span><span class="sxs-lookup"><span data-stu-id="3bb1e-134">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="3bb1e-135">Ccheapsize</span><span class="sxs-lookup"><span data-stu-id="3bb1e-135">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




