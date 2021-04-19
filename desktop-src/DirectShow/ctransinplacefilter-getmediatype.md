---
description: Die getmediatype-Methode ruft einen bevorzugten Medientyp für die Ausgabepin ab.
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Ctransinplacefilter. getmediatype-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2347e0466a7df848e0f0b2bccec325eedfefc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365998"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="ff5c2-103">Ctransinplacefilter. getmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="ff5c2-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="ff5c2-104">Die- `GetMediaType` Methode ruft einen bevorzugten Medientyp für die Ausgabepin ab.</span><span class="sxs-lookup"><span data-stu-id="ff5c2-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff5c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff5c2-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="ff5c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff5c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff5c2-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="ff5c2-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="ff5c2-108">NULL basierter Indexwert.</span><span class="sxs-lookup"><span data-stu-id="ff5c2-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="ff5c2-109">*pmediatype*</span><span class="sxs-lookup"><span data-stu-id="ff5c2-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="ff5c2-110">Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt, das den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="ff5c2-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff5c2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff5c2-111">Return value</span></span>

<span data-ttu-id="ff5c2-112">Gibt "E unerwartete" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="ff5c2-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff5c2-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff5c2-113">Remarks</span></span>

<span data-ttu-id="ff5c2-114">Diese Methode überschreibt die [**ctransformfilter:: getmediatype**](ctransformfilter-getmediatype.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ff5c2-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="ff5c2-115">In der **ctransinplacefilter** -Klasse ruft jede PIN die entgegengesetzte verbundene PIN auf, um bevorzugte Medientypen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="ff5c2-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="ff5c2-116">Die Eingabe-PIN Ruft die Eingabe-PIN des downstreamfilters auf, und die Ausgabe-PIN Ruft die Ausgabepin des Upstream-Filters auf.</span><span class="sxs-lookup"><span data-stu-id="ff5c2-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="ff5c2-117">Daher wird die-Methode des Filters `GetMediaType` nie aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ff5c2-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff5c2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff5c2-118">Requirements</span></span>



| <span data-ttu-id="ff5c2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff5c2-119">Requirement</span></span> | <span data-ttu-id="ff5c2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ff5c2-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff5c2-121">Header</span><span class="sxs-lookup"><span data-stu-id="ff5c2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ff5c2-122"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff5c2-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff5c2-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff5c2-123">Library</span></span><br/> | <dl> <span data-ttu-id="ff5c2-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ff5c2-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff5c2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff5c2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff5c2-126">**Ctransinplacefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ff5c2-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




