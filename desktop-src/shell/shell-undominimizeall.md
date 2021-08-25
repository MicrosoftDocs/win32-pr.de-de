---
description: Stellt alle Desktopfenster in dem Zustand wieder her, in dem sie sich vor dem letzten MinimizeAll-Befehl befanden.
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: Shell.UndoMinimizeALL-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5e2342bda1059e2bcb00893afb182e415840a4e650392fc3e1d3df4756cb2d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941570"
---
# <a name="shellundominimizeall-method"></a>Shell.UndoMinimizeALL-Methode

Stellt alle Desktopfenster in dem Zustand wieder her, in dem sie sich vor dem letzten [**MinimizeAll-Befehl**](shell-minimizeall.md) befanden. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von **Rückgängig Minimieren aller Windows** auf älteren Systemen oder ein zweites Klicken auf das Symbol Desktop **anzeigen** im Schnellstart Bereich der Taskleiste in Windows 2000 oder Windows XP.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **UndoMinimizeALL** verwendet. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

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



 

 




