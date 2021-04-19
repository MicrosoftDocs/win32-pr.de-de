---
description: Wird von der Medien Sitzung ausgelöst, wenn eine neue Präsentation gestartet wird. Dieses Ereignis zeigt an, wann die Präsentation gestartet wird und der Offset zwischen der Präsentationszeit und der Quell Zeit liegt.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Mesessionnotifypresentationtime-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349108"
---
# <a name="mesessionnotifypresentationtime-event"></a>Mesessionnotifypresentationtime-Ereignis

Wird von der Medien Sitzung ausgelöst, wenn eine neue Präsentation gestartet wird. Dieses Ereignis zeigt an, wann die Präsentation gestartet wird und der Offset zwischen der Präsentationszeit und der Quell Zeit liegt.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                                                                   | BESCHREIBUNG                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**\_ \_ Start \_ Präsentations \_ Zeit für MF-Ereignis**](mf-event-start-presentation-time-attribute.md)<br/>                       | Startzeit der Präsentation.<br/> <br/>                                                      |
| [**Zeit Offset der MF- \_ Ereignis \_ Präsentation \_ \_**](mf-event-presentation-time-offset-attribute.md)<br/>                     | Offset zwischen der Präsentationszeit und den Zeitstempeln der Medienquelle.<br/> <br/>                 |
| [**\_ \_ \_ \_ Zeitpunkt der Ausgabe Präsentation des MF-Ereignisses \_ bei der \_ Ausgabe**](mf-event-start-presentation-time-at-output-attribute.md)<br/> | Präsentationszeit, in der die Medien senken das erste Beispiel der neuen Topologie Rendering.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




