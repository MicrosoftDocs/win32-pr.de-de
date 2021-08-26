---
description: Wird von der Sequencerquelle ausgelöst, wenn ein Segment abgeschlossen wird, gefolgt von einem anderen Segment. Wenn das letzte Segment abgeschlossen ist, löst die Sequencerquelle ein MEEndOfPresentation-Ereignis aus.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: MEEndOfPresentationSegment-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b82f646ca76dbb6cc3cd8dc9e95dbaca2c55c504af261924918dbf790411e7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013700"
---
# <a name="meendofpresentationsegment-event"></a>MEEndOfPresentationSegment-Ereignis

Wird von der Sequencerquelle ausgelöst, wenn ein Segment abgeschlossen wird, gefolgt von einem anderen Segment. Wenn das letzte Segment abgeschlossen ist, löst die Sequencerquelle ein [MEEndOfPresentation-Ereignis](meendofpresentation.md) aus.

Die Mediensitzung leitet dieses Ereignis an die Anwendung weiter.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| attribute                                                                                               | Beschreibung                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**\_ \_ MF-EREIGNISQUELLENTOPOLOGIE \_ \_ ABGEBROCHEN**](mf-event-source-topology-canceled-attribute.md)<br/> | Gibt an, ob die Sequencerquelle dieses Segment abgebrochen hat.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> <dt>

[Informationen zur Sequencerquelle](about-the-sequencer-source.md)
</dt> <dt>

[Sequencer-Quellereignisse](sequencer-source-events.md)
</dt> </dl>

 

 




