---
title: Taskfolder. getsecuritydescriptor (Eigenschaft)
description: Bei der Skripterstellung wird die Sicherheits Beschreibung für den Ordner abgerufen.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Getsecuritydescriptor-Eigenschaft Taskplaner
- Getsecuritydescriptor-Eigenschaft Taskplaner, Task Folder-Objekt
- Task Folder-Objekt Taskplaner, getsecuritydescriptor-Eigenschaft
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346744"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a>Taskfolder. getsecuritydescriptor (Eigenschaft)

Bei der Skripterstellung wird die Sicherheits Beschreibung für den Ordner abgerufen.

## <a name="syntax"></a>Syntax


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Taskfolder. SETSECURITYDESCRIPTOR**](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[**Registeredtask. SETSECURITYDESCRIPTOR**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





