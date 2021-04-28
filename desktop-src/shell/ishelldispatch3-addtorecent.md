---
description: 'IShellDispatch3.AddToRecent-Methode: Fügt der Liste der zuletzt verwendeten Dateien (MRU) eine Datei hinzu.'
ms.assetid: aa5aef31-7f3f-4cc4-949d-1484de243ef3
title: IShellDispatch3.AddToRecent-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3.AddToRecent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8d31d05e9eef889d9018e4806cf4c882dba3060e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116928"
---
# <a name="ishelldispatch3addtorecent-method"></a>IShellDispatch3.AddToRecent-Methode

Fügt der Liste der zuletzt verwendeten Dateien (MRU) eine Datei hinzu.

## <a name="syntax"></a>Syntax


```JScript
IShellDispatch3.AddToRecent(
  varFile,
  [ bstrCategory ]
)
```


```VB

IShellDispatch3.AddToRecent( _
  ByVal varFile As Variant, _
  [ ByVal bstrCategory As BSTR ] _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*varFile* \[ In\]
</dt> <dd>

Typ: **Variant**

Eine **Zeichenfolge,** die den Pfad der Datei enthält, die der Liste der zuletzt verwendeten Dokumente hinzugefügt werden soll.

**Windows Vista:** Legen Sie diesen Parameter auf **NULL fest,** um den Ordner der letzten Dokumente zu löschen.

</dd> <dt>

*bstrCategory* \[ in, optional\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine **Zeichenfolge,** die den Namen der Kategorie enthält, in der die Datei gespeichert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="jscript"></a>JScript

Diese Methode gibt keinen Wert zurück.

### <a name="vb"></a>VB

Diese Methode gibt keinen Wert zurück.

## <a name="examples"></a>Beispiele

Die folgenden Beispiele zeigen die Verwendung von **AddToRecent** für JScript, VBScript und Visual Basic.

Jscript:


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



Vbscript:


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



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6.0 oder höher)</dt> </dl> |



 

 
