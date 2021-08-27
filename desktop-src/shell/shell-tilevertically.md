---
description: Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von Kacheln Windows Vertikal.
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: Shell.TileVertically-Methode (Shldisp.h)
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
ms.openlocfilehash: add315a9e5656279a6a16ab5a3a9adc46ec91ab7eef3b5ec835fda242ec5b706
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090130"
---
# <a name="shelltilevertically-method"></a>Shell.TileVertically-Methode

Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat den gleichen Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von **Kachel Windows Vertikal.**

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

Im folgenden Beispiel wird **TileVertically** in Use veranschaulicht. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



Vbscript:


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




