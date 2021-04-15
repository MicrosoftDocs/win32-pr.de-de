---
title: Berechtigungs Element ("Requirements dprivilegestype")
description: Gibt das Recht einer Aufgabe an, verschiedene systembezogene Vorgänge auszuführen, z. b. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Berechtigungs Element Taskplaner
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478387"
---
# <a name="privilege-requiredprivilegestype-element"></a>Berechtigungs Element ("Requirements dprivilegestype")

Gibt das Recht einer Aufgabe an, verschiedene systembezogene Vorgänge auszuführen, z. b. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

Das **Privileg** -Element wird durch den komplexen Typ "Requirements [**dprivilegestype**](taskschedulerschema-requiredprivilegestype-complextype.md) " definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                             | Abgeleitet von                                                                             | BESCHREIBUNG                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Requirements-Privilegien**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**Requirements dprivilegestype**](taskschedulerschema-requiredprivilegestype-complextype.md) | Enthält die Einstellungen, die der Taskplaner verwendet, um die Aufgabe auszuführen.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der C++-Entwicklung erfolgt der Zugriff auf diese Informationen über die [**IPrincipal2:: Requirements dprivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) -Eigenschaft.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein settings-Element, das das Recht eines Tasks angibt, verschiedene systembezogene Vorgänge auszuführen, z. b. das Herunterfahren des Systems, das Laden von Gerätetreibern oder das Ändern der Systemzeit.


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

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





