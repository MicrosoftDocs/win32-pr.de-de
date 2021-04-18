---
title: Logontype (principaltype)-Element
description: Gibt die Anmelde Methode für die Sicherheit an, die zum Ausführen der dem Prinzipal zugeordneten Tasks erforderlich ist.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Logontype-Element Taskplaner
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341368"
---
# <a name="logontype-principaltype-element"></a>Logontype (principaltype)-Element

Gibt die Anmelde Methode für die Sicherheit an, die zum Ausführen der dem Prinzipal zugeordneten Tasks erforderlich ist.

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

Das **logontype** -Element wird durch den komplexen Typ [**principaltype**](taskschedulerschema-principaltype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                           | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Bemerkungen

Das **logontype** -Element und das [**UserID**](taskschedulerschema-userid-principaltype-element.md) -Element werden verwendet, um den Benutzer zu definieren, der zum Ausführen dieser Aufgaben erforderlich ist, die diesen Prinzipal verwenden.

Bei der Skripterstellung wird der Anmeldetyp für den Prinzipal durch die Eigenschaft [**Principal. logontype**](principal-logontype.md) angegeben.

Bei der C++-Entwicklung wird der Anmeldetyp für den Prinzipal durch die [**IPrincipal:: logontype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) -Eigenschaft angegeben.

Dieses Element (definiert durch den einfachen Typ " [**logontype**](taskschedulerschema-logontype-simpletype.md) ") muss einen der folgenden Werte aufweisen.

-   S4U: der Benutzer muss sich mithilfe eines Diensts für die Benutzeranmeldung (S4U) anmelden. Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es ist kein Zugriff auf das Netzwerk oder verschlüsselte Dateien vorhanden.
-   Kennwort: der Benutzer muss sich mit einem Kennwort anmelden.
-   Interactivetoken: der Benutzer muss bereits angemeldet sein. Der Task wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.

Für einen Task, der eine MessageBox-Aktion enthält, wird das Meldungs Feld angezeigt, wenn die Aufgabe aktiviert ist und der Task einen interaktiven Anmeldetyp aufweist. Um den Aufgaben Anmeldetyp auf interaktiv festzulegen, geben Sie **interactivetoken** im- **<LogonType>** Element des Aufgaben Prinzipals an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





