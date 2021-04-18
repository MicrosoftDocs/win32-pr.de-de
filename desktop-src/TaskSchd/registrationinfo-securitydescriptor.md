---
title: RegistrationInfo. securityDescriptor (Eigenschaft)
description: Ruft bei der Skripterstellung die Sicherheits Beschreibung der Aufgabe ab oder legt diese fest.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- SecurityDescriptor-Eigenschaft Taskplaner
- SecurityDescriptor-Eigenschaft Taskplaner, RegistrationInfo-Objekt
- RegistrationInfo-Objekt Taskplaner, securityDescriptor-Eigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338114"
---
# <a name="registrationinfosecuritydescriptor-property"></a>RegistrationInfo. securityDescriptor (Eigenschaft)

Ruft bei der Skripterstellung die Sicherheits Beschreibung der Aufgabe ab oder legt diese fest. Wenn bei der Task Registrierung eine andere Sicherheits Beschreibung angegeben wird, ersetzt Sie den Sicherheits Deskriptor, der durch diese Eigenschaft festgelegt wird.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Sicherheits Beschreibung, die der Aufgabe zugeordnet ist.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die Sicherheits Beschreibung der Aufgabe mit dem [**securityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) -Element des Taskplaner-Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





