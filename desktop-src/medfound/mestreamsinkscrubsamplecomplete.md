---
description: Wird durch eine streamsenke ausgelöst, wenn eine Bereinigungs Anforderung abgeschlossen ist.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Mestreamsinkscrubsamplecomplete-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359530"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a>Mestreamsinkscrubsamplecomplete-Ereignis

Wird durch eine streamsenke ausgelöst, wenn eine Bereinigungs Anforderung abgeschlossen ist.

Ein Scrubbing tritt auf, wenn die Wiedergabe Rate 0 (null) ist und die Präsentationszeit mit einer angegebenen sreiben-Zeit gestartet wird. Wenn eine Medien Senke Scrubbing unterstützt, löst jeder Datenstrom auf der Senke dieses Ereignis aus, wenn die [**imfclockstaatink:: onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) -Methode aufgerufen wird, während die Wiedergabe Rate 0 (null) ist.

Wenn der Stream während des Bereinigungs Vorgang Daten rendert, sendet er das Ereignis, sobald die Daten gerendert werden. Wenn der Stream keine Daten gerendet, sendet er das Ereignis sofort nach dem Aufruf von [**onclockstart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                              | BESCHREIBUNG                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ scrubsample-Zeit für MF-Ereignis \_**](mf-event-scrubsample-time-attribute.md)<br/> | Präsentationszeit, für die Daten gerendert wurden. Wenn die Medien Senke während des Bereinigungs Vorgang keine Daten enthält, wird dieses Attribut nicht festgelegt.<br/> <br/> |



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

[Medien senken](media-sinks.md)
</dt> <dt>

[Mesessionscrubsamplecomplete](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




