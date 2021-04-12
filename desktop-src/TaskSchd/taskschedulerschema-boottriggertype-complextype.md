---
title: komplexer boottriggertype-Typ
description: Definiert das untergeordnete Element und die Sequenzierungs Informationen für das boottrigger-Element.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- komplexer boottriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d16634cacb9c17e5027ac9e6b6dd7abb26b78007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478192"
---
# <a name="boottriggertype-complex-type"></a>komplexer boottriggertype-Typ

Definiert das untergeordnete Element und die Sequenzierungs Informationen für das [**boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) -Element.

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
| [**Verzögern**](taskschedulerschema-delay-boottriggertype-element.md) | duration | Zeitspanne zwischen dem Starten des Systems und dem Auslösen des Auslösers. <br/> |



## <a name="remarks"></a>Bemerkungen

Zusätzlich zum untergeordneten-Element, das hier definiert ist, verwendet das [**boottrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) -Element auch untergeordnete Elemente, die durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert werden.

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

 

 





