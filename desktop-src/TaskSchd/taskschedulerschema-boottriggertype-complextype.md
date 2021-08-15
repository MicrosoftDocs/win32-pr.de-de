---
title: 'BootTriggerType : Komplexer Typ'
description: Definiert das untergeordnete Element und Sequenzierungsinformationen für das BootTrigger-Element.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- komplexer bootTriggerType-Typ Taskplaner
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc0b04bfaf08ecee87d02a2b410fd1df2fbbe584d5649a5e9fe2ea2e5efacebd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131859"
---
# <a name="boottriggertype-complex-type"></a>BootTriggerType : Komplexer Typ

Definiert das untergeordnete Element und Sequenzierungsinformationen für das [**BootTrigger-Element.**](taskschedulerschema-boottrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="bootTriggerType">
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



| Element                                                            | type     | BESCHREIBUNG                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [**Verzögern**](taskschedulerschema-delay-boottriggertype-element.md) | duration | Die Zeitspanne zwischen dem Start des Systems und dem Auslösen des Triggers. <br/> |



## <a name="remarks"></a>Hinweise

Zusätzlich zum hier definierten untergeordneten Element verwendet das [**BootTrigger-Element**](taskschedulerschema-boottrigger-triggergroup-element.md) auch untergeordnete Elemente, die vom komplexen [**triggerBaseType-Typ**](taskschedulerschema-triggerbasetype-complextype.md) definiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[komplexe Schematypen Taskplaner](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





