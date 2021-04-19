---
description: 'Wird ausgelöst, wenn eine Medienquelle eine neue Position ansucht. Eine Medienquelle löst dieses Ereignis aus, wenn die Quelle ausgeführt wird oder angehalten wurde und die Anwendung imfmediasource:: Start mit einer Startzeit aufruft, die nicht der aktuellen Position entspricht.'
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Mesourceseeked-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346988"
---
# <a name="mesourceseeked-event"></a>Mesourceseeked-Ereignis

Wird ausgelöst, wenn eine Medienquelle eine neue Position ansucht. Eine Medienquelle löst dieses Ereignis aus, wenn die Quelle ausgeführt wird oder angehalten wurde und die Anwendung [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) mit einer Startzeit aufruft, die nicht der aktuellen Position entspricht.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.



| VARTYPE           | BESCHREIBUNG                                                                |
|-------------------|----------------------------------------------------------------------------|
| VT \_ I8<br/> | Die neue Startposition in 100-Nanosecond-Einheiten.<br/> <br/> |



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

 

 




