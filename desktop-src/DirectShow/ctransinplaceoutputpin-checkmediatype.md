---
description: 'CTransInPlaceOutputPin.CheckMediaType-Methode: Die CheckMediaType-Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.'
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: CTransInPlaceOutputPin.CheckMediaType-Methode (Transip.h)
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
ms.openlocfilehash: 66cd29758e0b2d63db88db8b998cc79ec12efdd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094718"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="33a07-103">CTransInPlaceOutputPin.CheckMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="33a07-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="33a07-104">Die `CheckMediaType` -Methode bestimmt, ob der Pin einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="33a07-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="33a07-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33a07-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="33a07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33a07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33a07-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="33a07-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="33a07-108">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den vorgeschlagenen Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="33a07-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33a07-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33a07-109">Return value</span></span>

<span data-ttu-id="33a07-110">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="33a07-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="33a07-111">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="33a07-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="33a07-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="33a07-112">Return code</span></span>                                                                                                | <span data-ttu-id="33a07-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33a07-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="33a07-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33a07-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="33a07-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="33a07-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="33a07-116"><dt>**VFW \_ \_ E-TYP \_ NICHT \_ AKZEPTIERT**</dt></span><span class="sxs-lookup"><span data-stu-id="33a07-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="33a07-117">Der Medientyp wird nicht akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="33a07-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33a07-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33a07-118">Remarks</span></span>

<span data-ttu-id="33a07-119">Diese Methode überschreibt die [**CTransformOutputPin::CheckMediaType-Methode.**](ctransformoutputpin-checkmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="33a07-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="33a07-120">Wenn der Filter bereits streamingt und zwei Zuweisungen verwendet, lehnt diese Methode formatierte Änderungen ab.</span><span class="sxs-lookup"><span data-stu-id="33a07-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="33a07-121">Andernfalls ruft diese Methode die [**CTransformFilter::CheckInputType-Methode**](ctransformfilter-checkinputtype.md) des Filters auf, um den Medientyp zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="33a07-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="33a07-122">Wenn der Eingabepin verbunden ist, ruft er auch die [**IPin::QueryAccept-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Upstreamausgabepin auf.</span><span class="sxs-lookup"><span data-stu-id="33a07-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="33a07-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33a07-123">Requirements</span></span>



| <span data-ttu-id="33a07-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33a07-124">Requirement</span></span> | <span data-ttu-id="33a07-125">Wert</span><span class="sxs-lookup"><span data-stu-id="33a07-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33a07-126">Header</span><span class="sxs-lookup"><span data-stu-id="33a07-126">Header</span></span><br/>  | <dl> <span data-ttu-id="33a07-127"><dt>Transip.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="33a07-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="33a07-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33a07-128">Library</span></span><br/> | <dl> <span data-ttu-id="33a07-129"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="33a07-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33a07-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="33a07-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33a07-131">**CTransInPlaceOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="33a07-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




