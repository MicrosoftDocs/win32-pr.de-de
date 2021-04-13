---
title: Runlevel (runleveltype)-Element
description: Enthält einen Wert, der die Sicherheitskontext Ebene zum Ausführen des Tasks angibt.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Runlevel-Element Taskplaner
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341307"
---
# <a name="runlevel-runleveltype-element"></a>Runlevel (runleveltype)-Element

Enthält einen Wert, der die Sicherheitskontext Ebene zum Ausführen des Tasks angibt. Sie können angeben, dass eine Aufgabe mit den geringsten Rechten oder erhöhten Rechten ausgeführt werden soll. Der Wert 0 gibt an, dass der Task mit den niedrigsten Berechtigungen ausgeführt wird, und der Wert 1 gibt an, dass der Task mit erhöhten Rechten ausgeführt wird.

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

Das **Runlevel** -Element wird durch den einfachen [**runleveltype**](taskschedulerschema-runleveltype-simpletype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                  | Abgeleitet von                                                           | BESCHREIBUNG                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Prinzipal (principaltype)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Gibt die Sicherheits Anmelde Informationen für einen Prinzipal an. Mit diesen Anmelde Informationen wird der Sicherheitskontext definiert, unter dem eine Aufgabe ausgeführt wird. <br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**Runlevel-Eigenschaft von IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).

Informationen zur Skript Entwicklung finden Sie unter [**Principal. Runlevel**](principal-runlevel.md).

Wenn eine Aufgabe mit dem integrierten **\\ Administrator** Konto oder den Konten " [LocalSystem](/windows/desktop/Services/localsystem-account) " oder " [LocalService](/windows/desktop/Services/localservice-account) " registriert wird, wird die [**Runlevel**](principal-runlevel.md) -Eigenschaft ignoriert. Der Attribut Wert wird auch ignoriert, wenn die [Benutzerkontensteuerung (User Account Control](/windows/desktop/SecAuthZ/user-account-control) , UAC) ausgeschaltet ist.

Wenn eine Aufgabe mithilfe der Gruppe " **Administratoren** " für den Sicherheitskontext der Aufgabe registriert wird, müssen Sie die [**Runlevel**](principal-runlevel.md) -Eigenschaft auch auf "highestAvailable" festlegen, um die Aufgabe auszuführen. Weitere Informationen finden Sie unter [Sicherheits Kontexte für Aufgaben](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

