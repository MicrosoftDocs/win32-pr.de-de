---
description: Erstellt ein neues shellwindows-Objekt, das eine Kopie dieses shellwindows-Objekts ist, und gibt es zurück.
title: ShellWindows._NewEnum-Methode (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows._NewEnum
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 85e84c13-62aa-4502-b642-ca55273a800d
ms.openlocfilehash: ded5ae2c337e80359c012fb63a37aa13cc43b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218058"
---
# <a name="shellwindows_newenum-method"></a>Shellwindows. \_ Methode ' netwenum '

Erstellt ein neues [**shellwindows**](shellwindows.md) -Objekt, das eine Kopie dieses **shellwindows** -Objekts ist, und gibt es zurück.

## <a name="syntax"></a>Syntax


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Ein Objekt Verweis auf die [**shellwindows**](shellwindows.md) -Objekt Kopie.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird gezeigt, wie " **\_ netwenum** " verwendet wird. Die richtige Verwendung wird für VBScript und Visual Basic angezeigt. Diese Methode kann nicht mit JScript verwendet werden.

VBScript


```VB
<script language="VBScript">
    function fnShellWindowsNewEnumVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim objEnumItems
            
            for each objEnumItems in objShellWindows
                alert(objEnumItems.Type)
            next
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellWindowsNewEnumVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Dim vEnumItem As Variant
        
        For Each vEnumItem In objShellWindows
            Debug.Print vEnumItem.Type
        Next vEnumItem
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Exdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 
