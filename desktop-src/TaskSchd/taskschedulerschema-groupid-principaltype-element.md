---
title: GroupId -Element (principalType)
description: Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- GroupId-Element Taskplaner
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4376e7037c228ebf2d2ffdc193cc34e7f92647220251cd82f09b0b65c7f9a81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131839"
---
# <a name="groupid-principaltype-element"></a>GroupId -Element (principalType)

Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

Das **GroupId-Element** wird durch den komplexen [**PrincipalType-Typ**](taskschedulerschema-principaltype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                           | Beschreibung                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheitsanmeldeinformationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Hinweise

Sie können nicht gleichzeitig einen Gruppenbezeichner und einen Benutzerbezeichner angeben. Geben Sie entweder [**das UserId-**](taskschedulerschema-userid-principaltype-element.md) oder **das GroupId-Element** an, aber nicht beide.

Für die Skriptentwicklung wird der Gruppenbezeichner des Prinzipals mithilfe der [**Principal.GroupId-Eigenschaft**](principal-groupid.md) angegeben.

Für die C++-Entwicklung wird der Gruppenbezeichner des Prinzipals mithilfe der [**IPrincipal::GroupId-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) angegeben.

## <a name="examples"></a>Beispiele

Ein vollständiges Beispiel für den XML-Code für eine Aufgabe, die dieses Element verwendet, finden Sie unter [Logon Trigger Example (XML) .](logon-trigger-example--xml-.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





