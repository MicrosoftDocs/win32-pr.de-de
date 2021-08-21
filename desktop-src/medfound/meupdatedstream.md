---
description: Wird von einer Medienquelle ausgelöst, wenn sie einen stream neu startet oder sucht, der bereits aktiv ist.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: MEUpdatedStream-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5746b619f885ab7648110cbe58b66b7897c839031202d811becd33e1c84991a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974019"
---
# <a name="meupdatedstream-event"></a>MEUpdatedStream-Ereignis

Wird von einer Medienquelle ausgelöst, wenn sie einen stream neu startet oder sucht, der bereits aktiv ist.

Wenn die [**METHODE VERMEDIENMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) für eine Medienquelle aufgerufen wird, sendet die Medienquelle ein Ereignis für jeden ausgewählten Stream:

-   Die Quelle sendet das [MENewStream-Ereignis,](menewstream.md) wenn der Stream im vorherigen Aufruf von [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)nicht ausgewählt wurde, oder dies ist der erste Aufruf von **Start** für diese Medienquelle.

-   Die Quelle sendet das MEUpdatedStream-Ereignis, wenn der Stream bereits im vorherigen Aufruf von [**Start ausgewählt wurde.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)

Für nicht ausgewählte Streams werden keine Ereignisse gesendet.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE                | BESCHREIBUNG                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Zeiger auf die [**NSDRMediaStream-Schnittstelle des**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) Streams.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Beim ersten Aufruf von [**Start,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) bei dem ein Stream aktiv wird, sendet die Medienquelle ein [MENewStream-Ereignis](menewstream.md) für den Stream. Bei nachfolgenden **Aufrufen von Start** sendet die Medienquelle ein MEUpdatedStream-Ereignis, bis die Auswahl des Streams aufgehoben wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




