---
title: Sessionstatechangetrigger (triggergroup)-Element
description: Gibt einen-Endpunkt an, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.
ms.assetid: 38b0da3c-205f-48c5-83e6-ff7c432c02b9
keywords:
- Sessionstatechange-Element Taskplaner
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21847a929e79e2da53b1e66a23aec0c2f1c630f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742753"
---
# <a name="sessionstatechangetrigger-triggergroup-element"></a>Sessionstatechangetrigger (triggergroup)-Element

Gibt einen-Endpunkt an, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.

``` syntax
<xs:element name="SessionStateChangeTrigger"
    type="sessionStateChangeTriggerType"
 />
```

Das **sessionstatechangetrigger** -Element wird von [**triggergroup**](taskschedulerschema-triggergroup-group.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                           | Abgeleitet von                                                         | BESCHREIBUNG                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Trigger**](taskschedulerschema-triggers-tasktype-element.md) | [**triggerstype**](taskschedulerschema-triggerstype-complextype.md) | Gibt die Trigger an, die den Task starten.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                      | type                                                                                    | BESCHREIBUNG                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Verzögern**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Gibt einen Wert an, der die Länge der Verzögerung angibt, bevor ein Task gestartet wird, wenn eine Terminal Server-Sitzungs Zustandsänderung erkannt wird.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionstatechangetype**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Gibt die Art der Terminal Server-Sitzungs Änderung an, die einen Task Start auslöst.<br/>                                                     |
| [**UserID**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Gibt den Benutzer für die Terminal Server Sitzung an. Wenn eine Sitzungs Zustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.<br/>              |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird ein Sitzungs Status Änderungs-Auslösung mithilfe des [**sessionstatechangeghost**](sessionstatechangetrigger.md) -Objekts angegeben.

Bei der C++-Entwicklung wird ein Sitzungs Status Änderungs-Auslösung mithilfe der [**isessionstatechange-**](/windows/desktop/api/taskschd/nn-taskschd-isessionstatechangetrigger) Schnittstelle angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





