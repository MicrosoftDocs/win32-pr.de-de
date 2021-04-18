---
title: Getlastrestorestatus-Methode der SystemRestore-Klasse
description: Ruft den Status der letzten Systemwiederherstellung ab.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Getlastrestorestatus-Methode System Wiederherstellung
- Getlastrestorestatus-Methode System Wiederherstellung, SystemRestore-Klasse
- System Restore-Klassen System Wiederherstellung, getlastrestorestatus-Methode
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340760"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a>Getlastrestorestatus-Methode der SystemRestore-Klasse

Ruft den Status der letzten Systemwiederherstellung ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt einen der folgenden Statuswerte zurück.



| Rückgabewert                                                                 | BESCHREIBUNG                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0</dt> </dl> | Die letzte Wiederherstellung ist fehlgeschlagen.<br/>          |
| <dl> <dt>1</dt> </dl> | Die letzte Wiederherstellung war erfolgreich.<br/>  |
| <dl> <dt>2</dt> </dl> | Die letzte Wiederherstellung wurde unterbrochen.<br/> |



 

## <a name="examples"></a>Beispiele


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
End If
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                         |
| Namespace<br/>                | \\Standardwert<br/>                                                          |
| MOF<br/>                      | <dl> <dt>SR. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





