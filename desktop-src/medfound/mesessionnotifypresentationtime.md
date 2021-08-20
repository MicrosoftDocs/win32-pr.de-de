---
description: Wird von der Mediensitzung ausgelöst, wenn eine neue Präsentation gestartet wird. Dieses Ereignis gibt an, wann die Präsentation beginnt und der Offset zwischen der Präsentationszeit und der Quellzeit.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: MESessionNotifyPresentationTime-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10c1b1e443bd2c6a56a926d5355de5606bf2f2e25618269f8d4ed735538d92f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061764"
---
# <a name="mesessionnotifypresentationtime-event"></a>MESessionNotifyPresentationTime-Ereignis

Wird von der Mediensitzung ausgelöst, wenn eine neue Präsentation gestartet wird. Dieses Ereignis gibt an, wann die Präsentation beginnt und der Offset zwischen der Präsentationszeit und der Quellzeit.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                                                                   | Beschreibung                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**PRÄSENTATIONSZEIT FÜR \_ \_ MF-EREIGNISSTART \_ \_**](mf-event-start-presentation-time-attribute.md)<br/>                       | Startzeit für die Präsentation.<br/> <br/>                                                      |
| [**\_ \_ \_ MF-EREIGNISPRÄSENTATIONSZEITOFFSET \_**](mf-event-presentation-time-offset-attribute.md)<br/>                     | Offset zwischen der Präsentationszeit und den Zeitstempeln der Medienquelle.<br/> <br/>                 |
| [**PRÄSENTATIONSZEIT FÜR \_ MF-EREIGNISSTART \_ \_ BEI \_ \_ \_ AUSGABE**](mf-event-start-presentation-time-at-output-attribute.md)<br/> | Präsentationszeit, zu der die Mediensenken das erste Beispiel der neuen Topologie rendern.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BESENTMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




