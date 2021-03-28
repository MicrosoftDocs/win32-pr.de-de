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
# <a name="shellfolderitemextendedproperty-method"></a><span data-ttu-id="0a1d0-104">Shellfolderitem. ExtendedProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="0a1d0-104">ShellFolderItem.ExtendedProperty method</span></span>

<span data-ttu-id="0a1d0-105">Ruft den Wert einer Eigenschaft aus dem Eigenschaften Satz eines Elements ab.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-105">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="0a1d0-106">Die-Eigenschaft kann entweder anhand des Namens oder anhand des Format Bezeichners (fmtid) und des Eigenschafts Bezeichners (PID) des Eigenschaften Satzes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-106">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a1d0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a1d0-107">Syntax</span></span>


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a><span data-ttu-id="0a1d0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a1d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a1d0-109">*spropname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a1d0-109">*sPropName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a1d0-110">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="0a1d0-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="0a1d0-111">Ein **Zeichen** folgen Wert, der die Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-111">A **String** value that specifies the property.</span></span> <span data-ttu-id="0a1d0-112">Weitere Informationen finden Sie im Abschnitt Hinweise.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-112">See the Remarks section for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a1d0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a1d0-113">Return value</span></span>

<span data-ttu-id="0a1d0-114">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="0a1d0-114">Type: \**Variant\** _</span></span>

<span data-ttu-id="0a1d0-115">Wenn diese Methode zurückgegeben wird, enthält Sie den Wert der-Eigenschaft, wenn Sie für das angegebene Element vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-115">When this method returns, contains the value of the property, if it exists for the specified item.</span></span> <span data-ttu-id="0a1d0-116">Der Wert wird vollständig eingegeben – beispielsweise werden Datumsangaben als Datumsangaben, nicht als Zeichen folgen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-116">The value will have full typing—for example, dates are returned as dates, not strings.</span></span>

<span data-ttu-id="0a1d0-117">Diese Methode gibt eine Zeichenfolge der Länge 0 (null) zurück, wenn die Eigenschaft gültig ist, aber für das angegebene Element nicht vorhanden ist, andernfalls ein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-117">This method returns a zero-length string if the property is valid but does not exist for the specified item, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a1d0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a1d0-118">Remarks</span></span>

<span data-ttu-id="0a1d0-119">Es gibt zwei Möglichkeiten, eine Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-119">There are two ways to specify a property.</span></span> <span data-ttu-id="0a1d0-120">Der erste besteht darin, _sPropName \* den bekannten Namen der Eigenschaft, z. b. "Author" oder "Date", zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-120">The first is to assign the property's well-known name, such as "Author" or "Date", to _sPropName\*.</span></span> <span data-ttu-id="0a1d0-121">Allerdings ist jede Eigenschaft ein Member eines Component Object Model (com)-Eigenschaften Satzes und kann auch durch Angabe der Format-ID (fmtid) und der Eigen schafts-ID (PID) identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-121">However, each property is a member of a Component Object Model (COM) property set and can also be identified by specifying its format ID (FMTID) and property ID (PID).</span></span> <span data-ttu-id="0a1d0-122">Eine [**fmtid**](../stg/structured-storage-serialized-property-set-format.md) ist eine GUID, die den Eigenschaften Satz identifiziert, und eine [**PID**](../stg/structured-storage-serialized-property-set-format.md) ist eine ganze Zahl, die eine bestimmte Eigenschaft innerhalb des Eigenschaften Satzes identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-122">An [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) is a GUID that identifies the property set, and a [**PID**](../stg/structured-storage-serialized-property-set-format.md) is an integer that identifies a particular property within the property set.</span></span>

<span data-ttu-id="0a1d0-123">Es ist in der Regel effizienter, eine Eigenschaft anhand der Werte von fmtid/PID anzugeben, als den Namen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-123">Specifying a property by its FMTID/PID values is usually more efficient than using its name.</span></span> <span data-ttu-id="0a1d0-124">Um die fmtid/PID-Werte einer Eigenschaft mit **ExtendedProperty** zu verwenden, müssen Sie in einer scid kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-124">To use a property's FMTID/PID values with **ExtendedProperty**, they must be combined into an SCID.</span></span> <span data-ttu-id="0a1d0-125">Eine scid ist eine Zeichenfolge, die die fmtid/PID-Werte im Format "*fmtid \* \* PID*" enthält, wobei "fmtid" das Zeichen folgen Format der GUID des Eigenschafts Satzes ist.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-125">An SCID is a string that contains the FMTID/PID values in the form "*FMTID\*\*PID*", where the FMTID is the string form of the property set's GUID.</span></span> <span data-ttu-id="0a1d0-126">Beispielsweise ist die scid der Eigenschaft "Author" der Summary-Informations Eigenschaft "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span><span class="sxs-lookup"><span data-stu-id="0a1d0-126">For example, the SCID of the summary information property set's author property is "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span></span>

<span data-ttu-id="0a1d0-127">Eine Liste der von der Shell derzeit unterstützten fmtids und PIDs finden Sie unter [**shcolumnid**](./objects.md).</span><span class="sxs-lookup"><span data-stu-id="0a1d0-127">For a list of FMTIDs and PIDs that are currently supported by the Shell, see [**SHCOLUMNID**](./objects.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0a1d0-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a1d0-128">Examples</span></span>

<span data-ttu-id="0a1d0-129">Dieser Beispielcode veranschaulicht die Verwendung von **ExtendedProperty** zum Abrufen der Eigenschaften "Title" und "Autor" aus einem Word-Dokument.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-129">This sample code illustrates how to use **ExtendedProperty** to retrieve the "Title" and "Author" properties from a Word document.</span></span> <span data-ttu-id="0a1d0-130">Sobald das [**shellfolderitem**](shellfolderitem-object.md) -Objekt mit der Datei verknüpft ist, dann rufen *Sie in diesem* Beispiel den Wert der Eigenschaft ab, indem Sie seinen Namen an **ExtendedProperty** übergeben.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-130">Once you have the [**ShellFolderItem**](shellfolderitem-object.md) object associated with the file, *fiWordDoc* in this example, retrieve the property's value by passing its name to **ExtendedProperty**.</span></span>


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



<span data-ttu-id="0a1d0-131">Ein schnellerer und effizienterer Ansatz besteht darin, eine scid an **ExtendedProperty** zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-131">A faster and more efficient approach is to pass an SCID to **ExtendedProperty**.</span></span>


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



<span data-ttu-id="0a1d0-132">Die folgenden Beispiele zeigen die ordnungsgemäße Verwendung dieser Methode für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0a1d0-132">The following examples show the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0a1d0-133">JScript</span><span class="sxs-lookup"><span data-stu-id="0a1d0-133">JScript:</span></span>


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



<span data-ttu-id="0a1d0-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="0a1d0-134">VBScript:</span></span>


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



<span data-ttu-id="0a1d0-135">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="0a1d0-135">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0a1d0-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0a1d0-136">Requirements</span></span>



| <span data-ttu-id="0a1d0-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a1d0-137">Requirement</span></span> | <span data-ttu-id="0a1d0-138">Wert</span><span class="sxs-lookup"><span data-stu-id="0a1d0-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a1d0-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a1d0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0a1d0-140">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a1d0-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0a1d0-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a1d0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0a1d0-142">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a1d0-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0a1d0-143">Header</span><span class="sxs-lookup"><span data-stu-id="0a1d0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a1d0-144"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a1d0-144"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="0a1d0-145">IDL</span><span class="sxs-lookup"><span data-stu-id="0a1d0-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0a1d0-146"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0a1d0-146"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="0a1d0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0a1d0-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a1d0-148"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="0a1d0-148"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
