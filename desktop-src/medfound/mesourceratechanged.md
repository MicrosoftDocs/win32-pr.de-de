---
description: 'Wird von einer Medienquelle ausgelöst, wenn sich die Wiedergabe Rate ändert. Dieses Ereignis wird gesendet, nachdem die imfratecontrol:: abtrate-Methode asynchron abgeschlossen wurde.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Mesourceratechanged-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129809"
---
# <a name="mesourceratechanged-event"></a>Mesourceratechanged-Ereignis

Wird von einer Medienquelle ausgelöst, wenn sich die Wiedergabe Rate ändert. Dieses Ereignis wird gesendet, nachdem die [**imfratecontrol:: abtrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) -Methode asynchron abgeschlossen wurde.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE           | BESCHREIBUNG                                   |
|-------------------|-----------------------------------------------|
| VT \_ R4<br/> | Die neue Wiedergabe Rate.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects. h (Include mfdl. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Implementieren der Raten Steuerung](implementing-rate-control.md)
</dt> <dt>

[Ereignisse Media Foundation](media-foundation-events.md)
</dt> <dt>

[Raten Steuerung](rate-control.md)
</dt> <dt>

[**Imfratecontrol:: abtrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




