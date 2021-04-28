---
description: Shell.FindComputer-Methode: Zeigt das Dialogfeld Suchergebnisse: Computer an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt."
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type: 
- APIRef
- kbSyntax api_name: 
- Shell.FindComputer api_type: 
- COM-api_location: 
- Shell32.dll
---

# <a name="shellfindcomputer-method"></a>Shell.FindComputer-Methode

Zeigt das Dialogfeld **Suchergebnisse: Computer** an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.

## <a name="syntax"></a>Syntax


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die Verwendung von **FindComputer.** Das Ergebnis dieses Codes entspricht dem Drücken der Schaltfläche **Start,** klicken Sie auf **Suchen**, klicken Sie auf die Option **Drucker, Computer oder Personen, und** klicken Sie dann **auf Ein Computer im Netzwerk.** Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

Jscript:


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
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
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

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



 

 




