---
description: Enthält das übergeordnete Ordnerobjekt.
ms.assetid: b832948c-f599-4ada-8760-9280b86abfed
title: Folder.ParentFolder-Eigenschaft (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParentFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4d812d127884ca1c76533992a4ee4d8c527d151891239d715f5e3a7f8a5f0ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860267"
---
# <a name="folderparentfolder-property"></a>Folder.ParentFolder (Eigenschaft)

Enthält das übergeordnete [**Ordnerobjekt.**](folder.md)

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
ParentFolder = Folder.ParentFolder
```



## <a name="property-value"></a>Eigenschaftswert

Ein Objektverweis auf das ParentFolder-Objekt.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise ist die [**ParseName-Methode**](folder-parsename.md) nicht für den ordner Systemsteuerung (CSIDL \_ CONTROLS) implementiert. Wenn Sie versuchen, eine nichtimplementierte Methode auf 0x800A01BD fehler (dezimal 445) wird ausgelöst.

 

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von **ParentFolder** für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderParentFolderJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objParentFolder;
                
            objParentFolder = objFolder.ParentFolder;
            if (objParentFolder != null)
            {
                alert(objParentFolder.Title);
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderParentFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objParentFolder
                        
                set objParentFolder = objFolder.ParentFolder
                if (not objParentFolder is nothing) then
                    alert(objParentFolder.Title)
                end if
                set objParentFolder = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderParentFolderVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objParentFolder As Folder
                
        Set objParentFolder = objFolder.ParentFolder
        If (Not objParentFolder Is Nothing) Then
            Debug.Print objParentFolder.Title
        End If
        Set objParentFolder = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




