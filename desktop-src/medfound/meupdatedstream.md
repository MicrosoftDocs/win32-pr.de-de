---
description: Wird von einer Medienquelle ausgelöst, wenn Sie neu gestartet wird oder einen Datenstrom sucht, der bereits aktiv ist.
ms.assetid: 2d91a267-e109-45f5-886b-11b883cc5509
title: Meupdatedstream-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e3b2e6fdc5928a08306b344c02b5eaafc37e957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529603"
---
# <a name="meupdatedstream-event"></a>Meupdatedstream-Ereignis

Wird von einer Medienquelle ausgelöst, wenn Sie neu gestartet wird oder einen Datenstrom sucht, der bereits aktiv ist.

Wenn die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode für eine Medienquelle aufgerufen wird, sendet die Medienquelle ein Ereignis für jeden ausgewählten Stream:

-   Die Quelle sendet das Ereignis [menewstream](menewstream.md) , wenn der Datenstrom nicht im vorherigen [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)aufgerufen wurde, oder dies ist der erste **Start Start** für diese Medienquelle.

-   Die Quelle sendet das meupdatedstream-Ereignis, wenn der Stream bereits im vorherigen Aufrufen von " [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)" ausgewählt wurde.

Für nicht ausgewählte Streams werden keine Ereignisse gesendet.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE                | BESCHREIBUNG                                                                                        |
|------------------------|----------------------------------------------------------------------------------------------------|
| VT \_ unbekannt<br/> | Ein Zeiger auf die [**imfmediastream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Schnittstelle des Streams.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Beim ersten [**Start Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) , bei dem ein Stream aktiv wird, sendet die Medienquelle ein [menewstream](menewstream.md) -Ereignis für den Datenstrom. Bei nachfolgenden Aufrufen des **Starts** sendet die Medienquelle ein meupdatedstream-Ereignis, bis der Stream deaktiviert wird.

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

 

 




