---
description: Wird durch eine streamsenke ausgelöst, wenn der Übergang zum angehaltenen Zustand abgeschlossen wird.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: Mestreamsink angeh Ed-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17016285f2b88a1fc266b79f5eee45fea31f824c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347496"
---
# <a name="mestreamsinkpaused-event"></a>Mestreamsink-Ereignis

Wird durch eine streamsenke ausgelöst, wenn der Übergang zum angehaltenen Zustand abgeschlossen wird. Der Übergang zum Anhalten erfolgt, wenn die [**imfpresentationclock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) -Methode auf der Präsentations Uhr der Senke aufgerufen wird.

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

[Medien senken](media-sinks.md)
</dt> </dl>

 

 




