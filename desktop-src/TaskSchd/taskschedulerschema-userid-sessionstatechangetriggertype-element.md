---
title: UserID (sessionstatechangetriggertype)-Element
description: Enthält den Benutzer für die Terminal Server Sitzung. Wenn eine Sitzungs Zustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.
ms.assetid: 7605f444-b2c9-4bba-a035-f1307c01184f
keywords:
- UserID-Element Taskplaner
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd66a05d25ea9b44f124d55ccc0cbb2c628aeeb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518587"
---
# <a name="userid-sessionstatechangetriggertype-element"></a>UserID (sessionstatechangetriggertype)-Element

Enthält den Benutzer für die Terminal Server Sitzung. Wenn eine Sitzungs Zustandsänderung für diesen Benutzer erkannt wird, wird eine Aufgabe gestartet.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

Das **UserID** -Element wird durch den komplexen Typ [**sessionstatechangetriggertype**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                       | Abgeleitet von                                                                                           | BESCHREIBUNG                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| **Sessionstatechange-Auslösers** | [**sessionstatechangetriggertype**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Gibt einen-Endpunkt an, der einen Task startet, wenn sich der Status einer Terminal Server Sitzung ändert.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**UserId-Eigenschaft von isessionstatechangelöst**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_userid).

Informationen zur Skript Entwicklung finden Sie unter [**sessionstatechange-Benutzer-ID**](sessionstatechangetrigger-userid.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





