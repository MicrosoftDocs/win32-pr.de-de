---
title: Schedulebymonth (calendartriggertype)-Element
description: Gibt einen monatlichen Zeitplan an.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- Schedulebymonth-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fda84a1cd4373f7988fa66a5ad70c97dd371d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105362"
---
# <a name="schedulebymonth-calendartriggertype-element"></a>Schedulebymonth (calendartriggertype)-Element

Gibt einen monatlichen Zeitplan an. Der Task wird z. b. um 8:00 Uhr an bestimmten Tagen des Monats in bestimmten Monaten gestartet.

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

Das **schedulebymonth** -Element wird durch den komplexen Typ [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                             | Abgeleitet von                                                                       | BESCHREIBUNG                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**Calendarausgelöst**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendartriggertype**](taskschedulerschema-calendartriggertype-complextype.md) | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen Tag-of-the-Week-(Dow-)-auslöst an.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                  | type                                                                       | BESCHREIBUNG                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfMonth (monthlyscheduletype)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysofmonthtype**](taskschedulerschema-daysofmonthtype-complextype.md) | Gibt die Tage des Monats an, in denen der Task ausgeführt wird.<br/>  |
| [**Monate (monthlyscheduletype)**](taskschedulerschema-months-monthlyscheduletype-element.md)           | [**monthstype**](taskschedulerschema-monthstype-complextype.md)           | Gibt die Monate des Jahres an, in dem die Aufgabe ausgeführt wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Uhrzeit, zu der die Aufgabe gestartet wird, wird durch das [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) -Element festgelegt.

Bei der Skript Entwicklung wird ein monatlicher-Auslösung mit dem [**Monthly-Auslöserobjekt**](monthlytrigger.md) angegeben.

Bei der C++-Entwicklung wird ein monatlicher-Auslösers mithilfe der [**imonthly-**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) Schnittstelle angegeben.

Die unten aufgeführten untergeordneten Elemente werden von den komplexen Elementtypen [**monthlyscheduletype**](taskschedulerschema-monthlyscheduletype-complextype.md) definiert.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen monatlichen Kalender-, der einen Task (um 8:00 Uhr) am 1. und 15. Tag eines jeden Monats des Jahres startet.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
        </DaysOfMonth>
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
        </Months>
    </ScheduleByMonth>
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

 

 





