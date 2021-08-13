---
description: Ruft den Wert einer Eigenschaft aus dem Eigenschaftensatz eines Elements ab. Die Eigenschaft kann entweder durch den Namen oder durch den Formatbezeichner (FMTID) und den Eigenschaftenbezeichner (PID) des Eigenschaftensets angegeben werden.
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: ShellFolderItem.ExtendedProperty-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f5aa8ab3ba61d752cfe4d9f8ecd29bf4fcd06c3dbadde94e51ac9a05a8504b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452816"
---
# <a name="shellfolderitemextendedproperty-method"></a>ShellFolderItem.ExtendedProperty-Methode

Ruft den Wert einer Eigenschaft aus dem Eigenschaftensatz eines Elements ab. Die Eigenschaft kann entweder durch den Namen oder durch den Formatbezeichner (FMTID) und den Eigenschaftenbezeichner (PID) des Eigenschaftensets angegeben werden.

## <a name="syntax"></a>Syntax


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sPropName* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Ein **Zeichenfolgenwert,** der die -Eigenschaft angibt. Weitere Informationen finden Sie im Abschnitt Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **\* Variant**

Enthält nach der Rückgabe dieser Methode den Wert der -Eigenschaft, sofern er für das angegebene Element vorhanden ist. Der Wert enthält eine vollständige Eingabe, z. B. werden Datumsangaben als Datumsangaben und nicht als Zeichenfolgen zurückgegeben.

Diese Methode gibt eine Zeichenfolge der Länge 0 (null) zurück, wenn die Eigenschaft gültig ist, aber für das angegebene Element nicht vorhanden ist, oder andernfalls einen Fehlercode.

## <a name="remarks"></a>Hinweise

Es gibt zwei Möglichkeiten, eine Eigenschaft anzugeben. Die erste besteht im Zuweisen des bekannten Namens der Eigenschaft, z. B. "Author" oder "Date", *zu sPropName.* Jede Eigenschaft ist jedoch ein Member eines Component Object Model-Eigenschaftensatzes (COM) und kann auch durch Angabe ihrer Format-ID (FMTID) und Eigenschaften-ID (PID) identifiziert werden. Ein [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) ist eine GUID, die den Eigenschaftensatz identifiziert, und eine [**PID**](../stg/structured-storage-serialized-property-set-format.md) ist eine ganze Zahl, die eine bestimmte Eigenschaft innerhalb des Eigenschaftensets identifiziert.

Die Angabe einer Eigenschaft anhand ihrer FMTID-/PID-Werte ist in der Regel effizienter als die Verwendung ihres Namens. Um die FMTID-/PID-Werte einer Eigenschaft mit **ExtendedProperty** zu verwenden, müssen sie in einer SCID kombiniert werden. Eine SCID ist eine Zeichenfolge, die die FMTID/PID-Werte im Formular *"FMTID**PID"* enthält, wobei FMTID die Zeichenfolgenform der GUID des Eigenschaftensets ist. Beispielsweise ist der SCID der author-Eigenschaft des Eigenschaftssets für Zusammenfassungsinformationen "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".

Eine Liste der FMTIDs und PIDs, die derzeit von der Shell unterstützt werden, finden Sie unter [**SHCOLUMNID**](./objects.md).

## <a name="examples"></a>Beispiele

Dieser Beispielcode veranschaulicht die Verwendung von **ExtendedProperty** zum Abrufen der Eigenschaften "Title" und "Author" aus einem Word-Dokument. Sobald das [**ShellFolderItem-Objekt**](shellfolderitem-object.md) der Datei (in diesem Beispiel *fiWordDoc)* zugeordnet ist, rufen Sie den Wert der Eigenschaft ab, indem Sie ihren Namen **an ExtendedProperty übergeben.**


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



Ein schnellerer und effizienterer Ansatz besteht in der Übergeben einer SCID an **ExtendedProperty.**


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



Die folgenden Beispiele zeigen die ordnungsgemäße Verwendung dieser Methode für JScript, VBScript und Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
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
                    dim szReturn
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
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
Private Sub fnFolderItem2ExtendedPropertyVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
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
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



 

 
