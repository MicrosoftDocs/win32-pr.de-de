---
title: komplexer maintenancesettingstype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das maintenancesettings-Element.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- komplexer maintenancesettingstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742761"
---
# <a name="maintenancesettingstype-complex-type"></a>komplexer maintenancesettingstype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**maintenancesettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) -Element.

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
        >
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="P1D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                        | type    | BESCHREIBUNG                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stichtag**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | Gibt die Zeitspanne an, nach der der Taskplaner versucht, die Aufgabe während der automatischen Notfallwartung zu starten, wenn dieser während der regulären Wartung nicht fertiggestellt werden konnte.<br/> |
| **Exklusiv**                                                                  | boolean | Wenn diese Einstellung auf "true" festgelegt ist, wird die Aufgabe ausschließlich unter anderen Wartungs Tasks gestartet.<br/>                                                                                                 |
| [**Zeitraum**](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss.<br/>                                                                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komplexe Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





