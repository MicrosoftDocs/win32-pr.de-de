---
title: Deaktivieren der Methode der SystemRestore-Klasse
description: Deaktiviert die Überwachung auf einem bestimmten Laufwerk.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Wiederherstellung des Methoden Systems deaktivieren
- Methoden System Wiederherstellung deaktivieren, SystemRestore-Klasse
- SystemRestore-Klassen System Wiederherstellung, Methode deaktivieren
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104061"
---
# <a name="disable-method-of-the-systemrestore-class"></a>Deaktivieren der Methode der SystemRestore-Klasse

Deaktiviert die Überwachung auf einem bestimmten Laufwerk.

## <a name="syntax"></a>Syntax


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Laufwerk* \[ in\]
</dt> <dd>

Das Laufwerk, das deaktiviert werden soll. Die Laufwerks Zeichenfolge muss die Form "C: \\ " aufweisen. Wenn dieser Parameter das Systemlaufwerk oder eine leere Zeichenfolge ("") ist, werden keine Laufwerke überwacht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Andernfalls gibt die Methode einen der com-Fehlercodes zurück, die in WinError. h definiert sind.

## <a name="examples"></a>Beispiele


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
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

 

 





