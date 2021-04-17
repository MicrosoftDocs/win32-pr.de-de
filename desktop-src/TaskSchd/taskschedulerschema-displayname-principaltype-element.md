---
title: Display Name (principaltype)-Element
description: Gibt den Namen des Prinzipals an, der in der Taskplaner-Benutzeroberfläche angezeigt wird.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- Display Name-Element Taskplaner
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519135"
---
# <a name="displayname-principaltype-element"></a>Display Name (principaltype)-Element

Gibt den Namen des Prinzipals an, der in der Taskplaner-Benutzeroberfläche angezeigt wird.

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

Das **Display Name** -Element wird durch den komplexen [**principaltype**](taskschedulerschema-principaltype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                           | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird der Anzeige Name des Prinzipals mit der [**Principal. Display Name**](principal-displayname.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird der Anzeige Name des Prinzipals mithilfe der [**IPrincipal::D isplayname**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine mithilfe eines Gruppen Bezeichners und eines anzeigen Amens.


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



Der folgende XML-Code definiert einen Prinzipal mithilfe eines Benutzer Bezeichners und eines anzeigen Amens.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





