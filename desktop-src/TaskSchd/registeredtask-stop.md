---
title: RegisteredTask.Stop-Methode
description: Bei der Skripterstellung wird die registrierte Aufgabe sofort beendet.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Beenden der Taskplaner
- Stop-Methode Taskplaner , RegisteredTask-Objekt
- RegisteredTask-Objekt Taskplaner , Stop-Methode
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
ms.openlocfilehash: 0496a3b9c8adad0ad4095b6c8aed3888940fd699750350117f4bf503c442f4c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681660"
---
# <a name="registeredtaskstop-method"></a>RegisteredTask.Stop-Methode

Bei der Skripterstellung wird die registrierte Aufgabe sofort beendet.

## <a name="syntax"></a>Syntax


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Reserviert. Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **RegisteredTask.Stop-Funktion** beendet alle Instanzen der Aufgabe.

Systemkontobenutzer können eine Aufgabe beenden, Benutzer mit Administratorgruppenberechtigungen können eine Aufgabe beenden. Wenn ein Benutzer über Rechte zum Ausführen und Lesen einer Aufgabe verfügt, kann der Benutzer die Aufgabe beenden. Ein Benutzer kann die Aufgabeninstanzen beenden, die unter denselben Anmeldeinformationen wie das Benutzerkonto ausgeführt werden. In allen anderen Fällen wird dem Benutzer der Zugriff zum Beenden der Aufgabe verweigert.

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
</dt> </dl>

 

 





