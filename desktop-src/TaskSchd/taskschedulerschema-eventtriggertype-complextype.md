---
title: EventTriggerType Complex Type
description: Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das EventTrigger-Element.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- Komplexe EventTriggerType-Taskplaner
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0acd4bafa6033e461b69180862a8302e76f363b581d7f06b0812824f2031780b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612053"
---
# <a name="eventtriggertype-complex-type"></a>EventTriggerType Complex Type

Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das [**EventTrigger-Element.**](taskschedulerschema-eventtrigger-triggergroup-element.md)

``` syntax
<xs:complexType name="eventTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Subscription"
                    type="nonEmptyString"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="ValueQueries"
                    type="namedValues"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | type                                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                | Gibt die Zeit zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den Trigger auslöst.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md)      | Gibt eine Sequenz von Elementen an, die jeweils einen Namen und einen XPath-Abfragewert enthalten. Die Abfragen werden auf ein Ereignis angewendet, das von dem ereignisabonnement zurückgegeben wird, das im [**Subscription-Element angegeben**](taskschedulerschema-subscription-eventtriggertype-element.md) ist. Der Name für den XPath-Abfragewert kann als Variable im [**Body-Element**](taskschedulerschema-body-showmessagetype-element.md) im [**Aktionsabschnitt ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) einer Aufgabe verwendet werden. <br/> |



## <a name="remarks"></a>Hinweise

Zusätzlich zum hier definierten untergeordneten Element verwendet [**das EventTrigger-Element**](taskschedulerschema-eventtrigger-triggergroup-element.md) auch untergeordnete Elemente, die durch den [**komplexen TriggerBaseType-Typ**](taskschedulerschema-triggerbasetype-complextype.md) definiert werden.

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

 

 





