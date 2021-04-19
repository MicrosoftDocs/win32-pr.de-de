---
title: komplexer calendartriggertype-Typ
description: Definiert die untergeordneten Elemente und die Sequenzierungs Informationen für Kalender Elemente.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- komplexer calendartriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f45434fa68b6300157a29318ba257f43bac5992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346732"
---
# <a name="calendartriggertype-complex-type"></a>komplexer calendartriggertype-Typ

Definiert die untergeordneten Elemente und die Sequenzierungs Informationen für Kalender Elemente.

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                      | type                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Randomdelay**](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | duration                                                                                             | Enthält die Verzögerungszeit, die der Startzeit des Auslösers zufällig hinzugefügt wird. Das Format für diese Zeichenfolge ist P <days> dt <hours> H <minutes> M <seconds> S (z. b. P2DT5S ist eine Verzögerung von 2 Tagen, 5 Sekunden).<br/> |
| [**Schedulebyday**](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [**dailyscheduletype**](taskschedulerschema-dailyscheduletype-complextype.md)                       | Gibt einen täglichen Zeitplan an. Der Task wird z. b. täglich, jeden Tag, jeden dritten Tag usw. gestartet.<br/>                                                                                                               |
| [**Schedulebymonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [**monthlyscheduletype**](taskschedulerschema-monthlyscheduletype-complextype.md)                   | Gibt einen monatlichen Zeitplan an. Der Task wird z. b. um 8:00 Uhr an bestimmten Tagen des Monats in bestimmten Monaten gestartet. <br/>                                                                                                       |
| [**Schedulebymonthdayof-Woche**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Gibt einen-Vorgang an, durch den ein Auftrag an einem monatlichen Wochentag gestartet wird. Beispielsweise wird die Aufgabe an bestimmten Wochentagen, Wochen des Monats und Monaten des Jahres gestartet. <br/>                                               |
| [**Schedulebyweek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [**weeklyscheduletype**](taskschedulerschema-weeklyscheduletype-complextype.md)                     | Gibt einen wöchentlichen Zeitplan an. Der Task wird z. b. jede Woche um 8:00 Uhr an einem bestimmten Wochentag oder an einem bestimmten Wochentag in der Woche gestartet. <br/>                                                              |



## <a name="remarks"></a>Bemerkungen

Zusätzlich zum untergeordneten-Element, das hier definiert ist, verwendet das [**calendartrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) -Element auch die untergeordneten Elemente, die durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komplexe Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





