---
description: 'IShellDispatch.EjectPC-Methode: Wirft den Computer aus seiner Andockstation aus. Dies entspricht dem Klicken auf das Startmenü und dem Auswählen von Eject PC, wenn Ihr Computer diesen Befehl unterstützt.'
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: IShellDispatch.EjectPC-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e812365f50c0166c824afd7fb0b1dac7a82cbe11961f45e1fd89283692816232
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884390"
---
# <a name="ishelldispatchejectpc-method"></a>IShellDispatch.EjectPC-Methode

Wirft den Computer aus seiner Andockstation. Dies entspricht dem Klicken auf das **Startmenü** und dem Auswählen von **Eject PC**, wenn Ihr Computer diesen Befehl unterstützt.

## <a name="syntax"></a>Syntax


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird implementiert und über die [**Shell.EjectPC-Methode aufgerufen.**](shell-ejectpc.md)

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **EjectPC** in JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




