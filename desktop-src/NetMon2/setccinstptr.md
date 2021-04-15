---
description: Die setccinstptr-Funktion erfasst einen Kontext Instanz-Zeiger.
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: Setccinstptr-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526753"
---
# <a name="setccinstptr-function"></a><span data-ttu-id="2f3fa-103">Setccinstptr-Funktion</span><span class="sxs-lookup"><span data-stu-id="2f3fa-103">SetCCInstPtr function</span></span>

<span data-ttu-id="2f3fa-104">Die **setccinstptr** -Funktion erfasst einen Kontext Instanz-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="2f3fa-104">The **SetCCInstPtr** function captures a context instance pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f3fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f3fa-105">Syntax</span></span>


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a><span data-ttu-id="2f3fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f3fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f3fa-107">*lpcurrcaptureinst*</span><span class="sxs-lookup"><span data-stu-id="2f3fa-107">*lpCurCaptureInst*</span></span> 
</dt> <dd>

<span data-ttu-id="2f3fa-108">Zeiger auf die der Erfassung hinzugefügten Instanzdaten.</span><span class="sxs-lookup"><span data-stu-id="2f3fa-108">Pointer to the instance data added to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f3fa-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f3fa-109">Return value</span></span>

<span data-ttu-id="2f3fa-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="2f3fa-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f3fa-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f3fa-111">Remarks</span></span>

<span data-ttu-id="2f3fa-112">Verwenden Sie diese Funktion, um einen Zeiger auf einen Block zu speichern, der mit der **ccheap-Zuordnungs** Funktion zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="2f3fa-112">Use this function to store a pointer to a block that was allocated with the **CCHeapAlloc** function.</span></span> <span data-ttu-id="2f3fa-113">Jeder Parser kann eine einzelne Instanz der Daten für eine Erfassung festlegen.</span><span class="sxs-lookup"><span data-stu-id="2f3fa-113">Each parser can set a single instance of data on a capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f3fa-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f3fa-114">Requirements</span></span>



| <span data-ttu-id="2f3fa-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f3fa-115">Requirement</span></span> | <span data-ttu-id="2f3fa-116">Wert</span><span class="sxs-lookup"><span data-stu-id="2f3fa-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3fa-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f3fa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2f3fa-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f3fa-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2f3fa-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f3fa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2f3fa-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f3fa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2f3fa-121">Header</span><span class="sxs-lookup"><span data-stu-id="2f3fa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f3fa-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f3fa-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2f3fa-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f3fa-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f3fa-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f3fa-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f3fa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2f3fa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f3fa-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f3fa-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f3fa-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f3fa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f3fa-128">Getccinstptr</span><span class="sxs-lookup"><span data-stu-id="2f3fa-128">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="2f3fa-129">Ccheap-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="2f3fa-129">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="2f3fa-130">Ccheapfree</span><span class="sxs-lookup"><span data-stu-id="2f3fa-130">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="2f3fa-131">Ccheaprezuweisung</span><span class="sxs-lookup"><span data-stu-id="2f3fa-131">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="2f3fa-132">Ccheapsize</span><span class="sxs-lookup"><span data-stu-id="2f3fa-132">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




