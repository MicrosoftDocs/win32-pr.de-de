---
description: MEDeviceStreamCreated ist ein erweiterter Medienereignistyp, der mit einem MEUnknown-Medienereignis vom Geräte-MFT generiert wird.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: MEDeviceStreamCreated-Ereignis (mftransform.h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 99e13dae5db9d680909a435d5520f6b07d7d4b6c11782c340b72fcdd0eddc53a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878067"
---
# <a name="medevicestreamcreated-event"></a>MEDeviceStreamCreated-Ereignis

MEDeviceStreamCreated ist ein erweiterter Medienereignistyp, der mit einem MEUnknown-Medienereignis vom Geräte-MFT generiert wird.

Dieser Ereignistyp für erweiterte Medien hat keine Nutzlast.  Das entsprechende HRESULT sollte über die [**METHODE VONMEDIAEVENT::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) bereitgestellt werden.




## <a name="remarks"></a>Hinweise

Dieses erweiterte Medienereignis muss vom Geräte-MFT als Teil der Medientypauswahl im Ausgabestream des DMFT gesendet werden.  Wenn SetOutputStreamState für die SCHNITTSTELLE "SIGNALSDeviceTransform" aufgerufen wird, ist der DMFT dafür verantwortlich, die Änderung der erforderlichen Eingabestreamzustände mit dem [METransformInputStreamStateChanged-Medienereignis](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) zu signalisieren. Wenn die Änderung des Eingabedatenstromzustands von der Pipeline mit dem Aufruf von SetInputStreamState des DMFT bestätigt wurde, ist der DMFT dafür verantwortlich, die interne Zustandskonfiguration abzuschließen und den Ereignistyp **MEDeviceStreamCreated** für erweiterte Medien auszugeben.

Wenn dieser Ereignistyp für erweiterte Medien nicht ausgelöst wird, übermittelt der Gerätetransformations-Manager keine Eingabeframes an den DMFT.
Der Ereignistyp "Erweiterte Medien" muss auch als Attribut des ATTRIBUTSMEDIAEVENT festgelegt werden, die Ausgabestream-ID mithilfe des **MF_EVENT_MFT_INPUT_STREAM_ID** Attributs.

```cpp
IMFMediaEvent* pMediaEvent = nullptr;

hr = MFCreateMediaEvent (MEUnknown,
                         MEDeviceStreamCreated,
                         S_OK,
                         nullptr,
                         &pMediaEvent);
if (SUCCEEDED(hr))
{
    hr = pMediaEvent->SetUINT32(MF_EVENT_MFT_INPUT_STREAM_ID, GetOutputStreamId());
}

if (SUCCEEDED(hr))
{
    hr = m_pEventQueue->QueueEvent(pMediaEvent);
}

if (nullptr != pMediaEvent)
{
    pMediaEvent->Release();
    pMediaEvent = nullptr;
}

return hr;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>mftransform.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[StreamingAudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
