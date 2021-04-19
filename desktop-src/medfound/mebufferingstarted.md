---
description: Signalisiert, dass eine Medienquelle mit dem Puffern von Daten begonnen hat.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Mebufferingstarted-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb3baf8e66d44eb67ee4c1bbc54ae2e197db081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345798"
---
# <a name="mebufferingstarted-event"></a><span data-ttu-id="5e830-103">Mebufferingstarted-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5e830-103">MEBufferingStarted event</span></span>

<span data-ttu-id="5e830-104">Signalisiert, dass eine Medienquelle mit dem Puffern von Daten begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="5e830-104">Signals that a media source has started to buffer data.</span></span>

<span data-ttu-id="5e830-105">Eine Medienquelle kann dieses Ereignis senden, wenn die Quelle Daten puffert, während die Medien Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e830-105">A media source can send this event if the source buffers data while the Media Session is running.</span></span> <span data-ttu-id="5e830-106">Wenn die Medien Sitzung dieses Ereignis empfängt, hält Sie die Präsentationszeit an, bis die Medienquelle das [mebufferingbeendete](mebufferingstopped.md) -Ereignis sendet.</span><span class="sxs-lookup"><span data-stu-id="5e830-106">When the Media Session receives this event, it pauses the presentation clock until the media source sends the [MEBufferingStopped](mebufferingstopped.md) event.</span></span> <span data-ttu-id="5e830-107">Die Medien Sitzung leitet auch das mebufferingstarted-Ereignis an die Anwendung weiter.</span><span class="sxs-lookup"><span data-stu-id="5e830-107">The Media Session also forwards the MEBufferingStarted event to the application.</span></span>

<span data-ttu-id="5e830-108">Bytestreams, die die [**IMF bytestreambufferate**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) -Schnittstelle implementieren, senden ebenfalls dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="5e830-108">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="5e830-109">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="5e830-109">Event values</span></span>

<span data-ttu-id="5e830-110">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="5e830-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5e830-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5e830-111">VARTYPE</span></span>              | <span data-ttu-id="5e830-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e830-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5e830-113">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="5e830-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5e830-114">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="5e830-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5e830-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e830-115">Remarks</span></span>

<span data-ttu-id="5e830-116">Wenn eine Medienquelle das mebufferingstarted-Ereignis sendet, muss das Ereignis " [mebufferingbeendeten](mebufferingstopped.md) " gesendet werden, wenn die Daten Pufferung beendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e830-116">If a media source sends the MEBufferingStarted event, it must send the [MEBufferingStopped](mebufferingstopped.md) event when it stops buffering data.</span></span> <span data-ttu-id="5e830-117">Die Medienquelle muss ein entsprechendes mebufferingstarted-Ereignis für jedes mebufferingstarted-Ereignis senden.</span><span class="sxs-lookup"><span data-stu-id="5e830-117">The media source must send a matching MEBufferingStopped event for every MEBufferingStarted event.</span></span> <span data-ttu-id="5e830-118">Die Medienquelle sollte diese Ereignisse nicht weiterleiten, bevor die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode der Quelle aufgerufen wird, oder nachdem die [**imfmediasource:: stopenmethode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) der Quelle aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5e830-118">The media source should not forward these events before the source's [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called, or after the source's [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method is called.</span></span>

<span data-ttu-id="5e830-119">Wenn Sie ein Streaming von der Media Foundation Netzwerkquelle durchgeführt haben, können Sie den Puffer Status abrufen, indem Sie die **MF NetSource \_ bufferprogress \_ ID** -Statistik Abfragen.</span><span class="sxs-lookup"><span data-stu-id="5e830-119">If you are streaming from the Media Foundation network source, you can get the buffering progress by querying the **MFNETSOURCE\_BUFFERPROGRESS\_ID** statistic.</span></span> <span data-ttu-id="5e830-120">Weitere Informationen finden Sie unter [**MF-Quell \_ Statistik- \_ IDs**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="5e830-120">For more information, see [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>

## <a name="examples"></a><span data-ttu-id="5e830-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e830-121">Examples</span></span>


```C++
HRESULT GetBufferProgress(IMFMediaSession *pSession, DWORD *pProgress)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_BUFFERPROGRESS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pProgress = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="5e830-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e830-122">Requirements</span></span>



| <span data-ttu-id="5e830-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e830-123">Requirement</span></span> | <span data-ttu-id="5e830-124">Wert</span><span class="sxs-lookup"><span data-stu-id="5e830-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e830-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e830-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5e830-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e830-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5e830-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e830-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5e830-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e830-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e830-129">Header</span><span class="sxs-lookup"><span data-stu-id="5e830-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e830-130"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e830-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e830-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e830-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e830-132">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e830-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="5e830-133">Netzwerk in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5e830-133">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




