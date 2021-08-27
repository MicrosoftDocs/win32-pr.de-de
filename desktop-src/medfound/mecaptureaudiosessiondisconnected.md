---
description: Wird von einer Audioaufnahmequelle gesendet, wenn die Audiodesion getrennt wird, da sich der Benutzer von einer Windows-Terminal Services-Sitzung (WTS) abgemeldet hat.
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: MECaptureAudioSessionDisconnected-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567df4839776ecacb5e25992f5f8cef4795186cffc53fb8abb433418066f3c40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114170"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a>MECaptureAudioSessionDisconnected-Ereignis

Wird von einer Audioaufnahmequelle gesendet, wenn die Audiodesion getrennt wird, da sich der Benutzer von einer Windows-Terminal Services-Sitzung (WTS) abgemeldet hat.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE               | BESCHREIBUNG                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird vom Medienstream der Audioaufnahmequelle gesendet.

Die Erfassungsquelle sendet dieses Ereignis, wenn sie ein [**IAudioSessionEvents::OnSessionDisconnected-Ereignis**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) aus der Audiositzung empfängt, wobei der Grund für die Trennung gleich **DisconnectReasonSessionDisconnected ist.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 
