---
description: Enthält die Anzahl der Elemente in der Auflistung.
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: Shellwindows. Count-Eigenschaft (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a8d5b9e605650ba7d3cb6036e8abfac58c0b8597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980713"
---
# <a name="shellwindowscount-property"></a><span data-ttu-id="dbb13-103">Shellwindows. Count (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="dbb13-103">ShellWindows.Count property</span></span>

<span data-ttu-id="dbb13-104">Enthält die Anzahl der Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="dbb13-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="dbb13-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="dbb13-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb13-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbb13-106">Syntax</span></span>


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a><span data-ttu-id="dbb13-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="dbb13-107">Property value</span></span>

<span data-ttu-id="dbb13-108">Eine **ganze** Zahl, die einen Wert für die **count** -Eigenschaft enthält.</span><span class="sxs-lookup"><span data-stu-id="dbb13-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="dbb13-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbb13-109">Examples</span></span>

<span data-ttu-id="dbb13-110">Das folgende Beispiel zeigt die **Anzahl** in Verwendung.</span><span class="sxs-lookup"><span data-stu-id="dbb13-110">The following example shows **Count** in use.</span></span> <span data-ttu-id="dbb13-111">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dbb13-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="dbb13-112">JScript</span><span class="sxs-lookup"><span data-stu-id="dbb13-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Shell_Windows();
        if (objShellWindows != null)
        {
            var nCount;
            
            nCount = objShellWindows.Count;
            alert(nCount);
        }
    }
</script>
```



<span data-ttu-id="dbb13-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="dbb13-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsCountVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim nCount
            nCount = objShellWindows.Count

            alert(nCount)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="dbb13-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dbb13-114">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsCountVB()
    Dim objShell         As Shell
    Dim objShellWindows  As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="dbb13-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dbb13-115">Requirements</span></span>



| <span data-ttu-id="dbb13-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbb13-116">Requirement</span></span> | <span data-ttu-id="dbb13-117">Wert</span><span class="sxs-lookup"><span data-stu-id="dbb13-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb13-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbb13-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dbb13-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbb13-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dbb13-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbb13-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dbb13-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbb13-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dbb13-122">Header</span><span class="sxs-lookup"><span data-stu-id="dbb13-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbb13-123"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbb13-123"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="dbb13-124">DLL</span><span class="sxs-lookup"><span data-stu-id="dbb13-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbb13-125"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="dbb13-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




