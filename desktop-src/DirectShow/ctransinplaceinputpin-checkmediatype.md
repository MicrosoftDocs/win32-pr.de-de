---
description: 'CTransInPlaceInputPin.CheckMediaType-Methode: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.'
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: CTransInPlaceInputPin.CheckMediaType-Methode (Transip.h)
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
ms.openlocfilehash: 5de3cec87d740db42824b0d7abf1ee4bfc6aeecb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094798"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a><span data-ttu-id="e4984-103">CTransInPlaceInputPin.CheckMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="e4984-103">CTransInPlaceInputPin.CheckMediaType method</span></span>

<span data-ttu-id="e4984-104">Die `CheckMediaType` -Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e4984-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4984-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4984-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="e4984-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4984-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4984-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="e4984-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e4984-108">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="e4984-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4984-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4984-109">Return value</span></span>

<span data-ttu-id="e4984-110">Gibt S \_ OK zurück, wenn der vorgeschlagene Medientyp akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="e4984-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="e4984-111">Andernfalls wird S \_ FALSE oder ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4984-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4984-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4984-112">Remarks</span></span>

<span data-ttu-id="e4984-113">Diese Methode überschreibt die [**CTransformInputPin::CheckMediaType-Methode.**](ctransforminputpin-checkmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="e4984-113">This method overrides the [**CTransformInputPin::CheckMediaType**](ctransforminputpin-checkmediatype.md) method.</span></span> <span data-ttu-id="e4984-114">Sie ruft die [**CTransformFilter::CheckInputType-Methode**](ctransformfilter-checkinputtype.md) des Filters auf, um den Eingabetyp zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e4984-114">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the input type.</span></span> <span data-ttu-id="e4984-115">Wenn der Ausgabepin verbunden ist, ruft diese Methode auch die [**IPin::QueryAccept-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Downstreameingabepin auf.</span><span class="sxs-lookup"><span data-stu-id="e4984-115">If the output pin is connected, this method also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4984-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4984-116">Requirements</span></span>



| <span data-ttu-id="e4984-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4984-117">Requirement</span></span> | <span data-ttu-id="e4984-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e4984-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4984-119">Header</span><span class="sxs-lookup"><span data-stu-id="e4984-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e4984-120"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4984-120"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e4984-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4984-121">Library</span></span><br/> | <dl> <span data-ttu-id="e4984-122"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e4984-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4984-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4984-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4984-124">**CTransInPlaceInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e4984-124">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




