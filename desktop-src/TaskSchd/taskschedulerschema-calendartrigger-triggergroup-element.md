---
title: CalendarTrigger (triggerGroup)-Element
description: Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen DOW-Trigger (Day-of-the-Week) an.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- Kalendertrigger Taskplaner , XML-Element
- CalendarTrigger-Element Taskplaner
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d02b14fa056940a8139e87d9b471f6eaef84c311eb095073f274a9b4adf3c6dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516970"
---
# <a name="calendartrigger-triggergroup-element"></a>CalendarTrigger (triggerGroup)-Element

Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen DOW-Trigger (Day-of-the-Week) an.

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

Das **CalendarTrigger-Element** wird durch den komplexen [**CalendarTriggerType-Typ**](taskschedulerschema-calendartriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | Beschreibung                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die die Aufgabe starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                                            | Typ                                                                                                 | Beschreibung                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktiviert (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | boolean                                                                                              | Gibt an, dass der Trigger aktiviert ist.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | dateTime                                                                                             | Gibt das Datum und die Uhrzeit der Deaktivierung des Triggers an. Der Trigger kann die Aufgabe nicht starten, nachdem sie deaktiviert wurde.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | duration                                                                                             | Gibt die maximale Zeitdauer an, in der der Task vom Trigger gestartet werden kann.<br/>                                   |
| [**Wiederholung (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [**wiederholungstyp**](taskschedulerschema-repetitiontype-complextype.md)                             | Gibt an, wie oft der Task ausgeführt wird und wie lange das Wiederholungsmuster wiederholt wird, nachdem der Task gestartet wurde.<br/>          |
| [**ScheduleByDay (calendarTriggerType)**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Gibt einen täglichen Zeitplan an.<br/>                                                                                             |
| [**ScheduleByMonth (calendarTriggerType)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Gibt einen monatlichen Zeitplan an.<br/>                                                                                           |
| [**ScheduleByMonthDayOfWeek (calendarTriggerType)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Gibt einen Trigger an, der einen Auftrag nach einem monatlichen Wochentag startet.<br/>                                                |
| [**ScheduleByWeek (calendarTriggerType)**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Gibt einen wöchentlichen Zeitplan an.<br/>                                                                                            |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | dateTime                                                                                             | Gibt das Datum und die Uhrzeit der Aktivierung des Triggers an. Dieses Element ist erforderlich.<br/>                                    |



## <a name="attributes"></a>Attributes



| Name | Typ | BESCHREIBUNG                               |
|------|------|-------------------------------------------|
| Id   | ID   | Der Bezeichner des Triggers.<br/> |



## <a name="remarks"></a>Hinweise

Das [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) ist ein erforderliches Element für Zeit- und Kalendertrigger ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) und **CalendarTrigger**).

Die oben aufgeführten untergeordneten Elemente werden durch die [**komplexen Elementtypen triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) und [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) definiert.

Für die Skriptentwicklung werden Kalendertrigger mit einem der folgenden Objekte angegeben.

-   [**DailyTrigger**](dailytrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)

Für die C++-Entwicklung werden Kalendertrigger mithilfe einer der folgenden Schnittstellen angegeben.

-   [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die einen Kalendertrigger angibt, finden Sie unter Beispiel für tägliche [Trigger (XML).](daily-trigger-example--xml-.md)

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

 

 





