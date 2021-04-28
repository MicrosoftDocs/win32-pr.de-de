---
description: 'IShellDispatch.NameSpace-Methode: Erstellt ein Folder-Objekt für den angegebenen Ordner und gibt es zurück.'
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: IShellDispatch.NameSpace-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d1db0a3969350b4be4bc32e027bf2000036e099f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100518"
---
# <a name="ishelldispatchnamespace-method"></a>IShellDispatch.NameSpace-Methode

Erstellt ein [**Folder-Objekt für**](folder.md) den angegebenen Ordner und gibt es zurück.

## <a name="syntax"></a>Syntax


```JScript
retVal = IShellDispatch.NameSpace(
  vDir
)
```


```VB

IShellDispatch.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*vDir* \[ In\]
</dt> <dd>

Typ: **Variant**

Der Ordner, für den das Ordnerobjekt [**erstellt werden**](folder.md) soll. Dies kann eine Zeichenfolge sein, die den Pfad des Ordners oder einen der [**ShellSpecialFolderConstants-Werte angibt.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind. In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Typ: **[ **Ordner**](folder.md)\*\***

Objektverweis auf das [**Folder-Objekt**](folder.md) für den angegebenen Ordner. Wenn der Ordner nicht erfolgreich erstellt wurde, gibt dieser Wert **NULL zurück.**

### <a name="vb"></a>VB

Typ: **[ **Ordner**](folder.md)\*\***

Objektverweis auf das [**Folder-Objekt**](folder.md) für den angegebenen Ordner. Wenn der Ordner nicht erfolgreich erstellt wurde, gibt dieser Wert **NULL zurück.**

## <a name="remarks"></a>Bemerkungen

Diese Methode wird implementiert und über die [**Shell.NameSpace-Methode aufgerufen.**](shell-namespace.md)

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von [**NameSpace**](shell-namespace.md) in JScript, VBScript und Visual Basic.

Jscript:


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
        set objFolder = objShell.NameSpace("C:\")

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



| Anforderungen | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




