---
description: Enthält den Titel des Ordners.
ms.assetid: 95c064ff-4504-4e9c-80ac-47beca443ad4
title: Folder. Title-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Title
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8fc66d231d49d724749ae79b248b4dca9d917acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979681"
---
# <a name="foldertitle-property"></a><span data-ttu-id="ed918-103">Folder. Title (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ed918-103">Folder.Title property</span></span>

<span data-ttu-id="ed918-104">Enthält den Titel des Ordners.</span><span class="sxs-lookup"><span data-stu-id="ed918-104">Contains the title of the folder.</span></span>

<span data-ttu-id="ed918-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ed918-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed918-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed918-106">Syntax</span></span>


```JScript
strTitle = Folder.Title
```



## <a name="property-value"></a><span data-ttu-id="ed918-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ed918-107">Property value</span></span>

<span data-ttu-id="ed918-108">Eine Zeichenfolge, die den Titel des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="ed918-108">A string containing the object's title.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed918-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed918-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ed918-110">Nicht alle Methoden werden für alle Ordner implementiert.</span><span class="sxs-lookup"><span data-stu-id="ed918-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="ed918-111">Beispielsweise ist die Methode " [**Parser Name**](folder-parsename.md) " nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert.</span><span class="sxs-lookup"><span data-stu-id="ed918-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="ed918-112">Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ed918-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ed918-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed918-113">Examples</span></span>

<span data-ttu-id="ed918-114">Im folgenden Beispiel wird **Title** verwendet, um den Titel des Ordners abzurufen, der die Programm Gruppen des Benutzers enthält (in der Regel "Programme").</span><span class="sxs-lookup"><span data-stu-id="ed918-114">The following example uses **Title** to retrieve the title of the folder holding the user's program groups (usually "Programs").</span></span> <span data-ttu-id="ed918-115">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ed918-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ed918-116">JScript</span><span class="sxs-lookup"><span data-stu-id="ed918-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderTitleJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="ed918-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="ed918-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderTitleVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                alert(objFolder.Title)
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ed918-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ed918-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderTitleVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ed918-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ed918-119">Requirements</span></span>



| <span data-ttu-id="ed918-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed918-120">Requirement</span></span> | <span data-ttu-id="ed918-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ed918-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed918-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed918-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ed918-123">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed918-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ed918-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed918-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ed918-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed918-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ed918-126">Header</span><span class="sxs-lookup"><span data-stu-id="ed918-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed918-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed918-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ed918-128">IDL</span><span class="sxs-lookup"><span data-stu-id="ed918-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed918-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed918-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ed918-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ed918-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed918-131"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ed918-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




