---
description: Konstruktormethode.
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Ctransformfilter. ctransformfilter-Konstruktor (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39569dff69c2ab1ebb635cb69a4c71602a7400d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359413"
---
# <a name="ctransformfilterctransformfilter-constructor"></a><span data-ttu-id="40199-103">Ctransformfilter. ctransformfilter-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="40199-103">CTransformFilter.CTransformFilter constructor</span></span>

<span data-ttu-id="40199-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="40199-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="40199-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40199-105">Syntax</span></span>


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="40199-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40199-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40199-107">*pobjectname*</span><span class="sxs-lookup"><span data-stu-id="40199-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="40199-108">Zeichenfolge, die den debugnamen des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="40199-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="40199-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="40199-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="40199-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="40199-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="40199-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="40199-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="40199-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="40199-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="40199-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="40199-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="40199-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="40199-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="40199-115">Klassen Bezeichner des Filters.</span><span class="sxs-lookup"><span data-stu-id="40199-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40199-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40199-116">Remarks</span></span>

<span data-ttu-id="40199-117">Der Konstruktor erstellt nicht die Pins des Filters.</span><span class="sxs-lookup"><span data-stu-id="40199-117">The constructor does not create the filter's pins.</span></span> <span data-ttu-id="40199-118">Dies geschieht beim ersten Aufrufen der [**getpin**](ctransformfilter-getpin.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="40199-118">That happens during the first call to the [**GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="40199-119">Der Konstruktor initialisiert die [**m \_ pinput**](ctransformfilter-m-pinput.md) -und [**m \_ poutput**](ctransformfilter-m-poutput.md) -Element Variablen auf **null**.</span><span class="sxs-lookup"><span data-stu-id="40199-119">The constructor initializes the [**m\_pInput**](ctransformfilter-m-pinput.md) and [**m\_pOutput**](ctransformfilter-m-poutput.md) member variables to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="40199-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40199-120">Requirements</span></span>



| <span data-ttu-id="40199-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40199-121">Requirement</span></span> | <span data-ttu-id="40199-122">Wert</span><span class="sxs-lookup"><span data-stu-id="40199-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40199-123">Header</span><span class="sxs-lookup"><span data-stu-id="40199-123">Header</span></span><br/>  | <dl> <span data-ttu-id="40199-124"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40199-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="40199-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="40199-125">Library</span></span><br/> | <dl> <span data-ttu-id="40199-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="40199-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40199-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40199-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40199-128">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="40199-128">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




