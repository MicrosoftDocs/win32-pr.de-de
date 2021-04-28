---
description: 'CTransformFilter.GetMediaType-Methode: Die GetMediaType-Methode ruft einen bevorzugten Medientyp für den Ausgabepin ab.'
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: CTransformFilter.GetMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6415b8e3d8ae4e292b7e2592b123120927081ea8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095118"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="a64be-103">CTransformFilter.GetMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="a64be-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="a64be-104">Die `GetMediaType` -Methode ruft einen bevorzugten Medientyp für den Ausgabepin ab.</span><span class="sxs-lookup"><span data-stu-id="a64be-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="a64be-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a64be-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a64be-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a64be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a64be-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="a64be-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="a64be-108">Nullbasierter Indexwert.</span><span class="sxs-lookup"><span data-stu-id="a64be-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="a64be-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="a64be-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="a64be-110">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="a64be-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a64be-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a64be-111">Return value</span></span>

<span data-ttu-id="a64be-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="a64be-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a64be-113">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="a64be-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a64be-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a64be-114">Return code</span></span>                                                                                            | <span data-ttu-id="a64be-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a64be-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a64be-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a64be-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="a64be-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a64be-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="a64be-118"><dt>**VFW \_ S KEINE ELEMENTE \_ \_ \_ MEHR**</dt></span><span class="sxs-lookup"><span data-stu-id="a64be-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="a64be-119">Index liegt nicht im Bereich.</span><span class="sxs-lookup"><span data-stu-id="a64be-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="a64be-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a64be-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="a64be-121">Index kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a64be-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a64be-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a64be-122">Remarks</span></span>

<span data-ttu-id="a64be-123">Die [**CTransformOutputPin::GetMediaType-Methode**](ctransformoutputpin-getmediatype.md) des Ausgabepins ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="a64be-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="a64be-124">Die abgeleitete Klasse muss diese Methode implementieren.</span><span class="sxs-lookup"><span data-stu-id="a64be-124">The derived class must implement this method.</span></span> <span data-ttu-id="a64be-125">Weitere Informationen finden Sie unter [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="a64be-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a64be-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a64be-126">Requirements</span></span>



| <span data-ttu-id="a64be-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a64be-127">Requirement</span></span> | <span data-ttu-id="a64be-128">Wert</span><span class="sxs-lookup"><span data-stu-id="a64be-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a64be-129">Header</span><span class="sxs-lookup"><span data-stu-id="a64be-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a64be-130"><dt>Transfrm.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="a64be-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a64be-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a64be-131">Library</span></span><br/> | <dl> <span data-ttu-id="a64be-132"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a64be-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a64be-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a64be-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64be-134">**CTransformFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a64be-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




