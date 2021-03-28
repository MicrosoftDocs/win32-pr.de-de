---
description: Diese Ereignistyp Klasse wird verwendet, um anzugeben, dass Ereignisse in einer echt Zeit Sitzung verloren gegangen sind. Die folgende Syntax wird durch den MOF-Code vereinfacht.
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
ms.openlocfilehash: b689dd95aa1e078572d33de64f245e4844698d5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526384"
---
# <a name="rt_lostevent-class"></a>RT \_ lostevent-Klasse

Diese Ereignistyp Klasse wird verwendet, um anzugeben, dass Ereignisse in einer echt Zeit Sitzung verloren gegangen sind.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{32, 33, 34}, EventTypeName{"RTLostEvent", "RTLostBuffer", "RTLostFile"}]
class RT_LostEvent : Lost_Event
{
};
```

## <a name="members"></a>Member

Die **RT \_ lostevent** -Klasse definiert keine Member.

## <a name="remarks"></a>Bemerkungen

Der rtlostevent-Ereignistyp gibt an, dass mindestens ein Ereignis verloren gegangen ist. Der rtlostbuffer-Ereignistyp gibt an, dass mindestens ein Puffer verloren gegangen ist. Die Ereignis Typen rtlostevent und rtlostbuffer werden übermittelt, bevor Ereignisse aus dem Puffer verarbeitet werden.

Rtlostfile gibt an, dass die Unterstützungs Datei, die vom autologger zum Erfassen von Ereignissen verwendet wurde, verloren gegangen ist.

Das Verlust von Ereignissen hängt von der Häufigkeit ab, mit der die Ereignisse protokolliert werden, und davon, wie lange der Consumer die Verarbeitung der Ereignisse verbringt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                      |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_Ereignis Verlust**](lost-event.md)
</dt> </dl>

 

 




