---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp nach Indexwert ab.
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Cbasepin. getmediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c54c5cd769a8efa0c720c7050cca45b00b8209e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372763"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="2b218-103">Cbasepin. getmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="2b218-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="2b218-104">Die- `GetMediaType` Methode ruft einen bevorzugten Medientyp nach Indexwert ab.</span><span class="sxs-lookup"><span data-stu-id="2b218-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b218-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b218-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="2b218-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b218-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b218-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="2b218-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="2b218-108">NULL basierter Indexwert.</span><span class="sxs-lookup"><span data-stu-id="2b218-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="2b218-109">*pmediatype*</span><span class="sxs-lookup"><span data-stu-id="2b218-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="2b218-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="2b218-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b218-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b218-111">Return value</span></span>

<span data-ttu-id="2b218-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2b218-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2b218-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="2b218-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="2b218-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2b218-114">Return code</span></span>                                                                                            | <span data-ttu-id="2b218-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b218-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2b218-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2b218-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="2b218-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="2b218-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="2b218-118"><dt>**VFW \_ S \_ keine \_ weiteren \_ Elemente**</dt></span><span class="sxs-lookup"><span data-stu-id="2b218-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="2b218-119">Der Index liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="2b218-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="2b218-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="2b218-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="2b218-121">Index kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2b218-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="2b218-122"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="2b218-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="2b218-123">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="2b218-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="2b218-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b218-124">Remarks</span></span>

<span data-ttu-id="2b218-125">In der Liste der bevorzugten Medientypen der PIN gibt diese Methode den Typ mit dem Indexwert *iPosition* zurück.</span><span class="sxs-lookup"><span data-stu-id="2b218-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="2b218-126">Die [**cenummediatypes**](cenummediatypes.md) -Klasse ruft diese Methode auf, um bevorzugte Medientypen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="2b218-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="2b218-127">Die Basisklasse gibt "E unerwartete" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="2b218-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="2b218-128">Überschreiben Sie diese Methode in der abgeleiteten Klasse.</span><span class="sxs-lookup"><span data-stu-id="2b218-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b218-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b218-129">Requirements</span></span>



| <span data-ttu-id="2b218-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b218-130">Requirement</span></span> | <span data-ttu-id="2b218-131">Wert</span><span class="sxs-lookup"><span data-stu-id="2b218-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b218-132">Header</span><span class="sxs-lookup"><span data-stu-id="2b218-132">Header</span></span><br/>  | <dl> <span data-ttu-id="2b218-133"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b218-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2b218-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b218-134">Library</span></span><br/> | <dl> <span data-ttu-id="2b218-135">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2b218-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b218-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b218-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b218-137">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2b218-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




