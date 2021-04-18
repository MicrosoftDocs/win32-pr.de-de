---
title: komplexer eventtriggertype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das EventTrigger-Element.
ms.assetid: c678af6f-bdfb-4c4d-85d7-2d93abfc2a7d
keywords:
- komplexer ereignistriggertyp Taskplaner
topic_type:
- apiref
api_name:
- eventTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16c3d4257d89ebb8d0efb6dadcd3ac466b929c9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345495"
---
# <a name="eventtriggertype-complex-type"></a>komplexer eventtriggertype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) -Element.

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



| Element                                                                           | type                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](taskschedulerschema-delay-eventtriggertype-element.md)               | duration                                                                | Gibt die Zeitspanne zwischen dem Auftreten des Ereignisses und dem Start der Aufgabe an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Abonnement**](taskschedulerschema-subscription-eventtriggertype-element.md) | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md) | Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den-Triggern auslöst.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Valuequeries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md)      | Gibt eine Sequenz von Elementen an, die jeweils einen Namen und einen XPath-Abfrage Wert enthalten. Die Abfragen werden auf ein Ereignis angewendet, das von dem im [**Abonnement**](taskschedulerschema-subscription-eventtriggertype-element.md) Element angegebenen Ereignis Abonnement zurückgegeben wurde. Der Name des XPath-Abfrage Werts kann als Variable im [**Body**](taskschedulerschema-body-showmessagetype-element.md) -Element im [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) -Aktions Abschnitt einer Aufgabe verwendet werden. <br/> |



## <a name="remarks"></a>Bemerkungen

Zusätzlich zum untergeordneten-Element, das hier definiert ist, verwendet das [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) -Element auch untergeordnete Elemente, die durch den komplexen [**triggerbasetype**](taskschedulerschema-triggerbasetype-complextype.md) -Typ definiert werden.

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

 

 





