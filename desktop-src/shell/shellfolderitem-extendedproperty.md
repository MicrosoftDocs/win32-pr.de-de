---
description: Ruft den Wert einer Eigenschaft aus dem Eigenschaften Satz eines Elements ab. Die-Eigenschaft kann entweder anhand des Namens oder anhand des Format Bezeichners (fmtid) und des Eigenschafts Bezeichners (PID) des Eigenschaften Satzes angegeben werden.
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: Shellfolderitem. ExtendedProperty-Methode (Shldisp. h)
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
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980440"
---
# <a name="shellfolderitemextendedproperty-method"></a>Shellfolderitem. ExtendedProperty-Methode

Ruft den Wert einer Eigenschaft aus dem Eigenschaften Satz eines Elements ab. Die-Eigenschaft kann entweder anhand des Namens oder anhand des Format Bezeichners (fmtid) und des Eigenschafts Bezeichners (PID) des Eigenschaften Satzes angegeben werden.

## <a name="syntax"></a>Syntax


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*spropname* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Ein **Zeichen** folgen Wert, der die Eigenschaft angibt. Weitere Informationen finden Sie im Abschnitt Hinweise.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **Variant \** _

Wenn diese Methode zurückgegeben wird, enthält Sie den Wert der-Eigenschaft, wenn Sie für das angegebene Element vorhanden ist. Der Wert wird vollständig eingegeben – beispielsweise werden Datumsangaben als Datumsangaben, nicht als Zeichen folgen zurückgegeben.

Diese Methode gibt eine Zeichenfolge der Länge 0 (null) zurück, wenn die Eigenschaft gültig ist, aber für das angegebene Element nicht vorhanden ist, andernfalls ein Fehlercode.

## <a name="remarks"></a>Bemerkungen

Es gibt zwei Möglichkeiten, eine Eigenschaft anzugeben. Der erste besteht darin, _sPropName * den bekannten Namen der Eigenschaft, z. b. "Author" oder "Date", zuzuweisen. Allerdings ist jede Eigenschaft ein Member eines Component Object Model (com)-Eigenschaften Satzes und kann auch durch Angabe der Format-ID (fmtid) und der Eigen schafts-ID (PID) identifiziert werden. Eine [**fmtid**](../stg/structured-storage-serialized-property-set-format.md) ist eine GUID, die den Eigenschaften Satz identifiziert, und eine [**PID**](../stg/structured-storage-serialized-property-set-format.md) ist eine ganze Zahl, die eine bestimmte Eigenschaft innerhalb des Eigenschaften Satzes identifiziert.

Es ist in der Regel effizienter, eine Eigenschaft anhand der Werte von fmtid/PID anzugeben, als den Namen zu verwenden. Um die fmtid/PID-Werte einer Eigenschaft mit **ExtendedProperty** zu verwenden, müssen Sie in einer scid kombiniert werden. Eine scid ist eine Zeichenfolge, die die fmtid/PID-Werte im Format "*fmtid * * PID*" enthält, wobei "fmtid" das Zeichen folgen Format der GUID des Eigenschafts Satzes ist. Beispielsweise ist die scid der Eigenschaft "Author" der Summary-Informations Eigenschaft "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".

Eine Liste der von der Shell derzeit unterstützten fmtids und PIDs finden Sie unter [**shcolumnid**](./objects.md).

## <a name="examples"></a>Beispiele

Dieser Beispielcode veranschaulicht die Verwendung von **ExtendedProperty** zum Abrufen der Eigenschaften "Title" und "Autor" aus einem Word-Dokument. Sobald das [**shellfolderitem**](shellfolderitem-object.md) -Objekt mit der Datei verknüpft ist, dann rufen *Sie in diesem* Beispiel den Wert der Eigenschaft ab, indem Sie seinen Namen an **ExtendedProperty** übergeben.


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



Ein schnellerer und effizienterer Ansatz besteht darin, eine scid an **ExtendedProperty** zu übergeben.


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

JScript


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



VBScript


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



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



 

 
