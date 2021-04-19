---
title: DaysOfWeek-Element (weeklyscheduletype)
description: Gibt die Wochentage an, an denen der Task ausgeführt wird. | DaysOfWeek-Element (weeklyscheduletype)
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
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
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106366424"
---
# <a name="daysofweek-weeklyscheduletype-element"></a>DaysOfWeek-Element (weeklyscheduletype)

Gibt die Wochentage an, an denen der Task ausgeführt wird.

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

Das **DaysOfWeek** -Element wird durch den komplexen Typ " [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                                     | BESCHREIBUNG                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**Schedulebyweek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md) | Gibt einen wöchentlichen Zeitplan an.<br/> |



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

Die vorherigen untergeordneten Elemente werden durch den komplexen Typ [**daysofweektype**](taskschedulerschema-daysofweektype-complextype.md) definiert.

Bei der Skripterstellung wird das wöchentliche Intervall mithilfe der [**weeklyghost. weeksinterval**](weeklytrigger-weeksinterval.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird das wöchentliche Intervall mithilfe der [**iweeklyauslöst:: weeksinterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen täglichen Kalender-Auslösers, der jede Woche einen Task Montag bis Freitag (um 8:00 Uhr) startet.


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



Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen wöchentlichen-Auslösers verwendet, finden Sie unter Beispiel für einen [wöchentlichen Beispiel (XML)](weekly-trigger-example--xml-.md).

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

 

 





