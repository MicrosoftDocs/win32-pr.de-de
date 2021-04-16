---
title: komplexer Typ "Requirements dprivilegestype"
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das Requirements dprivileges (Requirements dprivilegestype)-Element.
ms.assetid: ae96282a-d167-47ea-9d37-2d682f746d23
keywords:
- komplexer Typ "Requirements dprivilegestype" Taskplaner
topic_type:
- apiref
api_name:
- requiredPrivilegesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a5ce81d96858488395e34f84232ca758ddabc59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479227"
---
# <a name="requiredprivilegestype-complex-type"></a>komplexer Typ "Requirements dprivilegestype"

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das Requirements [**dprivileges (Requirements dprivilegestype)**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) -Element.

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



| Element                                                                           | type                                                                  | BESCHREIBUNG                                                |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------|
| [**Berechtigung**](taskschedulerschema-privilege-requiredprivilegestype-element.md) | [**PrivilegeType**](taskschedulerschema-privilegetype-simpletype.md) | Gibt die erforderlichen Berechtigungen für den Task an. <br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komplexe Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





