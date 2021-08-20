---
description: Wird von einer Streamsenke ausgelöst, wenn der Übergang in den Ausführungszustand abgeschlossen ist.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: MEStreamSinkStarted-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b19d21559b8af53df47b2105f8c72b87a62b0439d1774257c044409554eaa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061234"
---
# <a name="mestreamsinkstarted-event"></a>MEStreamSinkStarted-Ereignis

Wird von einer Streamsenke ausgelöst, wenn der Übergang in den Ausführungszustand abgeschlossen ist. Der Übergang zur Ausführung tritt auf, wenn die [**METHODE DURCHTTPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) für die Präsentationsuhr der Senke aufgerufen wird. Die Mediensenke empfängt die Benachrichtigung über die [**EIGENE METHODE ZU BENACHRICHTIGUNGEN::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) oder [**BENACHRICHTIGUNGClockStateSink::OnClockRestart.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart)

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | Beschreibung                           |
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

[Mediensenken](media-sinks.md)
</dt> </dl>

 

 




