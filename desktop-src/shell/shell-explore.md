---
description: 'Shell.Explore-Methode: Öffnet einen angegebenen Ordner in einem Windows-Explorer Fenster.'
ms.assetid: a788a3c4-f316-4fae-9294-3872eee8f46a
title: Shell.Explore-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9ec1756ad6743c5bbac36f56087e6f3820cbb624
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104328"
---
# <a name="shellexplore-method"></a>Shell.Explore-Methode

Öffnet einen angegebenen Ordner in einem Windows-Explorer Fenster.

## <a name="syntax"></a>Syntax


```JScript
Shell.Explore(
  vDir
)
```


```VB

Shell.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*vDir* \[ In\]
</dt> <dd>

Typ: **Variant**

Der anzuzeigende Ordner. Dies kann eine Zeichenfolge sein, die den Pfad des Ordners oder einen der [**ShellSpecialFolderConstants-Werte**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) angibt. Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind. In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt **Explore** in use (In Verwendung untersuchen). Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

Jscript:


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

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



 

 




