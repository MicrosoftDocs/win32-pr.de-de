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
# <a name="foldergetdetailsof-method"></a><span data-ttu-id="1c7f0-104">Folder. GetDetailsOf-Methode</span><span class="sxs-lookup"><span data-stu-id="1c7f0-104">Folder.GetDetailsOf method</span></span>

<span data-ttu-id="1c7f0-105">Ruft Details zu einem Element in einem Ordner ab.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-105">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="1c7f0-106">Beispielsweise Größe, Typ oder Zeitpunkt der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-106">For example, its size, type, or the time of its last modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c7f0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c7f0-107">Syntax</span></span>


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a><span data-ttu-id="1c7f0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c7f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c7f0-109">*vitem*</span><span class="sxs-lookup"><span data-stu-id="1c7f0-109">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="1c7f0-110">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="1c7f0-110">Type: **Variant**</span></span>

<span data-ttu-id="1c7f0-111">Das Element, für das die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-111">The item for which to retrieve the information.</span></span> <span data-ttu-id="1c7f0-112">Dabei muss es sich um ein [**folderItem**](folderitem.md) -Objekt handeln.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-112">This must be a [**FolderItem**](folderitem.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="1c7f0-113">*icolumn*</span><span class="sxs-lookup"><span data-stu-id="1c7f0-113">*iColumn*</span></span> 
</dt> <dd>

<span data-ttu-id="1c7f0-114">Type: **Integer**</span><span class="sxs-lookup"><span data-stu-id="1c7f0-114">Type: **Integer**</span></span>

<span data-ttu-id="1c7f0-115">Ein **ganzzahliger** Wert, der die abzurufenden Informationen angibt.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-115">An **Integer** value that specifies the information to be retrieved.</span></span> <span data-ttu-id="1c7f0-116">Die für ein Element verfügbaren Informationen sind abhängig von dem Ordner, in dem Sie angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-116">The information available for an item depends on the folder in which it is displayed.</span></span> <span data-ttu-id="1c7f0-117">Dieser Wert entspricht der NULL basierten Spaltennummer, die in einer shellansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-117">This value corresponds to the zero-based column number that is displayed in a Shell view.</span></span> <span data-ttu-id="1c7f0-118">Bei einem Element im Dateisystem kann dies einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="1c7f0-118">For an item in the file system, this can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="1c7f0-119"> (0)</span><span class="sxs-lookup"><span data-stu-id="1c7f0-119">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1c7f0-120">Ruft den Namen des Elements ab.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-120">Retrieves the name of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="1c7f0-121">(1)</span><span class="sxs-lookup"><span data-stu-id="1c7f0-121">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1c7f0-122">Ruft die Größe des Elements ab.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-122">Retrieves the size of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="1c7f0-123">(2)</span><span class="sxs-lookup"><span data-stu-id="1c7f0-123">(2)</span></span>


</dt> <dd>

<span data-ttu-id="1c7f0-124">Ruft den Typ des Elements ab.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-124">Retrieves the type of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="1c7f0-125">(3)</span><span class="sxs-lookup"><span data-stu-id="1c7f0-125">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1c7f0-126">Ruft das Datum und die Uhrzeit der letzten Änderung des Elements ab.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-126">Retrieves the date and time that the item was last modified.</span></span>

</dd> <dt>



 <span data-ttu-id="1c7f0-127">(4)</span><span class="sxs-lookup"><span data-stu-id="1c7f0-127">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1c7f0-128">Ruft die Attribute des Elements ab.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-128">Retrieves the attributes of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="1c7f0-129">(-1)</span><span class="sxs-lookup"><span data-stu-id="1c7f0-129">(-1)</span></span>


</dt> <dd>

<span data-ttu-id="1c7f0-130">Ruft die infotip-Informationen für das Element ab.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-130">Retrieves the info tip information for the item.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c7f0-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c7f0-131">Return value</span></span>

<span data-ttu-id="1c7f0-132">Geben Sie Folgendes ein: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="1c7f0-132">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="1c7f0-133">Zeichenfolge, die das abgerufene Detail enthält.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-133">String containing the retrieved detail.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c7f0-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c7f0-134">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1c7f0-135">Nicht alle Methoden werden für alle Ordner implementiert.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-135">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="1c7f0-136">Beispielsweise ist die [_ *para Sender Name* \*](folder-parsename.md) -Methode nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-136">For example, the [_ *ParseName*\*](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="1c7f0-137">Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-137">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="1c7f0-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c7f0-138">Examples</span></span>

<span data-ttu-id="1c7f0-139">Im folgenden Beispiel wird **GetDetailsOf** verwendet, um den Typ der Datei mit dem Namen Clock.avi abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-139">The following example uses **GetDetailsOf** to retrieve the type of the file named Clock.avi.</span></span> <span data-ttu-id="1c7f0-140">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c7f0-140">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1c7f0-141">JScript</span><span class="sxs-lookup"><span data-stu-id="1c7f0-141">JScript:</span></span>


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



<span data-ttu-id="1c7f0-142">VBScript</span><span class="sxs-lookup"><span data-stu-id="1c7f0-142">VBScript:</span></span>


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



<span data-ttu-id="1c7f0-143">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1c7f0-143">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="1c7f0-144">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1c7f0-144">Requirements</span></span>



| <span data-ttu-id="1c7f0-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c7f0-145">Requirement</span></span> | <span data-ttu-id="1c7f0-146">Wert</span><span class="sxs-lookup"><span data-stu-id="1c7f0-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c7f0-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c7f0-147">Minimum supported client</span></span><br/> | <span data-ttu-id="1c7f0-148">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c7f0-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1c7f0-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c7f0-149">Minimum supported server</span></span><br/> | <span data-ttu-id="1c7f0-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1c7f0-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1c7f0-151">Header</span><span class="sxs-lookup"><span data-stu-id="1c7f0-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c7f0-152"><dt>Shlobj \_ Core. h (Include Shldisp. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c7f0-152"><dt>Shlobj\_core.h (include Shldisp.h)</dt></span></span> </dl>  |
| <span data-ttu-id="1c7f0-153">IDL</span><span class="sxs-lookup"><span data-stu-id="1c7f0-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1c7f0-154"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1c7f0-154"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1c7f0-155">DLL</span><span class="sxs-lookup"><span data-stu-id="1c7f0-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c7f0-156"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1c7f0-156"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
