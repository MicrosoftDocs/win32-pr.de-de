---
description: 'Die getmediatype-Methode ruft den Medientyp ab, wenn der Medientyp vom vorherigen Beispiel abweicht. Diese Methode implementiert die imediasample:: getmediatype-Methode.'
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Cmediasample. getmediatype-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352910"
---
# <a name="cmediasamplegetmediatype-method"></a><span data-ttu-id="1617f-104">Cmediasample. getmediatype-Methode</span><span class="sxs-lookup"><span data-stu-id="1617f-104">CMediaSample.GetMediaType method</span></span>

<span data-ttu-id="1617f-105">Die- `GetMediaType` Methode ruft den Medientyp ab, wenn der Medientyp vom vorherigen Beispiel abweicht.</span><span class="sxs-lookup"><span data-stu-id="1617f-105">The `GetMediaType` method retrieves the media type, if the media type differs from the previous sample.</span></span> <span data-ttu-id="1617f-106">Diese Methode implementiert die [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1617f-106">This method implements the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1617f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1617f-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="1617f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1617f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1617f-109">*PpMediaType*</span><span class="sxs-lookup"><span data-stu-id="1617f-109">*ppMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="1617f-110">Adresse einer Variablen, die einen Zeiger auf eine [**\_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur von am erhält.</span><span class="sxs-lookup"><span data-stu-id="1617f-110">Address of a variable that receives a pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="1617f-111">Wenn sich der Medientyp nicht im vorherigen Beispiel geändert hat, wird *\* PpMediaType* auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1617f-111">If the media type has not changed from the previous sample, *\*ppMediaType* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1617f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1617f-112">Return value</span></span>

<span data-ttu-id="1617f-113">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1617f-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="1617f-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1617f-114">Return code</span></span>                                                                                   | <span data-ttu-id="1617f-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1617f-115">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="1617f-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="1617f-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="1617f-117">Der Medientyp wurde im vorherigen Beispiel nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="1617f-117">The media type has not changed from the previous sample.</span></span><br/> |
| <dl> <span data-ttu-id="1617f-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1617f-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1617f-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="1617f-119">Success.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="1617f-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1617f-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1617f-121">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1617f-121">Insufficient memory.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="1617f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1617f-122">Remarks</span></span>

<span data-ttu-id="1617f-123">Wenn Sie den Medientyp abgeschlossen haben, geben Sie den Speicherblock frei, indem Sie die Dienstprogramm Funktion [**deletemediatype**](deletemediatype.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1617f-123">When you are done with the media type, free the memory block by calling the [**DeleteMediaType**](deletemediatype.md) utility function.</span></span>

<span data-ttu-id="1617f-124">Die Member-Variable [**cmediasample:: m \_ pmediatype**](cmediasample-m-pmediatype.md) gibt den Medientyp an.</span><span class="sxs-lookup"><span data-stu-id="1617f-124">The [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable specifies the media type.</span></span> <span data-ttu-id="1617f-125">Die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) gibt an, ob sich der Medientyp geändert hat.</span><span class="sxs-lookup"><span data-stu-id="1617f-125">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the media type has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1617f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1617f-126">Requirements</span></span>



| <span data-ttu-id="1617f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1617f-127">Requirement</span></span> | <span data-ttu-id="1617f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="1617f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1617f-129">Header</span><span class="sxs-lookup"><span data-stu-id="1617f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1617f-130"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1617f-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1617f-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1617f-131">Library</span></span><br/> | <dl> <span data-ttu-id="1617f-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1617f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1617f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1617f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1617f-134">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1617f-134">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




