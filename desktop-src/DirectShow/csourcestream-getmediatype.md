---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp ab. Diese Methode verwendet die Parameter *iPosition* und *pmediatype* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Csourcestream. getmediatype-Methode (Source. h)-iPosition-und pmediatype-Parameter
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
ms.openlocfilehash: 9d8936f08b952af069812859736a6a13ea9c0e4e
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106372538"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a><span data-ttu-id="55906-104">Csourcestream. getmediatype-Methode (Source. h)-iPosition-und pmediatype-Parameter</span><span class="sxs-lookup"><span data-stu-id="55906-104">CSourceStream.GetMediaType method (Source.h) - iPosition and pMediaType parameters</span></span>

<span data-ttu-id="55906-105">Die **getmediatype** -Methode ruft einen bevorzugten Medientyp ab.</span><span class="sxs-lookup"><span data-stu-id="55906-105">The **GetMediaType** method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="55906-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="55906-106">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="55906-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="55906-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55906-108">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="55906-108">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="55906-109">NULL basierter Indexwert.</span><span class="sxs-lookup"><span data-stu-id="55906-109">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="55906-110">*pmediatype*</span><span class="sxs-lookup"><span data-stu-id="55906-110">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="55906-111">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="55906-111">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55906-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55906-112">Return value</span></span>

<span data-ttu-id="55906-113">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="55906-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="55906-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="55906-114">Return code</span></span>                                                                                            | <span data-ttu-id="55906-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55906-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="55906-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55906-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="55906-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="55906-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="55906-118"><dt>**VFW \_ S \_ keine \_ weiteren \_ Elemente**</dt></span><span class="sxs-lookup"><span data-stu-id="55906-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="55906-119">Der Index liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="55906-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="55906-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="55906-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="55906-121">Index kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="55906-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="55906-122"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="55906-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="55906-123">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="55906-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="55906-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55906-124">Remarks</span></span>

<span data-ttu-id="55906-125">Es gibt zwei Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="55906-125">There are two versions of this method.</span></span> <span data-ttu-id="55906-126">Eine Version überschreibt die [**cbasepin:: getmediatype**](cbasepin-getmediatype.md) -Methode und übernimmt einen Indexwert als Parameter.</span><span class="sxs-lookup"><span data-stu-id="55906-126">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="55906-127">Die andere Version dient zum Abrufen eines einzelnen Medientyps, sodass der Index-Parameter fehlt.</span><span class="sxs-lookup"><span data-stu-id="55906-127">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="55906-128">Die Methode mit einem Parameter gibt "E unerwartete" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="55906-128">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="55906-129">Die zwei-Parameter-Methode überprüft, ob der *iPosition* -Parameter NULL ist, und ruft dann die Einzel Parameter Version auf.</span><span class="sxs-lookup"><span data-stu-id="55906-129">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="55906-130">Abhängig von der Anzahl der Medientypen, die von der PIN unterstützt werden, müssen Sie eine dieser Methoden überschreiben:</span><span class="sxs-lookup"><span data-stu-id="55906-130">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="55906-131">Wenn die PIN genau einen Medientyp unterstützt, überschreiben Sie die Einzel Parameter Version.</span><span class="sxs-lookup"><span data-stu-id="55906-131">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="55906-132">Füllen Sie den Medientyp aus, der von der PIN unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="55906-132">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="55906-133">Wenn die PIN mehr als einen Medientyp unterstützt, überschreiben Sie die Version mit zwei Parametern.</span><span class="sxs-lookup"><span data-stu-id="55906-133">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="55906-134">Überschreiben Sie außerdem die [**csourcestream:: checkmediatype**](csourcestream-checkmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="55906-134">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="55906-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55906-135">Requirements</span></span>



| <span data-ttu-id="55906-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55906-136">Requirement</span></span> | <span data-ttu-id="55906-137">Wert</span><span class="sxs-lookup"><span data-stu-id="55906-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55906-138">Header</span><span class="sxs-lookup"><span data-stu-id="55906-138">Header</span></span>  | <span data-ttu-id="55906-139">Source. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="55906-139">Source.h (include Streams.h)</span></span>                                                                                    |
| <span data-ttu-id="55906-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="55906-140">Library</span></span> | <span data-ttu-id="55906-141">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="55906-141">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="55906-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55906-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55906-143">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="55906-143">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




