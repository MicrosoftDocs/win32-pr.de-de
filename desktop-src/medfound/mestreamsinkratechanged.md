---
description: Wird von einer Streamsenke ausgelöst, wenn sich die Rate geändert hat.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: MEStreamSinkRateChanged-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43a3a4cbff4464f78e71d3047e2b9ccaddfcbf38adcb5e84bab8f5ae49c5d80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827140"
---
# <a name="mestreamsinkratechanged-event"></a>MEStreamSinkRateChanged-Ereignis

Wird von einer Streamsenke ausgelöst, wenn sich die Rate geändert hat.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Wenn eine Datenstromsenke Ratenänderungen unterstützt, sendet sie dieses Ereignis, nachdem die Ratenänderung abgeschlossen ist. Das -Ereignis wird einmal für jeden Aufruf der [**SINK-Methode VONClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) gesendet. Wenn die Ratenänderung nicht erfolgreich ist, ist der Ereignisstatuswert ein Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> <dt>

[Mediensenken](media-sinks.md)
</dt> </dl>

 

 




