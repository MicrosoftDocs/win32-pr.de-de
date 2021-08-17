---
title: RegisteredTask.SetSecurityDescriptor-Methode
description: Legt für die Skripterstellung den Sicherheitsdeskriptor fest, der als Anmeldeinformationen für den registrierten Task verwendet wird.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- SetSecurityDescriptor-Taskplaner
- SetSecurityDescriptor-Methode Taskplaner , RegisteredTask-Objekt
- RegisteredTask-Taskplaner , SetSecurityDescriptor-Methode
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
ms.openlocfilehash: c7ac6845624ab2032b9b90d742c1346081c3ba4719d0814cfd257d3787c2bf70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759591"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a>RegisteredTask.SetSecurityDescriptor-Methode

Legt für die Skripterstellung den Sicherheitsdeskriptor fest, der als Anmeldeinformationen für den registrierten Task verwendet wird.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sddl* \[ In\]
</dt> <dd>

Der Sicherheitsdeskriptor, der als Anmeldeinformationen für den registrierten Task verwendet wird.

> [!Note]  
> Wenn dem lokalen Systemkonto der Zugriff auf eine Aufgabe verweigert wird, kann Taskplaner Dienst zu unerwarteten Ergebnissen führen.

 

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Flags, die angeben, wie der Sicherheitsdeskriptor festgelegt wird. Das TASK \_ DONT \_ ADD PRINCIPAL \_ ACE-Flag (0x10) aus der TASK \_ [**\_ CREATION-Enumeration**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) kann angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Sie können die Zugriffssteuerungsliste (Access Control List, ACL) im Sicherheitsdeskriptor für eine Aufgabe angeben, um bestimmten Benutzern und Gruppen den Zugriff auf eine Aufgabe zu ermöglichen oder zu verweigern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder.GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





