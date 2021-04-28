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
# <a name="ishelldispatch3addtorecent-method"></a><span data-ttu-id="5c257-103">IShellDispatch3.AddToRecent-Methode</span><span class="sxs-lookup"><span data-stu-id="5c257-103">IShellDispatch3.AddToRecent method</span></span>

<span data-ttu-id="5c257-104">Fügt der Liste der zuletzt verwendeten Dateien (MRU) eine Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="5c257-104">Adds a file to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c257-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c257-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="5c257-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c257-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c257-107">*varFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5c257-107">*varFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c257-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5c257-108">Type: **Variant**</span></span>

<span data-ttu-id="5c257-109">Eine **Zeichenfolge,** die den Pfad der Datei enthält, die der Liste der zuletzt verwendeten Dokumente hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c257-109">A **String** that contains the path of the file to add to the list of recently used documents.</span></span>

<span data-ttu-id="5c257-110">**Windows Vista:** Legen Sie diesen Parameter auf **NULL fest,** um den Ordner der letzten Dokumente zu löschen.</span><span class="sxs-lookup"><span data-stu-id="5c257-110">**Windows Vista**: Set this parameter to **null** to clear the recent documents folder.</span></span>

</dd> <dt>

<span data-ttu-id="5c257-111">*bstrCategory* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="5c257-111">*bstrCategory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c257-112">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="5c257-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="5c257-113">Eine **Zeichenfolge,** die den Namen der Kategorie enthält, in der die Datei gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c257-113">A **String** that contains the name of the category in which to place the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c257-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5c257-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="5c257-115">JScript</span><span class="sxs-lookup"><span data-stu-id="5c257-115">JScript</span></span>

<span data-ttu-id="5c257-116">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5c257-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="5c257-117">VB</span><span class="sxs-lookup"><span data-stu-id="5c257-117">VB</span></span>

<span data-ttu-id="5c257-118">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5c257-118">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="5c257-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c257-119">Examples</span></span>

<span data-ttu-id="5c257-120">Die folgenden Beispiele zeigen die Verwendung von **AddToRecent** für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5c257-120">The following examples show the use of **AddToRecent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="5c257-121">Jscript:</span><span class="sxs-lookup"><span data-stu-id="5c257-121">JScript:</span></span>


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



<span data-ttu-id="5c257-122">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="5c257-122">VBScript:</span></span>


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



<span data-ttu-id="5c257-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="5c257-123">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5c257-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c257-124">Requirements</span></span>



| <span data-ttu-id="5c257-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c257-125">Requirement</span></span> | <span data-ttu-id="5c257-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5c257-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c257-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c257-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5c257-128">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c257-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="5c257-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c257-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5c257-130">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c257-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5c257-131">Header</span><span class="sxs-lookup"><span data-stu-id="5c257-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c257-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="5c257-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="5c257-133">Idl</span><span class="sxs-lookup"><span data-stu-id="5c257-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c257-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c257-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="5c257-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5c257-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c257-136"><dt>Shell32.dll (Version 6.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="5c257-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
