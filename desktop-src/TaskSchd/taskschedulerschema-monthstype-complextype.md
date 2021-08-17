---
title: monthsType Complex Type
description: Definiert die untergeordneten Elemente und Sequenzierungsinformationen für die Elemente Months (monthlyDayOfWeekScheduleType) und Months (monthlyScheduleType).
ms.assetid: f1faa67a-2f5f-4a00-a1df-2d44e218278b
keywords:
- monthsType complex type Taskplaner
topic_type:
- apiref
api_name:
- monthsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a0873f07cc76af9fab827c3df98a8f08ef300de93d4ae6b316809ba32aac87ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758746"
---
# <a name="monthstype-complex-type"></a>monthsType Complex Type

Definiert die untergeordneten Elemente und Sequenzierungsinformationen für [**die Elemente Months (monthlyDayOfWeekScheduleType)**](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) und [**Months (monthlyScheduleType).**](taskschedulerschema-months-monthlyscheduletype-element.md)

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



| Element                                                               | type | Beschreibung                                            |
|-----------------------------------------------------------------------|------|--------------------------------------------------------|
| [**April**](taskschedulerschema-april-monthstype-element.md)         | Nicht zutreffend  | Gibt an, dass die Aufgabe im April ausgeführt wird. <br/>     |
| [**August**](taskschedulerschema-august-monthstype-element.md)       | Nicht zutreffend  | Gibt an, dass die Aufgabe im August ausgeführt wird. <br/>    |
| [**Dezember**](taskschedulerschema-december-monthstype-element.md)   | Nicht zutreffend  | Gibt an, dass die Aufgabe im Dezember ausgeführt wird. <br/>  |
| [**Februar**](taskschedulerschema-february-monthstype-element.md)   | Nicht zutreffend  | Gibt an, dass die Aufgabe im Februar ausgeführt wird. <br/>  |
| [**January**](taskschedulerschema-january-monthstype-element.md)     | Nicht zutreffend  | Gibt an, dass die Aufgabe im Januar ausgeführt wird. <br/>   |
| [**Juli**](taskschedulerschema-july-monthstype-element.md)           | Nicht zutreffend  | Gibt an, dass die Aufgabe im Juli ausgeführt wird. <br/>      |
| [**June**](taskschedulerschema-june-monthstype-element.md)           | Nicht zutreffend  | Gibt an, dass die Aufgabe im Juni ausgeführt wird. <br/>      |
| [**März**](taskschedulerschema-march-monthstype-element.md)         | Nicht zutreffend  | Gibt an, dass die Aufgabe im März ausgeführt wird. <br/>     |
| [**May**](taskschedulerschema-may-monthstype-element.md)             | Nicht zutreffend  | Gibt an, dass die Aufgabe im Mai ausgeführt wird. <br/>       |
| [**November**](taskschedulerschema-november-monthstype-element.md)   | Nicht zutreffend  | Gibt an, dass die Aufgabe im November ausgeführt wird. <br/>  |
| [**Oktober**](taskschedulerschema-october-monthstype-element.md)     | Nicht zutreffend  | Gibt an, dass die Aufgabe im Oktober ausgeführt wird. <br/>   |
| [**September**](taskschedulerschema-september-monthstype-element.md) | Nicht zutreffend  | Gibt an, dass die Aufgabe im September ausgeführt wird. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Komplexe Schematypen](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





