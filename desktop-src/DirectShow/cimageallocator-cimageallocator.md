---
description: 'CImageAllocator.CImageAllocator-Konstruktor : Konstruktormethode.'
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: CImageAllocator.CImageAllocator-Konstruktor (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085758"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="ab21c-103">CImageAllocator.CImageAllocator-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="ab21c-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="ab21c-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ab21c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab21c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab21c-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ab21c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab21c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab21c-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="ab21c-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="ab21c-108">Zeiger auf den besitzenden Filter.</span><span class="sxs-lookup"><span data-stu-id="ab21c-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="ab21c-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="ab21c-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ab21c-110">Zeiger auf eine Zeichenfolge, die den Debugnamen der Zuweisung enthält.</span><span class="sxs-lookup"><span data-stu-id="ab21c-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="ab21c-111">Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="ab21c-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab21c-112">*Phr*</span><span class="sxs-lookup"><span data-stu-id="ab21c-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ab21c-113">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="ab21c-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ab21c-114">Legen Sie den Wert auf S \_ OK fest, bevor Sie das -Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab21c-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="ab21c-115">Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ab21c-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab21c-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab21c-116">Requirements</span></span>



| <span data-ttu-id="ab21c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab21c-117">Requirement</span></span> | <span data-ttu-id="ab21c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ab21c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab21c-119">Header</span><span class="sxs-lookup"><span data-stu-id="ab21c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ab21c-120"><dt>Winutil.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab21c-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab21c-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab21c-121">Library</span></span><br/> | <dl> <span data-ttu-id="ab21c-122"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ab21c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab21c-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ab21c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab21c-124">**CImageAllocator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ab21c-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




