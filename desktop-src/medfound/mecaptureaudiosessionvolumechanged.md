---
description: Wird von einer Audioaufnahmequelle gesendet, wenn sich das Volume ändert.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: MECaptureAudioSessionVolumeChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f2e83bdf03f61abac733a5e06310ff12c0797664d6a2405aed97210bf5ff42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878081"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a>MECaptureAudioSessionVolumeChanged-Ereignis

Wird von einer Audioaufnahmequelle gesendet, wenn sich das Volume ändert.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE               | Beschreibung                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Dieses Ereignis wird vom Medienstream der Audioaufnahmequelle gesendet.

Die Audioaufnahmequelle sendet dieses Ereignis, wenn eine externe Aktion das Volume ändert, z. B. wenn der Benutzer das Volume über die Systemsteuerung ändert. Die Erfassungsquelle sendet das Ereignis nicht, wenn die Anwendung das Volume direkt auf der Quelle ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




