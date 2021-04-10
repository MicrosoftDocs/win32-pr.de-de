---
title: StateChange (sessionstatechangetriggertype)-Element
description: Enthält die Art der Sitzungs Änderung für Terminal Server, die einen Task Start auslöst.
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
ms.openlocfilehash: 3991a767256184f23fbb9defda7e33465c0477e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106347"
---
# <a name="statechange-sessionstatechangetriggertype-element"></a>StateChange (sessionstatechangetriggertype)-Element

Enthält die Art der Sitzungs Änderung für Terminal Server, die einen Task Start auslöst.

``` syntax
<xs:element name="StateChange"
    type="sessionStateChangeType"
 />
```

Das **StateChange** -Element wird durch den komplexen Typ [**sessionstatechangetriggertype**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                       | Abgeleitet von                                                                                           | BESCHREIBUNG                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **Sessionstatechange-Auslösers** | [**sessionstatechangetriggertype**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Gibt einen-Endpunkt an, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**StateChange-Eigenschaft von isessionstatechangelöst**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_statechange).

Informationen zur Skript Entwicklung finden Sie unter [**sessionstatechange-Ereignis. StateChange**](sessionstatechangetrigger-statechange.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





