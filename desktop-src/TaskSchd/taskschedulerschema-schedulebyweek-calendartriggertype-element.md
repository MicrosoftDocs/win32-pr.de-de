---
title: Schedulebyweek (calendartriggertype)-Element
description: Gibt einen wöchentlichen Zeitplan an.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- wöchentlicher auslöserTaskplaner, XML-Element
- Schedulebyweek-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392174"
---
# <a name="schedulebyweek-calendartriggertype-element"></a>Schedulebyweek (calendartriggertype)-Element

Gibt einen wöchentlichen Zeitplan an. Der Task wird z. b. jede Woche um 8:00 Uhr an einem bestimmten Wochentag oder an einem bestimmten Wochentag in der Woche gestartet.

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

Das **schedulebyweek** -Element wird durch den komplexen Typ [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                             | Abgeleitet von                                                                       | BESCHREIBUNG                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Calendarausgelöst**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                               | type                                                                     | BESCHREIBUNG                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**DaysOfWeek**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) | Gibt die Wochentage an, an denen der Task ausgeführt wird.<br/>    |
| [**Weeksinterval**](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | unsignedByte                                                             | Gibt das Intervall zwischen den Wochen im Zeitplan an.<br/> |



## <a name="remarks"></a>Bemerkungen

Die oben aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md) definiert.

Die Uhrzeit, zu der die Aufgabe gestartet wird, wird durch das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element festgelegt.

Bei der Skripterstellung wird ein wöchentlicher-Auslösung mithilfe des [**Weekly-auslöserobjekts**](weeklytrigger.md) angegeben.

Bei der C++-Entwicklung wird ein wöchentlicher-Auslösers mithilfe der [**iweekly-**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) Schnittstelle angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen wöchentlichen Kalender--Auslösers, der jede Woche einen Task Montag bis Freitag (um 8:00 Uhr) startet.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





