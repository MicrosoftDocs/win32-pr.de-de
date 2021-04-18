---
title: Principal (principaltype)-Element
description: Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.
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
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340312"
---
# <a name="principal-principaltype-element"></a>Principal (principaltype)-Element

Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an. Mit diesen Anmelde Informationen wird der Sicherheitskontext definiert, unter dem eine Aufgabe ausgeführt wird.

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

Das **Principal** -Element wird durch den komplexen [**principaltype**](taskschedulerschema-principaltype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                               | Abgeleitet von                                                             | BESCHREIBUNG                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Principals**](taskschedulerschema-principals-tasktype-element.md) | [**principalstype**](taskschedulerschema-principalstype-complextype.md) | Gibt die dem Task zugeordneten Sicherheits Prinzipale an.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                      | type                                                          | BESCHREIBUNG                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) | **string**                                                    | Gibt den Namen des Prinzipals an, der in der Taskplaner-Benutzeroberfläche angezeigt wird.<br/>                 |
| [**GroupID**](taskschedulerschema-groupid-principaltype-element.md)         | **string**                                                    | Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen der dem Prinzipal zugeordneten Tasks erforderlich ist.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)     | [**logonType**](taskschedulerschema-logontype-simpletype.md) | Gibt die Anmelde Methode für die Sicherheit an, die zum Ausführen der dem Prinzipal zugeordneten Tasks erforderlich ist.<br/>  |
| [**UserID**](taskschedulerschema-userid-principaltype-element.md)           | **string**                                                    | Gibt die Benutzer-ID an, die erforderlich ist, um dem Prinzipal zugeordnete Tasks auszuführen<br/>              |



## <a name="attributes"></a>Attributes



| Name | type | BESCHREIBUNG                                        |
|------|------|----------------------------------------------------|
| Id   | id   | Der Bezeichner der Prinzipal Definition.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung werden die Sicherheits Anmelde Informationen für einen Prinzipal mithilfe des [**Prinzipal**](principal.md) Objekts angegeben.

Bei der C++-Entwicklung werden die Sicherheits Anmelde Informationen für einen Prinzipal mithilfe der [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) -Schnittstelle angegeben.

Die oben aufgeführten untergeordneten Elemente werden durch den komplexen Typ " [**principaltype**](taskschedulerschema-principaltype-complextype.md) " definiert. Informationen zur Sequenzierung für diese untergeordneten Elemente finden Sie unter [**principaltype**](taskschedulerschema-principaltype-complextype.md).

## <a name="examples"></a>Beispiele

Im folgenden XML-Code wird ein Prinzipal mit einer Benutzer-ID definiert.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



Der folgende XML-Code definiert einen Prinzipal mit einem Gruppen Bezeichner.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





