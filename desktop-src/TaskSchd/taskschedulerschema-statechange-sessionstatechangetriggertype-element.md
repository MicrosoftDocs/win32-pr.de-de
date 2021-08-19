---
title: StateChange (sessionStateChangeTriggerType)-Element
description: Enthält die Art der Terminalserversitzungsänderung, die einen Taskstart auslösen würde.
ms.assetid: 0b17a4a5-caa7-4b58-a1a4-cbc7564838bb
keywords:
- StateChange-Element Taskplaner
topic_type:
- apiref
api_name:
- StateChange
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88b7e46b23cf6778379a967e03d8f168de3b18d20a734812bacdad940850136a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356332"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a>StateChange (sessionStateChangeTriggerType)-Element

Enthält die Art der Terminalserversitzungsänderung, die einen Taskstart auslösen würde.

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

Das **StateChange-Element** wird vom komplexen [**SessionStateChangeTriggerType-Typ**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                       | Abgeleitet von                                                                                           | BESCHREIBUNG                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn sich der Zustand einer Terminalserversitzung ändert.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**StateChange-Eigenschaft von ISessionStateChangeTrigger.**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange)

Informationen zur Skriptentwicklung finden Sie unter [**SessionStateChangeTrigger.StateChange**](sessionstatechangetrigger-statechange.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





