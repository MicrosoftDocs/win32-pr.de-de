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
# <a name="mebufferingstarted-event"></a>Mebufferingstarted-Ereignis

Signalisiert, dass eine Medienquelle mit dem Puffern von Daten begonnen hat.

Eine Medienquelle kann dieses Ereignis senden, wenn die Quelle Daten puffert, während die Medien Sitzung ausgeführt wird. Wenn die Medien Sitzung dieses Ereignis empfängt, hält Sie die Präsentationszeit an, bis die Medienquelle das [mebufferingbeendete](mebufferingstopped.md) -Ereignis sendet. Die Medien Sitzung leitet auch das mebufferingstarted-Ereignis an die Anwendung weiter.

Bytestreams, die die [**IMF bytestreambufferate**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) -Schnittstelle implementieren, senden ebenfalls dieses Ereignis.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Wenn eine Medienquelle das mebufferingstarted-Ereignis sendet, muss das Ereignis " [mebufferingbeendeten](mebufferingstopped.md) " gesendet werden, wenn die Daten Pufferung beendet werden. Die Medienquelle muss ein entsprechendes mebufferingstarted-Ereignis für jedes mebufferingstarted-Ereignis senden. Die Medienquelle sollte diese Ereignisse nicht weiterleiten, bevor die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode der Quelle aufgerufen wird, oder nachdem die [**imfmediasource:: stopenmethode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) der Quelle aufgerufen wurde.

Wenn Sie ein Streaming von der Media Foundation Netzwerkquelle durchgeführt haben, können Sie den Puffer Status abrufen, indem Sie die **MF NetSource \_ bufferprogress \_ ID** -Statistik Abfragen. Weitere Informationen finden Sie unter [**MF-Quell \_ Statistik- \_ IDs**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




