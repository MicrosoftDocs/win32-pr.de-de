---
description: Wird von einer Medienquelle ausgelöst, die Topologien über die imfmediasourcetopologyprovider-Schnittstelle bereitstellt, z. b. die Sequencer-Quelle. Die Quelle löst das-Ereignis aus, wenn es eine neue Präsentation enthält. Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.
ms.assetid: c669b2c9-5ece-4045-b691-8a71bbf491e1
title: Menewpresentation-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70265a84cc7724fc6f5b6a77be2181149bd82176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215168"
---
# <a name="menewpresentation-event"></a>Menewpresentation-Ereignis

Wird von einer Medienquelle ausgelöst, die Topologien über die [**imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) -Schnittstelle bereitstellt, z. b. die Sequencer-Quelle. Die Quelle löst das-Ereignis aus, wenn es eine neue Präsentation enthält. Die Medien Sitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                                                                                                             |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Schnittstelle des Präsentations Deskriptors für die neue Präsentation.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Die Anwendung kann die Topologie abrufen, die dem Präsentations Deskriptor entspricht, indem [**imfmediasourcetopologyprovider:: getmediasourcetopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourcetopologyprovider-getmediasourcetopology) in der Medienquelle aufgerufen wird. Die Anwendung kann dann die neue Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)in eine Warteschlange stellen.

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

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 




