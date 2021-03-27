---
description: Enthält das folderItem-Objekt des Ordners.
ms.assetid: 0964505d-4138-4444-91d4-46c707c45688
title: Folder2. Self-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Self
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f49666096f35f9871f8a3b3c141d4bc169dea0c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214302"
---
# <a name="folder2self-property"></a><span data-ttu-id="7836b-103">Folder2. Self-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7836b-103">Folder2.Self property</span></span>

<span data-ttu-id="7836b-104">Enthält das [**folderItem**](folderitem.md) -Objekt des Ordners.</span><span class="sxs-lookup"><span data-stu-id="7836b-104">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span>

<span data-ttu-id="7836b-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7836b-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7836b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7836b-106">Syntax</span></span>


```JScript
Self = Folder2.Self
```



## <a name="property-value"></a><span data-ttu-id="7836b-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7836b-107">Property value</span></span>

<span data-ttu-id="7836b-108">Das Objekt, das zu dem [**folderItem**](folderitem.md) -Objekt des Ordners ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="7836b-108">The object that evaluates to the folder's [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="7836b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7836b-109">Examples</span></span>

<span data-ttu-id="7836b-110">Im folgenden Beispiel wird **Self** verwendet, um das [**folderItem**](folderitem.md) -Element für den Ordner "C: Windows" abzurufen \\ .</span><span class="sxs-lookup"><span data-stu-id="7836b-110">The following example uses **Self** to retrieve the [**FolderItem**](folderitem.md) for the C:\\Windows folder.</span></span> <span data-ttu-id="7836b-111">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7836b-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7836b-112">JScript</span><span class="sxs-lookup"><span data-stu-id="7836b-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectSelfJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="7836b-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="7836b-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectSelfVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder2.Self

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="7836b-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7836b-114">Visual Basic:</span></span>


```VB
Private Sub btnFolder2Self_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder2.Self()

        If (Not objFolderItem Is Nothing) Then
            'Add code here.
        End If

        Set objFolderItem = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7836b-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7836b-115">Requirements</span></span>



| <span data-ttu-id="7836b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7836b-116">Requirement</span></span> | <span data-ttu-id="7836b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7836b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7836b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7836b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7836b-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7836b-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7836b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7836b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7836b-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7836b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7836b-122">Header</span><span class="sxs-lookup"><span data-stu-id="7836b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7836b-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7836b-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7836b-124">IDL</span><span class="sxs-lookup"><span data-stu-id="7836b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7836b-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7836b-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7836b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7836b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7836b-127"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7836b-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7836b-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7836b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7836b-129">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="7836b-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="7836b-130">**Ordner**</span><span class="sxs-lookup"><span data-stu-id="7836b-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




