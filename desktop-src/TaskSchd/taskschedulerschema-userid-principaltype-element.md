---
title: UserID (principaltype)-Element
description: Gibt die Benutzer-ID an, die erforderlich ist, um die dem Prinzipal zugeordneten Tasks auszuführen
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
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
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392220"
---
# <a name="userid-principaltype-element"></a>UserID (principaltype)-Element

Gibt die Benutzer-ID an, die erforderlich ist, um die dem Prinzipal zugeordneten Tasks auszuführen

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

Das **UserID** -Element wird durch den komplexen [**principaltype**](taskschedulerschema-principaltype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                           | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Bemerkungen

Das **UserID** -Element und das [**logontype**](taskschedulerschema-logontype-principaltype-element.md) -Element werden verwendet, um den Benutzer zu definieren, der zum Ausführen dieser Aufgaben erforderlich ist, die diesen Prinzipal verwenden.

Sie können nicht gleichzeitig eine Benutzer-ID und einen Gruppen Bezeichner angeben. Geben Sie entweder das **UserID** -oder das [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) -Element an, aber nicht beides.

Bei der Skripterstellung wird die Benutzer-ID mithilfe der [**Principal. UserID**](principal-userid.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird der Benutzer Bezeichner mithilfe der [**IPrincipal:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Prinzip mithilfe eines Benutzer Bezeichners.


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





