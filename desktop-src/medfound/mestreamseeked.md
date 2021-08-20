---
description: Wird von einem Medienstream nach einem Aufruf von SEEKMediaSource::Start ausgelöst, wird eine Suche im Stream ausgelöst. Ein Medienstream löst dieses Ereignis aus, wenn die Medienquelle das MESourceSeeked-Ereignis auslöst.
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: MEStreamSeeked-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b03e58b11785a7b807f6793ff2ba6b2a4afa5f912d21e626938d7b3c725242f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061335"
---
# <a name="mestreamseeked-event"></a>MEStreamSeeked-Ereignis

Wird von einem Medienstream nach einem Aufruf von [**SEEKMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) ausgelöst, wird eine Suche im Stream ausgelöst. Ein Medienstream löst dieses Ereignis aus, wenn die Medienquelle das [MESourceSeeked-Ereignis](mesourceseeked.md) auslöst.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE           | Beschreibung                                                        |
|-------------------|--------------------------------------------------------------------|
| VT \_ I8<br/> | Neue Startzeit in Einheiten von 100 Nanosekunden.<br/> <br/> |



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

 

 




