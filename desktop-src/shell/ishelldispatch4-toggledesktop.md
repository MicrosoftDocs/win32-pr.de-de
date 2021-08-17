---
description: 'IShellDispatch4.ToggleDesktop-Methode: Zeigt den Desktop an oder blendet diesen aus.'
title: IShellDispatch4.ToggleDesktop-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 60199e18-b8da-48a6-b316-e7f07ff44b78
ms.openlocfilehash: d1cecab0450b1ce16ad2a4301801ea14aea284ac8fe7d5c1e63b5d8a211f22c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720774"
---
# <a name="ishelldispatch4toggledesktop-method"></a>IShellDispatch4.ToggleDesktop-Methode

Zeigt den Desktop an oder blendet den Desktop aus.

## <a name="syntax"></a>Syntax


```JScript
IShellDispatch4.ToggleDesktop()
```


```VB

IShellDispatch4.ToggleDesktop()
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode hat die gleiche Auswirkung wie die Schaltfläche **Desktop anzeigen** auf der Taskleiste. Sie blendet entweder alle geöffneten Fenster aus, um den Desktop anzuzeigen, oder sie blendet den Desktop aus, indem alle geöffneten Fenster angezeigt werden. Die **ToggleDesktop-Methode** zeigt keine Benutzeroberfläche an, sie ruft lediglich die Umschaltaktion auf.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die ordnungsgemäße Verwendung von **ToggleDesktop** für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6.0 oder höher)</dt> </dl> |



 

 




