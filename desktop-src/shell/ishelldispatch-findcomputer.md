---
description: IShellDispatch.FindComputer-Methode: Zeigt das Dialogfeld Suchergebnisse: Computer an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt."
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type: 
- APIRef
- kbSyntax api_name: 
- IShellDispatch.FindComputer api_type: 
- COM-api_location: 
- Shell32.dll
---

# <a name="ishelldispatchfindcomputer-method"></a>IShellDispatch.FindComputer-Methode

Zeigt das **Dialogfeld Suchergebnisse: Computer** an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.

## <a name="syntax"></a>Syntax


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell.FindComputer-Methode**](shell-findcomputer.md) aufgerufen.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **FindComputer** in JScript, VBScript und Visual Basic.

Jscript:


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



Vbscript:


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




