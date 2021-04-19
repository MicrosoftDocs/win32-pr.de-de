---
description: Die checkmediatype-Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Ctransinplaceinputpin. checkmediatype-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22f271759bc0ade6b820aed2039bbc16a2cf4a31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354085"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a><span data-ttu-id="6fbfa-103">Ctransinplaceinputpin. checkmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="6fbfa-103">CTransInPlaceInputPin.CheckMediaType method</span></span>

<span data-ttu-id="6fbfa-104">Die- `CheckMediaType` Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="6fbfa-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fbfa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fbfa-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="6fbfa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fbfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fbfa-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="6fbfa-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6fbfa-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="6fbfa-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fbfa-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6fbfa-109">Return value</span></span>

<span data-ttu-id="6fbfa-110">Gibt S \_ OK zurück, wenn der vorgeschlagene Medientyp zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="6fbfa-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="6fbfa-111">Andernfalls gibt S \_ false oder einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="6fbfa-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fbfa-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6fbfa-112">Remarks</span></span>

<span data-ttu-id="6fbfa-113">Diese Methode überschreibt die [**ctransforminputpin:: checkmediatype**](ctransforminputpin-checkmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6fbfa-113">This method overrides the [**CTransformInputPin::CheckMediaType**](ctransforminputpin-checkmediatype.md) method.</span></span> <span data-ttu-id="6fbfa-114">Die [**ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md) -Methode des Filters wird aufgerufen, um den Eingabetyp zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="6fbfa-114">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the input type.</span></span> <span data-ttu-id="6fbfa-115">Wenn die Ausgabe-PIN verbunden ist, ruft diese Methode auch die [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) -Methode für die downstreameingabepin auf.</span><span class="sxs-lookup"><span data-stu-id="6fbfa-115">If the output pin is connected, this method also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fbfa-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6fbfa-116">Requirements</span></span>



| <span data-ttu-id="6fbfa-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6fbfa-117">Requirement</span></span> | <span data-ttu-id="6fbfa-118">Wert</span><span class="sxs-lookup"><span data-stu-id="6fbfa-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fbfa-119">Header</span><span class="sxs-lookup"><span data-stu-id="6fbfa-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6fbfa-120"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fbfa-120"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6fbfa-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6fbfa-121">Library</span></span><br/> | <dl> <span data-ttu-id="6fbfa-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6fbfa-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fbfa-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6fbfa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fbfa-124">**Ctransinplaceinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6fbfa-124">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




