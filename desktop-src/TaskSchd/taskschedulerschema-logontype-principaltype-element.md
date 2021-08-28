---
title: LogonType-Element (principalType)
description: Gibt die Sicherheitsanmeldungsmethode an, die zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- LogonType-element Taskplaner
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9121179b744857d5e7d0bec5a2ae814c603c6b1c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885842"
---
# <a name="logontype-principaltype-element"></a>LogonType-Element (principalType)

Gibt die Sicherheitsanmeldungsmethode an, die zum Ausführen der aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

Das **LogonType-Element** wird durch den komplexen [**PrincipalType-Typ**](taskschedulerschema-principaltype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                           | Beschreibung                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Prinzipal**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheitsanmeldeinformationen für einen Prinzipal an.<br/> |



## <a name="remarks"></a>Hinweise

Das **LogonType-Element** und das [**UserId-Element**](taskschedulerschema-userid-principaltype-element.md) werden zusammen verwendet, um den Benutzer zu definieren, der zum Ausführen der Aufgaben erforderlich ist, die diesen Prinzipal verwenden.

Für die Skriptentwicklung wird der Anmeldetyp für den Prinzipal von der [**Principal.LogonType-Eigenschaft**](principal-logontype.md) angegeben.

Für die C++-Entwicklung wird der Anmeldetyp für den Prinzipal von der [**IPrincipal::LogonType-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) angegeben.

Dieses Element (definiert durch den [**einfachen LogonType-Typ)**](taskschedulerschema-logontype-simpletype.md) muss einen der folgenden Werte haben.

-   S4U: Der Benutzer muss sich mit einem Dienst für die Benutzeranmeldung (S4U) anmelden. Wenn eine S4U-Anmeldung verwendet wird, wird kein Kennwort vom System gespeichert, und es besteht kein Zugriff auf das Netzwerk oder verschlüsselte Dateien.
-   Kennwort: Der Benutzer muss sich mit einem Kennwort anmelden.
-   InteractiveToken: Der Benutzer muss bereits angemeldet sein. Die Aufgabe wird nur in einer vorhandenen interaktiven Sitzung ausgeführt.

Für eine Aufgabe, die eine Meldungsfeldaktion enthält, wird das Meldungsfeld angezeigt, wenn der Task aktiviert ist und der Task über einen interaktiven Anmeldetyp verfügt. Geben Sie **InteractiveToken** im **&lt; &gt; LogonType-Element** des Aufgabenprinzipals an, um den Taskanmeldungstyp als interaktiv festzulegen.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





