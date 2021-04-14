---
title: Registeredtask. stoppt-Methode
description: Bei der Skripterstellung wird die registrierte Aufgabe sofort beendet.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Taskplaner der Methode wird beendet
- Methode zum Taskplaner Ende, registeredtask-Objekt
- Registeredtask-Objekt Taskplaner, Methode "Ende"
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392176"
---
# <a name="registeredtaskstop-method"></a>Registeredtask. stoppt-Methode

Bei der Skripterstellung wird die registrierte Aufgabe sofort beendet.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ in\]
</dt> <dd>

Reserviert. Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Mit der **registeredtask. Stopp** -Funktion werden alle Instanzen der Aufgabe beendet.

System Kontobenutzer können eine Aufgabe abbrechen, Benutzer mit Administrator Gruppenberechtigungen können eine Aufgabe abbrechen, und wenn ein Benutzer über Rechte zum Ausführen und Lesen einer Aufgabe verfügt, kann der Benutzer die Aufgabe abbrechen. Ein Benutzer kann die Task Instanzen, die ausgeführt werden, mit denselben Anmelde Informationen wie das Benutzerkonto abbrechen. In allen anderen Fällen wird dem Benutzer der Zugriff verweigert, um den Task zu unterbinden.

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
</dt> </dl>

 

 





