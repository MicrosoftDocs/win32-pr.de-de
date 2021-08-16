---
title: Sunday (daysOfWeekType)-Element
description: Gibt an, dass die Aufgabe am Sonntag ausgeführt wird.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Sunday-Element Taskplaner
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 25a184d16d5239f2294f02ddb6144fa4b886d1f83e11cbbd6e481f7fda77e1ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356261"
---
# <a name="sunday-daysofweektype-element"></a>Sunday (daysOfWeekType)-Element

Gibt an, dass die Aufgabe am Sonntag ausgeführt wird.

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

Das **Sunday-Element** wird durch den komplexen [**DaysOfWeekType-Typ**](taskschedulerschema-daysofweektype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                  | Abgeleitet von                                                             | BESCHREIBUNG                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task nach einem wöchentlichen Zeitplan ausgeführt wird.<br/>              |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Wochentagskalender, der eine Aufgabe am Sonntag startet.


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





