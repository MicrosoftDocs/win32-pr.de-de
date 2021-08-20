---
title: Principal (principalType)-Element
description: Gibt die Sicherheitsanmeldeinformationen für einen Prinzipal an.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Principal-Element Taskplaner
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8301371acc7624b4beb9b548191afa641ed267592b246cca7ba71ff170a9bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059778"
---
# <a name="principal-principaltype-element"></a>Principal (principalType)-Element

Gibt die Sicherheitsanmeldeinformationen für einen Prinzipal an. Diese Anmeldeinformationen definieren den Sicherheitskontext, unter dem eine Aufgabe ausgeführt wird.

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

Das **Principal-Element** wird vom komplexen [**principalType-Typ**](taskschedulerschema-principaltype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                               | Abgeleitet von                                                             | Beschreibung                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Principals**](taskschedulerschema-principals-tasktype-element.md) | [**principalsType**](taskschedulerschema-principalstype-complextype.md) | Gibt die Sicherheitsprinzipale an, die dem Task zugeordnet sind.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                      | Typ                                                          | Beschreibung                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) | **string**                                                    | Gibt den Namen des Prinzipals an, der auf der Taskplaner Ui angezeigt wird.<br/>                 |
| [**Groupid**](taskschedulerschema-groupid-principaltype-element.md)         | **string**                                                    | Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)     | [**logonType**](taskschedulerschema-logontype-simpletype.md) | Gibt die Sicherheitsanmeldungsmethode an, die zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.<br/>  |
| [**Userid**](taskschedulerschema-userid-principaltype-element.md)           | **string**                                                    | Gibt den Benutzerbezeichner an, der zum Ausführen von Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.<br/>              |



## <a name="attributes"></a>Attributes



| Name | Typ | BESCHREIBUNG                                        |
|------|------|----------------------------------------------------|
| Id   | ID   | Bezeichner der Prinzipaldefinition.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung werden die Sicherheitsanmeldeinformationen für einen Prinzipal mithilfe des [**Principal-Objekts**](principal.md) angegeben.

Für die C++-Entwicklung werden die Sicherheitsanmeldeinformationen für einen Prinzipal mithilfe der [**IPrincipal-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) angegeben.

Die oben aufgeführten untergeordneten Elemente werden durch den komplexen [**principalType-Typ**](taskschedulerschema-principaltype-complextype.md) definiert. Sequenzierungsinformationen für diese untergeordneten Elemente finden Sie unter [**principalType**](taskschedulerschema-principaltype-complextype.md).

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert einen Prinzipal mit einem Benutzerbezeichner.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



Der folgende XML-Code definiert einen Prinzipal mit einem Gruppenbezeichner.


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





