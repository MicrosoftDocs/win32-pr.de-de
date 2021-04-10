---
title: Registeredtask. getsecuritydescriptor-Methode
description: Ruft bei der Skripterstellung die Sicherheits Beschreibung ab, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- Getsecuritydescriptor-Methode Taskplaner
- Getsecuritydescriptor-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, getsecuritydescriptor-Methode
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
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956928"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a>Registeredtask. getsecuritydescriptor-Methode

Ruft bei der Skripterstellung die Sicherheits Beschreibung ab, die als Anmelde Informationen für die registrierte Aufgabe verwendet wird.

## <a name="syntax"></a>Syntax


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*securityinformation* 
</dt> <dd>

Die Sicherheitsinformationen aus [**Sicherheits \_ Informationen**](/windows/desktop/SecAuthZ/security-information).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Sicherheits Beschreibung für den registrierten Task.

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

 

