---
title: RunLevel(runLevelType)-Element
description: Enthält einen -Wert, der die Sicherheitskontextebene für die Ausführung der Aufgabe angibt.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- RunLevel-Taskplaner
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 143db96de30e647c67abadc2a9fb4384ae9784604b9c679efd9de5fd2157f923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991090"
---
# <a name="runlevel-runleveltype-element"></a>RunLevel(runLevelType)-Element

Enthält einen -Wert, der die Sicherheitskontextebene für die Ausführung der Aufgabe angibt. Sie können angeben, dass eine Aufgabe mit den geringsten Rechten oder erhöhten Rechten ausgeführt werden soll. Der Wert 0 gibt an, dass die Aufgabe mit den niedrigsten Berechtigungen ausgeführt werden soll, und der Wert 1 gibt an, dass die Aufgabe mit erhöhten Rechten ausgeführt werden soll.

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

Das **RunLevel-Element** wird durch den einfachen [**RunLevelType-Typ**](taskschedulerschema-runleveltype-simpletype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                           | Beschreibung                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Principal (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheitsanmeldeinformationen für einen Prinzipal an. Diese Anmeldeinformationen definieren den Sicherheitskontext, unter dem ein Task ausgeführt wird. <br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**RunLevel-Eigenschaft von IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).

Informationen zur Skriptentwicklung finden Sie unter [**Principal.RunLevel**](principal-runlevel.md).

Wenn eine Aufgabe mithilfe des **integrierten \\ Administratorkontos** oder des [LocalSystem-](/windows/desktop/Services/localsystem-account) oder [LocalService-Kontos](/windows/desktop/Services/localservice-account) registriert wird, wird die [**RunLevel-Eigenschaft**](principal-runlevel.md) ignoriert. Der Attributwert wird auch ignoriert, wenn die Benutzerkontensteuerung (User [Account Control,](/windows/desktop/SecAuthZ/user-account-control) UAC) deaktiviert ist.

Wenn eine Aufgabe mithilfe der Gruppe Administratoren für den Sicherheitskontext der Aufgabe registriert wird, müssen Sie auch die [**RunLevel-Eigenschaft**](principal-runlevel.md) auf "HighestAvailable" festlegen, um die Aufgabe auszuführen.  Weitere Informationen finden Sie unter [Sicherheitskontexte für Tasks.](security-contexts-for-running-tasks.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

