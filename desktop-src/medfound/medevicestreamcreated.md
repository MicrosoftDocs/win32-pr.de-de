---
description: Medevicestreamcreated ist ein erweiterter Medien Ereignistyp, der vom Geräte-MFT mit einem meunknown-Medienereignis generiert wurde.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Mede vicestreamcreated-Ereignis (MF Transform. h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 632ebc305473cd596656a21f562be25d53c2bace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214888"
---
# <a name="medevicestreamcreated-event"></a>Mede vicestreamcreated-Ereignis

Medevicestreamcreated ist ein erweiterter Medien Ereignistyp, der vom Geräte-MFT mit einem meunknown-Medienereignis generiert wurde.

Dieser erweiterte Medien Ereignistyp hat keine Nutzlast.  Ein entsprechendes HRESULT sollte über die [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) -Methode bereitgestellt werden.




## <a name="remarks"></a>Bemerkungen

Dieses erweiterte Medienereignis muss von der MFT des Geräts als Teil der Medientyp Auswahl im Ausgabestream der DMFT gesendet werden.  Wenn setoutputstreamstate auf der imfdevicetransform-Schnittstelle aufgerufen wird, ist die DMFT für das signalisieren der Änderung in den erforderlichen eingabestreamzuständen mit dem [metransforminputstreamstatechanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) -Medienereignis verantwortlich. Wenn die eingabestreamstatusänderung von der Pipeline mit dem Aufrufs von "endputstreamstate" der DMFT bestätigt wurde, ist die DMFT dafür zuständig, die interne Zustands Konfiguration abzuschließen und den Ereignis Typ " **medevicestreamcreated** Extended Media" zu erhöhen.

Wenn dieser erweiterte Medien Ereignistyp nicht ausgelöst wird, stellt der geräteregistrierungs-Manager keine Eingabe Frames für die DMFT bereit.
Der Extended Media-Ereignistyp muss auch als Attribut von IMF Media Event festgelegt werden, der Ausgabestream-ID unter Verwendung des **MF_EVENT_MFT_INPUT_STREAM_ID** -Attributs.

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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>"MF Transform. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
