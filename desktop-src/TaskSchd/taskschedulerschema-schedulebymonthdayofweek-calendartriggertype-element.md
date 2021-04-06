---
title: Schedulebymonthdayoatweek (calendartriggertype)-Element
description: Gibt einen monatlichen Zeitplan an Wochentagen an.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- Schedulebymonthdayomaweek-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742889"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a>Schedulebymonthdayoatweek (calendartriggertype)-Element

Gibt einen monatlichen Zeitplan an Wochentagen an. Beispielsweise wird die Aufgabe an bestimmten Wochentagen, Wochen des Monats und Monaten des Jahres gestartet.

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

Das **schedulebymonthdayosweek** -Element wird durch den komplexen [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                             | Abgeleitet von                                                                       | BESCHREIBUNG                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Calendarausgelöst**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                   | type                                                                     | BESCHREIBUNG                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task ausgeführt wird.<br/>       |
| [**Monate**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [**monthstype**](taskschedulerschema-monthstype-complextype.md)         | Gibt die Monate des Jahres an, in dem die Aufgabe ausgeführt wird.<br/> |
| [**Wochen**](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | unsignedByte                                                             | Gibt das Intervall zwischen den Wochen im Zeitplan an.<br/>    |



## <a name="remarks"></a>Bemerkungen

Die Uhrzeit, zu der die Aufgabe gestartet wird, wird durch das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element festgelegt.

Bei der Skripterstellung wird ein monatlicher Tag-of-week-Wert mit dem [**monthlydowauslöserobjekt**](monthlydowtrigger.md) angegeben.

Bei der C++-Entwicklung wird ein monatlicher Wochentag mithilfe der [**imonthlydow-auslöserschnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) angegeben.

Die oben aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) definiert.

## <a name="examples"></a>Beispiele

Im folgenden XML-Code wird ein monatlicher Tag of week-Kalender-Auslösers definiert, mit dem eine Aufgabe (um 8:00 Uhr) am Montag der ersten Woche für jeden Monat des Jahres gestartet wird.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





