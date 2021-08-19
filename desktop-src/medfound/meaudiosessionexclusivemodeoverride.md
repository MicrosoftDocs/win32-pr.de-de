---
description: Wird vom Audiorenderer ausgelöst, wenn die Audiositzung durch eine Verbindung im exklusiven Modus vorzeitig beendet wird. Der Audiorenderer ist jetzt ungültig.
ms.assetid: f89acfe4-14a7-4051-a816-e5e0ba8db80a
title: MEAudioSessionExclusiveModeOverride-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6344a5d073e9dc29777e6cb181c77bcae79da8602b830ade86646459e4d0bea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114220"
---
# <a name="meaudiosessionexclusivemodeoverride-event"></a>MEAudioSessionExclusiveModeOverride-Ereignis

Wird vom Audiorenderer ausgelöst, wenn die Audiositzung durch eine Verbindung im exklusiven Modus vorzeitig beendet wird. Der Audiorenderer ist jetzt ungültig.

Die Mediensitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE                | BESCHREIBUNG                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Keine Ereignisdaten.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Zeiger auf die [**INTERFACESAudioPolicy-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird von der Streamsenke des Audiorenderers gesendet. Das Ereignis wird ausgelöst, wenn der Audiorenderer ein [**IAudioSessionEvents::OnSessionDisconnected-Ereignis**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) aus der Audiositzung empfängt, wobei der Grund für die Trennung gleich DisconnectReasonExclusiveModeOverride ist.

Der [**CURSORAUDIOPOLICY-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) ist, falls festgelegt, nicht nützlich, da der Audiostream nicht mehr gültig ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> <dt>

[StreamingAudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
