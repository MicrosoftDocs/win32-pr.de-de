---
description: Wird von der Medien Sitzung ausgelöst, wenn eine Bereinigungs Anforderung abgeschlossen ist.
ms.assetid: 1ae97022-3fb2-4c5e-9262-d5bdc2a62bee
title: Mesessionscrubsamplecomplete-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b076c2f2978831cc30521fcf49d71c04620c4dee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863611"
---
# <a name="mesessionscrubsamplecomplete-event"></a>Mesessionscrubsamplecomplete-Ereignis

Wird von der Medien Sitzung ausgelöst, wenn eine Bereinigungs Anforderung abgeschlossen ist.

Ein Scrubbing tritt auf, wenn die Wiedergabe Rate 0 (null) ist und die Anwendung [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)aufruft. Dieses Ereignis wird ausgelöst, nachdem jede streamsenke die Bereinigungs Anforderung abgeschlossen hat.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Mestreamsinkscrubsamplecomplete](mestreamsinkscrubsamplecomplete.md)
</dt> </dl>

 

 




