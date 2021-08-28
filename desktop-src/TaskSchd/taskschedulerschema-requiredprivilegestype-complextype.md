---
title: requiredPrivilegesType Complex Type
description: Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das RequiredPrivileges (requiredPrivilegesType)-Element.
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- komplexer requiredPrivilegesType-Taskplaner
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d79b75a4d4bb44aded7367fd4acfd758887815bba6fc6fcfd965f9123ac58c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658790"
---
# <a name="requiredprivilegestype-complex-type"></a>requiredPrivilegesType Complex Type

Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das [**RequiredPrivileges (requiredPrivilegesType)-Element.**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md)

``` syntax
<xs:complexType name="requiredPrivilegesType">
    <xs:all>
        <xs:element name="Privilege"
            type="privilegeType"
            minOccurs="1"
            maxOccurs="64"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                           | Typ                                                                  | Beschreibung                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [**Berechtigung**](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [**privilegeType**](taskschedulerschema-privilegetype-simpletype.md) | Gibt die erforderlichen Berechtigungen für den Task an. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Komplexe Schematypen](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





