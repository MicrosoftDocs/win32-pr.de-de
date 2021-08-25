---
title: Months (monthlyDayOfWeekScheduleType)-Element
description: Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Months-Element Taskplaner
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a963032a2d33f13158af249f2b867037cf50082be005efa579148031c8e30585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959600"
---
# <a name="months-monthlydayofweekscheduletype-element"></a>Months (monthlyDayOfWeekScheduleType)-Element

Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

Das **Months-Element** wird vom komplexen [**MonthlyDayOfWeekScheduleType-Typ**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                            | Abgeleitet von                                                                                         | Beschreibung                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Gibt einen Trigger an, der einen Auftrag für einen monatlichen Wochentag startet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | type | Beschreibung                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [**April**](taskschedulerschema-april-monthstype-element.md)         |      | Gibt an, dass der Task im April ausgeführt wird.<br/>     |
| [**August**](taskschedulerschema-august-monthstype-element.md)       |      | Gibt an, dass der Task im August ausgeführt wird.<br/>    |
| [**Dezember**](taskschedulerschema-december-monthstype-element.md)   |      | Gibt an, dass der Task im Dezember ausgeführt wird.<br/>  |
| [**Februar**](taskschedulerschema-february-monthstype-element.md)   |      | Gibt an, dass der Task im Februar ausgeführt wird.<br/>  |
| [**January**](taskschedulerschema-january-monthstype-element.md)     |      | Gibt an, dass der Task im Januar ausgeführt wird.<br/>   |
| [**Juli**](taskschedulerschema-july-monthstype-element.md)           |      | Gibt an, dass der Task im Juli ausgeführt wird.<br/>      |
| [**June**](taskschedulerschema-june-monthstype-element.md)           |      | Gibt an, dass der Task im Juni ausgeführt wird.<br/>      |
| [**März**](taskschedulerschema-march-monthstype-element.md)         |      | Gibt an, dass der Task im März ausgeführt wird.<br/>     |
| [**May**](taskschedulerschema-may-monthstype-element.md)             |      | Gibt an, dass der Task im Mai ausgeführt wird.<br/>       |
| [**November**](taskschedulerschema-november-monthstype-element.md)   |      | Gibt an, dass der Task im November ausgeführt wird.<br/>  |
| [**Oktober**](taskschedulerschema-october-monthstype-element.md)     |      | Gibt an, dass der Task im Oktober ausgeführt wird.<br/>   |
| [**September**](taskschedulerschema-september-monthstype-element.md) |      | Gibt an, dass der Task im September ausgeführt wird.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung werden die Monate eines Jahres für einen monatlichen Wochentagszeitplan mithilfe der [**MonthlyDOWTrigger.MonthsOfYear-Eigenschaft**](monthlydowtrigger-monthsofyear.md) angegeben.

Für die C++-Entwicklung werden die Monate eines Jahres für einen monatlichen Wochentagszeitplan mithilfe der [**IMonthlyDOWTrigger::MonthsOfYear-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) angegeben.

Die oben aufgeführten untergeordneten Elemente werden durch den komplexen Typ [**monthsType**](taskschedulerschema-monthstype-complextype.md) definiert.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen monatlichen Kalender für den Wochentag, der die Aufgabe am Montag der ersten Woche für jeden Monat des Jahres startet.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





