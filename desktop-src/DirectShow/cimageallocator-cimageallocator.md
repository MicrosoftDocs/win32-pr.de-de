---
description: Konstruktormethode.
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Cimagezuordcator. cimagezuordcator-Konstruktor (winutil. h)
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
ms.openlocfilehash: a5f6873e8cc073e0b716f94c980ecceba8f4512f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372134"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="88240-103">Cimagezuordcator. cimagezuordcator-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="88240-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="88240-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="88240-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="88240-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88240-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="88240-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="88240-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88240-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="88240-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="88240-108">Zeiger auf den besitzenden Filter.</span><span class="sxs-lookup"><span data-stu-id="88240-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="88240-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="88240-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="88240-110">Zeiger auf eine Zeichenfolge, die den debugnamen der Zuweisung enthält.</span><span class="sxs-lookup"><span data-stu-id="88240-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="88240-111">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="88240-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="88240-112">*PHR*</span><span class="sxs-lookup"><span data-stu-id="88240-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="88240-113">Zeiger auf einen **HRESULT** -Wert.</span><span class="sxs-lookup"><span data-stu-id="88240-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="88240-114">Legen Sie \_ vor dem Erstellen des Objekts den Wert auf S OK fest.</span><span class="sxs-lookup"><span data-stu-id="88240-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="88240-115">Wenn der Konstruktor fehlschlägt, wird der Wert auf einen Fehlercode festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88240-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88240-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88240-116">Requirements</span></span>



| <span data-ttu-id="88240-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88240-117">Requirement</span></span> | <span data-ttu-id="88240-118">Wert</span><span class="sxs-lookup"><span data-stu-id="88240-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88240-119">Header</span><span class="sxs-lookup"><span data-stu-id="88240-119">Header</span></span><br/>  | <dl> <span data-ttu-id="88240-120"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88240-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="88240-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="88240-121">Library</span></span><br/> | <dl> <span data-ttu-id="88240-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="88240-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88240-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88240-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88240-124">**Cimagezuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="88240-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




