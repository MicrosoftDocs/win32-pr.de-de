---
title: Requirements dprivileges (Requirements-privilegestype)-Element
description: Gibt die Berechtigungen an, die für die Aufgabe erforderlich sind.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Requirements dprivileges-Element Taskplaner
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106353"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a>Requirements dprivileges (Requirements-privilegestype)-Element

Gibt die Berechtigungen an, die für die Aufgabe erforderlich sind.

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

Das Element "Requirements **dprivileges** " wird durch den komplexen Typ "Requirements [**dprivilegestype**](taskschedulerschema-requiredprivilegestype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                           | BESCHREIBUNG                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal (principaltype)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**IPrincipal2:: Requirements dprivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) -Eigenschaft.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert die Verwendung eines Gruppen Bezeichners und der erforderlichen Berechtigungen.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





