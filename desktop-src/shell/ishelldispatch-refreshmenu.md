---
description: Erfahren Sie mehr über die IShellDispatch.RefreshMenu-Methode, die den Inhalt der Startmenü aktualisiert. Wird nur mit Systemen vor Windows XP verwendet.
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
ms.openlocfilehash: d9e1a3c326cfa79c7b754cc8a364e649cf2c9931
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404673"
---
# <a name="ishelldispatchrefreshmenu-method"></a>IShellDispatch.RefreshMenu-Methode

Aktualisiert den Inhalt  des Startmenüs. Wird nur mit Systemen vor Windows XP verwendet.

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

Diese Methode wird implementiert und über die [**Shell.TrayProperties-Methode**](shell-trayproperties.md) aufgerufen.

Die funktionen, die **RefreshMenu** bereitstellt, werden automatisch unter Windows XP oder höher verarbeitet. Rufen Sie diese Methode nicht unter Windows XP oder höher auf.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **RefreshMenu** in JScript, VBScript und Visual Basic.

Jscript:


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




