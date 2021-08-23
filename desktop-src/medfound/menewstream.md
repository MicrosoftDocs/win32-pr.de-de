---
description: Wird von einer Medienquelle ausgelöst, wenn ein neuer Stream gestartet wird.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: MENewStream-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499b7899c499e87a45e9b7f043db94724b41d729d3b836e7c9f8d71d83616841
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228770"
---
# <a name="menewstream-event"></a>MENewStream-Ereignis

Wird von einer Medienquelle ausgelöst, wenn ein neuer Stream gestartet wird.

Wenn die [**METHODE VERMEDIENMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) für eine Medienquelle aufgerufen wird, sendet die Medienquelle ein Ereignis für jeden ausgewählten Stream:

-   Die Quelle sendet das MENewStream-Ereignis, wenn der Stream im vorherigen Aufruf von [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)nicht ausgewählt wurde, oder dies ist der erste Aufruf von **Start** für diese Medienquelle.

-   Die Quelle sendet das [MEUpdatedStream-Ereignis,](meupdatedstream.md) wenn der Stream bereits im vorherigen Aufruf von [**Start ausgewählt wurde.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)

Für nicht ausgewählte Streams werden keine Ereignisse gesendet.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE                | BESCHREIBUNG                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Enthält einen Zeiger auf die [**BENUTZEROBERFLÄCHEMediaStream-Schnittstelle des**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) Streams.<br/> <br/> |



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

 

 




