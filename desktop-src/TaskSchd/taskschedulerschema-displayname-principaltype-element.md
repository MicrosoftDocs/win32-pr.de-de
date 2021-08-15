---
title: DisplayName-Element (principalType)
description: Gibt den Namen des Prinzipals an, der auf der benutzeroberfläche Taskplaner wird.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- DisplayName-Element Taskplaner
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ff653a2b2991622b2446bcc0fc74d7063319c2bb6b45556313034a3afb42480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356913"
---
# <a name="displayname-principaltype-element"></a>DisplayName-Element (principalType)

Gibt den Namen des Prinzipals an, der auf der benutzeroberfläche Taskplaner wird.

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

Das **DisplayName-Element** wird durch den komplexen [**principalType-Typ**](taskschedulerschema-principaltype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                           | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheitsanmeldeinformationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird der Anzeigename des Prinzipals mithilfe der [**Principal.DisplayName-Eigenschaft**](principal-displayname.md) angegeben.

Für die C++-Entwicklung wird der Anzeigename des Prinzipals mithilfe der [**IPrincipal::D isplayName-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen mithilfe eines Gruppenbezeichners und eines Anzeigenamens.


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



Der folgende XML-Code definiert einen Prinzipal unter Verwendung eines Benutzerbezeichners und eines Anzeigenamens.


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





