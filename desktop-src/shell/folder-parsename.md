---
description: Erstellt ein FolderItem-Objekt, das ein angegebenes Element darstellt, und gibt es zurück.
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
title: Folder.ParseName-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParseName
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 582341c97b6373fa0c04abf69642930328a34223a7c7b0dbc7792d8c7aec4680
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093090"
---
# <a name="folderparsename-method"></a>Folder.ParseName-Methode

Erstellt ein [**FolderItem-Objekt,**](folderitem.md) das ein angegebenes Element darstellt, und gibt es zurück.

## <a name="syntax"></a>Syntax


```JScript
retVal = Folder.ParseName(
  bName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bName* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine Zeichenfolge, die den Namen des Elements angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FolderItem**](folderitem.md)\*\***

Ein Objektverweis auf das [**FolderItem-Objekt.**](folderitem.md)

## <a name="remarks"></a>Hinweise

**ParseName** sollte nicht für virtuelle Ordner wie Eigene Dokumente.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **ParseName verwendet,** um ein Objekt zu erstellen, das das Ordnerelement darstellt, Clock.avi im Ordner C: \\ Windows ist. Die richtige Verwendung wird für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
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
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
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



 

 
