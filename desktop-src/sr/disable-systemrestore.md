---
title: Disable-Methode der SystemRestore-Klasse
description: Deaktiviert die Überwachung auf einem bestimmten Laufwerk.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Deaktivieren der Methode "Systemwiederherstellung"
- Disable method System Restore , SystemRestore class
- SystemRestore-Klasse Systemwiederherstellung , Disable-Methode
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
ms.openlocfilehash: 41a05d53ee13e2f06c2f4765d2947f49a417ed798965406185619dfce207cf76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452921"
---
# <a name="disable-method-of-the-systemrestore-class"></a>Disable-Methode der SystemRestore-Klasse

Deaktiviert die Überwachung auf einem bestimmten Laufwerk.

## <a name="syntax"></a>Syntax


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Laufwerk* \[ In\]
</dt> <dd>

Das zu deaktivierende Laufwerk. Die Laufwerkszeichenfolge sollte das Format "C: \\ " haben. Wenn dieser Parameter das Systemlaufwerk oder eine leere Zeichenfolge ("") ist, werden keine Laufwerke überwacht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Andernfalls gibt die -Methode einen der in WinError.h definierten COM-Fehlercodes zurück.

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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                         |
| Namespace<br/>                | \\Stammstandard<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





