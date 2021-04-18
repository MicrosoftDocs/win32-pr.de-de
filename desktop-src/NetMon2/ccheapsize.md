---
description: Die ccheapsize-Funktion gibt die Größe des Arbeitsspeichers zurück, der von der ccheap-Zuordnungs Funktion belegt wird.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: Ccheapsize-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ae196253a66fc68f9066615b39c48f6921e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358562"
---
# <a name="ccheapsize-function"></a><span data-ttu-id="23b6b-103">Ccheapsize-Funktion</span><span class="sxs-lookup"><span data-stu-id="23b6b-103">CCHeapSize function</span></span>

<span data-ttu-id="23b6b-104">Die **ccheapsize** -Funktion gibt die Größe des Arbeitsspeichers zurück, der von der **ccheap-Zuordnungs** Funktion belegt wird.</span><span class="sxs-lookup"><span data-stu-id="23b6b-104">The **CCHeapSize** function returns the size of the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="23b6b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23b6b-105">Syntax</span></span>


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="23b6b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="23b6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b6b-107">*lpmem*</span><span class="sxs-lookup"><span data-stu-id="23b6b-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="23b6b-108">Zeiger auf zugewiesenen Speicher.</span><span class="sxs-lookup"><span data-stu-id="23b6b-108">Pointer to the allocated memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23b6b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23b6b-109">Return value</span></span>

<span data-ttu-id="23b6b-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Größe des angeforderten Speicherblocks, gemessen in Bytes.</span><span class="sxs-lookup"><span data-stu-id="23b6b-110">If the function is successful, the return value is the size of the requested memory block   measured in bytes.</span></span>

<span data-ttu-id="23b6b-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="23b6b-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="23b6b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23b6b-112">Requirements</span></span>



| <span data-ttu-id="23b6b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23b6b-113">Requirement</span></span> | <span data-ttu-id="23b6b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="23b6b-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="23b6b-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23b6b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="23b6b-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23b6b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="23b6b-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23b6b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="23b6b-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23b6b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="23b6b-119">Header</span><span class="sxs-lookup"><span data-stu-id="23b6b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="23b6b-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="23b6b-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="23b6b-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="23b6b-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="23b6b-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23b6b-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="23b6b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="23b6b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23b6b-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23b6b-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b6b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23b6b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23b6b-126">Setccinstptr</span><span class="sxs-lookup"><span data-stu-id="23b6b-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="23b6b-127">Getccinstptr</span><span class="sxs-lookup"><span data-stu-id="23b6b-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="23b6b-128">Ccheap-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="23b6b-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="23b6b-129">Ccheapfree</span><span class="sxs-lookup"><span data-stu-id="23b6b-129">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="23b6b-130">Ccheaprezuweisung</span><span class="sxs-lookup"><span data-stu-id="23b6b-130">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> </dl>

 

 




