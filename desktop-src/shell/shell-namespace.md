---
description: 'Shell.NameSpace-Methode: Erstellt ein Folder-Objekt für den angegebenen Ordner und gibt es zurück.'
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Shell.NameSpace-Methode (Shldisp.h)
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
ms.openlocfilehash: 41542f133961104180257b9c15b1843f3458bf6d9d2dd156fa3d97ea7b9ca87d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857739"
---
# <a name="shellnamespace-method"></a>Shell.NameSpace-Methode

Erstellt ein [**Folder-Objekt**](folder.md) für den angegebenen Ordner und gibt es zurück.

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

*vDir* \[ In\]
</dt> <dd>

Typ: **Variant**

Der Ordner, für den das [**Folder-Objekt**](folder.md) erstellt werden soll. Dies kann eine Zeichenfolge sein, die den Pfad des Ordners oder einen der [**ShellSpecialFolderConstants-Werte**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) angibt. Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind. In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **[ **Ordner**](folder.md)\*\***

Objektverweis auf das [**Folder-Objekt**](folder.md) für den angegebenen Ordner. Wenn der Ordner nicht erfolgreich erstellt wurde, gibt dieser Wert **NULL zurück.**

### <a name="vb"></a>VB

Typ: **[ **Ordner**](folder.md)\*\***

Objektverweis auf das [**Folder-Objekt**](folder.md) für den angegebenen Ordner. Wenn der Ordner nicht erfolgreich erstellt wurde, gibt dieser Wert **NULL zurück.**

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **NameSpace** verwendet. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript:


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



Vbscript:


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




