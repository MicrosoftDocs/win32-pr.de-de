---
description: Wird vom Audiorenderer ausgelöst, wenn sich das Standardaudioformat für das Audiogerät ändert. Der Audiorenderer ist jetzt ungültig.
ms.assetid: eeef764a-f6d2-4f6e-9af3-acd5fd7bc55c
title: MEAudioSessionFormatChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab0464aa4bd98ec0143838762ac3fcc3efd88e03528b1d5732e2d5423a711640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013870"
---
# <a name="meaudiosessionformatchanged-event"></a>MEAudioSessionFormatChanged-Ereignis

Wird vom Audiorenderer ausgelöst, wenn sich das Standardaudioformat für das Audiogerät ändert. Der Audiorenderer ist jetzt ungültig.

Die Mediensitzung gibt dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE                | Beschreibung                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Keine Ereignisdaten.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Zeiger auf die [**BENUTZEROBERFLÄCHEAudioPolicy-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird von der Streamsenke des Audiorenderers gesendet. Das Ereignis wird ausgelöst, wenn der Audiorenderer ein [**IAudioSessionEvents::OnSessionDisconnected-Ereignis**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) aus der Audiositzung im Benutzermodus empfängt, deren Trennungsgrund **disconnectreasonFormatChanged** entspricht.

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

 

 
