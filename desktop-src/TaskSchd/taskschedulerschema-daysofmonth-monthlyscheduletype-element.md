---
title: DaysOfMonth (monthlyscheduletype)-Element
description: Gibt die Tage des Monats an, in denen der Task ausgeführt wird.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- DaysOfMonth-Element Taskplaner
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344274"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a>DaysOfMonth (monthlyscheduletype)-Element

Gibt die Tage des Monats an, in denen der Task ausgeführt wird.

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

Das **daysOfMonth** -Element wird durch den komplexen [**monthlyscheduletype**](taskschedulerschema-monthlyscheduletype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                    | Abgeleitet von                                                                                         | BESCHREIBUNG                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**Schedulebymonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Gibt einen-Vorgang an, der einen Auftrag für einen monatlichen Wochentag startet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                        | type                                                                    | BESCHREIBUNG                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**Tag**](taskschedulerschema-day-daysofmonthtype-element.md) | [**dayoatmonthtype**](taskschedulerschema-dayofmonthtype-simpletype.md) | Gibt den Tag des Monats an, in dem die Aufgabe ausgeführt wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung werden die Tage des Monats für den Zeitplan mithilfe der [**Monthly-Eigenschaft. daysOfMonth**](monthlytrigger-daysofmonth.md) angegeben.

Bei der C++-Entwicklung werden die Tage des Monats für den Zeitplan mithilfe der [**imonthly-Eigenschaft:D aysofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) -Eigenschaft angegeben.

Das untergeordnete Element muss für jeden Tag des Monats, an dem die Aufgabe ausgeführt werden soll, wiederholt werden.

## <a name="examples"></a>Beispiele

Mit dem folgenden XML-Code wird ein monatlicher Kalender-Auslösers definiert, der am 1. Tag jedes Monats eine Aufgabe (um 8:30 Uhr) startet.


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
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
        <Months>
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

 

 





