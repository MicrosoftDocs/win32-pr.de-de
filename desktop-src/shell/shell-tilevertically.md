---
description: Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und nebeneinander Fenster nebeneinander auswählen.
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: Shell. tilevertikal-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8ecea9df2bcbb2e410841231ed7eca170872e015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980608"
---
# <a name="shelltilevertically-method"></a>Shell. tilevertikal-Methode

Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und nebeneinander **Fenster** nebeneinander auswählen.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = Shell.TileVertically()
```


```VB

Shell.TileVertically() As Integer
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **tilevertikal** verwendet. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileVertically

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileVertically

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



 

 




