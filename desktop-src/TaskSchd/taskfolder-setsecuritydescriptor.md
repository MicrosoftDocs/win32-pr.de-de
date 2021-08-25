---
title: TaskFolder.SetSecurityDescriptor (Eigenschaft)
description: Legt für die Skripterstellung den Sicherheitsdeskriptor für den Ordner fest.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Eigenschafteneigenschaft "SetSecurityDescriptor Taskplaner
- SetSecurityDescriptor-Eigenschaft Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , SetSecurityDescriptor-Eigenschaft
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
ms.openlocfilehash: 8416e14a5415de86f8ad3f4a1181ce231ecfbdc875e36e9e3fd14014de8c4935
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033790"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a>TaskFolder.SetSecurityDescriptor (Eigenschaft)

Legt für die Skripterstellung den Sicherheitsdeskriptor für den Ordner fest.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Sie können die Zugriffssteuerungsliste (Access Control List, ACL) im Sicherheitsdeskriptor für einen Taskordner angeben, um bestimmten Benutzern und Gruppen den Zugriff auf einen Aufgabenordner zu ermöglichen oder zu verweigern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**TaskFolder.GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





