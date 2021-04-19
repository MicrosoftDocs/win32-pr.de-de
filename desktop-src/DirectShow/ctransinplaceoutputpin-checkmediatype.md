---
description: Die checkmediatype-Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Ctransinplaceoutputpin. checkmediatype-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0a422851bc7e09075076decc39d57b85d1052ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367611"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="e8bb3-103">Ctransinplaceoutputpin. checkmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="e8bb3-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="e8bb3-104">Die- `CheckMediaType` Methode bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e8bb3-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8bb3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8bb3-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="e8bb3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8bb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8bb3-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="e8bb3-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e8bb3-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="e8bb3-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8bb3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8bb3-109">Return value</span></span>

<span data-ttu-id="e8bb3-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e8bb3-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e8bb3-111">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8bb3-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="e8bb3-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e8bb3-112">Return code</span></span>                                                                                                | <span data-ttu-id="e8bb3-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8bb3-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="e8bb3-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8bb3-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="e8bb3-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e8bb3-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="e8bb3-116"><dt>**VFW \_ E- \_ Typ \_ nicht \_ akzeptiert**</dt></span><span class="sxs-lookup"><span data-stu-id="e8bb3-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="e8bb3-117">Der Medientyp wurde nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="e8bb3-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e8bb3-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8bb3-118">Remarks</span></span>

<span data-ttu-id="e8bb3-119">Diese Methode überschreibt die [**ctransformoutputpin:: checkmediatype**](ctransformoutputpin-checkmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e8bb3-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="e8bb3-120">Wenn der Filter bereits Streaming ist und zwei Zuweisungen verwendet, lehnt diese Methode alle Formatänderungen ab.</span><span class="sxs-lookup"><span data-stu-id="e8bb3-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="e8bb3-121">Andernfalls ruft diese Methode die [**ctransformfilter:: checkinputtype**](ctransformfilter-checkinputtype.md) -Methode des Filters auf, um den Medientyp zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e8bb3-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="e8bb3-122">Wenn die eingabepin verbunden ist, wird auch die [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) -Methode für die upstreamausgabepin aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e8bb3-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8bb3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8bb3-123">Requirements</span></span>



| <span data-ttu-id="e8bb3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8bb3-124">Requirement</span></span> | <span data-ttu-id="e8bb3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e8bb3-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8bb3-126">Header</span><span class="sxs-lookup"><span data-stu-id="e8bb3-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e8bb3-127"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8bb3-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e8bb3-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8bb3-128">Library</span></span><br/> | <dl> <span data-ttu-id="e8bb3-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e8bb3-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8bb3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8bb3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8bb3-131">**Ctransinplaceoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e8bb3-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




