---
title: TaskFolder.GetSecurityDescriptor-Eigenschaft
description: Ruft für die Skripterstellung den Sicherheitsdeskriptor für den Ordner ab.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- GetSecurityDescriptor-Eigenschaft Taskplaner
- GetSecurityDescriptor-Eigenschaft Taskplaner , TaskFolder-Objekt
- TaskFolder-Objekt Taskplaner , GetSecurityDescriptor-Eigenschaft
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
ms.openlocfilehash: 851565299b7e6d1c29e2e53d87fb27aa30297921cc194f3cce753fc8d22a6bc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080320"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a>TaskFolder.GetSecurityDescriptor-Eigenschaft

Ruft für die Skripterstellung den Sicherheitsdeskriptor für den Ordner ab.

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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TaskFolder.SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





