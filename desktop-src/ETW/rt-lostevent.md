---
description: Diese Ereignistypklasse wird verwendet, um anzugeben, dass Ereignisse in einer Echtzeitsitzung verloren gegangen sind. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 19c747c0-2d9f-49c5-81e4-06a870371bac
title: RT_LostEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RT_LostEvent
api_type:
- NA
api_location: ''
ms.openlocfilehash: d0944b843c8deb38012242111b6c5057ccf7cb8557c69caefe9a87283d2ae418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328740"
---
# <a name="rt_lostevent-class"></a>RT \_ LostEvent-Klasse

Diese Ereignistypklasse wird verwendet, um anzugeben, dass Ereignisse in einer Echtzeitsitzung verloren gegangen sind.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a>Member

Die **RT \_ LostEvent-Klasse** definiert keine Member.

## <a name="remarks"></a>Hinweise

Der RTLostEvent-Ereignistyp gibt an, dass mindestens ein Ereignis verloren gegangen ist. Der RTLostBuffer-Ereignistyp gibt an, dass ein oder mehrere Puffer verloren gegangen sind. Die Ereignistypen RTLostEvent und RTLostBuffer werden übermittelt, bevor Ereignisse aus dem Puffer verarbeitet werden.

Die RTLostFile gibt an, dass die unterstützungsdatei, die von der AutoLogger zum Erfassen von Ereignissen verwendet wird, verloren gegangen ist.

Das Aussenden von Ereignissen hängt von der Häufigkeit ab, mit der die Ereignisse protokolliert werden, und davon, wie viel Zeit der Consumer mit der Verarbeitung der Ereignisse verbringt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Verlorenes \_ Ereignis**](lost-event.md)
</dt> </dl>

 

 




