---
title: komplexer registrationtriggertype-Typ
description: Definiert untergeordnete Elemente und Sequenzierungs Informationen für das Registration-Auslöserelement.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- komplexer registrationtriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ddb55436a0a6980a8909da636a02ca59244ca85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392082"
---
# <a name="registrationtriggertype-complex-type"></a>komplexer registrationtriggertype-Typ

Definiert untergeordnete Elemente und Sequenzierungs Informationen für das [**Registration-Auslöserelement**](taskschedulerschema-registrationtrigger-triggergroup-element.md) .

``` syntax
<xs:complexType name="registrationTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
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



| Element                                                                    | type     | BESCHREIBUNG                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [**Verzögern**](taskschedulerschema-delay-registrationtriggertype-element.md) | duration | Gibt die Zeitspanne zwischen dem Registrieren der Aufgabe und dem Start der Aufgabe an.<br/> |



## <a name="remarks"></a>Bemerkungen

Zusätzlich zu den hier definierten untergeordneten Elementen verwendet das [**registrationtrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) -Element auch untergeordnete Elemente, die durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert werden.

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

 

 





