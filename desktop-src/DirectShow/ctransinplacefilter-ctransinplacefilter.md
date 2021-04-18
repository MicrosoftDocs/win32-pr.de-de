---
description: Konstruktormethode.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Ctransinplacefilter. ctransinplacefilter-Konstruktor (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 091ea6e6a52d4cc9221ddb29db34b4823111a395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365806"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a><span data-ttu-id="2dfe1-103">Ctransinplacefilter. ctransinplacefilter-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="2dfe1-103">CTransInPlaceFilter.CTransInPlaceFilter constructor</span></span>

<span data-ttu-id="2dfe1-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dfe1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dfe1-105">Syntax</span></span>


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a><span data-ttu-id="2dfe1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dfe1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dfe1-107">*pobjectname*</span><span class="sxs-lookup"><span data-stu-id="2dfe1-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="2dfe1-108">Zeichenfolge, die den debugnamen des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="2dfe1-109">Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="2dfe1-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="2dfe1-110">*lpUnk*</span><span class="sxs-lookup"><span data-stu-id="2dfe1-110">*lpUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="2dfe1-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="2dfe1-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="2dfe1-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2dfe1-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="2dfe1-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="2dfe1-115">Klassen Bezeichner des Filters.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-115">Class identifier of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="2dfe1-116">*PHR*</span><span class="sxs-lookup"><span data-stu-id="2dfe1-116">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="2dfe1-117">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-117">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2dfe1-118">*bmodifiesdata*</span><span class="sxs-lookup"><span data-stu-id="2dfe1-118">*bModifiesData*</span></span> 
</dt> <dd>

<span data-ttu-id="2dfe1-119">Boolescher Wert, der angibt, ob der Filter die Eingabedaten ändert.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-119">Boolean value that specifies whether the filter modifies the input data.</span></span> <span data-ttu-id="2dfe1-120">**True** gibt an, dass der Filter die Daten ändert.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-120">If **TRUE**, the filter modifies the data.</span></span> <span data-ttu-id="2dfe1-121">Andernfalls übergibt der Filter die Daten unverändert.</span><span class="sxs-lookup"><span data-stu-id="2dfe1-121">Otherwise, the filter passes the data downstream unchanged.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2dfe1-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2dfe1-122">Requirements</span></span>



| <span data-ttu-id="2dfe1-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2dfe1-123">Requirement</span></span> | <span data-ttu-id="2dfe1-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2dfe1-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dfe1-125">Header</span><span class="sxs-lookup"><span data-stu-id="2dfe1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2dfe1-126"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2dfe1-126"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2dfe1-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2dfe1-127">Library</span></span><br/> | <dl> <span data-ttu-id="2dfe1-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2dfe1-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dfe1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dfe1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dfe1-130">**Ctransinplacefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2dfe1-130">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




