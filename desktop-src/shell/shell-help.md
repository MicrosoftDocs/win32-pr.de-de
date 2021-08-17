---
description: Zeigt die Windows Hilfe- und Supportcenter an. Diese Methode hat die gleiche Auswirkung wie das Klicken auf die Startmenü und das Auswählen von Hilfe und Support.
ms.assetid: fc13fef8-dac8-4c59-936d-8da0e63e06d4
title: Shell.Help-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3bd471f4252caaf33edfd5429160b6ff8a2b0bdd901507a7f2074dff95509e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968559"
---
# <a name="shellhelp-method"></a>Shell.Help-Methode

Zeigt die Windows Hilfe- und Supportcenter an. Diese Methode hat die gleiche Auswirkung wie das Klicken auf das **Startmenü** und das Auswählen von **Hilfe und Support.**

## <a name="syntax"></a>Syntax


```JScript
Shell.Help()
```


```VB

Shell.Help()
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **Die Hilfe** wird verwendet. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Help();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Help

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Help

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



 

 




