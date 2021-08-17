---
title: Weeks-Element (monthlyDayOfWeekScheduleType)
description: Gibt die Wochen des Monats an, in denen die Aufgabe ausgeführt wird.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Weeks-Taskplaner
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81219236012146dac54965af471412369d5c5bb34319897d4d821bb10a730aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757977"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a>Weeks-Element (monthlyDayOfWeekScheduleType)

Gibt die Wochen des Monats an, in denen die Aufgabe ausgeführt wird.

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

Das **Weeks-Element** wird durch den komplexen [**MonthlyDayOfWeekScheduleType-Typ**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                      | Abgeleitet von                                                                                         | Beschreibung                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Gibt einen Trigger an, der einen Auftrag nach einem monatlichen Wochentag startet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                    | type                                                        | Beschreibung                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [**Woche**](taskschedulerschema-week-weekstype-element.md) | [**weekType**](taskschedulerschema-weektype-simpletype.md) | Gibt eine bestimmte Woche des Monats an.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung werden die Wochen des Monats mithilfe der [**MonthlyDOWTrigger.WeeksOfMonth-Eigenschaft**](monthlydowtrigger-weeksofmonth.md) angegeben.

Für die C++-Entwicklung werden die Wochen des Monats mithilfe der [**IMonthlyDOWTrigger::WeeksOfMonth-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) angegeben.

Wenn Sie die Wochen des Monats angeben, verwenden Sie 1-4, um die ersten vier Wochen des Monats anzugeben, oder verwenden Sie die Zeichenfolge "Last", um die letzte Woche anzugeben, unabhängig davon, in welcher Woche sie sich befindet.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen monatlichen Wochentagskalender, der die Aufgabe für jeden Monat des Jahres am Montag der ersten Woche startet.


```XML
<ScheduleByMonthDayOfWeek>
    <Weeks>
        <Week>1</Week>
    </Weeks>
    <DaysOfWeek>
        <Monday/>
    </DaysOfWeek>
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
 </ScheduleByMonthDayOfWeek>
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

 

 





