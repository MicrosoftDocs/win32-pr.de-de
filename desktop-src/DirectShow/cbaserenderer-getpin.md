---
description: Die getpin-Methode ruft eine PIN ab.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Cbaserderderer. getpin-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b67b926e0af604e0a25ea7c09b417baf3647fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358268"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="c4312-103">Cbaserderderer. getpin-Methode</span><span class="sxs-lookup"><span data-stu-id="c4312-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="c4312-104">Die- `GetPin` Methode ruft eine PIN ab.</span><span class="sxs-lookup"><span data-stu-id="c4312-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4312-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4312-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="c4312-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4312-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4312-107">*n*</span><span class="sxs-lookup"><span data-stu-id="c4312-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="c4312-108">Die Nummer der angegebenen PIN.</span><span class="sxs-lookup"><span data-stu-id="c4312-108">Number of the specified pin.</span></span> <span data-ttu-id="c4312-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c4312-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4312-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4312-110">Return value</span></span>

<span data-ttu-id="c4312-111">Gibt den [**cbaserenderer:: m \_ pinputpin**](cbaserenderer-m-pinputpin.md) -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="c4312-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4312-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4312-112">Remarks</span></span>

<span data-ttu-id="c4312-113">Diese Methode implementiert die [**cbasefilter:: getpin**](cbasefilter-getpin.md) -Methode, die rein virtuell in der **cbasefilter** -Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="c4312-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="c4312-114">Der Filter unterstützt genau eine PIN (die Eingabe-PIN).</span><span class="sxs-lookup"><span data-stu-id="c4312-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="c4312-115">Beim ersten Aufruf dieser Methode wird die PIN als neues [**crendererinputpin**](crendererinputpin.md) -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="c4312-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4312-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4312-116">Requirements</span></span>



| <span data-ttu-id="c4312-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4312-117">Requirement</span></span> | <span data-ttu-id="c4312-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c4312-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4312-119">Header</span><span class="sxs-lookup"><span data-stu-id="c4312-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c4312-120"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4312-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c4312-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4312-121">Library</span></span><br/> | <dl> <span data-ttu-id="c4312-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c4312-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4312-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4312-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4312-124">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c4312-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




