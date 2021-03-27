---
description: Ruft Details zu einem Element in einem Ordner ab. Beispielsweise Größe, Typ oder Zeitpunkt der letzten Änderung.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Folder. GetDetailsOf-Methode (shlobj \_ Core. h)
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
ms.openlocfilehash: 3ab89f00f254778a2417644d894f1e9e81eb43cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958643"
---
# <a name="foldergetdetailsof-method"></a>Folder. GetDetailsOf-Methode

Ruft Details zu einem Element in einem Ordner ab. Beispielsweise Größe, Typ oder Zeitpunkt der letzten Änderung.

## <a name="syntax"></a>Syntax


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vitem* 
</dt> <dd>

Typ: **Variant**

Das Element, für das die Informationen abgerufen werden sollen. Dabei muss es sich um ein [**folderItem**](folderitem.md) -Objekt handeln.

</dd> <dt>

*icolumn* 
</dt> <dd>

Type: **Integer**

Ein **ganzzahliger** Wert, der die abzurufenden Informationen angibt. Die für ein Element verfügbaren Informationen sind abhängig von dem Ordner, in dem Sie angezeigt wird. Dieser Wert entspricht der NULL basierten Spaltennummer, die in einer shellansicht angezeigt wird. Bei einem Element im Dateisystem kann dies einer der folgenden Werte sein:

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

Ruft die infotip-Informationen für das Element ab.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Geben Sie Folgendes ein: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _

Zeichenfolge, die das abgerufene Detail enthält.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise ist die [_ *para Sender Name* *](folder-parsename.md) -Methode nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert. Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird **GetDetailsOf** verwendet, um den Typ der Datei mit dem Namen Clock.avi abzurufen. Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.

JScript


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



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shlobj \_ Core. h (Include Shldisp. h)</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 
