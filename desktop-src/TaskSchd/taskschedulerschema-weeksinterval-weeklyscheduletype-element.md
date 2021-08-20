---
title: WeeksInterval (weeklyScheduleType) -Element
description: Gibt das Intervall zwischen den Wochen im Zeitplan an.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- WeeksInterval-Element Taskplaner
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c59e4f4b163e5e96418c84bf2925e45cf3a54da1bbb50e17ad9282409438ff3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059758"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a>WeeksInterval (weeklyScheduleType) -Element

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

Das -Element wird durch den komplexen [**WeeklyScheduleType-Typ**](taskschedulerschema-weeklyscheduletype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                                     | Beschreibung                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) | Gibt einen wöchentlichen Zeitplan an.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird das wöchentliche Intervall mithilfe der [**WeeklyTrigger.WeeksInterval-Eigenschaft**](weeklytrigger-weeksinterval.md) angegeben.

Für die C++-Entwicklung wird das wöchentliche Intervall mithilfe der [**IWeeklyTrigger::WeeksInterval-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen wöchentlichen Kalendertrigger, der jeden Montag bis Freitag (um 8:00 Uhr) eine Aufgabe startet.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





