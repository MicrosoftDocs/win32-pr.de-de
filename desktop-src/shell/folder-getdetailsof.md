---
description: Ruft Details zu einem Element in einem Ordner ab. Dies kann beispielsweise die Größe, der Typ oder der Zeitpunkt der letzten Änderung sein.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Folder.GetDetailsOf-Methode (Shlobj \_ core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c703150069bc839f2d20024c0de8f3197fba09c5c3571e3de818dec3f3d6737c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860328"
---
# <a name="foldergetdetailsof-method"></a>Folder.GetDetailsOf-Methode

Ruft Details zu einem Element in einem Ordner ab. Dies kann beispielsweise die Größe, der Typ oder der Zeitpunkt der letzten Änderung sein.

## <a name="syntax"></a>Syntax


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vItem* 
</dt> <dd>

Typ: **Variant**

Das Element, für das die Informationen abgerufen werden. Dies muss ein [**FolderItem-Objekt**](folderitem.md) sein.

</dd> <dt>

*iColumn* 
</dt> <dd>

Typ: **Integer**

Ein **Ganzzahlwert,** der die abzurufenden Informationen angibt. Die für ein Element verfügbaren Informationen hängen vom Ordner ab, in dem es angezeigt wird. Dieser Wert entspricht der nullbasierten Spaltennummer, die in einer Shellansicht angezeigt wird. Für ein Element im Dateisystem kann dies einer der folgenden Werte sein:

<dt>



  (0)


</dt> <dd>

Ruft den Namen des Elements ab.

</dd> <dt>



 (1)


</dt> <dd>

Ruft die Größe des Elements ab.

</dd> <dt>



 (2)


</dt> <dd>

Ruft den Typ des Elements ab.

</dd> <dt>



 (3)


</dt> <dd>

Ruft das Datum und die Uhrzeit der letzten Änderung des Elements ab.

</dd> <dt>



 (4)


</dt> <dd>

Ruft die Attribute des Elements ab.

</dd> <dt>



 (-1)


</dt> <dd>

Ruft die Infoinfoinformationen für das Element ab.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

Eine Zeichenfolge, die die abgerufenen Details enthält.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise ist die [**ParseName-Methode**](folder-parsename.md) nicht für den ordner Systemsteuerung (CSIDL \_ CONTROLS) implementiert. Wenn Sie versuchen, eine nichtimplementierte Methode auf 0x800A01BD fehler (dezimal 445) wird ausgelöst.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **GetDetailsOf verwendet,** um den Typ der Datei mit dem Namen Clock.avi. Die richtige Verwendung wird für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
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
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
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
| Header<br/>                   | <dl> <dt>Shlobj \_ core.h (include Shldisp.h)</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 
