---
title: Weeksinterval-Element (weeklyscheduletype)
description: Gibt das Intervall zwischen den Wochen im Zeitplan an.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- Weeksinterval-Element Taskplaner
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747ca4b73ff18bdb3e29d8b909d72b8d2367d89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392133"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a>Weeksinterval-Element (weeklyscheduletype)

Gibt das Intervall zwischen den Wochen im Zeitplan an.

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

Das-Element wird durch den komplexen Typ " [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                                     | BESCHREIBUNG                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**Schedulebyweek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md) | Gibt einen wöchentlichen Zeitplan an.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird das wöchentliche Intervall mithilfe der [**weeklyghost. weeksinterval**](weeklytrigger-weeksinterval.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird das wöchentliche Intervall mithilfe der [**iweeklyauslöst:: weeksinterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) -Eigenschaft angegeben.

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

 

 





