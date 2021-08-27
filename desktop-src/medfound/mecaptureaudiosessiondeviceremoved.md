---
description: Wird von einer Audioerfassungsquelle gesendet, wenn das Gerät entfernt wird.
ms.assetid: A249D8B4-15A8-4AD3-8316-2886E5C37825
title: MECaptureAudioSessionDeviceRemoved-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1c3b0e9acbf627800f69ad8ba374edc4b6f075268e61d2c71618c07e8c95645
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114200"
---
# <a name="mecaptureaudiosessiondeviceremoved-event"></a>MECaptureAudioSessionDeviceRemoved-Ereignis

Wird von einer Audioerfassungsquelle gesendet, wenn das Gerät entfernt wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE               | Beschreibung                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird vom Medienstream der Audioerfassungsquelle gesendet.

Die Erfassungsquelle sendet dieses Ereignis, wenn sie ein [**IAudioSessionEvents::OnSessionDisconnected-Ereignis**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) aus der Audiositzung empfängt, deren Trennungsgrund **disconnectreasonDeviceRemoval** entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 
