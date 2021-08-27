---
description: Wird von einem Medienstream ausgelöst, wenn die Quelle ohne Suche gestartet wird. Ein Medienstream löst dieses Ereignis aus, wenn die Medienquelle das MESourceStarted-Ereignis auslöst.
ms.assetid: 6652e440-5de9-4767-b7a6-9d919ceece38
title: MEStreamStarted-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a385516a6f0f973dd5bd0453d6c9751a0f7411a8ea43cb6acb936d8601c5272
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113940"
---
# <a name="mestreamstarted-event"></a>MEStreamStarted-Ereignis

Wird von einem Medienstream ausgelöst, wenn die Quelle ohne Suche gestartet wird. Ein Medienstream löst dieses Ereignis aus, wenn die Medienquelle das [MESourceStarted-Ereignis](mesourcestarted.md) auslöst.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | BESCHREIBUNG                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/>                                                                          |
| VT \_ I8<br/>    | Die Startzeit in Einheiten von 100 Nanosekunden relativ zu den Zeitstempeln in den Stichproben.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




