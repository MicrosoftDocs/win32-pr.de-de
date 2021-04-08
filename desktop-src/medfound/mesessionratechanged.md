---
description: 'Wird von der Medien Sitzung ausgelöst, wenn sich die Wiedergabe Rate ändert. Dieses Ereignis wird gesendet, nachdem die imfratecontrol:: abtrate-Methode asynchron abgeschlossen wurde.'
ms.assetid: 6bef923f-4083-46e1-9a2e-49a6825467ec
title: Mesessionratechanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4cbbd8254dfb988c94cf2016164726d578d8906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863612"
---
# <a name="mesessionratechanged-event"></a>Mesessionratechanged-Ereignis

Wird von der Medien Sitzung ausgelöst, wenn sich die Wiedergabe Rate ändert. Dieses Ereignis wird gesendet, nachdem die [**imfratecontrol:: abtrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) -Methode asynchron abgeschlossen wurde.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE           | BESCHREIBUNG                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------|
| VT \_ R4<br/> | Die neue Wiedergabe Rate, ausgedrückt als Verhältnis der normalen Wiedergabe Rate.<br/> <br/> |



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

 

 




