---
description: Enthält das Folder-Objekt des Elements, wenn das Element ein Ordner ist.
ms.assetid: 87afd0b6-245b-4550-9f21-aa0426ba8470
title: FolderItem.GetFolder-Eigenschaft (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.GetFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ad1f136fdc59291b36bb5d609269b97e7ab7a5f9d74eccbbedf204d4c2d4e014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458880"
---
# <a name="folderitemgetfolder-property"></a>FolderItem.GetFolder-Eigenschaft

Enthält das [**Folder-Objekt**](folder.md) des Elements, wenn das Element ein Ordner ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
objGetFolder = FolderItem.GetFolder
```



## <a name="property-value"></a>Eigenschaftswert

Eine Variable vom Typ [**IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) die das [**Folder-Objekt**](folder.md) empfängt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **GetFolder** verwendet, um das [**Folder-Objekt**](folder.md) für den Ordner System32 abzurufen. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript:


```JScript
<script language="JScript">
    function fnGetFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("system32");
            if (objFolderItem != null)
            {
                var objFolder;
                
                objFolder = objFolderItem.GetFolder;
                if (objFolder != null)
                {
                    ...
                }
            }
        }
    }
 </script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnGetFolderVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(36)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("system32")
                if (not objFolderItem is nothing) then
                    dim objFolder
                                
                    set objFolder = objFolderItem.GetFolder
                    if (not objFolder is nothing) then
                        'Add code here         
                    end if
                    set objFolder = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnGetFolderVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("system32")
                If (Not objFolderItem Is Nothing) Then
                    Dim objFolder As Folder2
                    
                    Set objFolder = objFolderItem.GetFolder
                        If (Not objFolder Is Nothing) Then
                            'Add code here
                            Debug.Print "Yes"
                        Else
                            'Folder object returned nothing
                        End If
                    Set objFolder = Nothing
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shlobj.h (include Shldisp.h)</dt> </dl>        |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FolderItem**](folderitem.md)
</dt> <dt>

[**IsFolder**](folderitem-isfolder.md)
</dt> </dl>

 

 
