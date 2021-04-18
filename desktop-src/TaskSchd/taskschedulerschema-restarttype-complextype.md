---
title: komplexer restarttype-Typ
description: Definiert die untergeordneten Elemente und Sequenz Informationen für das restartonfailure-Element.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- komplexer restarttype-Typ Taskplaner
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519127"
---
# <a name="restarttype-complex-type"></a>komplexer restarttype-Typ

Definiert die untergeordneten Elemente und Sequenz Informationen für das [restartonfailure](taskschedulerschema-restartonfailure-settingstype-element.md) -Element.

``` syntax
<xs:complexType name="restartType">
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
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                              | type | BESCHREIBUNG                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [**Countdown**](taskschedulerschema-count-restarttype-element.md)       |      | Anzahl der Versuche, den Task neu zu starten.<br/> |
| [**Intervall**](taskschedulerschema-interval-restarttype-element.md) |      | Gibt an, wie lange versucht wird, die Aufgabe zu starten.<br/>      |



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

 

 





