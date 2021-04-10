---
description: Die Funktion "ccheapfree" gibt den von der Funktion "cbillizuzuordnungs" zugeordneten Speicher frei.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: Ccheapfree-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e89ca9a7d00559724edc6679a0ed99e4bdf9c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131860"
---
# <a name="ccheapfree-function"></a><span data-ttu-id="db260-103">Ccheapfree-Funktion</span><span class="sxs-lookup"><span data-stu-id="db260-103">CCHeapFree function</span></span>

<span data-ttu-id="db260-104">Die Funktion " **ccheapfree** " gibt den von der Funktion " **cbillizuzuordnungs** " zugeordneten Speicher frei.</span><span class="sxs-lookup"><span data-stu-id="db260-104">The **CCHeapFree** function releases the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="db260-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db260-105">Syntax</span></span>


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="db260-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="db260-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db260-107">*lpmem*</span><span class="sxs-lookup"><span data-stu-id="db260-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="db260-108">Zeiger auf den Arbeitsspeicher, der von dieser Funktion freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="db260-108">Pointer to the memory that this function releases.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db260-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db260-109">Return value</span></span>

<span data-ttu-id="db260-110">Wenn die **ccheapfree** -Funktion erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="db260-110">If the **CCHeapFree** function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="db260-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="db260-111">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="db260-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db260-112">Requirements</span></span>



| <span data-ttu-id="db260-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db260-113">Requirement</span></span> | <span data-ttu-id="db260-114">Wert</span><span class="sxs-lookup"><span data-stu-id="db260-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="db260-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db260-115">Minimum supported client</span></span><br/> | <span data-ttu-id="db260-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db260-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="db260-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db260-117">Minimum supported server</span></span><br/> | <span data-ttu-id="db260-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db260-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="db260-119">Header</span><span class="sxs-lookup"><span data-stu-id="db260-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="db260-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="db260-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="db260-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="db260-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="db260-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db260-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="db260-123">DLL</span><span class="sxs-lookup"><span data-stu-id="db260-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db260-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db260-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db260-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db260-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db260-126">Setccinstptr</span><span class="sxs-lookup"><span data-stu-id="db260-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="db260-127">Getccinstptr</span><span class="sxs-lookup"><span data-stu-id="db260-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="db260-128">Ccheap-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="db260-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="db260-129">Ccheaprezuweisung</span><span class="sxs-lookup"><span data-stu-id="db260-129">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="db260-130">Ccheapsize</span><span class="sxs-lookup"><span data-stu-id="db260-130">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




