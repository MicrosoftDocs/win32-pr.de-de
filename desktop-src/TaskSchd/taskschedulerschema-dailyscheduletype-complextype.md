---
title: komplexer dailyscheduletype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das schedulebyday-Element.
ms.assetid: e0b1b09f-d72a-4a85-9059-4a917bc0104a
keywords:
- komplexer dailyscheduletype-Typ Taskplaner
topic_type:
- apiref
api_name:
- dailyScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5982ab7e72a79dc909a4e91fafe363ca4703639d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346743"
---
# <a name="dailyscheduletype-complex-type"></a>komplexer dailyscheduletype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**schedulebyday**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) -Element.

``` syntax
<xs:complexType name="dailyScheduleType">
    <xs:all>
        <xs:element name="DaysInterval"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="unsignedInt"
                >
                    <xs:minInclusive
                        value="1"
                     />
                    <xs:maxInclusive
                        value="365"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                            | type | BESCHREIBUNG                                                          |
|------------------------------------------------------------------------------------|------|----------------------------------------------------------------------|
| [**Daysinterval**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |      | Gibt das Intervall zwischen den Tagen im Zeitplan an. <br/> |



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

 

 





