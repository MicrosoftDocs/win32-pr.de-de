---
description: 'Die setmediatype-Methode legt den Medientyp für das Beispiel fest. Diese Methode implementiert die imediasample:: setmediatype-Methode.'
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Cmediasample. setmediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f46fc4e8c348b1d03d19e815f658e0f637b8f880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357556"
---
# <a name="cmediasamplesetmediatype-method"></a><span data-ttu-id="bb5b5-104">Cmediasample. setmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="bb5b5-104">CMediaSample.SetMediaType method</span></span>

<span data-ttu-id="bb5b5-105">Die- `SetMediaType` Methode legt den Medientyp für das Beispiel fest.</span><span class="sxs-lookup"><span data-stu-id="bb5b5-105">The `SetMediaType` method sets the media type for the sample.</span></span> <span data-ttu-id="bb5b5-106">Diese Methode implementiert die [**imediasample:: setmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bb5b5-106">This method implements the [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb5b5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb5b5-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="bb5b5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb5b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb5b5-109">*pmediatype*</span><span class="sxs-lookup"><span data-stu-id="bb5b5-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="bb5b5-110">Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur.</span><span class="sxs-lookup"><span data-stu-id="bb5b5-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb5b5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb5b5-111">Return value</span></span>

<span data-ttu-id="bb5b5-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="bb5b5-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="bb5b5-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bb5b5-113">Return code</span></span>                                                                                   | <span data-ttu-id="bb5b5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb5b5-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="bb5b5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb5b5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bb5b5-116">Erfolg</span><span class="sxs-lookup"><span data-stu-id="bb5b5-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="bb5b5-117"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="bb5b5-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bb5b5-118">Nicht genügend Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="bb5b5-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb5b5-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb5b5-119">Remarks</span></span>

<span data-ttu-id="bb5b5-120">Diese Methode legt die Member-Variable [**cmediasample:: m \_ pmediatype**](cmediasample-m-pmediatype.md) fest, die den Medientyp angibt, und die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , die angibt, ob sich der Medientyp geändert hat.</span><span class="sxs-lookup"><span data-stu-id="bb5b5-120">This method sets the [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable, which specifies the media type, and the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the media type has changed.</span></span>

<span data-ttu-id="bb5b5-121">Diese Methode erstellt eine Kopie der am- \_ \_ Medientyp Struktur.</span><span class="sxs-lookup"><span data-stu-id="bb5b5-121">This method makes a copy of the AM\_MEDIA\_TYPE structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb5b5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb5b5-122">Requirements</span></span>



| <span data-ttu-id="bb5b5-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb5b5-123">Requirement</span></span> | <span data-ttu-id="bb5b5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="bb5b5-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5b5-125">Header</span><span class="sxs-lookup"><span data-stu-id="bb5b5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bb5b5-126"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb5b5-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bb5b5-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb5b5-127">Library</span></span><br/> | <dl> <span data-ttu-id="bb5b5-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bb5b5-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb5b5-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb5b5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb5b5-130">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bb5b5-130">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




