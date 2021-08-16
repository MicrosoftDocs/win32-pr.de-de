---
title: UserId (sessionStateChangeTriggerType) -Element
description: Enthält den Benutzer für die Terminalserversitzung. Wenn eine Änderung des Sitzungszustands für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
keywords:
- UserId-Element Taskplaner
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6f6ddaf196f83d727e4641df6e59375033eb60c076451d70866d9d227ca457d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355575"
---
# <a name="userid-sessionstatechangetriggertype-element"></a>UserId (sessionStateChangeTriggerType) -Element

Enthält den Benutzer für die Terminalserversitzung. Wenn eine Änderung des Sitzungszustands für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

Das **UserId-Element** wird durch den komplexen [**SessionStateChangeTriggerType-Typ**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                       | Abgeleitet von                                                                                           | BESCHREIBUNG                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn sich der Status einer Terminalserversitzung ändert.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**UserId-Eigenschaft von ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).

Informationen zur Skriptentwicklung finden Sie unter [**SessionStateChangeTrigger.UserId**](sessionstatechangetrigger-userid.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





