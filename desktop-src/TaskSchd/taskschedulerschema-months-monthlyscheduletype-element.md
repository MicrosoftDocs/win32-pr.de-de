---
title: Months(monthlyScheduleType)-Element
description: Gibt die Monate des Jahres an, in denen die Aufgabe für einen monatlichen Zeitplan ausgeführt wird.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
keywords:
- Months-Taskplaner
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b655b47fc3135006f8629246d63350d36a4b32e92398a00f40ae86fe3f70d1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796500"
---
# <a name="months-monthlyscheduletype-element"></a>Months(monthlyScheduleType)-Element

Gibt die Monate des Jahres an, in denen die Aufgabe für einen monatlichen Zeitplan ausgeführt wird.

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

Das **Months-Element** wird durch den komplexen [**monthlyScheduleType-Typ**](taskschedulerschema-monthlyscheduletype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                    | Abgeleitet von                                                                       | Beschreibung                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) | Gibt einen monatlichen Zeitplan an. <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | Typ | Beschreibung                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [**April (monthsType)**](taskschedulerschema-april-monthstype-element.md)         |      | Gibt an, dass die Aufgabe im April ausgeführt wird.<br/>     |
| [**August (monthsType)**](taskschedulerschema-august-monthstype-element.md)       |      | Gibt an, dass die Aufgabe im August ausgeführt wird.<br/>    |
| [**Dezember (monthsType)**](taskschedulerschema-december-monthstype-element.md)   |      | Gibt an, dass die Aufgabe im Dezember ausgeführt wird.<br/>  |
| [**Februar (monthsType)**](taskschedulerschema-february-monthstype-element.md)   |      | Gibt an, dass die Aufgabe im Februar ausgeführt wird.<br/>  |
| [**Januar (monthsType)**](taskschedulerschema-january-monthstype-element.md)     |      | Gibt an, dass die Aufgabe im Januar ausgeführt wird.<br/>   |
| [**Juli (monthsType)**](taskschedulerschema-july-monthstype-element.md)           |      | Gibt an, dass die Aufgabe im Juli ausgeführt wird.<br/>      |
| [**Juni (monthsType)**](taskschedulerschema-june-monthstype-element.md)           |      | Gibt an, dass die Aufgabe im Juni ausgeführt wird.<br/>      |
| [**März (monthsType)**](taskschedulerschema-march-monthstype-element.md)         |      | Gibt an, dass die Aufgabe im März ausgeführt wird.<br/>     |
| [**Mai (monthsType)**](taskschedulerschema-may-monthstype-element.md)             |      | Gibt an, dass die Aufgabe im Mai ausgeführt wird.<br/>       |
| [**November (monthsType)**](taskschedulerschema-november-monthstype-element.md)   |      | Gibt an, dass die Aufgabe im November ausgeführt wird.<br/>  |
| [**Oktober (monthsType)**](taskschedulerschema-october-monthstype-element.md)     |      | Gibt an, dass die Aufgabe im Oktober ausgeführt wird.<br/>   |
| [**September (monthsType)**](taskschedulerschema-september-monthstype-element.md) |      | Gibt an, dass die Aufgabe im September ausgeführt wird.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung werden die Monate des Zeitplans mithilfe der [**MonthlyTrigger.MonthsOfYear-Eigenschaft**](monthlytrigger-monthsofyear.md) angegeben.

Bei der C++-Entwicklung werden die Monate des Zeitplans mithilfe der [**IMonthlyTrigger::MonthsOfYear-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen monatlichen Kalender, der die Aufgabe am 1. und 15. Tag jedes Monats des Jahres startet.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





