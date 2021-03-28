---
description: Ruft das folderitemverbs-Objekt des Elements ab. Bei diesem Objekt handelt es sich um eine Auflistung von Verben, die für das Element ausgeführt werden können.
ms.assetid: e31160cd-093a-45a6-a066-58120c44eb2c
title: FolderItem. Verbs-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Verbs
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f15c2471f749748f7928a45aa03037d955c75d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127841"
---
# <a name="folderitemverbs-method"></a><span data-ttu-id="56c01-104">FolderItem. Verbs-Methode</span><span class="sxs-lookup"><span data-stu-id="56c01-104">FolderItem.Verbs method</span></span>

<span data-ttu-id="56c01-105">Ruft das [**folderitemverbs**](folderitemverbs.md) -Objekt des Elements ab.</span><span class="sxs-lookup"><span data-stu-id="56c01-105">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="56c01-106">Bei diesem Objekt handelt es sich um eine Auflistung von Verben, die für das Element ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="56c01-106">This object is the collection of verbs that can be executed on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c01-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56c01-107">Syntax</span></span>


```JScript
retVal = FolderItem.Verbs()
```



## <a name="parameters"></a><span data-ttu-id="56c01-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="56c01-108">Parameters</span></span>

<span data-ttu-id="56c01-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="56c01-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56c01-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56c01-110">Return value</span></span>

<span data-ttu-id="56c01-111">Type: **[ **folderitemverbs**](folderitemverbs.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="56c01-111">Type: **[**FolderItemVerbs**](folderitemverbs.md)\*\***</span></span>

<span data-ttu-id="56c01-112">Ein Objekt Verweis auf das [**folderitemverbs**](folderitemverbs.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="56c01-112">An object reference to the [**FolderItemVerbs**](folderitemverbs.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="56c01-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56c01-113">Examples</span></span>

<span data-ttu-id="56c01-114">Im folgenden Beispiel werden **Verben** verwendet, um das [**folderitemverbs**](folderitemverbs.md) -Objekt abzurufen, das den Satz von Verben darstellt, der im Windows-Ordner ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="56c01-114">The following example uses **Verbs** to retrieve the [**FolderItemVerbs**](folderitemverbs.md) object representing the set of verbs that can be executed on the Windows folder.</span></span> <span data-ttu-id="56c01-115">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="56c01-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="56c01-116">JScript</span><span class="sxs-lookup"><span data-stu-id="56c01-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var objItemVerbs;
                
                objItemVerbs = objFolderItem.Verbs();
                if (objItemVerbs != null)
                {
                    // Add code here
                }
            }
        }
    }
</script>
```



<span data-ttu-id="56c01-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="56c01-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemVerbsVB()
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
                    dim objItemVerbs
                    
                    set objItemVerbs = objFolderItem.Verbs
                        if (not objItemVerbs is nothing) then
                            'Add code here
                        end if
                    set objItemVerbs = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="56c01-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="56c01-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemVerbsVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim objItemVerbs As FolderItemVerbs
                    
                    Set objItemVerbs = objFolderItem.Verbs
                        If (Not objItemVerbs Is Nothing) Then
                            'Add code here
                        End If
                    Set objItemVerbs = Nothing
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="56c01-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="56c01-119">Requirements</span></span>



| <span data-ttu-id="56c01-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56c01-120">Requirement</span></span> | <span data-ttu-id="56c01-121">Wert</span><span class="sxs-lookup"><span data-stu-id="56c01-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56c01-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56c01-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56c01-123">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56c01-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="56c01-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56c01-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56c01-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56c01-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="56c01-126">Header</span><span class="sxs-lookup"><span data-stu-id="56c01-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="56c01-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="56c01-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="56c01-128">IDL</span><span class="sxs-lookup"><span data-stu-id="56c01-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56c01-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56c01-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="56c01-130">DLL</span><span class="sxs-lookup"><span data-stu-id="56c01-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56c01-131"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="56c01-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56c01-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="56c01-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c01-133">**Von folderItem**</span><span class="sxs-lookup"><span data-stu-id="56c01-133">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="56c01-134">**Invokeverb**</span><span class="sxs-lookup"><span data-stu-id="56c01-134">**InvokeVerb**</span></span>](folderitem-invokeverb.md)
</dt> <dt>

[<span data-ttu-id="56c01-135">**Doit**</span><span class="sxs-lookup"><span data-stu-id="56c01-135">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




