---
description: Legt einen Platzhalterfilter fest, der auf die zurückgegebenen Elemente angewendet werden soll.
ms.assetid: 19ca82c5-16ff-46c7-8ea1-ddbfc2ce3ac9
title: FolderItems3.Filter-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems3.Filter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: dd4983d340645e916595534f17dccb2ef09e2f5c185b6eaf97cc7de2e52669dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032588"
---
# <a name="folderitems3filter-method"></a>FolderItems3.Filter-Methode

Legt einen Platzhalterfilter fest, der auf die zurückgegebenen Elemente angewendet werden soll.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = FolderItems3.Filter(
  grfFlags,
  bstrFilter
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*grfFlags* \[ In\]
</dt> <dd>

Typ: **Integer**

Dieser Parameter kann eines der flags sein, die in [**SHCONTF aufgeführt sind.**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf)

</dd> <dt>

*bstrFilter* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine Filterzeichenfolge, die angibt, was in der [**FolderItems-Auflistung aufgelistet werden**](folderitems.md) soll.

</dd> </dl>

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von **Filter** für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItems3FilterJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems3;
            
            objFolderItems3 = objFolder.Items();
            if (objFolderItems3 != null)
            {
                var SHCONTF_NONFOLDERS = 64;
                
                alert(objFolderItems3.Count);
                objFolderItems3.Filter(SHCONTF_NONFOLDERS, "*.txt");
                alert(objFolderItems3.Count);
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderItems3FilterVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems3
                        
                set objFolderItems3 = objFolder.Items()
                if (not objFolderItems3 is nothing) then
                    dim SHCONTF_NONFOLDERS
                
                    SHCONTF_NONFOLDERS = 64
                    alert(objFolderItems3.Count)
                    objFolderItems3.Filter SHCONTF_NONFOLDERS, "*.txt"
                    alert(objFolderItems3.Count)
                end if
                set objFolderItems3 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnFolderItems3FilterVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems3 As FolderItems3
            
            Set objFolderItems3 = objFolder.Items
                If (Not objFolderItems3 Is Nothing) Then
                    Dim SHCONTF_NONFOLDERS As Long
                    
                    SHCONTF_NONFOLDERS = 64
                    Debug.Print objFolderItems3.Count
                    objFolderItems3.Filter SHCONTF_NONFOLDERS, "*.exe"
                    Debug.Print objFolderItems3.Count
                End If
            Set objFolderItems3 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FolderItems3**](folderitems3-object.md)
</dt> <dt>

[**FolderItems2**](folderitems2-object.md)
</dt> <dt>

[**FolderItem**](folderitem.md)
</dt> </dl>

 

 
