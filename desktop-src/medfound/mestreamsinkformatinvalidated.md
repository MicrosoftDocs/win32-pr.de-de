---
description: Wird von einer streamsenke gesendet, wenn das downstreamformat ungültig geworden ist und erneut ausgehandelt werden muss.
ms.assetid: 732B3BDD-F394-430F-B895-AF18ED61114D
title: Mestreamsinkformatinvalidate-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39c4453c0d5720ffb57f1277946f9cf891ed443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348441"
---
# <a name="mestreamsinkformatinvalidated-event"></a>Mestreamsinkformatinvalidate-Ereignis

Wird von einer streamsenke gesendet, wenn das downstreamformat ungültig geworden ist und erneut ausgehandelt werden muss.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Daten, die in der Senke in der Warteschlange nach der aktuellen Wiedergabe Position eingereiht wurden, sollten erneut gesendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                                           |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




