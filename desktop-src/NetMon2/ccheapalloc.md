---
description: Die ccheapbelegc-Funktion ordnet Speicher auf der Grundlage der Erfassung zu.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: Cbillienc-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864799"
---
# <a name="ccheapalloc-function"></a><span data-ttu-id="d1a4d-103">Cbillienc-Funktion</span><span class="sxs-lookup"><span data-stu-id="d1a4d-103">CCHeapAlloc function</span></span>

<span data-ttu-id="d1a4d-104">Die **ccheapbelegc** -Funktion ordnet Speicher auf der Grundlage der Erfassung zu.</span><span class="sxs-lookup"><span data-stu-id="d1a4d-104">The **CCHeapAlloc** function allocates memory on a capture-by-capture basis.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1a4d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1a4d-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="d1a4d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1a4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a4d-107">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="d1a4d-107">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a4d-108">Angeforderte Länge des zugeordneten Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="d1a4d-108">Requested length of memory allocated.</span></span>

</dd> <dt>

<span data-ttu-id="d1a4d-109">*bzeroinit*</span><span class="sxs-lookup"><span data-stu-id="d1a4d-109">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="d1a4d-110">Indikator dafür, ob zugewiesener Arbeitsspeicher initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d1a4d-110">Indicator of whether allocated memory was initialized.</span></span> <span data-ttu-id="d1a4d-111">Wenn der Parameterwert **true** ist, wird der zugeordnete Arbeitsspeicher mit 0 (null) initialisiert.</span><span class="sxs-lookup"><span data-stu-id="d1a4d-111">If the parameter value is **TRUE**, the allocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1a4d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d1a4d-112">Return value</span></span>

<span data-ttu-id="d1a4d-113">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d1a4d-113">If the function is successful, the return value is a pointer to the allocated memory.</span></span> <span data-ttu-id="d1a4d-114">Wenn Sie den belegten Arbeitsspeicher nicht mehr benötigen, können Sie den Speicher freigeben, indem Sie die [**ccheapfree**](ccheapfree.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d1a4d-114">When you have finished using the allocated memory, free the memory by calling the [**CCHeapFree**](ccheapfree.md) function.</span></span>

<span data-ttu-id="d1a4d-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="d1a4d-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a4d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1a4d-116">Requirements</span></span>



| <span data-ttu-id="d1a4d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d1a4d-117">Requirement</span></span> | <span data-ttu-id="d1a4d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d1a4d-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a4d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d1a4d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a4d-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1a4d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d1a4d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d1a4d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a4d-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d1a4d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d1a4d-123">Header</span><span class="sxs-lookup"><span data-stu-id="d1a4d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1a4d-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1a4d-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d1a4d-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d1a4d-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1a4d-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1a4d-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d1a4d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d1a4d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1a4d-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1a4d-128"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1a4d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1a4d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a4d-130">**Setccinstptr**</span><span class="sxs-lookup"><span data-stu-id="d1a4d-130">**SetCCInstPtr**</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="d1a4d-131">**Getccinstptr**</span><span class="sxs-lookup"><span data-stu-id="d1a4d-131">**GetCCInstPtr**</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="d1a4d-132">**Ccheapfree**</span><span class="sxs-lookup"><span data-stu-id="d1a4d-132">**CCHeapFree**</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="d1a4d-133">**Ccheaprezuweisung**</span><span class="sxs-lookup"><span data-stu-id="d1a4d-133">**CCHeapReAlloc**</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="d1a4d-134">**Ccheapsize**</span><span class="sxs-lookup"><span data-stu-id="d1a4d-134">**CCHeapSize**</span></span>](ccheapsize.md)
</dt> </dl>

 

 




