---
description: Signalisiert, dass eine Medienquelle die Pufferung der Daten beendet hat.
ms.assetid: 11b1290d-d462-4aa0-a358-b3f6447c99d8
title: Mebufferingbeendete-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e996ec160f57ec598196b388170741705adb9a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344299"
---
# <a name="mebufferingstopped-event"></a>Mebufferingbeendete-Ereignis

Signalisiert, dass eine Medienquelle die Pufferung der Daten beendet hat.

Eine Medienquelle sendet diese Nachricht, wenn Sie das Puffern von Daten nach dem Senden des [mebufferingstarted](mebufferingstarted.md) -Ereignisses stoppt.

Bytestreams, die die [**IMF bytestreambufferate**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) -Schnittstelle implementieren, senden ebenfalls dieses Ereignis.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Wenn die Medien Sitzung dieses Ereignis empfängt, wird die Präsentations Uhr neu gestartet. Die Medien Sitzung leitet das Ereignis auch an die Anwendung weiter.

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

 

 




