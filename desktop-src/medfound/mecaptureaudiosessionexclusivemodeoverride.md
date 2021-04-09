---
description: Wird von einer audioerfassungs Quelle gesendet, wenn das Audiogerät von einem anderen Programm im exklusiven Modus geöffnet wird.
ms.assetid: E9CC8507-38AB-4049-8DAC-767EC0ECE270
title: Mecaptureaudiosessionexclusivemodeoverride-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2051e6073b06f62823b95c80d7d4cfaf21de2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751280"
---
# <a name="mecaptureaudiosessionexclusivemodeoverride-event"></a>Mecaptureaudiosessionexclusivemodeoverride-Ereignis

Wird von einer audioerfassungs Quelle gesendet, wenn das Audiogerät von einem anderen Programm im exklusiven Modus geöffnet wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE               | BESCHREIBUNG                           |
|-----------------------|---------------------------------------|
| VT \_ leer <br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird vom Mediendaten Strom der audioerfassungs Quelle gesendet.

Die Erfassungs Quelle sendet dieses Ereignis, wenn es ein [**iaudiosessionevents:: onsessiongetrennte**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) -Ereignis von der Audiositzung empfängt, bei der der Trennungsgrund gleich **disconnecsquonexclusivemodeoverride** ist.

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

 

 
