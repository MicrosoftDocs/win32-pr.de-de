---
title: komplexer timeTriggerType-Typ
description: Definiert den Basistyp für das TimeTrigger-Element.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- komplexer timeTriggerType-Typ Taskplaner
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6f44f0959a9f67e4bfee0b0ef5dd7f095ffbadce
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734135"
---
# <a name="timetriggertype-complex-type"></a>komplexer timeTriggerType-Typ

Definiert den Basistyp für das [**TimeTrigger-Element.**](taskschedulerschema-timetrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                        | Typ     | BESCHREIBUNG                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RandomDelay**](taskschedulerschema-randomdelay-timetriggertype-element.md) | duration | Gibt die Verzögerungszeit an, die zufällig zur Startzeit des Triggers hinzugefügt wird. Das Format für diese Zeichenfolge lautet `P<days>DT<hours>H<minutes>M<seconds>S` (p2DT5S ist z. B. eine Verzögerung von 2 Tagen und 5 Sekunden). <br/> |



## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass dieses Element keine untergeordneten Elemente zu den elementen hinzufüge, die vom komplexen [**triggerBaseType-Typ**](taskschedulerschema-triggerbasetype-complextype.md) definiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[komplexe Schematypen Taskplaner](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





