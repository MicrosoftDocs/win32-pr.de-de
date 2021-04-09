---
description: Wird von einer audioerfassungs Quelle gesendet, wenn die audioumzierung getrennt wird, weil der Benutzer von einer Windows-Terminal Dienste-Sitzung (WTS) abgemeldet wurde.
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Mecaptureaudiosessiongetrennte-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae45ecded4a2a412525da70133845c2487aa604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130036"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a>Mecaptureaudiosessiongetrennte-Ereignis

Wird von einer audioerfassungs Quelle gesendet, wenn die audioumzierung getrennt wird, weil der Benutzer von einer Windows-Terminal Dienste-Sitzung (WTS) abgemeldet wurde.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE               | BESCHREIBUNG                           |
|-----------------------|---------------------------------------|
| VT \_ leer <br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird vom Mediendaten Strom der audioerfassungs Quelle gesendet.

Die Erfassungs Quelle sendet dieses Ereignis, wenn es ein [**iaudiosessionevents:: onsessiongetrennte**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) -Ereignis von der Audiositzung empfängt, bei der der Trennungsgrund " **disconnecsquonsessiongetrennte**" entspricht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 
