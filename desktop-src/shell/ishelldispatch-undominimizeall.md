---
description: Stellt alle Desktop Fenster in dem Zustand wieder her, in dem Sie sich vor dem letzten minimizeall-Befehl befanden.
ms.assetid: 32BDE544-C4FF-4a64-99AF-F8960AEC4690
title: Ishelldispatch. undominimizeall-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1b11fdd7a0a82a11baa20b0f3a63a31a8a46b701
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527332"
---
# <a name="ishelldispatchundominimizeall-method"></a>Ishelldispatch. undominimizeall-Methode

Stellt alle Desktop Fenster in dem Zustand wieder her, in dem Sie sich vor dem letzten [**minimizeall**](shell-minimizeall.md) -Befehl befanden. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von " **alle Fenster minimieren** (auf älteren Systemen)" oder ein zweites klicken auf das Symbol " **Desktop anzeigen** " in der Taskleiste.

## <a name="syntax"></a>Syntax


```JScript
IShellDispatch.UndoMinimizeALL()
```


```VB

IShellDispatch.UndoMinimizeALL()
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist implementiert, und der Zugriff darauf erfolgt über die [**Shell. undominimizeall**](./shell-undominimizeall.md) -Methode.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **undominimizeall** in JScript, VBScript und Visual Basic veranschaulicht.

JScript


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.UndoMinimizeALL();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 
