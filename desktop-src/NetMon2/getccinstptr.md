---
description: Die getccinstptr-Funktion gibt den Zeiger auf die Instanzdaten zurück, die dem Aufzeichnungs Kontext hinzugefügt wurden.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: Getccinstptr-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750089"
---
# <a name="getccinstptr-function"></a><span data-ttu-id="f0237-103">Getccinstptr-Funktion</span><span class="sxs-lookup"><span data-stu-id="f0237-103">GetCCInstPtr function</span></span>

<span data-ttu-id="f0237-104">Die **getccinstptr** -Funktion gibt den Zeiger auf die Instanzdaten zurück, die dem Aufzeichnungs Kontext hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="f0237-104">The **GetCCInstPtr** function returns the pointer to the instance data added to the capture context.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0237-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0237-105">Syntax</span></span>


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a><span data-ttu-id="f0237-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0237-106">Parameters</span></span>

<span data-ttu-id="f0237-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f0237-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0237-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f0237-108">Return value</span></span>

<span data-ttu-id="f0237-109">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf die Instanzdaten einer bestimmten Erfassung.</span><span class="sxs-lookup"><span data-stu-id="f0237-109">If the function is successful, the return value is a pointer to the instance data of a specific capture.</span></span>

<span data-ttu-id="f0237-110">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="f0237-110">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0237-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0237-111">Requirements</span></span>



| <span data-ttu-id="f0237-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0237-112">Requirement</span></span> | <span data-ttu-id="f0237-113">Wert</span><span class="sxs-lookup"><span data-stu-id="f0237-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f0237-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0237-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f0237-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0237-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f0237-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0237-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f0237-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f0237-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f0237-118">Header</span><span class="sxs-lookup"><span data-stu-id="f0237-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0237-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0237-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f0237-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f0237-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0237-121"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0237-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f0237-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f0237-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0237-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0237-123"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0237-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0237-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0237-125">Setccinstptr</span><span class="sxs-lookup"><span data-stu-id="f0237-125">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="f0237-126">Ccheap-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="f0237-126">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="f0237-127">Ccheapfree</span><span class="sxs-lookup"><span data-stu-id="f0237-127">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="f0237-128">Ccheaprezuweisung</span><span class="sxs-lookup"><span data-stu-id="f0237-128">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="f0237-129">Ccheapsize</span><span class="sxs-lookup"><span data-stu-id="f0237-129">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




