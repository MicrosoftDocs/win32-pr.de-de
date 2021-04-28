---
description: 'Shell.Windows-Methode: Erstellt ein ShellWindows-Objekt und gibt es zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.'
title: Shell.Windows-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ffa6311c-8bbe-45c4-9b06-069779d2306d
ms.openlocfilehash: d46e27781dc569b473615926509f51ed9d089af3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104068"
---
# <a name="shellwindows-method"></a>Shell.Windows-Methode

Erstellt ein [**ShellWindows-Objekt**](shellwindows.md) und gibt es zurück. Dieses Objekt stellt eine Auflistung aller geöffneten Fenster dar, die zur Shell gehören.

## <a name="syntax"></a>Syntax


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

Ein Objektverweis auf das [**ShellWindows-Objekt.**](shellwindows.md)

### <a name="vb"></a>VB

Typ: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

Ein Objektverweis auf das [**ShellWindows-Objekt.**](shellwindows.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **Windows** verwendet, um das [**ShellWindows-Objekt**](shellwindows.md) abzurufen und die Anzahl der darin enthaltenen Elemente anzuzeigen. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

Jscript:


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objShell.Windows();

        if (objShellWindows != null)
        {
            var Shell = new ActiveXObject("WScript.Shell");
            Shell.Popup(objShellWindows.Count);
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellWindowsVBS()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objShell.Windows

        if (not objShellWindows is nothing) then
            WScript.Echo objShellWindows.Count
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objShell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
