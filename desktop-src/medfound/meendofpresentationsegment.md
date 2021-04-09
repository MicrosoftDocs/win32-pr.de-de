---
description: Wird von der Sequencer-Quelle ausgelöst, wenn ein Segment abgeschlossen wird, gefolgt von einem anderen Segment. Wenn das abschließende Segment abgeschlossen ist, löst die Sequencer-Quelle ein meendof Presentation-Ereignis aus.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Meendofpresentationsegment-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863620"
---
# <a name="meendofpresentationsegment-event"></a>Meendof presentationsegment-Ereignis

Wird von der Sequencer-Quelle ausgelöst, wenn ein Segment abgeschlossen wird, gefolgt von einem anderen Segment. Wenn das abschließende Segment abgeschlossen ist, löst die Sequencer-Quelle ein [meendof Presentation](meendofpresentation.md) -Ereignis aus.

Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                                               | BESCHREIBUNG                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**die MF- \_ Ereignis \_ Quell \_ Topologie wurde \_ abgebrochen**](mf-event-source-topology-canceled-attribute.md)<br/> | Gibt an, ob die Sequencer-Quelle dieses Segment abgebrochen hat.<br/> <br/> |



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

[Informationen über die Sequencer-Quelle](about-the-sequencer-source.md)
</dt> <dt>

[Sequencer-Quell Ereignisse](sequencer-source-events.md)
</dt> </dl>

 

 




