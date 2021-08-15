---
description: Wird vom Streamingaudiorenderer (SAR) gesendet, wenn sich die Lautstärke oder der Stummschaltungszustand der Audiositzung ändert.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: MEAudioSessionVolumeChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721de9751cac284cb25d390d948f0f686447c04eaa613c1fecd4bf3503bce76d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465400"
---
# <a name="meaudiosessionvolumechanged-event"></a>MEAudioSessionVolumeChanged-Ereignis

Wird vom Streamingaudiorenderer (SAR) gesendet, wenn sich die Lautstärke oder der Stummschaltungszustand der Audiositzung ändert.

Die Mediensitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE                | BESCHREIBUNG                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/>   | Keine Ereignisdaten.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Zeiger auf die [**INTERFACESAudioPolicy-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird von der Streamsenke der SAR ausgelöst. Das Ereignis wird ausgelöst, wenn die SAR ein [**IAudioSessionEvents::OnSimpleVolumeChanged-Ereignis**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) aus der Audiositzung empfängt. Rufen Sie ZUM Abrufen der neuen Volumeebene und des stummgeschalteten [**Zustands DIE AUFRUFESIMPLEAudioVolume::GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) und [**DIESimpleAudioVolume::GetMute**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute)auf.

Die SAR sendet dieses Ereignis, wenn eine externe Aktion das Volume ändert, z. B. wenn der Benutzer das Volume über das Systemvolume-Steuerungsprogramm (SndVol) ändert. Die SAR sendet das Ereignis nicht, wenn die Anwendung das Volume direkt auf dem SAR ändert.

Außerdem sendet die SAR dieses Ereignis nicht, wenn sich das Kanalvolume ändert ([**IAudioSessionEvents::OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[StreamingAudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
