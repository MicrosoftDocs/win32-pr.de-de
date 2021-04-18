---
description: Wird von einem Medienstrom ausgelöst, wenn die Quelle startet, ohne zu suchen. Ein Mediendaten Strom löst dieses Ereignis aus, wenn die Medienquelle das mesourcestarted-Ereignis auslöst.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: Mestreamstarted-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479726c1295b4497080b2e15abdde1558f0d4888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368203"
---
# <a name="mestreamstarted-event"></a>Mestreamstarted-Ereignis

Wird von einem Medienstrom ausgelöst, wenn die Quelle startet, ohne zu suchen. Ein Mediendaten Strom löst dieses Ereignis aus, wenn die Medienquelle das [mesourcestarted](mesourcestarted.md) -Ereignis auslöst.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/>                                                                          |
| VT \_ I8<br/>    | Die Startzeit in 100-Nanosecond-Einheiten in Relation zu den Zeitstempeln der Stichproben.<br/> <br/> |



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

 

 




