---
title: RequiredPrivileges-Element (requiredPrivilegesType)
description: Gibt die Berechtigungen an, die für den Task erforderlich sind.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- RequiredPrivileges-Element Taskplaner
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e395a61aace07dccb27eab04d9c0299115c25f16d84cd42e3d607435478f8060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611487"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a>RequiredPrivileges-Element (requiredPrivilegesType)

Gibt die Berechtigungen an, die für den Task erforderlich sind.

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

Das **RequiredPrivileges-Element** wird durch den komplexen [**requiredPrivilegesType-Typ**](taskschedulerschema-requiredprivilegestype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                           | Beschreibung                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheitsanmeldeinformationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Hinweise

Für die C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**IPrincipal2::RequiredPrivilege-Eigenschaft.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege)

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert die Verwendung eines Gruppenbezeichners und der erforderlichen Berechtigungen.


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





