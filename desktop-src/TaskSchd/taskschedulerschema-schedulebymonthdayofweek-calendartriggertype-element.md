---
title: ScheduleByMonthDayOfWeek (calendarTriggerType)-Element
description: Gibt einen monatlichen Zeitplan für den Wochentag an.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- ScheduleByMonthDayOfWeek-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 185608ea5a8805511de8430c82e6eecabd9cc5b9622fed85d71e26dd39f20cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099880"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a>ScheduleByMonthDayOfWeek (calendarTriggerType)-Element

Gibt einen monatlichen Zeitplan für den Wochentag an. Die Aufgabe wird beispielsweise an bestimmten Wochentagen, Wochen des Monats und Monaten des Jahres gestartet.

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

Das **ScheduleByMonthDayOfWeek-Element** wird durch den komplexen [**Typ monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                             | Abgeleitet von                                                                       | BESCHREIBUNG                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen DOW-Trigger (Day-of-the-Week) an.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                   | type                                                                     | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task ausgeführt wird.<br/>       |
| [**Monate**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthsType**](taskschedulerschema-monthstype-complextype.md)         | Gibt die Monate des Jahres an, in dem der Task ausgeführt wird.<br/> |
| [**Wochen**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | unsignedByte                                                             | Gibt das Intervall zwischen den Wochen im Zeitplan an.<br/>    |



## <a name="remarks"></a>Hinweise

Die Tageszeit, zu der der Task gestartet wird, wird vom [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) festgelegt.

Für die Skriptentwicklung wird ein monatlicher Wochentagstrigger mithilfe des [**MonthlyDOWTrigger-Objekts**](monthlydowtrigger.md) angegeben.

Für die C++-Entwicklung wird ein monatlicher Wochentagstrigger mithilfe der [**IMonthlyDOWTrigger-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) angegeben.

Die oben aufgeführten untergeordneten Elemente werden durch die komplexen [**Elementtypen monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) definiert.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen monatlichen Kalendertrigger für den Wochentag, der eine Aufgabe ( um 8:00 Uhr) am Montag der ersten Woche für jeden Monat des Jahres startet.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
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
</CalendarTrigger>
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

 

 





