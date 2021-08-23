---
title: Monday (daysOfWeekType)-Element
description: Gibt an, dass der Task am Montag ausgeführt wird.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- Monday-Element Taskplaner
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 22bd1028a36efa6e2fe96a300b221073dbf87f14e77621d8b1591f85c7f6fd6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513930"
---
# <a name="monday-daysofweektype-element"></a>Monday (daysOfWeekType)-Element

Gibt an, dass der Task am Montag ausgeführt wird.

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

Das **Monday-Element** wird durch den komplexen Typ [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                  | Abgeleitet von                                                             | Beschreibung                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**DaysOfWeek (monthlyDayOfWeekScheduleType)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task für einen monatlichen Wochentag ausgeführt wird.<br/> |
| [**DaysOfWeek (weeklyScheduleType)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task nach einem wöchentlichen Zeitplan ausgeführt wird.<br/>              |



## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Wochentagskalender, der eine Aufgabe am Montag startet.


```XML
<DaysOfWeek>
    <Monday/>
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

 

 





