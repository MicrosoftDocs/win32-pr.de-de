---
description: 'Shell.ShutdownWindows-Methode: Zeigt das Dialogfeld Windows herunterfahren an. Dies entspricht dem Klicken auf den Startmenü und dem Auswählen von Herunterfahren.'
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: Shell.ShutdownWindows-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 2a3c0746caccb360f6f7f0156b72a57ed0a2d2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083668"
---
# <a name="shellshutdownwindows-method"></a>Shell.ShutdownWindows-Methode

Zeigt das Dialogfeld **Windows herunterfahren** an. Dies entspricht dem Klicken auf das **Menü Start** und der Auswahl von **Herunterfahren.**

## <a name="syntax"></a>Syntax


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel **wird ShutdownWindows** verwendet. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

Jscript:


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



Visual Basic:


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

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



 

 




