---
description: Kachelt alle Fenster auf dem Desktop horizontal. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von gestapeltes Fenster anzeigen.
ms.assetid: 85785510-6B75-450a-A9BB-6C3B4F6194E2
title: Ishelldispatch. tilehorizontale-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 06491f797de4a9fcb5c431d85cff71fbc78d605c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130092"
---
# <a name="ishelldispatchtilehorizontally-method"></a>Ishelldispatch. tilehorizontdent-Methode

Kachelt alle Fenster auf dem Desktop horizontal. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von **Gestapeltes Fenster anzeigen**.

## <a name="syntax"></a>Syntax


```JScript
IShellDispatch.TileHorizontally()
```


```VB

IShellDispatch.TileHorizontally()
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert, und der Zugriff erfolgt über die [**Shell. tilehorizontale**](shell-tilehorizontally.md) -Methode.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Verwendung von **tilehorizontin** JScript, VBScript und Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileHorizontally();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileHorizontally

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



 

 




