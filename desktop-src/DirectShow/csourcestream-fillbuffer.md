---
description: Die FillBuffer-Methode füllt ein Medien Beispiel mit Daten.
ms.assetid: dddad8c7-44f1-4ba3-8fb1-7e7e88e40941
title: Csourcestream. FillBuffer-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.FillBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3611ad8b590bb823abccdecf9d3d138c70441a07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371061"
---
# <a name="csourcestreamfillbuffer-method"></a><span data-ttu-id="b2d93-103">Csourcestream. FillBuffer-Methode</span><span class="sxs-lookup"><span data-stu-id="b2d93-103">CSourceStream.FillBuffer method</span></span>

<span data-ttu-id="b2d93-104">Die- `FillBuffer` Methode füllt ein Medien Beispiel mit Daten.</span><span class="sxs-lookup"><span data-stu-id="b2d93-104">The `FillBuffer` method fills a media sample with data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d93-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2d93-105">Syntax</span></span>


```C++
virtual HRESULT FillBuffer(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="b2d93-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2d93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2d93-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="b2d93-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b2d93-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="b2d93-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2d93-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2d93-109">Return value</span></span>

<span data-ttu-id="b2d93-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b2d93-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b2d93-111">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b2d93-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="b2d93-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b2d93-112">Return code</span></span>                                                                             | <span data-ttu-id="b2d93-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b2d93-113">Description</span></span>              |
|-----------------------------------------------------------------------------------------|--------------------------|
| <dl> <span data-ttu-id="b2d93-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b2d93-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="b2d93-115">Ende des Streams</span><span class="sxs-lookup"><span data-stu-id="b2d93-115">End of stream</span></span><br/> |
| <dl> <span data-ttu-id="b2d93-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b2d93-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="b2d93-117">Erfolg</span><span class="sxs-lookup"><span data-stu-id="b2d93-117">Success</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="b2d93-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2d93-118">Remarks</span></span>

<span data-ttu-id="b2d93-119">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="b2d93-119">The derived class must implement this method.</span></span>

<span data-ttu-id="b2d93-120">Das für diese Methode angegebene Medien Beispiel hat keine Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="b2d93-120">The media sample given to this method has no time stamps.</span></span> <span data-ttu-id="b2d93-121">Die abgeleitete Klasse sollte die [**imediasample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) -Methode aufrufen, um die Zeitstempel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b2d93-121">The derived class should call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method to set the time stamps.</span></span> <span data-ttu-id="b2d93-122">Wenn dies für den Medientyp angebracht ist, sollte die abgeleitete Klasse auch die Medien Zeiten festlegen, indem Sie die [**imediasample:: setmediatime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="b2d93-122">If appropriate for the media type, the derived class should also set the media times, by calling the [**IMediaSample::SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) method.</span></span> <span data-ttu-id="b2d93-123">Weitere Informationen finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="b2d93-123">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

<span data-ttu-id="b2d93-124">Gibt "S \_ false" am Ende des Streams zurück.</span><span class="sxs-lookup"><span data-stu-id="b2d93-124">Return S\_FALSE at the end of the stream.</span></span> <span data-ttu-id="b2d93-125">Dies bewirkt, dass die **csourcestream** -Klasse das Ende der Stream-Benachrichtigung sendet und die Puffer Verarbeitungs Schleife stoppt.</span><span class="sxs-lookup"><span data-stu-id="b2d93-125">This causes the **CSourceStream** class to send the end-of-stream notification and halt the buffer processing loop.</span></span> <span data-ttu-id="b2d93-126">Weitere Informationen finden Sie unter [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="b2d93-126">See [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2d93-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2d93-127">Requirements</span></span>



| <span data-ttu-id="b2d93-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2d93-128">Requirement</span></span> | <span data-ttu-id="b2d93-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b2d93-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d93-130">Header</span><span class="sxs-lookup"><span data-stu-id="b2d93-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b2d93-131"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2d93-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b2d93-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2d93-132">Library</span></span><br/> | <dl> <span data-ttu-id="b2d93-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b2d93-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2d93-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2d93-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d93-135">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b2d93-135">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




