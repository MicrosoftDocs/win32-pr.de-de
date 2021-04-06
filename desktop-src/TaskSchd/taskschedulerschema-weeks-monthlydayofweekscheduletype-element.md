---
title: Wochen (monthlydayosweekscheduletype)-Element
description: Gibt die Wochen des Monats an, in denen der Task ausgeführt wird.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Wochen Element Taskplaner
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743312"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a>Wochen (monthlydayosweekscheduletype)-Element

Gibt die Wochen des Monats an, in denen der Task ausgeführt wird.

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

Das **weeks** -Element wird durch den komplexen [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                      | Abgeleitet von                                                                                         | BESCHREIBUNG                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**Schedulebymonthdayof-Woche**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Gibt einen-Vorgang an, durch den ein Auftrag an einem monatlichen Wochentag gestartet wird.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                    | type                                                        | BESCHREIBUNG                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [**Mitte**](taskschedulerschema-week-weekstype-element.md) | [**weektype**](taskschedulerschema-weektype-simpletype.md) | Gibt eine bestimmte Woche des Monats an.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Entwicklung von Skripts werden die Wochen des Monats mithilfe der [**monthlydowauslöst. weeksofmonth**](monthlydowtrigger-weeksofmonth.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung werden die Wochen des Monats mithilfe der [**imonthlydowauslöst:: weeksofmonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) -Eigenschaft angegeben.

Wenn Sie die Wochen des Monats angeben, verwenden Sie 1-4, um die ersten vier Wochen des Monats anzugeben, oder verwenden Sie die Zeichenfolge "Last", um die letzte Woche anzugeben, unabhängig von der Woche, an der Sie sich befindet.

## <a name="examples"></a>Beispiele

Im folgenden XML-Code wird ein monatlicher Wochentag definiert, der die Aufgabe am Montag der ersten Woche für jeden Monat des Jahres startet.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





