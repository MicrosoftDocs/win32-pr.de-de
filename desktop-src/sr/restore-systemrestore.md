---
title: Restore-Methode der SystemRestore-Klasse
description: Initiiert eine Systemwiederherstellung.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Restore Method System Restore
- Restore Method System Restore, SystemRestore-Klasse
- SystemRestore-Klassen System Wiederherstellung, Restore-Methode
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740312"
---
# <a name="restore-method-of-the-systemrestore-class"></a>Restore-Methode der SystemRestore-Klasse

Initiiert eine Systemwiederherstellung. Der Aufrufer muss einen Systemneustart erzwingen. Die tatsächliche Wiederherstellung erfolgt während des Neustarts.

## <a name="syntax"></a>Syntax


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Sequencennummer* \[ in\]
</dt> <dd>

Die Sequenznummer des Wiederherstellungs Punkts. Um die Sequenznummer für einen bestimmten Wiederherstellungspunkt zu ermitteln, zählen Sie alle Wiederherstellungspunkte im System auf.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Andernfalls gibt die Methode einen der com-Fehlercodes zurück, die in WinError. h definiert sind.

## <a name="examples"></a>Beispiele


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                         |
| Namespace<br/>                | \\ \\ Standardwert<br/>                                                        |
| MOF<br/>                      | <dl> <dt>SR. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





