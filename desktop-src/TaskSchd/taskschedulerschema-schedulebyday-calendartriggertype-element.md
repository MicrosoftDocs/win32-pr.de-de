---
title: ScheduleByDay (calendarTriggerType)-Element
description: Gibt einen täglichen Zeitplan an.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- täglicher Trigger Taskplaner , XML-Element
- ScheduleByDay-Element Taskplaner
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f29cc4b702ba93aec44e3460279976f50c5563463accfb58b920ad79b757126a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131582"
---
# <a name="schedulebyday-calendartriggertype-element"></a>ScheduleByDay (calendarTriggerType)-Element

Gibt einen täglichen Zeitplan an. Die Aufgabe beginnt beispielsweise täglich um 8:00 Uhr, jeden zweiten Tag, jeden dritten Tag usw.

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

Das **ScheduleByDay-Element** wird durch den komplexen [**calendarTriggerType-Typ**](taskschedulerschema-calendartriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                             | Abgeleitet von                                                                       | Beschreibung                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Gibt einen täglichen, wöchentlichen, monatlichen oder monatlichen DOW-Trigger (Day-of-the-Week) an.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | Typ             | Beschreibung                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [**DaysInterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | **unsignedByte** | Gibt das Intervall zwischen den Tagen im Zeitplan an.<br/> |



## <a name="remarks"></a>Hinweise

Das zuvor aufgeführte untergeordnete Element wird durch die komplexen Elementtypen [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) definiert.

Die Tageszeit, zu der der Task gestartet wird, wird vom [**StartBoundary-Element**](taskschedulerschema-startboundary-triggerbasetype-element.md) festgelegt.

Für die Skriptentwicklung wird ein täglicher Trigger mit dem [**DailyTrigger-Objekt**](weeklytrigger.md) angegeben.

Für die C++-Entwicklung wird ein täglicher Trigger mithilfe der [**IDailyTrigger-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen täglichen Kalendertrigger, der die Aufgabe täglich startet.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die einen täglichen Zeitplan angibt, finden Sie unter Beispiel für [täglichen Trigger (XML).](daily-trigger-example--xml-.md)

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

 

 





