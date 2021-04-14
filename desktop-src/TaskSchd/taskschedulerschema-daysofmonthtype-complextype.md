---
title: komplexer daysofmonthtype-Typ
description: Definiert das untergeordnete Element und die Sequenzierungs Informationen für das daysOfMonth (monthlyscheduletype)-Element.
ms.assetid: 8258c090-c836-497e-8e5b-db4782277822
keywords:
- komplexer daysofmonthtype-Typ Taskplaner
topic_type:
- apiref
api_name:
- daysOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f1459528b47bf01a9e336b758b739c3f5751ee1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392119"
---
# <a name="daysofmonthtype-complex-type"></a>komplexer daysofmonthtype-Typ

Definiert das untergeordnete Element und die Sequenzierungs Informationen für das [**daysOfMonth (monthlyscheduletype)**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) -Element.

``` syntax
<xs:complexType name="daysOfMonthType">
    <xs:sequence>
        <xs:element name="Day"
            type="dayOfMonthType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                        | type                                                                    | BESCHREIBUNG                                                          |
|----------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**Tag**](taskschedulerschema-day-daysofmonthtype-element.md) | [**dayoatmonthtype**](taskschedulerschema-dayofmonthtype-simpletype.md) | Gibt den Tag des Monats an, in dem die Aufgabe ausgeführt wird. <br/> |



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

 

 





