---
title: ScheduleByWeek (calendarTriggerType)-Element
description: Gibt einen wöchentlichen Zeitplan an.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- wöchentlicher Trigger Taskplaner , XML-Element
- ScheduleByWeek-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddf37c6261ba28c4cb4f59c47ee8ebd8c09afc4e36c3d1aa218efe8caa81e8c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002278"
---
# <a name="schedulebyweek-calendartriggertype-element"></a>ScheduleByWeek (calendarTriggerType)-Element

Gibt einen wöchentlichen Zeitplan an. Die Aufgabe beginnt beispielsweise jede Woche um 8:00 Uhr an einem bestimmten Wochentag oder jede andere Woche an einem bestimmten Wochentag.

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

Das **ScheduleByWeek-Element** wird durch den komplexen [**calendarTriggerType-Typ**](taskschedulerschema-calendartriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                             | Abgeleitet von                                                                       | BESCHREIBUNG                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen DOW-Trigger (Day-of-the-Week) an.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                               | type                                                                     | BESCHREIBUNG                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task ausgeführt wird.<br/>    |
| [**WeeksInterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | unsignedByte                                                             | Gibt das Intervall zwischen den Wochen im Zeitplan an.<br/> |



## <a name="remarks"></a>Hinweise

Die oben aufgeführten untergeordneten Elemente werden durch die komplexen Elementtypen [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) definiert.

Die Tageszeit, zu der der Task gestartet wird, wird vom [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) festgelegt.

Für die Skriptentwicklung wird ein wöchentlicher Trigger mit dem [**WeeklyTrigger-Objekt**](weeklytrigger.md) angegeben.

Für die C++-Entwicklung wird ein wöchentlicher Trigger mithilfe der [**IWeeklyTrigger-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen wöchentlichen Kalendertrigger, der eine Aufgabe montags bis freitags (um 8:00 Uhr) jede Woche startet.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
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

 

 





