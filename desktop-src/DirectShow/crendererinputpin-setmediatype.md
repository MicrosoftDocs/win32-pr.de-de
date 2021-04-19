---
description: 'Die setmediatype-Methode legt den Medientyp für die Verbindung fest. Diese Methode überschreibt die cbasepin:: setmediatype-Methode.'
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: Crendererinputpin. setmediatype-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca70878f8f6358a3297c22cbb9ac8e49ba0ce310
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374007"
---
# <a name="crendererinputpinsetmediatype-method"></a><span data-ttu-id="1bc70-104">Crendererinputpin. setmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="1bc70-104">CRendererInputPin.SetMediaType method</span></span>

<span data-ttu-id="1bc70-105">Die- `SetMediaType` Methode legt den Medientyp für die Verbindung fest.</span><span class="sxs-lookup"><span data-stu-id="1bc70-105">The `SetMediaType` method sets the media type for the connection.</span></span> <span data-ttu-id="1bc70-106">Diese Methode überschreibt die [**cbasepin:: setmediatype**](cbasepin-setmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1bc70-106">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc70-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bc70-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="1bc70-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bc70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bc70-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="1bc70-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1bc70-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="1bc70-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bc70-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1bc70-111">Return value</span></span>

<span data-ttu-id="1bc70-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1bc70-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bc70-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bc70-113">Requirements</span></span>



| <span data-ttu-id="1bc70-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1bc70-114">Requirement</span></span> | <span data-ttu-id="1bc70-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1bc70-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc70-116">Header</span><span class="sxs-lookup"><span data-stu-id="1bc70-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1bc70-117"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc70-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1bc70-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1bc70-118">Library</span></span><br/> | <dl> <span data-ttu-id="1bc70-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc70-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bc70-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bc70-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc70-121">**Crendererinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1bc70-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




