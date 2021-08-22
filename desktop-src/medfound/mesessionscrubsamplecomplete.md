---
description: Wird von der Mediensitzung ausgelöst, wenn eine Bereinigungsanforderung abgeschlossen wird.
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: MESessionScrubSampleComplete-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2fdaa6ffe9693fc6a033fd0c33ff519a73dcda3a32c303844da04e6af01404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974173"
---
# <a name="mesessionscrubsamplecomplete-event"></a>MESessionScrubSampleComplete-Ereignis

Wird von der Mediensitzung ausgelöst, wenn eine Bereinigungsanforderung abgeschlossen wird.

Die Bereinigung erfolgt, wenn die Wiedergaberate 0 (null) ist und die Anwendung [**DEN AUFRUF ANSTMediaSession::Start auf aufruft.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) Dieses Ereignis wird ausgelöst, nachdem jede Streamsenke die Bereinigungsanforderung abgeschlossen hat.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




