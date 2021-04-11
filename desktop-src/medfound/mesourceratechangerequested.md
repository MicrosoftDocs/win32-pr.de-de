---
description: 'Wird von einer Medienquelle ausgelöst, um eine neue Wiedergabe Rate anzufordern. Die Anwendung sollte imfratecontrol:: setRate mit der angeforderten Rate abrufen. Eine Medienquelle kann dieses Ereignis auch dann erhöhen, wenn die Wiedergabe mit der aktuellen Rate nicht fortgesetzt werden kann.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Mesourceratechangerequjects-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215161"
---
# <a name="mesourceratechangerequested-event"></a>Mesourceratechangerequnost-Ereignis

Wird von einer Medienquelle ausgelöst, um eine neue Wiedergabe Rate anzufordern. Die Anwendung sollte [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) mit der angeforderten Rate abrufen. Eine Medienquelle kann dieses Ereignis auch dann erhöhen, wenn die Wiedergabe mit der aktuellen Rate nicht fortgesetzt werden kann.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE           | BESCHREIBUNG                                             |
|-------------------|---------------------------------------------------------|
| VT \_ R4<br/> | Die angeforderte neue Wiedergabe Rate.<br/> <br/> |



## <a name="attributes"></a>Attribute

Für dieses Ereignis sind die folgenden Attribute definiert:



| Attribut                                                                    | BESCHREIBUNG                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**MF- \_ Ereignis wird \_ \_ dünner**](mf-event-do-thinning-attribute.md)<br/> | Gibt an, ob die Medienquelle auch eine Verdünnung anfordert.<br/> <br/> |



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

 

 




