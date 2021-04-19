---
description: Wird vom streamingaudiorenderer (SAR) gesendet, wenn sich das Volume oder der stumm Zustand der Audiositzung ändert.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Meaudiosessionvolumechaning-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429edd8a26ed7f4ca1e764c7fbea1c6930c4871c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359897"
---
# <a name="meaudiosessionvolumechanged-event"></a>Meaudiosessionvolumechaning-Ereignis

Wird vom streamingaudiorenderer (SAR) gesendet, wenn sich das Volume oder der stumm Zustand der Audiositzung ändert.

Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ leer<br/>   | Keine Ereignisdaten.<br/> <br/>                                                     |
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imfaudiopolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) -Schnittstelle.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Ereignis wird von der streamsenke der SAR ausgelöst. Das Ereignis wird ausgelöst, wenn der SAR ein [**iaudiosessionevents:: onsimplevolumechaning**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) -Ereignis aus der Audiositzung empfängt. Um die neue Volumeebene abzurufen und den Zustand stumm zu schalten, nennen Sie [**imfsimpleaudiovolume:: getmastervolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) und [**imfsimpleaudiovolume:: getstumm**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).

Der SAR sendet dieses Ereignis, wenn das Volume durch eine externe Aktion geändert wird – z. b. wenn der Benutzer das Volume über das System Volume-Control Program (sndvol) ändert. Der SAR sendet das Ereignis nicht, wenn die Anwendung das Volume direkt in der SAR ändert.

Außerdem sendet der SAR dieses Ereignis nicht, wenn sich das Kanal Volume ändert ([**iaudiosessionevents:: onchannelvolumechaning**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Streamingaudiorenderer](streaming-audio-renderer.md)
</dt> </dl>

 

 
