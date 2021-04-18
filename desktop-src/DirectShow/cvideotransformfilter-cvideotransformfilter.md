---
description: Konstruktormethode.
ms.assetid: 4dad635f-4637-4f40-9f02-a91b59d05278
title: Cvideotransformfilter. cvideotransformfilter-Konstruktor (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.CVideoTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63e642182a0f968db5bda06e0af410d02455eb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360980"
---
# <a name="cvideotransformfiltercvideotransformfilter-constructor"></a><span data-ttu-id="3e34f-103">Cvideotransformfilter. cvideotransformfilter-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="3e34f-103">CVideoTransformFilter.CVideoTransformFilter constructor</span></span>

<span data-ttu-id="3e34f-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="3e34f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e34f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e34f-105">Syntax</span></span>


```C++
CVideoTransformFilter(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="3e34f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e34f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e34f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="3e34f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3e34f-108">Zeichenfolge, die den debugnamen des Filters enthält.</span><span class="sxs-lookup"><span data-stu-id="3e34f-108">String containing the debug name of the filter.</span></span> <span data-ttu-id="3e34f-109">Weitere Informationen finden Sie unter [**cbaseobject:: cbaseobject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="3e34f-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e34f-110">*Kro*</span><span class="sxs-lookup"><span data-stu-id="3e34f-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3e34f-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="3e34f-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="3e34f-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts.</span><span class="sxs-lookup"><span data-stu-id="3e34f-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="3e34f-113">Andernfalls legen Sie diesen Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="3e34f-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3e34f-114">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="3e34f-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="3e34f-115">Klassen Bezeichner des Filters.</span><span class="sxs-lookup"><span data-stu-id="3e34f-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e34f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e34f-116">Requirements</span></span>



| <span data-ttu-id="3e34f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e34f-117">Requirement</span></span> | <span data-ttu-id="3e34f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3e34f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e34f-119">Header</span><span class="sxs-lookup"><span data-stu-id="3e34f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3e34f-120"><dt>Vtrans. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e34f-120"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3e34f-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3e34f-121">Library</span></span><br/> | <dl> <span data-ttu-id="3e34f-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3e34f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e34f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e34f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e34f-124">**Cvideotransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3e34f-124">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




