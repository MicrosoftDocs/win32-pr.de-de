---
title: 'registrationTriggerType : Komplexer Typ'
description: Definiert untergeordnete Elemente und Sequenzinformationen für das RegistrationTrigger-Element.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- 'registrationTriggerType: komplexer Typ Taskplaner'
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dab91ecc0eed065a4ce3eea9d64bebae2e10560a43ab57308ea68e82dc17dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772280"
---
# <a name="registrationtriggertype-complex-type"></a>registrationTriggerType : Komplexer Typ

Definiert untergeordnete Elemente und Sequenzinformationen für das [**RegistrationTrigger-Element.**](taskschedulerschema-registrationtrigger-triggergroup-element.md)

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



| Element                                                                    | Typ     | Beschreibung                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [**Verzögern**](taskschedulerschema-delay-registrationtriggertype-element.md) | duration | Gibt die Zeitspanne zwischen der Registrierung des Tasks und dem Start des Tasks an.<br/> |



## <a name="remarks"></a>Hinweise

Zusätzlich zu den hier definierten untergeordneten Elementen verwendet das [**RegistrationTrigger-Element**](taskschedulerschema-registrationtrigger-triggergroup-element.md) auch untergeordnete Elemente, die vom komplexen [**triggerBaseType-Typ**](taskschedulerschema-triggerbasetype-complextype.md) definiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[komplexe Typen Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





