---
description: Wird vom Audiorenderer ausgelöst, wenn sich das Audiositzungssymbol ändert.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: MEAudioSessionIconChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ce466cf88b93c9cf806a2a6b70f76b084e8aa0b2c8fb2910a7391337a13b2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062459"
---
# <a name="meaudiosessioniconchanged-event"></a>MEAudioSessionIconChanged-Ereignis

Wird vom Audiorenderer ausgelöst, wenn sich das Audiositzungssymbol ändert.

Die Mediensitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE                | Beschreibung                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Keine Ereignisdaten.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Zeiger auf die [**INTERFACESAudioPolicy-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird von der Streamsenke des Audiorenderers gesendet. Das Ereignis wird ausgelöst, wenn der Audiorenderer ein [**IAudioSessionEvents::OnIconPathChanged-Ereignis**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) aus der Audiositzung empfängt.

Rufen Sie ZUM Abrufen des neuen Symbols [**DEN AUFRUF VONAUDIOPOLICY::GetIconPath auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORCHESTRAAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> <dt>

[StreamingAudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
