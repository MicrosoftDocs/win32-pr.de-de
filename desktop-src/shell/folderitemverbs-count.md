---
description: Enthält die Anzahl der Elemente in der Auflistung.
ms.assetid: a676593b-ea78-433d-a622-221028245c3a
title: Folderitemverbs. Count-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b41e78261dfc9bc72e9262615bc395a9d559e33a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994719"
---
# <a name="folderitemverbscount-property"></a><span data-ttu-id="2797e-103">Folderitemverbs. Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2797e-103">FolderItemVerbs.Count property</span></span>

<span data-ttu-id="2797e-104">Enthält die Anzahl der Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="2797e-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="2797e-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2797e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2797e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2797e-106">Syntax</span></span>


```JScript
iCount = FolderItemVerbs.Count
```



## <a name="property-value"></a><span data-ttu-id="2797e-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2797e-107">Property value</span></span>

<span data-ttu-id="2797e-108">Eine **ganze** Zahl, die die **count** -Eigenschaft empfängt.</span><span class="sxs-lookup"><span data-stu-id="2797e-108">An **Integer** that receives the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="2797e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2797e-109">Examples</span></span>

<span data-ttu-id="2797e-110">Im folgenden Beispiel wird **count** verwendet, um die Anzahl der für den System Steuerungs Ordner verfügbaren Verben abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2797e-110">The following example uses **Count** to retrieve the count of verbs available for the Control Panel folder.</span></span> <span data-ttu-id="2797e-111">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2797e-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2797e-112">JScript</span><span class="sxs-lookup"><span data-stu-id="2797e-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);
        if (objFolder2 != null)
        {
            var objVerbs;
            
            objVerbs = objFolder2.Self.Verbs();

            if (objVerbs != null)
            {
                var nCount;
                nCount = objVerbs.Count;

                alert(nCount);
            }
        }
    }
</script>
```



<span data-ttu-id="2797e-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="2797e-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2797e-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2797e-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsCountVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2797e-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2797e-115">Requirements</span></span>



| <span data-ttu-id="2797e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2797e-116">Requirement</span></span> | <span data-ttu-id="2797e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2797e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2797e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2797e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2797e-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2797e-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2797e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2797e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2797e-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2797e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2797e-122">Header</span><span class="sxs-lookup"><span data-stu-id="2797e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2797e-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2797e-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2797e-124">IDL</span><span class="sxs-lookup"><span data-stu-id="2797e-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2797e-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2797e-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2797e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2797e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2797e-127"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="2797e-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




