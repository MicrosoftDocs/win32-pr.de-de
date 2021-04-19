---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp für die Ausgabepin ab.
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Ctransformfilter. getmediatype-Methode (Transfrm. h)
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
ms.openlocfilehash: ba751e291a1ffa8e030be7e77cfd456956718baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361634"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="0fb47-103">Ctransformfilter. getmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="0fb47-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="0fb47-104">Die- `GetMediaType` Methode ruft einen bevorzugten Medientyp für die Ausgabepin ab.</span><span class="sxs-lookup"><span data-stu-id="0fb47-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb47-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fb47-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="0fb47-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fb47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fb47-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="0fb47-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="0fb47-108">NULL basierter Indexwert.</span><span class="sxs-lookup"><span data-stu-id="0fb47-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="0fb47-109">*pmediatype*</span><span class="sxs-lookup"><span data-stu-id="0fb47-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="0fb47-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="0fb47-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fb47-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fb47-111">Return value</span></span>

<span data-ttu-id="0fb47-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0fb47-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0fb47-113">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fb47-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0fb47-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0fb47-114">Return code</span></span>                                                                                            | <span data-ttu-id="0fb47-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fb47-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0fb47-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0fb47-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="0fb47-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="0fb47-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="0fb47-118"><dt>**VFW \_ S \_ keine \_ weiteren \_ Elemente**</dt></span><span class="sxs-lookup"><span data-stu-id="0fb47-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="0fb47-119">Der Index liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="0fb47-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="0fb47-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="0fb47-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="0fb47-121">Index kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0fb47-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0fb47-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fb47-122">Remarks</span></span>

<span data-ttu-id="0fb47-123">Die [**ctransformoutputpin:: getmediatype**](ctransformoutputpin-getmediatype.md) -Methode der Ausgabe-PIN ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="0fb47-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="0fb47-124">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="0fb47-124">The derived class must implement this method.</span></span> <span data-ttu-id="0fb47-125">Weitere Informationen finden Sie unter [**cbasepin:: getmediatype**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="0fb47-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb47-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fb47-126">Requirements</span></span>



| <span data-ttu-id="0fb47-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fb47-127">Requirement</span></span> | <span data-ttu-id="0fb47-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0fb47-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb47-129">Header</span><span class="sxs-lookup"><span data-stu-id="0fb47-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0fb47-130"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0fb47-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0fb47-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0fb47-131">Library</span></span><br/> | <dl> <span data-ttu-id="0fb47-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0fb47-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fb47-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fb47-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb47-134">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0fb47-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




