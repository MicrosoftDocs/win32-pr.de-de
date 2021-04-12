---
title: Monate (monthlyscheduletype)-Element
description: Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
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
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105369"
---
# <a name="months-monthlyscheduletype-element"></a>Monate (monthlyscheduletype)-Element

Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

Das **Monats** Element wird durch den komplexen [**monthlyscheduletype**](taskschedulerschema-monthlyscheduletype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                    | Abgeleitet von                                                                       | BESCHREIBUNG                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [**Schedulebymonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyscheduletype**](taskschedulerschema-monthlyscheduletype-complextype.md) | Gibt einen monatlichen Zeitplan an. <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type | BESCHREIBUNG                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**April (monthstype)**](taskschedulerschema-april-monthstype-element.md)         |      | Gibt an, dass der Task im April ausgeführt wird.<br/>     |
| [**August (monthstype)**](taskschedulerschema-august-monthstype-element.md)       |      | Gibt an, dass der Task im August ausgeführt wird.<br/>    |
| [**Dezember (monthstype)**](taskschedulerschema-december-monthstype-element.md)   |      | Gibt an, dass der Task im Dezember ausgeführt wird.<br/>  |
| [**Februar (monthstype)**](taskschedulerschema-february-monthstype-element.md)   |      | Gibt an, dass der Task im Februar ausgeführt wird.<br/>  |
| [**Januar (monthstype)**](taskschedulerschema-january-monthstype-element.md)     |      | Gibt an, dass der Task im Januar ausgeführt wird.<br/>   |
| [**Juli (monthstype)**](taskschedulerschema-july-monthstype-element.md)           |      | Gibt an, dass der Task im Juli ausgeführt wird.<br/>      |
| [**Juni (monthstype)**](taskschedulerschema-june-monthstype-element.md)           |      | Gibt an, dass der Task im Juni ausgeführt wird.<br/>      |
| [**März (monthstype)**](taskschedulerschema-march-monthstype-element.md)         |      | Gibt an, dass der Task im März ausgeführt wird.<br/>     |
| [**Mai (monthstype)**](taskschedulerschema-may-monthstype-element.md)             |      | Gibt an, dass der Task im Mai ausgeführt wird.<br/>       |
| [**November (monthstype)**](taskschedulerschema-november-monthstype-element.md)   |      | Gibt an, dass der Task im November ausgeführt wird.<br/>  |
| [**Oktober (monthstype)**](taskschedulerschema-october-monthstype-element.md)     |      | Gibt an, dass der Task im Oktober ausgeführt wird.<br/>   |
| [**September (monthstype)**](taskschedulerschema-september-monthstype-element.md) |      | Gibt an, dass der Task im September ausgeführt wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung werden die Monate des Zeitplans mithilfe der [**Monthly-Eigenschaft. MONTHSOFYEAR**](monthlytrigger-monthsofyear.md) angegeben.

Bei der C++-Entwicklung werden die Monate des Zeitplans mithilfe der [**imonthlyauslöst:: MONTHSOFYEAR**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Im folgenden XML-Code wird ein monatlicher Kalender definiert, der die Aufgabe am 1. und 15. Tag eines jeden Monats des Jahres startet.


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
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

 

 





