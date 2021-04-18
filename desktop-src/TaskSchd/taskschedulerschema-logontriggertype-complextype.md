---
title: komplexer logontriggertype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das Logon-Auslöserelement.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- komplexer logontriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340015"
---
# <a name="logontriggertype-complex-type"></a>komplexer logontriggertype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**Logon-Auslöserelement**](taskschedulerschema-logontrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | type                                                                    | BESCHREIBUNG                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Verzögern**](taskschedulerschema-delay-logontriggertype-element.md)   | duration                                                                | Zeitraum zwischen dem Zeitpunkt, an dem sich der Benutzer anmeldet, und dem Start der Aufgabe.<br/>         |
| [**UserID**](taskschedulerschema-userid-logontriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Der Bezeichner des Benutzers. Der Task wird gestartet, wenn sich dieser Benutzer auf dem Computer anmeldet.<br/> |



## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den hier definierten untergeordneten Elementen verwendet das [**logontrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) -Element auch untergeordnete Elemente, die durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert werden.

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

 

 





