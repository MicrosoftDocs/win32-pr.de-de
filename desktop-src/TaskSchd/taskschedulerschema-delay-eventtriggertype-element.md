---
title: Delay(eventTriggerType)-Element
description: Gibt die Zeit zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Delay-Taskplaner
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9c9523b450d5f1ea86bdf09afba26604ebfe8055661fc18c439b4e30c97169d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357106"
---
# <a name="delay-eventtriggertype-element"></a>Delay(eventTriggerType)-Element

Gibt die Zeit zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an. Das Format für diese Zeichenfolge ist PnYnMnDTnHnMnS, Dabei steht nY für die Anzahl von Jahren, nM für die Anzahl von Monaten, nD für die Anzahl von Tagen, "T" für das Datums-/Uhrzeittrennzeichen, nH für die Anzahl von Stunden, nM für die Anzahl von Minuten und nS für die Anzahl von Sekunden (PT5M gibt beispielsweise 5 Minuten an, und P1M4DT2H5M gibt einen Monat, vier Tage, zwei Stunden und fünf Minuten an). Weitere Informationen zum Dauertyp finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Das **Delay-Element** wird durch den komplexen [**EventTriggerType-Typ**](taskschedulerschema-eventtriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn ein Systemereignis auftritt.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird die Ereignistriggerverzögerung durch die [**EventTrigger.Delay-Eigenschaft**](eventtrigger-delay.md) angegeben.

Für die C++-Entwicklung wird die Ereignistriggerverzögerung durch die [**IEventTrigger::D elay-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





