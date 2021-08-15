---
description: Erfahren Sie mehr über die IShellDispatch.RefreshMenu-Methode, die den Inhalt des Startmenü. Wird nur mit Systemen vor Windows XP verwendet.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: IShellDispatch.RefreshMenu-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac5bb37f5880011fcabcfcc0e923196857694012a547b0391326a9fe5d8424f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969059"
---
# <a name="ishelldispatchrefreshmenu-method"></a>IShellDispatch.RefreshMenu-Methode

Aktualisiert den Inhalt des **Startmenüs.** Wird nur mit Systemen vor Windows XP verwendet.

## <a name="syntax"></a>Syntax


```JScript
IShellDispatch.RefreshMenu()
```


```VB

IShellDispatch.RefreshMenu()
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode wird implementiert und über die [**Shell.TrayProperties-Methode aufgerufen.**](shell-trayproperties.md)

Die funktionalität, die **RefreshMenu** bietet, wird automatisch unter xp Windows höher behandelt. Rufen Sie diese Methode nicht auf Windows XP oder höher auf.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **RefreshMenu** in JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.RefreshMenu

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



 

 




