---
title: PrincipalType Complex Type
description: Definiert das Attribut, die untergeordneten Elemente und die Sequenzierungsinformationen für das Principal-Element.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- Taskplaner des komplexen principalType-Typs
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6b2d7e71642ab0294f6e930eef40c5841aa5832fcc3a8d1c45aef2d7e80bbda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611912"
---
# <a name="principaltype-complex-type"></a>PrincipalType Complex Type

Definiert das Attribut, die untergeordneten Elemente und die Sequenzierungsinformationen für das [**Principal-Element.**](taskschedulerschema-principal-principaltype-element.md)

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



| Element                                                                                             | type                                                                                     | Beschreibung                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md)                        | Zeichenfolge                                                                                   | Gibt den Namen des Prinzipals an, der auf der Taskplaner Benutzeroberfläche angezeigt wird.<br/>                 |
| [**Groupid**](taskschedulerschema-groupid-principaltype-element.md)                                | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)                            | [**logonType**](taskschedulerschema-logontype-simpletype.md)                            | Gibt die Sicherheitsanmeldungsmethode an, die zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.<br/>        |
| [**ProcessTokenSidType**](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [**processTokenSidType**](taskschedulerschema-processtokensidtype-simpletype.md)        | Gibt die Typen der Prozesssicherheits-ID (SID) an, die von Tasks verwendet werden können.<br/>                              |
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Gibt die erforderlichen Berechtigungen zum Ausführen des Tasks an.<br/>                                                               |
| [**Runlevel**](taskschedulerschema-runlevel-principaltype-element.md)                              | [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md)                      | Gibt die Berechtigungsebene an, auf der der Task ausgeführt wird.<br/>                                                     |
| [**Userid**](taskschedulerschema-userid-principaltype-element.md)                                  | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | Gibt den Benutzerbezeichner an, der zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.<br/>              |



## <a name="attributes"></a>Attributes



| Name | type | BESCHREIBUNG                                           |
|------|------|-------------------------------------------------------|
| id   | ID   | Gibt den Bezeichner des Prinzipals an.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[komplexe Typen Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





