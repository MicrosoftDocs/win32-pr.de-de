---
description: Enthält das übergeordnete Ordner Objekt.
ms.assetid: b832948c-f599-4ada-8760-9280b86abfed
title: Folder. para Folder-Eigenschaft (Shldisp. h)
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
ms.openlocfilehash: 200d8f8c931bd81015f52226bed5a4e584951e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959698"
---
# <a name="folderparentfolder-property"></a><span data-ttu-id="cbae5-103">Folder. para Folder-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="cbae5-103">Folder.ParentFolder property</span></span>

<span data-ttu-id="cbae5-104">Enthält das übergeordnete [**Ordner**](folder.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="cbae5-104">Contains the parent [**Folder**](folder.md) object.</span></span>

<span data-ttu-id="cbae5-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cbae5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbae5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbae5-106">Syntax</span></span>


```JScript
ParentFolder = Folder.ParentFolder
```



## <a name="property-value"></a><span data-ttu-id="cbae5-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="cbae5-107">Property value</span></span>

<span data-ttu-id="cbae5-108">Ein Objekt Verweis auf das Objekt "objektfolder".</span><span class="sxs-lookup"><span data-stu-id="cbae5-108">An object reference to the ParentFolder object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbae5-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbae5-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cbae5-110">Nicht alle Methoden werden für alle Ordner implementiert.</span><span class="sxs-lookup"><span data-stu-id="cbae5-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="cbae5-111">Beispielsweise ist die Methode " [**Parser Name**](folder-parsename.md) " nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert.</span><span class="sxs-lookup"><span data-stu-id="cbae5-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="cbae5-112">Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="cbae5-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="cbae5-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cbae5-113">Examples</span></span>

<span data-ttu-id="cbae5-114">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung von "Parameter **Folder** " für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cbae5-114">The following example shows the proper usage of **ParentFolder** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cbae5-115">JScript</span><span class="sxs-lookup"><span data-stu-id="cbae5-115">JScript:</span></span>


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



<span data-ttu-id="cbae5-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="cbae5-116">VBScript:</span></span>


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



<span data-ttu-id="cbae5-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cbae5-117">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cbae5-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cbae5-118">Requirements</span></span>



| <span data-ttu-id="cbae5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cbae5-119">Requirement</span></span> | <span data-ttu-id="cbae5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cbae5-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbae5-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cbae5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cbae5-122">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbae5-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cbae5-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cbae5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cbae5-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cbae5-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cbae5-125">Header</span><span class="sxs-lookup"><span data-stu-id="cbae5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbae5-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbae5-126"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cbae5-127">IDL</span><span class="sxs-lookup"><span data-stu-id="cbae5-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cbae5-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cbae5-128"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cbae5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cbae5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbae5-130"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="cbae5-130"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




