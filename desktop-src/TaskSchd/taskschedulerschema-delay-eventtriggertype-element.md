---
title: Delay (eventtriggertype)-Element
description: Gibt die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- Verzögertes Element Taskplaner
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de1117ff4f7e0f823b1b213721521e1b526125bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341042"
---
# <a name="delay-eventtriggertype-element"></a>Delay (eventtriggertype)-Element

Gibt die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an. Das Format dieser Zeichenfolge lautet pnynmndtnhnmns. dabei ist "NY" die Anzahl der Jahre, "nm" die Anzahl von Monaten, "ND" die Anzahl der Tage, "t" ist das Trennzeichen für Datum/Uhrzeit, "NH" die Anzahl von Stunden, "nm" die Anzahl der Minuten und "NS" die Anzahl von Sekunden (z Weitere Informationen zum Duration-Typ finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

Das **Delay** -Element wird durch den komplexen Typ [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) | Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung wird die Ereignis Trigger-Verzögerung von der [**EventTrigger. Delay**](eventtrigger-delay.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird die Verzögerung des Ereignis Auslösers durch die [**ieventvent::D Elay**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) -Eigenschaft angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





