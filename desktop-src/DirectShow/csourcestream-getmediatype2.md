---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp ab.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Csourcestream. getmediatype-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62d79faab8d48d748f4a2c787dd1cbc8f6d2ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372601"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a><span data-ttu-id="bae8d-103">Csourcestream. getmediatype-Methode (Quelle. h)</span><span class="sxs-lookup"><span data-stu-id="bae8d-103">CSourceStream.GetMediaType method (Source.h)</span></span>

<span data-ttu-id="bae8d-104">Die- `GetMediaType` Methode ruft einen bevorzugten Medientyp ab.</span><span class="sxs-lookup"><span data-stu-id="bae8d-104">The `GetMediaType` method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bae8d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bae8d-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="bae8d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bae8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bae8d-107">*pmediatype*</span><span class="sxs-lookup"><span data-stu-id="bae8d-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="bae8d-108">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="bae8d-108">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bae8d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bae8d-109">Return value</span></span>

<span data-ttu-id="bae8d-110">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bae8d-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="bae8d-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bae8d-111">Return code</span></span>                                                                                            | <span data-ttu-id="bae8d-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bae8d-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bae8d-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bae8d-113"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="bae8d-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="bae8d-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="bae8d-115"><dt>**VFW \_ S \_ keine \_ weiteren \_ Elemente**</dt></span><span class="sxs-lookup"><span data-stu-id="bae8d-115"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="bae8d-116">Der Index liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="bae8d-116">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="bae8d-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="bae8d-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="bae8d-118">Index kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="bae8d-118">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="bae8d-119"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="bae8d-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="bae8d-120">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="bae8d-120">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="bae8d-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bae8d-121">Remarks</span></span>

<span data-ttu-id="bae8d-122">Es gibt zwei Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="bae8d-122">There are two versions of this method.</span></span> <span data-ttu-id="bae8d-123">Eine Version überschreibt die [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) -Methode und übernimmt einen Indexwert als Parameter.</span><span class="sxs-lookup"><span data-stu-id="bae8d-123">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="bae8d-124">Die andere Version dient zum Abrufen eines einzelnen Medientyps, sodass der Index-Parameter fehlt.</span><span class="sxs-lookup"><span data-stu-id="bae8d-124">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="bae8d-125">Die Methode mit einem Parameter gibt "E unerwartete" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="bae8d-125">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="bae8d-126">Die zwei-Parameter-Methode überprüft, ob der *iPosition* -Parameter NULL ist, und ruft dann die Einzel Parameter Version auf.</span><span class="sxs-lookup"><span data-stu-id="bae8d-126">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="bae8d-127">Abhängig von der Anzahl der Medientypen, die von der PIN unterstützt werden, müssen Sie eine dieser Methoden überschreiben:</span><span class="sxs-lookup"><span data-stu-id="bae8d-127">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="bae8d-128">Wenn die PIN genau einen Medientyp unterstützt, überschreiben Sie die Einzel Parameter Version.</span><span class="sxs-lookup"><span data-stu-id="bae8d-128">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="bae8d-129">Füllen Sie den Medientyp aus, der von der PIN unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="bae8d-129">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="bae8d-130">Wenn die PIN mehr als einen Medientyp unterstützt, überschreiben Sie die Version mit zwei Parametern.</span><span class="sxs-lookup"><span data-stu-id="bae8d-130">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="bae8d-131">Überschreiben Sie außerdem die [**csourcestream:: checkmediatype**](csourcestream-checkmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bae8d-131">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bae8d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bae8d-132">Requirements</span></span>



| <span data-ttu-id="bae8d-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bae8d-133">Requirement</span></span> | <span data-ttu-id="bae8d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="bae8d-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae8d-135">Header</span><span class="sxs-lookup"><span data-stu-id="bae8d-135">Header</span></span><br/>  | <dl> <span data-ttu-id="bae8d-136"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bae8d-136"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bae8d-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bae8d-137">Library</span></span><br/> | <dl> <span data-ttu-id="bae8d-138">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bae8d-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bae8d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bae8d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bae8d-140">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bae8d-140">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




