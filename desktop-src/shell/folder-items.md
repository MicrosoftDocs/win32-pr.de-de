---
description: Ruft ein FolderItems-Objekt ab, das die Auflistung von Elementen im Ordner darstellt.
ms.assetid: ef2965ec-c8ab-4108-8e5e-b4fd5370521a
title: Folder.Items-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Items
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e698c74cd8cc04265ef75e01062f8aa05171f660f5cf5eb7253d04d3397ed984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093134"
---
# <a name="folderitems-method"></a>Folder.Items-Methode

Ruft ein [**FolderItems-Objekt**](folderitems.md) ab, das die Auflistung von Elementen im Ordner darstellt.

## <a name="syntax"></a>Syntax


```JScript
retVal = Folder.Items()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FolderItems**](folderitems.md)\*\***

Ein Objektverweis auf das [**FolderItems-Objekt.**](folderitems.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise ist die [**ParseName-Methode**](folder-parsename.md) nicht für den ordner Systemsteuerung (CSIDL \_ CONTROLS) implementiert. Wenn Sie versuchen, eine nichtimplementierte Methode auf 0x800A01BD fehler (dezimal 445) wird ausgelöst.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **Items verwendet,** um die Anzahl der Elemente im Ordner C: Windows \\ zu bestimmen. Die richtige Verwendung wird für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderObjectItemsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItems = new Object;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                document.write (objFolderItems.Count);
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderObjectItemsVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItems

            set objFolderItems = objFolder.Items

            if (not objFolderItems Is Nothing) then
                document.write objFolderItems.Count
            end if

            set objFolderItem = nothing
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnFolderObjectItems_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItems As FolderItems

        Set objFolderItems = objFolder.Items()

        If (Not objFolderItems Is Nothing) Then
            Dim vCount As Variant

            vCount = objFolderItems.Count
        End If

        Set objFolderItems = Nothing
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



 

 




