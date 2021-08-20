---
description: Signalisiert, dass eine Medienquelle die Pufferung von Daten beendet hat.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: MEBufferingStopped-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e953ae5d7a79c04c33f4d0b4f9c87faa1e5798ed95d2d3bae29dbd0fab8b12a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878082"
---
# <a name="mebufferingstopped-event"></a>MEBufferingStopped-Ereignis

Signalisiert, dass eine Medienquelle die Pufferung von Daten beendet hat.

Eine Medienquelle sendet diese, wenn die Pufferung von Daten nach dem Senden des [MEBufferingStarted-Ereignisses beendet](mebufferingstarted.md) wird.

Bytestreams, die die [**BEYBYTEStreamBuffering-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) implementieren, senden ebenfalls dieses Ereignis.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue abgerufen werden,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sind:



| VARTYPE              | Beschreibung                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Wenn die Mediensitzung dieses Ereignis empfängt, wird die Präsentationsuhr neu gestartet. Die Mediensitzung gibt das Ereignis auch an die Anwendung weiter.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (einschließlich Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




