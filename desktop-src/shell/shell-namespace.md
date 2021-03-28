---
description: Erstellt ein Ordner Objekt für den angegebenen Ordner und gibt dieses zurück.
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Shell. Namespace-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 856a86efb4aca6ae7c1d4c8a3a81b5bc722a3963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216065"
---
# <a name="shellnamespace-method"></a>Shell. Namespace-Methode

Erstellt ein [**Ordner**](folder.md) Objekt für den angegebenen Ordner und gibt dieses zurück.

## <a name="syntax"></a>Syntax


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*vdir* \[ in\]
</dt> <dd>

Typ: **Variant**

Der Ordner, für den das [**Ordner**](folder.md) Objekt erstellt werden soll. Dabei kann es sich um eine Zeichenfolge handeln, die den Pfad des Ordners oder einen der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Werte angibt. Beachten Sie, dass die in **shellspecialfolderconstants** gefundenen Konstanten Namen in Visual Basic verfügbar sind, jedoch nicht in VBScript oder JScript. In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **[ **Ordner**](folder.md)\*\***

Objekt Verweis auf das [**Ordner**](folder.md) Objekt für den angegebenen Ordner. Wenn der Ordner nicht erfolgreich erstellt wurde, gibt dieser Wert **null** zurück.

### <a name="vb"></a>VB

Typ: **[ **Ordner**](folder.md)\*\***

Objekt Verweis auf das [**Ordner**](folder.md) Objekt für den angegebenen Ordner. Wenn der Ordner nicht erfolgreich erstellt wurde, gibt dieser Wert **null** zurück.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie **Namespace** verwendet wird. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
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



 

 




