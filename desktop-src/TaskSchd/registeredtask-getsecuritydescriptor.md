---
title: RegisteredTask.GetSecurityDescriptor-Methode
description: Ruft für die Skripterstellung den Sicherheitsdeskriptor ab, der als Anmeldeinformationen für den registrierten Task verwendet wird.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- GetSecurityDescriptor-Taskplaner
- GetSecurityDescriptor-Methode Taskplaner , RegisteredTask-Objekt
- RegisteredTask-Taskplaner , GetSecurityDescriptor-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a832413f6d5373a07a7201341d3b412843f3c8eba3414326eeaa8316a9caedd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118859129"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a>RegisteredTask.GetSecurityDescriptor-Methode

Ruft für die Skripterstellung den Sicherheitsdeskriptor ab, der als Anmeldeinformationen für den registrierten Task verwendet wird.

## <a name="syntax"></a>Syntax


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*securityInformation* 
</dt> <dd>

Die Sicherheitsinformationen aus [**SECURITY \_ INFORMATION**](/windows/desktop/SecAuthZ/security-information).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Sicherheitsbeschreibung für den registrierten Task.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder.GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

