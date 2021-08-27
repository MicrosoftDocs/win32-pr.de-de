---
title: SessionStateChangeTrigger (triggerGroup)-Element
description: Gibt einen Trigger an, der eine Aufgabe startet, wenn sich der Status einer Terminalserversitzung ändert.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- SessionStateChangeTrigger-Element Taskplaner
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d22b2f47584f437c01575ffecfb6d5c25e312b9584ba46abc9d6997e14187eaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099820"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a>SessionStateChangeTrigger (triggerGroup)-Element

Gibt einen Trigger an, der eine Aufgabe startet, wenn sich der Status einer Terminalserversitzung ändert.

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

Das **SessionStateChangeTrigger-Element** wird durch die [**triggerGroup definiert.**](taskschedulerschema-triggergroup-group.md)

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Auslöser**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die die Aufgabe starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                      | type                                                                                    | BESCHREIBUNG                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Gibt einen Wert an, der die Länge der Verzögerung angibt, bevor ein Task gestartet wird, wenn eine Änderung des Sitzungszustands des Terminalservers erkannt wird.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Gibt die Art der Terminalserver-Sitzungsänderung an, die einen Taskstart auslösen würde.<br/>                                                     |
| [**Userid**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Gibt den Benutzer für die Terminalserversitzung an. Wenn eine Änderung des Sitzungszustands für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.<br/>              |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird ein Sitzungszustandsänderungstrigger mithilfe des [**SessionStateChangeTrigger-Objekts**](sessionstatechangetrigger.md) angegeben.

Für die C++-Entwicklung wird ein Sitzungszustandsänderungstrigger mithilfe der [**ISessionStateChangeTrigger-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





