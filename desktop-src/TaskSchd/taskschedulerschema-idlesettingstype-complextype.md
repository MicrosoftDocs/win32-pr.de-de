---
title: komplexer idlesettingstype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das idlesettings (settingstype)-Element.
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- komplexer idlesettingstype-Typ Taskplaner
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338133"
---
# <a name="idlesettingstype-complex-type"></a>komplexer idlesettingstype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**idlesettings (settingstype)**](taskschedulerschema-idlesettings-settingstype-element.md) -Element.

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
        <xs:element name="Duration"
            default="PT10M"
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
        <xs:element name="WaitTimeout"
            default="PT1H"
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
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                  | type    | BESCHREIBUNG                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](taskschedulerschema-duration-idlesettingstype-element.md)                |         | Gibt die Zeitspanne an, die zum Starten der Aufgabe in einer Leerlauf Bedingung zulässig ist.<br/>                                                                                                                     |
| [**Neustartondle**](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | boolean | Der Task wird neu gestartet, sobald eine Leerlauf Bedingung gestartet wird.<br/>                                                                                                                                             |
| [**Stoponidleend**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | boolean | Gibt an, dass der Task beendet wird, wenn die Leerlauf Bedingung endet, bevor die Leerlauf Dauer überschritten wird.<br/>                                                                                                 |
| [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | Gibt die Zeitspanne an, die gewartet werden soll, bis eine Leerlauf Bedingung gestartet wird. Wenn für dieses Element kein Wert angegeben wird, wartet der Taskplaner-Dienst unbegrenzt, bis eine Leerlauf Bedingung auftritt.<br/> |



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

 

 





