---
description: Wird vom Audiorenderer ausgelöst, wenn das Audiogerät entfernt wird. Der Audiorenderer ist jetzt ungültig.
ms.assetid: a65a3931-e0d6-47ac-b545-9d616e914109
title: MEAudioSessionDeviceRemoved-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c51dbc79550f9f24b3f049f8ee7de7f0554b0f12507c860c88ee273afc5960e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062729"
---
# <a name="meaudiosessiondeviceremoved-event"></a>MEAudioSessionDeviceRemoved-Ereignis

Wird vom Audiorenderer ausgelöst, wenn das Audiogerät entfernt wird. Der Audiorenderer ist jetzt ungültig.

Die Mediensitzung gibt dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE                | Beschreibung                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Keine Ereignisdaten.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Zeiger auf die [**BENUTZEROBERFLÄCHEAudioPolicy-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird von der Streamsenke des Audiorenderers gesendet. Das Ereignis wird ausgelöst, wenn der Audiorenderer ein [**IAudioSessionEvents::OnSessionDisconnected-Ereignis**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) aus der Audiositzung empfängt, bei dem der Grund für die Trennung gleich **DisconnectReasonDeviceRemoval ist.**

Wenn [**festgelegt, ist**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) der ZEIGER FÜR DIE TOOdioPolicy nicht nützlich, da der Audiodatenstrom nicht mehr gültig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
