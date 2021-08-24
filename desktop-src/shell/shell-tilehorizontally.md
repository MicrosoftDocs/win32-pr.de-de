---
description: Kacheln aller Fenster auf dem Desktop horizontal. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von Windows Horizontal.
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: Shell.TileHorizontally-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da11496ca9993c87f78a9209a2c6d04bc0167349a6c0b955a3b2823335f30464
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709480"
---
# <a name="shelltilehorizontally-method"></a>Shell.TileHorizontally-Methode

Kacheln aller Fenster auf dem Desktop horizontal. Diese Methode hat die gleiche Wirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von **Windows horizontal**.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **TileHorizontally** verwendet. Die richtige Verwendung wird für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

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



 

 




