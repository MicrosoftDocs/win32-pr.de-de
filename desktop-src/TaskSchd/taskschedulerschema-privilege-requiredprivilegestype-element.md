---
title: Privilege (requiredPrivilegesType)-Element
description: Gibt das Recht eines Tasks an, verschiedene systembezogene Vorgänge auszuführen, z. B. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Berechtigungselement Taskplaner
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f181c2dbe21e31c752a44a4a3b0e27abd0f9396939c9a9dcee3127f796760527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758318"
---
# <a name="privilege-requiredprivilegestype-element"></a>Privilege (requiredPrivilegesType)-Element

Gibt das Recht eines Tasks an, verschiedene systembezogene Vorgänge auszuführen, z. B. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

Das **Privilege-Element** wird durch den [**komplexen requiredPrivilegesType-Typ**](taskschedulerschema-requiredprivilegestype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                             | Abgeleitet von                                                                             | Beschreibung                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Enthält die Einstellungen, die der Taskplaner zum Ausführen der Aufgabe verwendet.<br/> |



## <a name="remarks"></a>Hinweise

Für die C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**IPrincipal2::RequiredPrivilege-Eigenschaft.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege)

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Einstellungselement, das das Recht eines Tasks angibt, verschiedene systembezogene Vorgänge auszuführen, z. B. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.


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

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





