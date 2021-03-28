---
description: Enthält den Namen des Verbs.
ms.assetid: d18fddac-eb51-4031-a572-1bfef2f757a9
title: FolderItemVerb.Name-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerb.Name
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5d352f02486f1d7304d4c474aa836401bfef635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977000"
---
# <a name="folderitemverbname-property"></a>FolderItemVerb.Name-Eigenschaft

Enthält den Namen des Verbs.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
strName = FolderItemVerb.Name
```



## <a name="property-value"></a>Eigenschaftswert

Eine Variable vom Typ [**BSTR**](/previous-versions/windows/desktop/automat/bstr) , die die Name-Eigenschaft empfängt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **Name** verwendet, um den Namen des ersten Elements in der Auflistung von Verben abzurufen, auf die der Programmordner des Benutzers antwortet. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


```JScript
<script language="JScript">
    function fnFolderItemVerbNameJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objVerbs;
            
            objVerbs = objFolder.Self.Verbs();
            if (objVerbs != null)
            {
                var szReturn = "";
                
                szReturn = objVerbs.Item(0).Name;
                alert(szReturn);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemVerbNameVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objVerbs
                
                set objVerbs = objFolder.Self.Verbs
                    if (not objVerbs is nothing) then
                        dim szReturn
                        
                        szReturn = objVerbs.Item(0).Name
                        alert(szReturn)
                    end if
                set objVerbs = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnFolderItemVerbNameVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder2 Is Nothing) Then
        Dim objVerbs As FolderItemVerbs
        
        Set objVerbs = objFolder2.Self.Verbs
            If (Not objVerbs Is Nothing) Then
                Dim szReturn As String
                
                szReturn = objVerbs.Item(0).Name
                Debug.Print szReturn
            End If
        Set objVerbs = Nothing
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



 

 
