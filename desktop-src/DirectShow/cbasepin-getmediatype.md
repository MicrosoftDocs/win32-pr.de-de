---
description: 'CBasePin.GetMediaType-Methode: Die GetMediaType-Methode ruft einen bevorzugten Medientyp nach Indexwert ab.'
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: CBasePin.GetMediaType-Methode (Amfilter.h)
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
ms.openlocfilehash: 186f2eddbedf4eb0565a4ca66ff4ed7e5b080090
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099368"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="da740-103">CBasePin.GetMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="da740-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="da740-104">Die `GetMediaType` -Methode ruft einen bevorzugten Medientyp nach Indexwert ab.</span><span class="sxs-lookup"><span data-stu-id="da740-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="da740-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da740-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="da740-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da740-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da740-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="da740-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="da740-108">Nullbasierter Indexwert.</span><span class="sxs-lookup"><span data-stu-id="da740-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="da740-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="da740-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="da740-110">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="da740-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da740-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da740-111">Return value</span></span>

<span data-ttu-id="da740-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="da740-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="da740-113">Mögliche Werte sind die werte in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="da740-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="da740-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="da740-114">Return code</span></span>                                                                                            | <span data-ttu-id="da740-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da740-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="da740-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="da740-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="da740-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="da740-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="da740-118"><dt>**VFW \_ S KEINE ELEMENTE \_ \_ \_ MEHR**</dt></span><span class="sxs-lookup"><span data-stu-id="da740-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="da740-119">Index liegt nicht im Bereich.</span><span class="sxs-lookup"><span data-stu-id="da740-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="da740-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="da740-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="da740-121">Index kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="da740-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="da740-122"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="da740-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="da740-123">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="da740-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="da740-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da740-124">Remarks</span></span>

<span data-ttu-id="da740-125">Aus der Liste der bevorzugten Medientypen des Pins gibt diese Methode den Typ mit dem Indexwert *iPosition zurück.*</span><span class="sxs-lookup"><span data-stu-id="da740-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="da740-126">Die [**CEnumMediaTypes-Klasse**](cenummediatypes.md) ruft diese Methode auf, um bevorzugte Medientypen aufzählen.</span><span class="sxs-lookup"><span data-stu-id="da740-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="da740-127">Die Basisklasse gibt E \_ UNEXPECTED zurück.</span><span class="sxs-lookup"><span data-stu-id="da740-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="da740-128">Überschreiben Sie diese Methode in der abgeleiteten Klasse.</span><span class="sxs-lookup"><span data-stu-id="da740-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="da740-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da740-129">Requirements</span></span>



| <span data-ttu-id="da740-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da740-130">Requirement</span></span> | <span data-ttu-id="da740-131">Wert</span><span class="sxs-lookup"><span data-stu-id="da740-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da740-132">Header</span><span class="sxs-lookup"><span data-stu-id="da740-132">Header</span></span><br/>  | <dl> <span data-ttu-id="da740-133"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="da740-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="da740-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da740-134">Library</span></span><br/> | <dl> <span data-ttu-id="da740-135"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="da740-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da740-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="da740-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da740-137">**CBasePin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="da740-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




