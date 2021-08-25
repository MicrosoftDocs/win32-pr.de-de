---
title: UserId (principalType)-Element
description: Gibt den Benutzerbezeichner an, der zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
keywords:
- UserId-Element Taskplaner
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 955dcc93b826b4f86bffd3371ab9907e56dfe7f35649aee603cb18716868f535
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959530"
---
# <a name="userid-principaltype-element"></a>UserId (principalType)-Element

Gibt den Benutzerbezeichner an, der zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

Das **UserId-Element** wird durch den komplexen [**principalType-Typ**](taskschedulerschema-principaltype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                           | Beschreibung                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheitsanmeldeinformationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Hinweise

Das **UserId-Element** und das [**LogonType-Element**](taskschedulerschema-logontype-principaltype-element.md) werden zusammen verwendet, um den Benutzer zu definieren, der zum Ausführen der Aufgaben erforderlich ist, die diesen Prinzipal verwenden.

Sie können keinen Benutzerbezeichner und einen Gruppenbezeichner gleichzeitig angeben. Geben Sie entweder die **UserId** oder das [**GroupId-Element**](taskschedulerschema-groupid-principaltype-element.md) an, aber nicht beides.

Für die Skriptentwicklung wird der Benutzerbezeichner mithilfe der [**Principal.UserId-Eigenschaft**](principal-userid.md) angegeben.

Für die C++-Entwicklung wird der Benutzerbezeichner mithilfe der [**IPrincipal::UserId-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert ein Prinzip mithilfe eines Benutzerbezeichners.


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





