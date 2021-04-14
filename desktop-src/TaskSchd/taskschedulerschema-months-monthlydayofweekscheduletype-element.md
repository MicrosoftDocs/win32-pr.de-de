---
title: Monate (monthlydayosweekscheduletype)-Element
description: Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Monate-Element Taskplaner
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391694"
---
# <a name="months-monthlydayofweekscheduletype-element"></a>Monate (monthlydayosweekscheduletype)-Element

Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Wochentag ausgeführt wird.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

Das **Monats** Element wird durch den komplexen Typ [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                                                            | Abgeleitet von                                                                                         | BESCHREIBUNG                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**Schedulebymonthdayoatweek (calendartriggertype)**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [**monthlydayosweekscheduletype**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | Gibt einen-Vorgang an, der einen Auftrag für einen monatlichen Wochentag startet.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | type | BESCHREIBUNG                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [**Am**](taskschedulerschema-april-monthstype-element.md)         |      | Gibt an, dass der Task im April ausgeführt wird.<br/>     |
| [**August**](taskschedulerschema-august-monthstype-element.md)       |      | Gibt an, dass der Task im August ausgeführt wird.<br/>    |
| [**Dezember**](taskschedulerschema-december-monthstype-element.md)   |      | Gibt an, dass der Task im Dezember ausgeführt wird.<br/>  |
| [**Februar**](taskschedulerschema-february-monthstype-element.md)   |      | Gibt an, dass der Task im Februar ausgeführt wird.<br/>  |
| [**January**](taskschedulerschema-january-monthstype-element.md)     |      | Gibt an, dass der Task im Januar ausgeführt wird.<br/>   |
| [**Juli**](taskschedulerschema-july-monthstype-element.md)           |      | Gibt an, dass der Task im Juli ausgeführt wird.<br/>      |
| [**June**](taskschedulerschema-june-monthstype-element.md)           |      | Gibt an, dass der Task im Juni ausgeführt wird.<br/>      |
| [**März**](taskschedulerschema-march-monthstype-element.md)         |      | Gibt an, dass der Task im März ausgeführt wird.<br/>     |
| [**May**](taskschedulerschema-may-monthstype-element.md)             |      | Gibt an, dass der Task im Mai ausgeführt wird.<br/>       |
| [**November**](taskschedulerschema-november-monthstype-element.md)   |      | Gibt an, dass der Task im November ausgeführt wird.<br/>  |
| [**Vom**](taskschedulerschema-october-monthstype-element.md)     |      | Gibt an, dass der Task im Oktober ausgeführt wird.<br/>   |
| [**September**](taskschedulerschema-september-monthstype-element.md) |      | Gibt an, dass der Task im September ausgeführt wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Entwicklung von Skripts werden die Monate eines Jahres für einen monatlichen Wochentag mithilfe der Eigenschaft [**monthlydowauslöst. MONTHSOFYEAR**](monthlydowtrigger-monthsofyear.md) angegeben.

Bei der C++-Entwicklung werden die Monate eines Jahres für einen monatlichen Wochentag mithilfe der [**imonthlydowauslöst:: MONTHSOFYEAR**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) -Eigenschaft angegeben.

Die oben aufgeführten untergeordneten Elemente werden durch den komplexen [**monthstype**](taskschedulerschema-monthstype-complextype.md) -Typ definiert.

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

 

 





