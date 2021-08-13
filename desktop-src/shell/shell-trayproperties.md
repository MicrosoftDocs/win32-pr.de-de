---
description: 'Shell.TrayProperties-Methode: Zeigt das Dialogfeld Eigenschaften der Taskleiste und des Startmenüs an. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von Eigenschaften.'
ms.assetid: 0d82d847-9e6f-461e-b938-fe8fd49a636f
title: Shell.TrayProperties-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TrayProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ef9ed639383b468b68f75e43f1b38b2952795ceb1990f580a766174334dadd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452826"
---
# <a name="shelltrayproperties-method"></a>Shell.TrayProperties-Methode

Zeigt das Dialogfeld **Taskleiste und Startmenüeigenschaften** an. Diese Methode hat die gleiche Auswirkung wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von **Eigenschaften.**

## <a name="syntax"></a>Syntax


```JScript
iRetVal = Shell.TrayProperties()
```


```VB

Shell.TrayProperties() As Integer
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt **TrayProperties** in Verwendung. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnShellTrayPropertiesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TrayProperties();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellTrayPropertiesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TrayProperties

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellTrayPropertiesVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TrayProperties

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



 

 




