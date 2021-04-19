---
description: Die checkstreamstate-Methode bestimmt, ob ein Medien Beispiel übermittelt oder verworfen werden soll.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Cbasestreamcontrol. checkstreamstate-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352916"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a><span data-ttu-id="f6fa1-103">Cbasestreamcontrol. checkstreamstate-Methode</span><span class="sxs-lookup"><span data-stu-id="f6fa1-103">CBaseStreamControl.CheckStreamState method</span></span>

<span data-ttu-id="f6fa1-104">Die- `CheckStreamState` Methode bestimmt, ob ein Medien Beispiel übermittelt oder verworfen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-104">The `CheckStreamState` method determines whether a media sample should be delivered or discarded.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6fa1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6fa1-105">Syntax</span></span>


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="f6fa1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6fa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6fa1-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="f6fa1-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="f6fa1-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6fa1-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6fa1-109">Return value</span></span>

<span data-ttu-id="f6fa1-110">Gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-110">Returns one of the following values.</span></span>



| <span data-ttu-id="f6fa1-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f6fa1-111">Return code</span></span>                                                                                       | <span data-ttu-id="f6fa1-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6fa1-112">Description</span></span>                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="f6fa1-113"><dt>**Stream- \_ verwerfen**</dt></span><span class="sxs-lookup"><span data-stu-id="f6fa1-113"><dt>**STREAM\_DISCARDING**</dt></span></span> </dl> | <span data-ttu-id="f6fa1-114">Verwerfen Sie dieses Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-114">Discard this sample.</span></span><br/> |
| <dl> <span data-ttu-id="f6fa1-115"><dt>**Stream \_ fließt**</dt></span><span class="sxs-lookup"><span data-stu-id="f6fa1-115"><dt>**STREAM\_FLOWING**</dt></span></span> </dl>    | <span data-ttu-id="f6fa1-116">Liefern Sie dieses Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-116">Deliver this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f6fa1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6fa1-117">Remarks</span></span>

<span data-ttu-id="f6fa1-118">Ruft diese Methode auf, wenn Ihre PIN ein Beispiel empfängt.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-118">Call this method when your pin receives a sample.</span></span> <span data-ttu-id="f6fa1-119">Übermitteln Sie das Beispiel nur dann, wenn der Rückgabewert Stream \_ fließt.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-119">Deliver the sample only if the return value is STREAM\_FLOWING.</span></span> <span data-ttu-id="f6fa1-120">Wenn der Rückgabewert Stream- \_ verwerfen ist, verwerfen Sie das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-120">If the return value is STREAM\_DISCARDING, discard the sample.</span></span>

<span data-ttu-id="f6fa1-121">Wenn die PIN Beispiele verwirft, sollte das nächste Beispiel, das es als Diskontinuität bereitstellt, durch Aufrufen der [**imediasample:: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) -Methode gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-121">If the pin discards any samples, it should mark the next sample that it delivers as a discontinuity, by calling the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="f6fa1-122">Wenn Ihr Filter die [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) -Schnittstelle implementiert, um zu zählen, wie viele Frames Sie löscht, zählen Sie keinen verworfenen Frame als einen gelöschten Frame.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-122">If your filter implements the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface to count how many frames it drops, do not count a discarded frame as a dropped frame.</span></span>

<span data-ttu-id="f6fa1-123">Wenn der Rückgabewert Stream \_ -verwerfen ist, wird die-Methode blockiert, bis die Verweis Zeit die Startzeit des Beispiels erreicht.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-123">When the return value is STREAM\_DISCARDING, the method blocks until the reference time reaches the sample's start time.</span></span> <span data-ttu-id="f6fa1-124">Dadurch wird verhindert, dass Ihre PIN die Stichproben zu schnell verwerfen.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-124">This prevents your pin from discarding samples too quickly.</span></span> <span data-ttu-id="f6fa1-125">Wenn der Filter angehalten ist, ist die Wartezeit unendlich, bis der Filter ausgeführt, beendet oder leert.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-125">If the filter is paused, the wait time is infinite, until the filter runs, stops, or flushes data.</span></span> <span data-ttu-id="f6fa1-126">(Filter Zustandsänderungen und Streaming erfolgen in separaten Threads, sodass dies keinen Deadlock verursacht.)</span><span class="sxs-lookup"><span data-stu-id="f6fa1-126">(Filter state changes and streaming happen on separate threads, so this does not cause any deadlock.)</span></span>

<span data-ttu-id="f6fa1-127">Die **cbasestreamcontrol:: streamcontrolstate** -Enumeration ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="f6fa1-127">The **CBaseStreamControl::StreamControlState** enumeration is defined as follows:</span></span>


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a><span data-ttu-id="f6fa1-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6fa1-128">Examples</span></span>

<span data-ttu-id="f6fa1-129">Im folgenden Beispiel wird davon ausgegangen, dass die PIN eine Member-Variable mit dem Namen m \_ flastsampleverworfen verwendet, um Diskontinuitäten nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="f6fa1-129">The following example assumes that the pin uses a member variable named m\_fLastSampleDiscarded to keep track of discontinuities.</span></span>


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="f6fa1-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6fa1-130">Requirements</span></span>



| <span data-ttu-id="f6fa1-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6fa1-131">Requirement</span></span> | <span data-ttu-id="f6fa1-132">Wert</span><span class="sxs-lookup"><span data-stu-id="f6fa1-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6fa1-133">Header</span><span class="sxs-lookup"><span data-stu-id="f6fa1-133">Header</span></span><br/>  | <dl> <span data-ttu-id="f6fa1-134"><dt>"Strauch. h" (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6fa1-134"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f6fa1-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f6fa1-135">Library</span></span><br/> | <dl> <span data-ttu-id="f6fa1-136">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f6fa1-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6fa1-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6fa1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6fa1-138">**Cbasestreamcontrol-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f6fa1-138">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




