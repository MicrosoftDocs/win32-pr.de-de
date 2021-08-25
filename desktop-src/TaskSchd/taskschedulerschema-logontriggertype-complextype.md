---
title: LogonTriggerType Complex Type
description: Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das LogonTrigger-Element.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- Komplexer LogonTriggerType-Taskplaner
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85cbbeaa5d911b1ef9677c79980167a66cdf410c7aa63597b02b007795dfbd81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991211"
---
# <a name="logontriggertype-complex-type"></a>LogonTriggerType Complex Type

Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das [**LogonTrigger-Element.**](taskschedulerschema-logontrigger-triggergroup-element.md)

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



| Element                                                               | type                                                                    | Beschreibung                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**Verzögern**](taskschedulerschema-delay-logontriggertype-element.md)   | duration                                                                | Die Zeit zwischen dem Zeitpunkt, in dem sich der Benutzer anmeldet, und dem Start der Aufgabe.<br/>         |
| [**Userid**](taskschedulerschema-userid-logontriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Bezeichner des Benutzers. Die Aufgabe wird gestartet, wenn sich dieser Benutzer beim Computer anmeldet.<br/> |



## <a name="remarks"></a>Hinweise

Zusätzlich zu den hier definierten untergeordneten Elementen verwendet das [**LogonTrigger-Element**](taskschedulerschema-logontrigger-triggergroup-element.md) auch untergeordnete Elemente, die durch den [**komplexen TriggerBaseType-Typ**](taskschedulerschema-triggerbasetype-complextype.md) definiert werden.

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

 

 





