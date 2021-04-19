---
title: komplexer monthlyscheduletype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das schedulebymonth (calendartriggertype)-Element.
ms.assetid: 3ade775c-ca44-403e-9602-80095c7dba1a
keywords:
- komplexer monthlyscheduletype-Typ Taskplaner
topic_type:
- apiref
api_name:
- monthlyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 132c2fafe2b05a01380c13aae2ab7cb3ddaa5330
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339554"
---
# <a name="monthlyscheduletype-complex-type"></a>komplexer monthlyscheduletype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**schedulebymonth (calendartriggertype)**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) -Element.

``` syntax
<xs:complexType name="monthlyScheduleType">
    <xs:all>
        <xs:element name="DaysOfMonth"
            type="daysOfMonthType"
            minOccurs="0"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type                                                                       | BESCHREIBUNG                                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysofmonthtype**](taskschedulerschema-daysofmonthtype-complextype.md) | Gibt die Tage des Monats an, in denen der Task ausgeführt wird.<br/>                         |
| [**Monate**](taskschedulerschema-months-monthlyscheduletype-element.md)           | [**monthstype**](taskschedulerschema-monthstype-complextype.md)           | Gibt die Monate des Jahres an, in denen der Task für einen monatlichen Zeitplan ausgeführt wird.<br/> |



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

 

 





