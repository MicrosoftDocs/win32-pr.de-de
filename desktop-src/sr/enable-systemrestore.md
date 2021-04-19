---
title: Enable-Methode der SystemRestore-Klasse
description: Aktiviert die Überwachung auf einem bestimmten Laufwerk.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Aktivieren der Methoden System Wiederherstellung
- Methoden System Wiederherstellung aktivieren, SystemRestore-Klasse
- System Restore-Klassen System Wiederherstellung, Enable-Methode
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342446"
---
# <a name="enable-method-of-the-systemrestore-class"></a>Enable-Methode der SystemRestore-Klasse

Aktiviert die Überwachung auf einem bestimmten Laufwerk.

## <a name="syntax"></a>Syntax


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Laufwerk* \[ in\]
</dt> <dd>

Das zu aktivierende Laufwerk. Die Laufwerks Zeichenfolge muss die Form "C: \\ " aufweisen. Wenn es sich bei diesem Parameter um das Systemlaufwerk oder eine leere Zeichenfolge ("") handelt, werden alle Laufwerke überwacht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Andernfalls gibt die Methode einen der com-Fehlercodes zurück, die in WinError. h definiert sind.

## <a name="remarks"></a>Bemerkungen

Die **enable** -Methode wartet nicht darauf, dass die Überwachung vollständig aktiviert wird, bevor Sie zurückkehrt, da dies einige Zeit in Anspruch nehmen kann. Stattdessen wird sofort nach dem Start des System Wiederherstellungs Dienstanbieter und des Filter Treibers zurückgegeben.

Zum Aktivieren der Systemwiederherstellung auf einem nicht-System Laufwerk müssen Sie zuerst die Systemwiederherstellung auf dem Systemlaufwerk aktivieren.

Diese Methode schlägt im abgesicherten Modus fehl.

## <a name="examples"></a>Beispiele


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
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

 

 





