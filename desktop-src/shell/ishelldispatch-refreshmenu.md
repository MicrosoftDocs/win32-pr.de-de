---
description: Aktualisiert den Inhalt des Start Menüs. Wird nur mit Systemen vor Windows XP verwendet.
ms.assetid: D36FA5A0-AF03-4627-86E0-869BF1440958
title: Ishelldispatch. erfrischend Menu-Methode (Shldisp. h)
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
ms.openlocfilehash: 98728ef48ffb9ef4383cf9ba567606758b7a015c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978096"
---
# <a name="ishelldispatchrefreshmenu-method"></a>Ishelldispatch. erfrischend Menu-Methode

Aktualisiert den Inhalt des **Start** Menüs. Wird nur mit Systemen vor Windows XP verwendet.

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

## <a name="remarks"></a>Bemerkungen

Diese Methode ist implementiert, und der Zugriff erfolgt über die [**Shell. trayproperties**](shell-trayproperties.md) -Methode.

Die Funktionalität, die das Aktualitäts **Menü** bereitstellt, wird automatisch unter Windows XP oder höher behandelt. Diese Methode darf nicht unter Windows XP oder höher aufgerufen werden.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung des **aktuerfrischenden Menüs** in JScript, VBScript und Visual Basic veranschaulicht.

JScript


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.RefreshMenu();
    }
</script>
```



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 




