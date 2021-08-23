---
description: Signalisiert, dass eine Medienquelle begonnen hat, Daten zu puffern.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: MEBufferingStarted-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55a691b723fc2e09487752ee8f5226e32504d60a6d68a4652bbb2b5b3e5aa7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724270"
---
# <a name="mebufferingstarted-event"></a>MEBufferingStarted-Ereignis

Signalisiert, dass eine Medienquelle begonnen hat, Daten zu puffern.

Eine Medienquelle kann dieses Ereignis senden, wenn die Quelle Daten puffert, während die Mediensitzung ausgeführt wird. Wenn die Mediensitzung dieses Ereignis empfängt, wird die Präsentationsuhr angehalten, bis die Medienquelle das [MEBufferingStopped-Ereignis](mebufferingstopped.md) sendet. Die Mediensitzung leitet auch das MEBufferingStarted-Ereignis an die Anwendung weiter.

Bytestreams, die die [**INTERFACESByteStreamBuffering-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) implementieren, senden auch dieses Ereignis.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Wenn eine Medienquelle das MEBufferingStarted-Ereignis sendet, muss sie das [MEBufferingStopped-Ereignis](mebufferingstopped.md) senden, wenn das Puffern von Daten beendet wird. Die Medienquelle muss für jedes MEBufferingStarted-Ereignis ein entsprechendes MEBufferingStopped-Ereignis senden. Diese Ereignisse sollten von der Medienquelle nicht weitergeleitet werden, bevor die [**METHODE "CSVMediaSource::Start"**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) der Quelle aufgerufen wird oder nachdem die [**METHODE "WFMediaSource::Stop"**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) der Quelle aufgerufen wurde.

Wenn Sie von der Media Foundation Netzwerkquelle streamen, können Sie den Pufferfortschritt abrufen, indem Sie die **STATISTIK MFNETSOURCE \_ BUFFERPROGRESS \_ ID** abfragen. Weitere Informationen finden Sie unter [**MFNETSOURCE \_ STATISTICS \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

## <a name="examples"></a>Beispiele


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




