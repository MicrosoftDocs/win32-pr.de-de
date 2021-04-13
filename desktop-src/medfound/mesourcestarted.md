---
description: Wird ausgelöst, wenn eine Medienquelle startet, ohne zu suchen.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Mesourcestarted-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528262"
---
# <a name="mesourcestarted-event"></a>Mesourcestarted-Ereignis

Wird ausgelöst, wenn eine Medienquelle startet, ohne zu suchen.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten. Die Startzeit war von der aktuellen Position.<br/> <br/>                            |
| VT \_ I8<br/>    | Die Startzeit in 100-Nanosecond-Einheiten in Relation zu den Zeitstempeln der Stichproben.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                                     | BESCHREIBUNG                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Beginn der MF- \_ Ereignis \_ Quelle \_ \_**](mf-event-source-actual-start-attribute.md)<br/> | Startzeit. Die Medienquelle legt dieses Attribut fest, wenn es von seiner aktuellen Position neu gestartet wird.<br/> <br/>                     |
| [**der MF- \_ Ereignis \_ Quelle wurde \_ \_ gestartet.**](mf-event-source-fake-start-attribute.md)<br/>     | Gibt an, ob die aktuelle Segment Topologie leer ist. Die Sequencer-Quelle legt dieses Attribut fest.<br/> <br/>             |
| [**der MF- \_ Ereignis \_ Quelle \_ ProjectStart**](mf-event-source-projectstart-attribute.md)<br/>  | Die Startzeit für ein Segment relativ zum Beginn der Präsentation. Die Sequencer-Quelle legt dieses Attribut fest.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Eine Medienquelle löst dieses Ereignis aus, wenn es von einem beendeten Zustand gestartet wird, oder startet von einem angehaltenen Zustand an derselben Position in der Quelle. Das-Ereignis wird ausgelöst, wenn die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode S OK zurückgibt \_ .

Wenn die Medienquelle von der aktuellen Position aus startet und der vorherige Zustand der Quelle ausgeführt oder angehalten wurde, können die Ereignisdaten leer (VT \_ Empty) sein. Wenn die Ereignisdaten VT \_ leer sind, kann die Medienquelle das [**\_ \_ \_ tatsächliche \_ Start Attribut der MF-Ereignis Quelle**](mf-event-source-actual-start-attribute.md) mit der tatsächlichen Startzeit festlegen.

Wenn die Medienquelle an einer neuen Position beginnt oder der vorherige Zustand der Quelle beendet wurde, müssen die Ereignisdaten die Startzeit (VT \_ I8) sein.

Wenn die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Methode eine Suche auslöst, sendet die Medienquelle das [mesourceseeked](mesourceseeked.md) -Ereignis anstelle von mesourcestarted.

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

 

 




