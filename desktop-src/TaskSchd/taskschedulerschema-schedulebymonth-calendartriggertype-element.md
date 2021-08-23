---
title: ScheduleByMonth (calendarTriggerType)-Element
description: Gibt einen monatlichen Zeitplan an.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- ScheduleByMonth-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a03fcc3b30e4fe684926baaba2815132c9f2f06bf4373b4e9fbbc181e187bf6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513810"
---
# <a name="schedulebymonth-calendartriggertype-element"></a>ScheduleByMonth (calendarTriggerType)-Element

Gibt einen monatlichen Zeitplan an. Die Aufgabe beginnt z. B. um 8:00 Uhr an bestimmten Tagen des Monats für bestimmte Monate.

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

Das **ScheduleByMonth-Element** wird vom komplexen [**calendarTriggerType-Typ**](taskschedulerschema-calendartriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                             | Abgeleitet von                                                                       | Beschreibung                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen DOW-Trigger (Day-of-the-Week) an.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                  | Typ                                                                       | Beschreibung                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**DaysOfMonth (monthlyScheduleType)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Gibt die Tage des Monats an, an denen der Task ausgeführt wird.<br/>  |
| [**Months (monthlyScheduleType)**](taskschedulerschema-months-monthlyscheduletype-element.md)           | [**monthsType**](taskschedulerschema-monthstype-complextype.md)           | Gibt die Monate des Jahres an, in dem der Task ausgeführt wird.<br/> |



## <a name="remarks"></a>Hinweise

Die Tageszeit, zu der der Task gestartet wird, wird vom [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) festgelegt.

Für die Skriptentwicklung wird ein monatlicher Trigger mit dem [**MonthlyTrigger-Objekt**](monthlytrigger.md) angegeben.

Für die C++-Entwicklung wird ein monatlicher Trigger mithilfe der [**IMonthlyTrigger-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) angegeben.

Die unten aufgeführten untergeordneten Elemente werden durch die komplexen [**Elementtypen monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) definiert.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen monatlichen Kalendertrigger, der eine Aufgabe ( um 8:00 Uhr) am 1. und 15. Tag jedes Monats des Jahres startet.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





