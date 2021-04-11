---
description: 'Wird von einem Mediendaten Strom nach einem imfmediasource:: Start-Rückruf ausgelöst und bewirkt eine Suche im Stream. Ein Mediendaten Strom löst dieses Ereignis aus, wenn die Medienquelle das mesourceseeked-Ereignis auslöst.'
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Mestreamseeked-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215159"
---
# <a name="mestreamseeked-event"></a>Mestreamseeked-Ereignis

Wird von einem Mediendaten Strom nach einem [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Rückruf ausgelöst und bewirkt eine Suche im Stream. Ein Mediendaten Strom löst dieses Ereignis aus, wenn die Medienquelle das [mesourceseeked](mesourceseeked.md) -Ereignis auslöst.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE           | BESCHREIBUNG                                                        |
|-------------------|--------------------------------------------------------------------|
| VT \_ I8<br/> | Neue Startzeit in 100-Nanosecond-Einheiten.<br/> <br/> |



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

 

 




