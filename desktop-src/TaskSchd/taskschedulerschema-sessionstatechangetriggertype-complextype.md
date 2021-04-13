---
title: komplexer sessionstatechangetriggertype-Typ
description: Definiert die Elemente, die zum Erstellen eines Task Auslösers für die Konsolen Verbindung oder die Verbindung, Remote Verbindung oder Verbindung oder Arbeitsstations Sperre und-Sperre verwendet werden.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- komplexer sessionstatechangetriggertype-Typ Taskplaner
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341298"
---
# <a name="sessionstatechangetriggertype-complex-type"></a>komplexer sessionstatechangetriggertype-Typ

Definiert die Elemente, die zum Erstellen eines Task Auslösers für die Konsolen Verbindung oder die Verbindung, Remote Verbindung oder Verbindung oder Arbeitsstations Sperre und-Sperre verwendet werden.

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
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
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                      | type                                                                                    | BESCHREIBUNG                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Gibt einen Wert an, der die Länge der Verzögerung angibt, bevor ein Task gestartet wird, wenn eine Terminal Server-Sitzungs Zustandsänderung erkannt wird.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionstatechangetype**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Gibt die Art der Terminal Server-Sitzungs Änderung an, die einen Task Start auslöst.<br/>                                                     |
| [**UserID**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Gibt den Benutzer für die Terminal Server Sitzung an. Wenn eine Sitzungs Zustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.<br/>              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





