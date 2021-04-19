---
title: DaysOfWeek-Element (monthlydayosweekscheduletype)
description: Gibt die Wochentage an, an denen der Task ausgeführt wird. | DaysOfWeek-Element (monthlydayosweekscheduletype)
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
keywords:
- DaysOfWeek-Element Taskplaner
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106367329"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a>DaysOfWeek-Element (monthlydayosweekscheduletype)

Gibt die Wochentage an, an denen der Task ausgeführt wird.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

Das **DaysOfWeek** -Element wird durch den komplexen [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                      | Abgeleitet von                                                                                         | BESCHREIBUNG                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**Schedulebymonthdayof-Woche**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Gibt einen-Vorgang an, der einen Auftrag für einen monatlichen Wochentag startet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                   | type | BESCHREIBUNG                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Am**](taskschedulerschema-friday-daysofweektype-element.md)       |      | Gibt an, dass der Task am Freitag ausgeführt wird.<br/>    |
| [**Pfingst**](taskschedulerschema-monday-daysofweektype-element.md)       |      | Gibt an, dass der Task am Montag ausgeführt wird.<br/>    |
| [**Samstag**](taskschedulerschema-saturday-daysofweektype-element.md)   |      | Gibt an, dass der Task am Samstag ausgeführt wird.<br/>  |
| [**Sunday**](taskschedulerschema-sunday-daysofweektype-element.md)       |      | Gibt an, dass der Task am Sonntag ausgeführt wird.<br/>    |
| [**Mitteilte**](taskschedulerschema-thursday-daysofweektype-element.md)   |      | Gibt an, dass der Task am Donnerstag ausgeführt wird.<br/>  |
| [**Mitteilte**](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | Gibt an, dass der Task am Dienstag ausgeführt wird.<br/>   |
| [**Mittwochs**](taskschedulerschema-wednesday-daysofweektype-element.md) |      | Gibt an, dass der Task am Mittwoch ausgeführt wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Entwicklung von Skripts werden die Wochentage für einen monatlichen Wochentag mit Wochentag mithilfe der Eigenschaft [**monthlydowauslöst. DaysOfWeek**](monthlydowtrigger-daysofweek.md) angegeben.

Bei der C++-Entwicklung werden die Wochentage für einen monatlichen Wochentag mithilfe der [**imonthlydowauslöst::D aysofweek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) -Eigenschaft angegeben.

Die oben aufgeführten untergeordneten Elemente werden durch den komplexen Typ [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) definiert.

## <a name="examples"></a>Beispiele

Im folgenden XML-Code wird ein monatlicher Wochentag definiert, der die Aufgabe am Montag der ersten Woche für jeden Monat des Jahres startet.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





