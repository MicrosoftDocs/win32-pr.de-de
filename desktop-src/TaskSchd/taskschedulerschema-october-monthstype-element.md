---
title: October (monthsType)-Element
description: Gibt an, dass die Aufgabe im Oktober ausgeführt wird.
ms.assetid: 62c8bb3e-a70f-45b8-8d80-7a7eef9dfaeb
keywords:
- Oktober-Element Taskplaner
topic_type:
- apiref
api_name:
- October
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65f14f0ccaa2831bc4aae24ce45a520f746a57b2e9d03d70b64714bafa69e25b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125730"
---
# <a name="october-monthstype-element"></a>October (monthsType)-Element

Gibt an, dass die Aufgabe im Oktober ausgeführt wird.

``` syntax
<xs:element name="October">
    <xs:complexType />
</xs:element>
```

Das **October-Element** wird durch den komplexen [**monthsType-Typ**](taskschedulerschema-monthstype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                          | Abgeleitet von                                                     | Beschreibung                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Monate (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**Monate (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [**monthsType**](taskschedulerschema-monthstype-complextype.md) | Gibt die Monate des Jahres an, in denen die Aufgabe für einen monatlichen Zeitplan ausgeführt wird.<br/>             |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Kalender für Monate, in dem die Aufgabe im Oktober ausgeführt wird.


```XML
<Months>
    <October/>
</Months>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





