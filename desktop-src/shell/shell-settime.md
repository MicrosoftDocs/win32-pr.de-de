---
description: Zeigt das Dialogfeld Datums-und Uhrzeit Eigenschaften an. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von Datum/Uhrzeit anpassen.
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: Shell. setTime-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b610effe87bd9e4ab33a6e8396e90f79e7bbbe9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979761"
---
# <a name="shellsettime-method"></a>Shell. setTime-Methode

Zeigt das Dialogfeld **Datums-und Uhrzeit Eigenschaften** an. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von **Datum/Uhrzeit anpassen**.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung von **setTime** veranschaulicht. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
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



 

 




