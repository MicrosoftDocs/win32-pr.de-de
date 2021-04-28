---
description: 'CTransInPlaceFilter.GetMediaType-Methode: Die GetMediaType-Methode ruft einen bevorzugten Medientyp für den Ausgabepin ab.'
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: CTransInPlaceFilter.GetMediaType-Methode (Transip.h)
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
ms.openlocfilehash: 8678f9b18e40f529da282909015a7c75695770ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094808"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="8991c-103">CTransInPlaceFilter.GetMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="8991c-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="8991c-104">Die `GetMediaType` -Methode ruft einen bevorzugten Medientyp für den Ausgabepin ab.</span><span class="sxs-lookup"><span data-stu-id="8991c-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8991c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8991c-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="8991c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8991c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8991c-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="8991c-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="8991c-108">Nullbasierter Indexwert.</span><span class="sxs-lookup"><span data-stu-id="8991c-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="8991c-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="8991c-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="8991c-110">Zeiger auf ein [**CMediaType-Objekt,**](cmediatype.md) das den Medientyp empfängt.</span><span class="sxs-lookup"><span data-stu-id="8991c-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8991c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8991c-111">Return value</span></span>

<span data-ttu-id="8991c-112">Gibt E \_ UNEXPECTED zurück.</span><span class="sxs-lookup"><span data-stu-id="8991c-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="8991c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8991c-113">Remarks</span></span>

<span data-ttu-id="8991c-114">Diese Methode überschreibt die [**CTransformFilter::GetMediaType-Methode.**](ctransformfilter-getmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="8991c-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="8991c-115">In der **CTransInPlaceFilter-Klasse** ruft jeder Pin den gegenüberliegenden verbundenen Pin auf, um bevorzugte Medientypen zu aufzählen.</span><span class="sxs-lookup"><span data-stu-id="8991c-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="8991c-116">Der Eingabepin ruft den Eingabepin des Downstreamfilters auf, und der Ausgabepin ruft den Ausgabepin des Upstreamfilters auf.</span><span class="sxs-lookup"><span data-stu-id="8991c-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="8991c-117">Daher wird die -Methode `GetMediaType` des Filters nie aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8991c-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="8991c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8991c-118">Requirements</span></span>



| <span data-ttu-id="8991c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8991c-119">Requirement</span></span> | <span data-ttu-id="8991c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8991c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8991c-121">Header</span><span class="sxs-lookup"><span data-stu-id="8991c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8991c-122"><dt>Transip.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8991c-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8991c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8991c-123">Library</span></span><br/> | <dl> <span data-ttu-id="8991c-124"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8991c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8991c-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8991c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8991c-126">**CTransInPlaceFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8991c-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




