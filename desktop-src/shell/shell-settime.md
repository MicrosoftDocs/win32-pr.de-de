---
description: Zeigt das Dialogfeld Datums- und Uhrzeiteigenschaften an. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Uhr im Taskleistenstatusbereich und das Auswählen von Datum/Uhrzeit anpassen.
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: Shell.SetTime-Methode (Shldisp.h)
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
ms.openlocfilehash: cff10e89cfdc8ba038be2b619264c02b1c7b168d4ecb35cd625683f648121be6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452840"
---
# <a name="shellsettime-method"></a>Shell.SetTime-Methode

Zeigt das Dialogfeld **Datums- und Uhrzeiteigenschaften** an. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Uhr im Taskleistenstatusbereich und das Auswählen **von Datum/Uhrzeit anpassen.**

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

Im folgenden Beispiel **wird SetTime** verwendet. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



Vbscript:


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




