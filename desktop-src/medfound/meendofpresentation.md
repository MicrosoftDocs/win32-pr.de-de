---
description: Wird von einer Medienquelle ausgelöst, wenn eine Präsentation endet. Dieses Ereignis signalisiert, dass alle Datenströme in der Präsentation vollständig sind. Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.
ms.assetid: 259b00ae-a91b-461b-a12f-f7291ecc04ff
title: Meendofpresentation-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e3a904725908d83afd54bbd64012420075037a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350558"
---
# <a name="meendofpresentation-event"></a>Meendof Presentation-Ereignis

Wird von einer Medienquelle ausgelöst, wenn eine Präsentation endet. Dieses Ereignis signalisiert, dass alle Datenströme in der Präsentation vollständig sind. Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                                               | BESCHREIBUNG                                                                               |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**die MF- \_ Ereignis \_ Quell \_ Topologie wurde \_ abgebrochen**](mf-event-source-topology-canceled-attribute.md)<br/> | Gibt an, ob die Sequencer-Quelle diese Präsentation abgebrochen hat.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




