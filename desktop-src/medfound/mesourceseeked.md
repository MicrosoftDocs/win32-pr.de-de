---
description: Wird ausgelöst, wenn eine Medienquelle an eine neue Position sucht. Eine Medienquelle löst dieses Ereignis aus, wenn die Quelle ausgeführt wird oder angehalten wird und die Anwendung MIT einer Startzeit aufruft, die nicht der aktuellen Position entspricht.
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: MESourceSeeked-Ereignis (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b913089ca40895a782f3c013b752db25fe754443ae6d79b410da98e759b4b8ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941410"
---
# <a name="mesourceseeked-event"></a>MESourceSeeked-Ereignis

Wird ausgelöst, wenn eine Medienquelle an eine neue Position sucht. Eine Medienquelle löst dieses Ereignis aus, wenn die Quelle ausgeführt wird oder angehalten wird und die Anwendung [**MIT**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) einer Startzeit aufruft, die nicht der aktuellen Position entspricht.

## <a name="event-values"></a>Ereigniswerte

Mögliche Werte, die von [**DERMEDIAEVENT::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind:



| VARTYPE           | BESCHREIBUNG                                                                |
|-------------------|----------------------------------------------------------------------------|
| VT \_ I8<br/> | Die neue Anfangsposition in Einheiten von 100 Nanosekunden.<br/> <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (include Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Ereignisse](media-foundation-events.md)
</dt> </dl>

 

 




