---
title: DaysOfWeek (monthlyDayOfWeekScheduleType) -Element
description: Gibt die Wochentage an, an denen der Task ausgeführt wird. | DaysOfWeek (monthlyDayOfWeekScheduleType) -Element
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
keywords:
- DaysOfWeek-Taskplaner
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c7ed2a597c1b92245a34dae510c079a5b5aa7a4e7893a78dbb70d7bc5988d580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357140"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a>DaysOfWeek (monthlyDayOfWeekScheduleType) -Element

Gibt die Wochentage an, an denen der Task ausgeführt wird.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

Das **DaysOfWeek-Element** wird durch den komplexen [**monthlyDayOfWeekScheduleType-Typ**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                      | Abgeleitet von                                                                                         | BESCHREIBUNG                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Gibt einen Trigger an, der einen Auftrag für einen monatlichen Wochentag startet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                   | type | BESCHREIBUNG                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Freitag**](taskschedulerschema-friday-daysofweektype-element.md)       |      | Gibt an, dass die Aufgabe am Freitag ausgeführt wird.<br/>    |
| [**Montag**](taskschedulerschema-monday-daysofweektype-element.md)       |      | Gibt an, dass die Aufgabe am Montag ausgeführt wird.<br/>    |
| [**Samstag**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | Gibt an, dass die Aufgabe am Samstag ausgeführt wird.<br/>  |
| [**Sonntag**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | Gibt an, dass die Aufgabe am Sonntag ausgeführt wird.<br/>    |
| [**Thursday**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | Gibt an, dass die Aufgabe am Donnerstag ausgeführt wird.<br/>  |
| [**Tuesday**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | Gibt an, dass die Aufgabe am Dienstag ausgeführt wird.<br/>   |
| [**Wednesday**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | Gibt an, dass die Aufgabe am Mittwoch ausgeführt wird.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung werden die Wochentage für einen monatlichen Wochentagskalender mithilfe der [**MonthlyDOWTrigger.DaysOfWeek-Eigenschaft**](monthlydowtrigger-daysofweek.md) angegeben.

Bei der C++-Entwicklung werden die Wochentage für einen monatlichen Wochentagskalender mithilfe der [**IMonthlyDOWTrigger::D aysOfWeek-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) angegeben.

Die oben genannten untergeordneten Elemente werden durch den [**komplexen DaysOfWeekType-Typ**](taskschedulerschema-daysofweektype-complextype.md) definiert.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen monatlichen Wochentagskalender, der die Aufgabe für jeden Monat des Jahres am Montag der ersten Woche startet.


```XML
<ScheduleByMonthDayOfWeek>
    <Weeks>
        <Week>1</Week>
    </Weeks>
    <DaysOfWeek>
        <Monday/>
    </DaysOfWeek>
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonthDayOfWeek>
```



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

 

 





