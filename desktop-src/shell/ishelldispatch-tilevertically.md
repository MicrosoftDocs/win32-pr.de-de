---
description: Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und Fenster nebeneinander anzeigen auswählen.
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: Ishelldispatch. tilevertikal-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 42f98ae99814495029c67d41b05e86182c6b8b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978080"
---
# <a name="ishelldispatchtilevertically-method"></a>Ishelldispatch. tilevertikal-Methode

Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und **Fenster nebeneinander anzeigen** auswählen.

## <a name="syntax"></a>Syntax


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell. tilevertikal**](shell-tilevertically.md) -Methode aufgerufen.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **tilevertikal** in JScript, VBScript und Visual Basic veranschaulicht.

JScript


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

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



 

 




