---
title: Taskfolder. SETSECURITYDESCRIPTOR (Eigenschaft)
description: Bei der Skripterstellung wird die Sicherheits Beschreibung für den Ordner festgelegt.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- SETSECURITYDESCRIPTOR-Eigenschaft Taskplaner
- SETSECURITYDESCRIPTOR-Eigenschaft Taskplaner, Task Folder-Objekt
- Task Folder-Objekt Taskplaner, SETSECURITYDESCRIPTOR-Eigenschaft
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949645"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a>Taskfolder. SETSECURITYDESCRIPTOR (Eigenschaft)

Bei der Skripterstellung wird die Sicherheits Beschreibung für den Ordner festgelegt.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Sie können die Zugriffs Steuerungs Liste (ACL) in der Sicherheits Beschreibung für einen Aufgaben Ordner angeben, um bestimmten Benutzern und Gruppen den Zugriff auf einen Aufgaben Ordner zu gewähren oder zu verweigern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Registeredtask. SETSECURITYDESCRIPTOR**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**Taskfolder. getsecuritydescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





