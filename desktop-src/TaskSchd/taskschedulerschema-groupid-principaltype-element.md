---
title: GroupId-Element (principaltype)
description: Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen dieser Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- GroupId-Element Taskplaner
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040871"
---
# <a name="groupid-principaltype-element"></a>GroupId-Element (principaltype)

Gibt den Bezeichner der Benutzergruppe an, die zum Ausführen dieser Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

Das **GroupID** -Element wird durch den komplexen [**principaltype**](taskschedulerschema-principaltype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                           | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Bemerkungen

Sie können nicht gleichzeitig einen Gruppen Bezeichner und eine Benutzer-ID angeben. Geben Sie entweder die Elemente [**UserID**](taskschedulerschema-userid-principaltype-element.md) oder **GroupID** an, aber nicht beides.

Bei der Skript Entwicklung wird der Gruppen Bezeichner des Prinzipals mit der [**Principal. GroupID**](principal-groupid.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird der Gruppen Bezeichner des Prinzipals mithilfe der [**IPrincipal:: GroupID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) -Eigenschaft angegeben.

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die dieses Element verwendet, finden Sie unter [Logon-auslöserbeispiel (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





