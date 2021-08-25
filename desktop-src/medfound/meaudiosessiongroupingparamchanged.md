---
description: Wird vom Audiorenderer ausgelöst, wenn sich die Gruppierungsparameter für die Audiositzung ändern.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: MEAudioSessionGroupingParamChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9a271ebaa4e3a0044dc425de2d6a7f313e17d63c693acede63773e94619c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957510"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a>MEAudioSessionGroupingParamChanged-Ereignis

Wird vom Audiorenderer ausgelöst, wenn sich die Gruppierungsparameter für die Audiositzung ändern.

Die Mediensitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE                | Beschreibung                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Zeiger auf die [**INTERFACESAudioPolicy-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird von der Streamsenke des Audiorenderers gesendet. Das Ereignis wird ausgelöst, wenn der Audiorenderer ein [**IAudioSessionEvents::OnGroupingParamChanged-Ereignis**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) aus der Audiositzung empfängt.

Rufen Sie ZUM Abrufen der neuen Gruppierungsparameter [**DEN AUFRUF VONAUDIOPOLICY::GetGroupingParam auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)

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

[**ORCHESTRAAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[StreamingAudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
