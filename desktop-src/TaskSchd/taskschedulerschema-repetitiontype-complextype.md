---
title: komplexer Wiederholungstyp
description: Definiert die untergeordneten Elemente und Sequenz Informationen für das Wiederholungs Element (triggerbasetype).
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- komplexer Wiederholungstyp Taskplaner
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa9ee8c08a79f5db053b772c86929f98a72f011c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392081"
---
# <a name="repetitiontype-complex-type"></a>komplexer Wiederholungstyp

Definiert die untergeordneten Elemente und Sequenz Informationen für das [**Wiederholungs Element (triggerbasetype)**](taskschedulerschema-repetition-triggerbasetype-element.md) .

``` syntax
<xs:complexType name="repetitionType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Duration"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                   | type    | BESCHREIBUNG                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-repetitiontype-element.md)                   |         | Gibt an, wie lange das Muster wiederholt wird. Wenn kein Wert angegeben wird, wird das Muster unbegrenzt wiederholt.<br/> |
| [**Intervall**](taskschedulerschema-interval-repetitiontype-element.md)                   |         | Gibt die Zeitspanne zwischen den einzelnen Neustarts der Aufgabe an.<br/>                                              |
| [**Stopatdurationend**](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | boolean | Gibt an, dass eine laufende Instanz der Aufgabe am Ende der Wiederholungsmuster Dauer beendet wird.<br/>     |



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

 

 





