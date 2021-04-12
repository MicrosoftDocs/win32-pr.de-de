---
title: komplexer principaltype-Typ
description: Definiert das Attribut, die untergeordneten Elemente und die Sequenzierungs Informationen für das Prinzipal Element.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- komplexer principaltype-Typ Taskplaner
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478168"
---
# <a name="principaltype-complex-type"></a>komplexer principaltype-Typ

Definiert das Attribut, die untergeordneten Elemente und die Sequenzierungs Informationen für das [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) Element.

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                             | type                                                                                     | BESCHREIBUNG                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md)                        | Zeichenfolge                                                                                   | Gibt den Namen des Prinzipals an, der in der Taskplaner-Benutzeroberfläche angezeigt wird.<br/>                 |
| [**GroupID**](taskschedulerschema-groupid-principaltype-element.md)                                | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)                            | [**logonType**](taskschedulerschema-logontype-simpletype.md)                            | Gibt die Sicherheits Anmelde Methode an, die zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.<br/>        |
| [**Processtokensidtype**](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [**processtokensidtype**](taskschedulerschema-processtokensidtype-simpletype.md)        | Gibt die Typen der Prozess Sicherheits-ID (SID) an, die von Tasks verwendet werden können.<br/>                              |
| [**Requirements-Privilegien**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**Requirements dprivilegestype**](taskschedulerschema-requiredprivilegestype-complextype.md) | Gibt die erforderlichen Berechtigungen zum Ausführen der Aufgabe an.<br/>                                                               |
| [**Ausführungs Ebene**](taskschedulerschema-runlevel-principaltype-element.md)                              | [**runleveltype**](taskschedulerschema-runleveltype-simpletype.md)                      | Gibt die Berechtigungsebene an, auf der die Aufgabe ausgeführt wird.<br/>                                                     |
| [**UserID**](taskschedulerschema-userid-principaltype-element.md)                                  | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | Gibt die Benutzer-ID an, die zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.<br/>              |



## <a name="attributes"></a>Attributes



| Name | type | BESCHREIBUNG                                           |
|------|------|-------------------------------------------------------|
| id   | id   | Gibt den Bezeichner des Prinzipals an.<br/> |



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

 

 





