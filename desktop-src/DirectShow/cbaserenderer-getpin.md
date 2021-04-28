---
description: 'CBaseRenderer.GetPin-Methode: Die GetPin-Methode ruft einen Pin ab.'
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: CBaseRenderer.GetPin-Methode (Renbase.h)
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
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119888"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="1f5d2-103">CBaseRenderer.GetPin-Methode</span><span class="sxs-lookup"><span data-stu-id="1f5d2-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="1f5d2-104">Die `GetPin` -Methode ruft einen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="1f5d2-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f5d2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f5d2-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="1f5d2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f5d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f5d2-107">*n*</span><span class="sxs-lookup"><span data-stu-id="1f5d2-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="1f5d2-108">Die Nummer des angegebenen Pins.</span><span class="sxs-lookup"><span data-stu-id="1f5d2-108">Number of the specified pin.</span></span> <span data-ttu-id="1f5d2-109">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="1f5d2-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f5d2-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f5d2-110">Return value</span></span>

<span data-ttu-id="1f5d2-111">Gibt den [**\_ PInputPin-Zeiger CBaseRenderer::m**](cbaserenderer-m-pinputpin.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="1f5d2-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f5d2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f5d2-112">Remarks</span></span>

<span data-ttu-id="1f5d2-113">Diese Methode implementiert die [**CBaseFilter::GetPin-Methode,**](cbasefilter-getpin.md) die in der **CBaseFilter-Klasse** rein virtuell ist.</span><span class="sxs-lookup"><span data-stu-id="1f5d2-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="1f5d2-114">Der Filter unterstützt genau einen Pin (den Eingabepin).</span><span class="sxs-lookup"><span data-stu-id="1f5d2-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="1f5d2-115">Beim ersten Aufrufen dieser Methode wird der Pin als neues [**CRendererInputPin-Objekt**](crendererinputpin.md) erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f5d2-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f5d2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f5d2-116">Requirements</span></span>



| <span data-ttu-id="1f5d2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f5d2-117">Requirement</span></span> | <span data-ttu-id="1f5d2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1f5d2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f5d2-119">Header</span><span class="sxs-lookup"><span data-stu-id="1f5d2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1f5d2-120"><dt>Renbase.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f5d2-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1f5d2-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f5d2-121">Library</span></span><br/> | <dl> <span data-ttu-id="1f5d2-122"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1f5d2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f5d2-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f5d2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f5d2-124">**CBaseRenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1f5d2-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




