---
description: Ruft ein-Objekt ab, das das übergeordnete Element des Elements darstellt.
ms.assetid: 612e76d8-d8bc-419c-b319-75b1f324840a
title: FolderItem. Parent-Eigenschaft (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f2da3504596c3b351318b33c929dad3b5a958165
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749161"
---
# <a name="folderitemparent-property"></a><span data-ttu-id="7ba67-103">FolderItem. Parent (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7ba67-103">FolderItem.Parent property</span></span>

<span data-ttu-id="7ba67-104">Ruft ein-Objekt ab, das das übergeordnete Element des Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="7ba67-104">Gets an object that represents the parent of the item.</span></span>

<span data-ttu-id="7ba67-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7ba67-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba67-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ba67-106">Syntax</span></span>


```JScript
objParent = FolderItem.Parent
```



## <a name="property-value"></a><span data-ttu-id="7ba67-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7ba67-107">Property value</span></span>

<span data-ttu-id="7ba67-108">Eine Variable vom Typ [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , die das übergeordnete Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="7ba67-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the parent object.</span></span>

## <a name="examples"></a><span data-ttu-id="7ba67-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ba67-109">Examples</span></span>

<span data-ttu-id="7ba67-110">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung des über **geordneten** Elements für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7ba67-110">The following example shows the proper use of **Parent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7ba67-111">JScript</span><span class="sxs-lookup"><span data-stu-id="7ba67-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



<span data-ttu-id="7ba67-112">VBScript</span><span class="sxs-lookup"><span data-stu-id="7ba67-112">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnFolderItemParentVB()
        dim objShell
        dim objFolder2
        dim ssfWINDOWS

        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem

                set objFolderItem = objFolder2.Self
                    if (not objFolderItem is nothing) then
                        dim objParent

                        set objParent = objFolderItem.Parent
                            if (not objParent is nothing) then
                                alert("Got parent object")
                            end if
                        set objParent = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder2 = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7ba67-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7ba67-113">Visual Basic:</span></span>


```VB
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



## <a name="requirements"></a><span data-ttu-id="7ba67-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7ba67-114">Requirements</span></span>



| <span data-ttu-id="7ba67-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ba67-115">Requirement</span></span> | <span data-ttu-id="7ba67-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba67-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba67-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ba67-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba67-118">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ba67-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7ba67-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ba67-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba67-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ba67-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7ba67-121">Header</span><span class="sxs-lookup"><span data-stu-id="7ba67-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ba67-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ba67-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7ba67-123">IDL</span><span class="sxs-lookup"><span data-stu-id="7ba67-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ba67-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ba67-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7ba67-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7ba67-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ba67-126"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7ba67-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
