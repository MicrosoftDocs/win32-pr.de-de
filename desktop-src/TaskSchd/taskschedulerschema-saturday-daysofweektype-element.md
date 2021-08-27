---
title: Saturday (daysOfWeekType)-Element
description: Gibt an, dass die Aufgabe am Samstag ausgeführt wird.
ms.assetid: def26a72-c143-466a-b5b0-6105078afffa
keywords:
- Saturday-Element Taskplaner
topic_type:
- apiref
api_name:
- Saturday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0592d4f5f005afa1136d06261b05d4d4a942ac490140d384bb9174555b49c253
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099900"
---
# <a name="saturday-daysofweektype-element"></a>Saturday (daysOfWeekType)-Element

Gibt an, dass die Aufgabe am Samstag ausgeführt wird.

``` syntax
<xs:element name="Saturday">
    <xs:complexType />
</xs:element>
```

Das **Saturday-Element** wird durch den komplexen [**DaysOfWeekType-Typ**](taskschedulerschema-daysofweektype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                  | Abgeleitet von                                                             | BESCHREIBUNG                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task nach einem wöchentlichen Zeitplan ausgeführt wird.<br/>              |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Wochentagskalender, der eine Aufgabe am Samstag startet.


```XML
<DaysOfWeek>
    <Saturday/>
</DaysOfWeek>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





