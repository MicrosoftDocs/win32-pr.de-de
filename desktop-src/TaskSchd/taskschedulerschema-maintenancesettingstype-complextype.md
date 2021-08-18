---
title: 'maintenanceSettingsType : Komplexer Typ'
description: Definiert die untergeordneten Elemente und Sequenzinformationen für das MaintenanceSettings-Element.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- 'maintenanceSettingsType: komplexer Typ Taskplaner'
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0733d16ec929b4e67774fc436c1530b67d70392b2655525b2aaaa642c2ea346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139203"
---
# <a name="maintenancesettingstype-complex-type"></a>maintenanceSettingsType : Komplexer Typ

Definiert die untergeordneten Elemente und Sequenzinformationen für das [**MaintenanceSettings-Element.**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md)

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



| Element                                                                        | type    | Beschreibung                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Stichtag**](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | Gibt die Zeitspanne an, nach der der Taskplaner versucht, den Task während der automatischen Notfallwartung zu starten, wenn er während der regulären Wartung nicht abgeschlossen werden konnte.<br/> |
| **Exklusiv**                                                                  | boolean | Wenn diese Einstellung auf TRUE festgelegt ist, wird der Task ausschließlich mit anderen Wartungstasks gestartet.<br/>                                                                                                 |
| [**Zeitraum**](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | Gibt an, wie oft der Task während der automatischen Wartung gestartet werden muss.<br/>                                                                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[komplexe Typen Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





