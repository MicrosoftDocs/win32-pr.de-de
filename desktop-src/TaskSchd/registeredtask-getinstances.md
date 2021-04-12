---
title: Registeredtask. getinhaltungen-Methode
description: Gibt für die Skripterstellung alle zurzeit auf dem registrierten Task aktuell laufenden Instanzen zurück.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Die getinhaltungen-Methode Taskplaner
- Getinhaltungen-Methode Taskplaner, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, getinhaltungen-Methode
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105243"
---
# <a name="registeredtaskgetinstances-method"></a>Registeredtask. getinhaltungen-Methode

Gibt für die Skripterstellung alle zurzeit auf dem registrierten Task aktuell laufenden Instanzen zurück.

> [!Note]  
> **Registeredtask. getinhaltungen** gibt nur Instanzen der aktuell registrierten Aufgabe zurück, die unter oder unterhalb des Sicherheits Kontexts eines Benutzers ausgeführt werden. Bei Mitgliedern der Gruppe "Administratoren" gibt " **getinhaltungen** " z. b. alle Instanzen der aktuell registrierten Aufgabe zurück. für Mitglieder der Gruppe "Benutzer" gibt " **getinhaltungen** " jedoch nur Instanzen der aktuell registrierten Aufgabe zurück, die im Sicherheitskontext der Benutzergruppe ausgeführt werden.

 

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*flags* 
</dt> <dd>

Dieser Parameter ist für die zukünftige Verwendung reserviert und muss auf 0 (null) festgelegt werden.

</dd> <dt>

*runningtasks* \[ vorgenommen\]
</dt> <dd>

Ein [**runningtaskcollection**](runningtaskcollection.md) -Objekt, das alle derzeit aktuell aktuell laufenden Instanzen der Aufgabe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

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
</dt> <dt>

[**Registeredtask**](registeredtask.md)
</dt> </dl>

 

 





