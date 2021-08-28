---
description: Enthält das FolderItem-Objekt des Ordners.
ms.assetid: 0964505d-4138-4444-91d4-46c707c45688
title: Folder2.Self-Eigenschaft (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Self
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a3f363300ae38817d39a9a6fb253f8d4a7bf34f4357b47e7e961b5cee5d5bb12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093096"
---
# <a name="folder2self-property"></a>Folder2.Self (Eigenschaft)

Enthält das [**FolderItem-Objekt des**](folderitem.md) Ordners.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
Self = Folder2.Self
```



## <a name="property-value"></a>Eigenschaftswert

Das Objekt, das als [**FolderItem-Objekt des Ordners ausgewertet**](folderitem.md) wird.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **Self verwendet,** um [**folderItem für**](folderitem.md) den Ordner C: Windows \\ abzurufen. Die richtige Verwendung wird für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolder2ObjectSelfJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolder2ObjectSelfVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder2.Self

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnFolder2Self_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder2.Self()

        If (Not objFolderItem Is Nothing) Then
            'Add code here.
        End If

        Set objFolderItem = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ordner2**](folder2-object.md)
</dt> <dt>

[**Ordner**](folder.md)
</dt> </dl>

 

 




