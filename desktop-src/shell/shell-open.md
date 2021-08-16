---
description: 'Shell.Open-Methode: Öffnet den angegebenen Ordner.'
ms.assetid: 96ed9360-fb8f-4f7e-aefb-4a63ec95df07
title: Shell.Open-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3a4e8119955f46a5547873019d75209903dbf1efc9a40ed427c501ffee1cbf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968519"
---
# <a name="shellopen-method"></a>Shell.Open-Methode

Öffnet den angegebenen Ordner.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = Shell.Open(
  vDir
)
```


```VB

Shell.Open( _
  ByVal vDir As Variant _
) As Integer
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*vDir* \[ In\]
</dt> <dd>

Typ: **Variant**

Eine Zeichenfolge, die den Pfad des Ordners oder einen der [**ShellSpecialFolderConstants-Werte**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) angibt. Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind. In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.

Wenn *vDir* auf einen der [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) festgelegt ist und der spezielle Ordner nicht vorhanden ist, erstellt diese Funktion den Ordner.

</dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt **Open** in use . Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objShell.Shell.Open(ssfWINDOWS);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Shell.Open("C:\\")

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Shell**](shell.md)
</dt> <dt>

[**Erkunden**](shell-explore.md)
</dt> </dl>

 

 




