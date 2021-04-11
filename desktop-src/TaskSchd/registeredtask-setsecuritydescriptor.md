---
title: Registeredtask. SETSECURITYDESCRIPTOR-Methode
description: Bei der Skripterstellung wird die Sicherheits Beschreibung festgelegt, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- SETSECURITYDESCRIPTOR-Methode Taskplaner
- SETSECURITYDESCRIPTOR-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, SETSECURITYDESCRIPTOR-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105686"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a>Registeredtask. SETSECURITYDESCRIPTOR-Methode

Bei der Skripterstellung wird die Sicherheits Beschreibung festgelegt, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SDDL* \[ in\]
</dt> <dd>

Die Sicherheits Beschreibung, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.

> [!Note]  
> Wenn dem lokalen System Konto der Zugriff auf eine Aufgabe verweigert wird, kann der Taskplaner Dienst unerwartete Ergebnisse liefern.

 

</dd> <dt>

*Flags* \[ in\]
</dt> <dd>

Flags, die angeben, wie die Sicherheits Beschreibung festgelegt wird. Der Task \_ " \_ \_ Prinzipal- \_ ACE-Flag (0x10)" aus der [**\_ Taskerstellungs**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) -Enumeration kann nicht hinzugefügt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Sie können die Zugriffs Steuerungs Liste (ACL) in der Sicherheits Beschreibung für eine Aufgabe angeben, um bestimmten Benutzern und Gruppen den Zugriff auf eine Aufgabe zu gewähren oder zu verweigern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Registeredtask**](registeredtask.md)
</dt> <dt>

[**Taskfolder. getsecuritydescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**Registeredtask. SETSECURITYDESCRIPTOR**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





