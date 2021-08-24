---
description: Wird von einer Streamsenke ausgelöst, wenn eine Bereinigungsanforderung abgeschlossen wird.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: MEStreamSinkScrubSampleComplete-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ae6e0ea7a90db33fe21d39017ac99908ace86bb263e0ad6e2047f70e70f5de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715170"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a>MEStreamSinkScrubSampleComplete-Ereignis

Wird von einer Streamsenke ausgelöst, wenn eine Bereinigungsanforderung abgeschlossen wird.

Die Bereinigung erfolgt, wenn die Wiedergaberate 0 (null) ist und die Präsentationsuhr mit einer angegebenen Srubbingzeit gestartet wird. Wenn eine Mediensenke die Bereinigung unterstützt, löst jeder Stream in der Senke dieses Ereignis aus, wenn die [**Bereinigungsmethode VONClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) aufgerufen wird, während die Wiedergaberate 0 (null) ist.

Wenn der Stream Daten während der Bereinigung rendert, sendet er das Ereignis, sobald die Daten gerendert werden. Wenn der Stream keine Daten rendert, sendet er das Ereignis sofort nach dem Aufruf von [**OnClockStart.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                              | Beschreibung                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ EVENT \_ SCRUBSAMPLE \_ TIME**](mf-event-scrubsample-time-attribute.md)<br/> | Präsentationszeit, für die Daten gerendert wurden. Wenn die Mediensenke während der Bereinigung keine Daten rendert, wird dieses Attribut nicht festgelegt.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> <dt>

[Mediensenken](media-sinks.md)
</dt> <dt>

[MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




