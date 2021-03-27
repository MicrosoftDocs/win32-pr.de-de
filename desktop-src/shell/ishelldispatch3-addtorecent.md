---
description: Fügt der Liste der zuletzt verwendeten (MRU) eine Datei hinzu.
ms.assetid: aa5aef31-7f3f-4cc4-949d-1484de243ef3
title: IShellDispatch3. addtorecent-Methode (Shldisp. h)
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
ms.openlocfilehash: 3f52e6b90b7be078cc8177e9c3fe3093ba5c681e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753072"
---
# <a name="ishelldispatch3addtorecent-method"></a><span data-ttu-id="b0e23-103">IShellDispatch3. addtorecent-Methode</span><span class="sxs-lookup"><span data-stu-id="b0e23-103">IShellDispatch3.AddToRecent method</span></span>

<span data-ttu-id="b0e23-104">Fügt der Liste der zuletzt verwendeten (MRU) eine Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="b0e23-104">Adds a file to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0e23-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="b0e23-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0e23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e23-107">*varFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0e23-107">*varFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e23-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="b0e23-108">Type: **Variant**</span></span>

<span data-ttu-id="b0e23-109">Eine **Zeichenfolge** , die den Pfad der Datei enthält, die der Liste der zuletzt verwendeten Dokumente hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0e23-109">A **String** that contains the path of the file to add to the list of recently used documents.</span></span>

<span data-ttu-id="b0e23-110">**Windows Vista**: Legen Sie diesen Parameter auf **null** fest, um den Ordner zuletzt verwendete Dokumente zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b0e23-110">**Windows Vista**: Set this parameter to **null** to clear the recent documents folder.</span></span>

</dd> <dt>

<span data-ttu-id="b0e23-111">*bstrincategory* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="b0e23-111">*bstrCategory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e23-112">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b0e23-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b0e23-113">Eine **Zeichenfolge** , die den Namen der Kategorie enthält, in der die Datei platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0e23-113">A **String** that contains the name of the category in which to place the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e23-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0e23-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b0e23-115">JScript</span><span class="sxs-lookup"><span data-stu-id="b0e23-115">JScript</span></span>

<span data-ttu-id="b0e23-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b0e23-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b0e23-117">VB</span><span class="sxs-lookup"><span data-stu-id="b0e23-117">VB</span></span>

<span data-ttu-id="b0e23-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b0e23-118">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="b0e23-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0e23-119">Examples</span></span>

<span data-ttu-id="b0e23-120">In den folgenden Beispielen wird die Verwendung von **addtor ecent** für JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b0e23-120">The following examples show the use of **AddToRecent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b0e23-121">JScript</span><span class="sxs-lookup"><span data-stu-id="b0e23-121">JScript:</span></span>


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



<span data-ttu-id="b0e23-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="b0e23-122">VBScript:</span></span>


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



<span data-ttu-id="b0e23-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b0e23-123">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b0e23-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b0e23-124">Requirements</span></span>



| <span data-ttu-id="b0e23-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0e23-125">Requirement</span></span> | <span data-ttu-id="b0e23-126">Wert</span><span class="sxs-lookup"><span data-stu-id="b0e23-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e23-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0e23-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e23-128">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0e23-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="b0e23-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0e23-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e23-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0e23-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b0e23-131">Header</span><span class="sxs-lookup"><span data-stu-id="b0e23-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0e23-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0e23-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b0e23-133">IDL</span><span class="sxs-lookup"><span data-stu-id="b0e23-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0e23-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0e23-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b0e23-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b0e23-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0e23-136"><dt>Shell32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b0e23-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
