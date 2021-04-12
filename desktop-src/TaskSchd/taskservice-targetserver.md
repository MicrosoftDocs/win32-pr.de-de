---
title: TaskService. TargetServer (Eigenschaft)
description: Ruft bei der Skripterstellung den Namen des Computers ab, auf dem der Taskplaner-Dienst ausgeführt wird, mit dem der Benutzer verbunden ist.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- TargetServer-Eigenschaft Taskplaner
- TargetServer-Eigenschaft Taskplaner, Task Service-Objekt
- Task Service-Objekt Taskplaner, TargetServer-Eigenschaft
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519095"
---
# <a name="taskservicetargetserver-property"></a>TaskService. TargetServer (Eigenschaft)

Ruft bei der Skripterstellung den Namen des Computers ab, auf dem der Taskplaner-Dienst ausgeführt wird, mit dem der Benutzer verbunden ist.

## <a name="syntax"></a>Syntax


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Name des Computers, auf dem der Taskplaner-Dienst ausgeführt wird, mit dem der Benutzer verbunden ist.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt eine leere Zeichenfolge zurück, wenn der Benutzer eine IP-Adresse, einen localhost oder "." als Parameter übergibt, und gibt den Namen des Computers zurück, auf dem der Taskplaner-Dienst ausgeführt wird, wenn der Benutzer keinen Parameterwert übergibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





