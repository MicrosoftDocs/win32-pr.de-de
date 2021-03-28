---
description: Gibt an, ob das Element Teil des Dateisystems ist.
ms.assetid: 321a2109-88b5-4a41-9a67-dab3e82e95d8
title: FolderItem. IsFile-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFileSystem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 852f022e1c24fa24c158ee4eb68dca44e6f010a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977057"
---
# <a name="folderitemisfilesystem-property"></a>FolderItem. IsFile-Eigenschaft

Gibt an, ob das Element Teil des Dateisystems ist.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
bIsFileSystem = FolderItem.IsFileSystem
```



## <a name="property-value"></a>Eigenschaftswert

Ein **boolescher** Wert, der **true** empfängt, wenn das Element Teil des Dateisystems ist, andernfalls **false** .

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung von **IsFile** System verwendet, um zu bestimmen, ob der Windows-Ordner Teil des Dateisystems ist. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JScript
<script language="JScript">
    function fnIsFileSystemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsFileSystem;
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnIsFileSystemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim bReturn
                                
                    bReturn = objFolderItem.IsFileSystem
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
Private Sub fnIsFileSystemVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsFileSystem
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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 




