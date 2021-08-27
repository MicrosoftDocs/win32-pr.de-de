---
title: LogonType(principalType)-Element
description: Gibt die Sicherheitsanmeldungsmethode an, die zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- LogonType-Element Taskplaner
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cbe8add61dc25c472ab25087988b300346697eb901cf2a69d7506402db86a31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125800"
---
# <a name="logontype-principaltype-element"></a>LogonType(principalType)-Element

Gibt die Sicherheitsanmeldungsmethode an, die zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

Das **LogonType-Element** wird durch den komplexen [**principalType-Typ**](taskschedulerschema-principaltype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                           | Beschreibung                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheitsanmeldeinformationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Hinweise

Das **LogonType-Element** und das [**UserId-Element**](taskschedulerschema-userid-principaltype-element.md) werden zusammen verwendet, um den Benutzer zu definieren, der zum Ausführen dieser Aufgaben erforderlich ist, die diesen Prinzipal verwenden.

Für die Skriptentwicklung wird der Anmeldetyp für den Prinzipal durch die [**Principal.LogonType-Eigenschaft**](principal-logontype.md) angegeben.

Für die C++-Entwicklung wird der Anmeldetyp für den Prinzipal durch die [**IPrincipal::LogonType-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) angegeben.

Dieses Element (definiert durch den einfachen [**LogonType-Typ)**](taskschedulerschema-logontype-simpletype.md) muss einen der folgenden Werte aufweisen.

-   S4U: Der Benutzer muss sich mithilfe eines Diensts für die Benutzeranmeldung (S4U) anmelden. Wenn eine S4U-Anmeldung verwendet wird, wird vom System kein Kennwort gespeichert, und es besteht kein Zugriff auf das Netzwerk oder verschlüsselte Dateien.
-   Kennwort: Der Benutzer muss sich mit einem Kennwort anmelden.
-   InteractiveToken: Der Benutzer muss bereits angemeldet sein. Die Aufgabe wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.

Für eine Aufgabe, die eine Meldungsfeldaktion enthält, wird das Meldungsfeld angezeigt, wenn der Task aktiviert ist und der Task einen interaktiven Anmeldetyp auf hat. Um den Anmeldetyp der Aufgabe auf interaktiv festzulegen, geben Sie **InteractiveToken** im **<LogonType>** -Element des Aufgabenprinzipals an.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





