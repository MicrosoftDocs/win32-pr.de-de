---
description: Wird durch eine Medienquelle ausgelöst, wenn ein neuer Stream gestartet wird.
ms.assetid: 1bc8b265-b7a1-4068-89f7-c0da03dfb874
title: Menewstream-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60394d442b24dcdc234ada2dd3fd418e6ab7b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347301"
---
# <a name="menewstream-event"></a>Menewstream-Ereignis

Wird durch eine Medienquelle ausgelöst, wenn ein neuer Stream gestartet wird.

Wenn die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode für eine Medienquelle aufgerufen wird, sendet die Medienquelle ein Ereignis für jeden ausgewählten Stream:

-   Die Quelle sendet das Ereignis menewstream, wenn der Datenstrom nicht im vorherigen [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)aufgerufen wurde, oder dies ist der erste **Start Start** für diese Medienquelle.

-   Die Quelle sendet das [meupdatedstream](meupdatedstream.md) -Ereignis, wenn der Stream bereits im vorherigen Aufrufen von " [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)" ausgewählt wurde.

Für nicht ausgewählte Streams werden keine Ereignisse gesendet.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------|
| VT \_ unbekannt<br/> | Enthält einen Zeiger auf die [**imfmediastream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Schnittstelle des Streams.<br/> <br/> |



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

 

 




