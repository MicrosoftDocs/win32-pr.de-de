---
title: restartType Complex Type
description: Definiert die untergeordneten Elemente und Sequenzinformationen für das RestartOnFailure-Element.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- restartType complex type Taskplaner
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 996debc2c8e3d7d00ca7b42facde582f918d72736426ed326691461d800f8562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516479"
---
# <a name="restarttype-complex-type"></a>restartType Complex Type

Definiert die untergeordneten Elemente und Sequenzinformationen für das [RestartOnFailure-Element.](taskschedulerschema-restartonfailure-settingstype-element.md)

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



| Element                                                              | Typ | Beschreibung                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [**Anzahl**](taskschedulerschema-count-restarttype-element.md)       |      | Anzahl der Versuche, den Task neu zu starten.<br/> |
| [**Intervall**](taskschedulerschema-interval-restarttype-element.md) |      | Gibt an, wie lange versucht wird, die Aufgabe zu starten.<br/>      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Komplexe Schematypen](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





