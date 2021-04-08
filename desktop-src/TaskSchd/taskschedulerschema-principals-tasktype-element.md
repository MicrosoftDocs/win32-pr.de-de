---
title: Principals (TaskType)-Element
description: Gibt die Sicherheits Kontexte an, die verwendet werden können, um den Task auszuführen.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Principals-Element Taskplaner
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949516"
---
# <a name="principals-tasktype-element"></a>Principals (TaskType)-Element

Gibt die Sicherheits Kontexte an, die verwendet werden können, um den Task auszuführen.

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

Das **Principals** -Element wird durch den komplexen [**TaskType**](taskschedulerschema-tasktype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                          | Abgeleitet von                                                 | BESCHREIBUNG                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Aufgabe**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                  | type                                                                   | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Bemerkungen

Sie können bis zu 32 Prinzipale für eine Aufgabe angeben.

Bei der Skripterstellung werden die Prinzipale einer Aufgabe mithilfe der [**Taskdefinition. Principal**](taskdefinition-principal.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung werden die Prinzipale einer Aufgabe mithilfe der [**Principal-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal)angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert zwei Prinzipale: eine Benutzer-ID und einen gruppenbezeichnerprinzipal für die Aufgabe.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
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

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





