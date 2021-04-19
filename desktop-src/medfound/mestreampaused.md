---
description: Wird von einem Medienstream ausgelöst, wenn die imfmediasource::P ause-Methode asynchron abgeschlossen wird.
ms.assetid: 8fafb9a1-95a4-44b6-acd6-fb007d515915
title: Mestreampaused-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78147c7cdd7cb6e391052111e11ef0ac92b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348442"
---
# <a name="mestreampaused-event"></a>Mestreampaused-Ereignis

Wird von einem Medienstream ausgelöst, wenn die [**imfmediasource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) -Methode asynchron abgeschlossen wird.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE              | BESCHREIBUNG                           |
|----------------------|---------------------------------------|
| VT \_ leer<br/> | Keine Ereignisdaten.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Jeder aktive Stream in der Präsentation sendet dieses Ereignis.

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

 

 




