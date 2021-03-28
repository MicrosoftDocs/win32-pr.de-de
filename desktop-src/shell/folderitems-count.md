---
description: Enthält die Anzahl der Elemente in der Auflistung.
ms.assetid: 383382d5-7e3f-4b27-bebf-6b79dbe677b8
title: Folderitems. Count-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 814a8248a54c5b58624a721f006bc8d4f974ba92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977041"
---
# <a name="folderitemscount-property"></a>Folderitems. Count-Eigenschaft

Enthält die Anzahl der Elemente in der Auflistung.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
iCount = FolderItems.Count
```



## <a name="property-value"></a>Eigenschaftswert

Eine **ganze** Zahl, die einen Wert für die **count** -Eigenschaft enthält.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **count** verwendet, um die Anzahl der Elemente im Windows-Ordner abzurufen. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JScript
<script language="JScript">
    function fnFolderItemsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var nCount;
                
                nCount = objFolderItems.Count;
                alert(nCount);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderItemsCountVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
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



 

 




