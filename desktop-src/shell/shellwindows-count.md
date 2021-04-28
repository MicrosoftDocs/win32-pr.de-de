---
description: 'ShellWindows.Count-Eigenschaft: Enthält die Anzahl der Elemente in der Auflistung.'
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: ShellWindows.Count-Eigenschaft (Exdisp.h)
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
ms.openlocfilehash: b2b33dc11e6bf909043ac5391965e1ebd225d376
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103938"
---
# <a name="shellwindowscount-property"></a><span data-ttu-id="8b174-103">ShellWindows.Count-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8b174-103">ShellWindows.Count property</span></span>

<span data-ttu-id="8b174-104">Enthält die Anzahl der Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="8b174-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="8b174-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8b174-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b174-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b174-106">Syntax</span></span>


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a><span data-ttu-id="8b174-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8b174-107">Property value</span></span>

<span data-ttu-id="8b174-108">Eine **ganze Zahl,** die einen Wert für die **Count-Eigenschaft** enthält.</span><span class="sxs-lookup"><span data-stu-id="8b174-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="8b174-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b174-109">Examples</span></span>

<span data-ttu-id="8b174-110">Im folgenden Beispiel wird Count in use **(Anzahl** in Verwendung) gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b174-110">The following example shows **Count** in use.</span></span> <span data-ttu-id="8b174-111">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b174-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8b174-112">Jscript:</span><span class="sxs-lookup"><span data-stu-id="8b174-112">JScript:</span></span>


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



<span data-ttu-id="8b174-113">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="8b174-113">VBScript:</span></span>


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



<span data-ttu-id="8b174-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8b174-114">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8b174-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b174-115">Requirements</span></span>



| <span data-ttu-id="8b174-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b174-116">Requirement</span></span> | <span data-ttu-id="8b174-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8b174-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b174-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b174-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8b174-119">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b174-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8b174-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b174-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8b174-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b174-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8b174-122">Header</span><span class="sxs-lookup"><span data-stu-id="8b174-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b174-123"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="8b174-123"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="8b174-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8b174-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b174-125"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="8b174-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




