---
description: Fügt der Liste der zuletzt verwendeten (MRU) eine Datei hinzu.
ms.assetid: 26D2AE5A-FC7E-4c7c-9F10-8D3D7AA236E7
title: Shell. addtorecent-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.AddToRecent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c4372cc6cfac25f94e607f14734a9f544cd4fcbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980808"
---
# <a name="shelladdtorecent-method"></a>Shell. addtorecent-Methode

Fügt der Liste der zuletzt verwendeten (MRU) eine Datei hinzu.

## <a name="syntax"></a>Syntax


```JScript
Shell.AddToRecent(
  varFile,
  [ bstrCategory ]
)
```


```VB

Shell.AddToRecent( _
  ByVal varFile As Variant, _
  [ ByVal bstrCategory As BSTR ] _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*varFile* \[ in\]
</dt> <dd>

Typ: **Variant**

Eine **Zeichenfolge** , die den Pfad der Datei enthält, die der Liste der zuletzt verwendeten Dokumente hinzugefügt werden soll.

**Windows Vista**: Legen Sie diesen Parameter auf **null** fest, um den Ordner zuletzt verwendete Dokumente zu löschen.

</dd> <dt>

*bstrincategory* \[ in, optional\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge** , die den Namen der Kategorie enthält, in der die Datei platziert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird die Verwendung von **addtor ecent** für JScript, VBScript und Visual Basic veranschaulicht.

JScript


```JScript
<script language="JScript">
    function fnIShellDispatch3AddToRecentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("system.ini");
            if (objFolderItem != null)
            {
                objShell.AddToRecent(objFolderItem.Path);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
     function fnIShellDispatch3AddToRecentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
            
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("system.ini")
                if (not objFolderItem is nothing) then
                    objShell.AddToRecent (objFolderItem.Path)
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnIShellDispatch3AddToRecent()
    Dim objShell  As Shell
    Dim objFolder As Folder
    Dim ssfWINDOWS As Long

    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem

        Set objFolderItem = objFolder.ParseName("system.ini")
        If (Not objFolderItem Is Nothing) Then
            objShell.AddToRecent (objFolderItem.Path)
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6,0 oder höher)</dt> </dl> |



 

 
