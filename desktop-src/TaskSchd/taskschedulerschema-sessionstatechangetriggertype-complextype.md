---
title: komplexer SessionStateChangeTriggerType-Typ
description: Definiert die Elemente, die zum Erstellen eines Aufgabentriggers für Konsolenverbindung oder -trennung, Remoteverbindung oder -trennung oder Benachrichtigungen zum Sperren oder Entsperren der Arbeitsstation verwendet werden.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- komplexer sessionStateChangeTriggerType-Typ Taskplaner
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e9779ae2f609f721e4417dc08698e9720bd4cbe03c2b59787edcf862c8d284d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990940"
---
# <a name="sessionstatechangetriggertype-complex-type"></a>komplexer SessionStateChangeTriggerType-Typ

Definiert die Elemente, die zum Erstellen eines Aufgabentriggers für Konsolenverbindung oder -trennung, Remoteverbindung oder -trennung oder Benachrichtigungen zum Sperren oder Entsperren der Arbeitsstation verwendet werden.

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
| [**Verzögern**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Gibt einen Wert an, der die Länge der Verzögerung angibt, bevor ein Task gestartet wird, wenn eine Änderung des Terminalserver-Sitzungszustands erkannt wird.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Gibt die Art der Terminalserversitzungsänderung an, die einen Taskstart auslösen würde.<br/>                                                     |
| [**Userid**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Gibt den Benutzer für die Terminalserversitzung an. Wenn eine Sitzungszustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.<br/>              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





