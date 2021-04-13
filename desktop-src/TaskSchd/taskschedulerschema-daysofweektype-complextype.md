---
title: komplexer tagsofweektype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für die Elemente DaysOfWeek (weeklyscheduletype) und DaysOfWeek (monthlydayosweekscheduletype).
ms.assetid: b3315582-af7a-4d4c-8f6f-61de12a85f46
keywords:
- komplexer tagsofweektype-Typ Taskplaner
topic_type:
- apiref
api_name:
- daysOfWeekType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4a1b5e6aeaa77c0bdfe12b1d5b68fde018f236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341337"
---
# <a name="daysofweektype-complex-type"></a>komplexer tagsofweektype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für die Elemente [**DaysOfWeek (weeklyscheduletype)**](taskschedulerschema-daysofweek-weeklyscheduletype-element.md) und [**DaysOfWeek (monthlydayosweekscheduletype)**](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) .

``` syntax
<xs:complexType name="daysOfWeekType">
    <xs:all>
        <xs:element name="Monday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Tuesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Wednesday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Thursday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Friday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Saturday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
        <xs:element name="Sunday"
            minOccurs="0"
        >
            <xs:complexType />
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                   | type | BESCHREIBUNG                         |
|---------------------------------------------------------------------------|------|-------------------------------------|
| [**Am**](taskschedulerschema-friday-daysofweektype-element.md)       | –  | Der Task wird am Freitag ausgeführt. <br/>    |
| [**Pfingst**](taskschedulerschema-monday-daysofweektype-element.md)       | –  | Der Task wird am Montag ausgeführt.<br/>     |
| [**Samstag**](taskschedulerschema-saturday-daysofweektype-element.md)   | –  | Der Task wird am Samstag ausgeführt. <br/>  |
| [**Sunday**](taskschedulerschema-sunday-daysofweektype-element.md)       | –  | Der Task wird am Sonntag ausgeführt. <br/>    |
| [**Mitteilte**](taskschedulerschema-thursday-daysofweektype-element.md)   | –  | Task wird am Donnerstag ausgeführt <br/>   |
| [**Mitteilte**](taskschedulerschema-tuesday-daysofweektype-element.md)     | –  | Der Task wird am Dienstag ausgeführt. <br/>   |
| [**Mittwochs**](taskschedulerschema-wednesday-daysofweektype-element.md) | –  | Der Task wird am Mittwoch ausgeführt. <br/> |



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

 

 





