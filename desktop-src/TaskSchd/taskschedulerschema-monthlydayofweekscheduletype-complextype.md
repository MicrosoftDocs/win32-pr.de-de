---
title: komplexer monthlydayosweekscheduletype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das schedulebymonthdayoorweek-Element.
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- komplexer monthlydayosweekscheduletype-Typ Taskplaner
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 782715aed5cbf59a98e996bfa18fdd7c1022227a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345498"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a>komplexer monthlydayosweekscheduletype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**schedulebymonthdayoorweek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) -Element.

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                   | type                                                                     | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen die Aufgabe ausgeführt wird.<br/>   |
| [**Monate**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthstype**](taskschedulerschema-monthstype-complextype.md)         | Gibt die Monate des Jahres an, in dem die Aufgabe ausgeführt wird.<br/> |
| [**Wochen**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [**weekstype**](taskschedulerschema-weekstype-complextype.md)           | Gibt die Wochen des Monats an, in denen der Task ausgeführt wird.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komplexe Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





