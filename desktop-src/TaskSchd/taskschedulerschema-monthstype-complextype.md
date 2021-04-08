---
title: komplexer monthstype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für die Monate (monthlydayosweekscheduletype) und die Monate (monthlyscheduletype).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- komplexer monthstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6a19000073fd12e05aa915921850264979a0541
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740440"
---
# <a name="monthstype-complex-type"></a>komplexer monthstype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für die [**Monate (monthlydayosweekscheduletype)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) und die [**Monate (monthlyscheduletype)**](taskschedulerschema-months-monthlyscheduletype-element.md) .

``` syntax
<xs:complexType name="monthsType">
    <xs:all>
        <xs:element name="January"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="February"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="March"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="April"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="May"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="June"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="July"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="August"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="September"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="October"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="November"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="December"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | type | BESCHREIBUNG                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [**Am**](taskschedulerschema-april-monthstype-element.md)         | –  | Gibt an, dass der Task im April ausgeführt wird. <br/>     |
| [**August**](taskschedulerschema-august-monthstype-element.md)       | –  | Gibt an, dass der Task im August ausgeführt wird. <br/>    |
| [**Dezember**](taskschedulerschema-december-monthstype-element.md)   | –  | Gibt an, dass der Task im Dezember ausgeführt wird. <br/>  |
| [**Februar**](taskschedulerschema-february-monthstype-element.md)   | –  | Gibt an, dass der Task im Februar ausgeführt wird. <br/>  |
| [**January**](taskschedulerschema-january-monthstype-element.md)     | –  | Gibt an, dass der Task im Januar ausgeführt wird. <br/>   |
| [**Juli**](taskschedulerschema-july-monthstype-element.md)           | –  | Gibt an, dass der Task im Juli ausgeführt wird. <br/>      |
| [**June**](taskschedulerschema-june-monthstype-element.md)           | –  | Gibt an, dass der Task im Juni ausgeführt wird. <br/>      |
| [**März**](taskschedulerschema-march-monthstype-element.md)         | –  | Gibt an, dass der Task im März ausgeführt wird. <br/>     |
| [**May**](taskschedulerschema-may-monthstype-element.md)             | –  | Gibt an, dass der Task im Mai ausgeführt wird. <br/>       |
| [**November**](taskschedulerschema-november-monthstype-element.md)   | –  | Gibt an, dass der Task im November ausgeführt wird. <br/>  |
| [**Vom**](taskschedulerschema-october-monthstype-element.md)     | –  | Gibt an, dass der Task im Oktober ausgeführt wird. <br/>   |
| [**September**](taskschedulerschema-september-monthstype-element.md) | –  | Gibt an, dass der Task im September ausgeführt wird. <br/> |



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

 

 





