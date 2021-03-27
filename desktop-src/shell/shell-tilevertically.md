---
description: Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und nebeneinander Fenster nebeneinander auswählen.
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: Shell. tilevertikal-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8ecea9df2bcbb2e410841231ed7eca170872e015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980608"
---
# <a name="shelltilevertically-method"></a><span data-ttu-id="7ceee-104">Shell. tilevertikal-Methode</span><span class="sxs-lookup"><span data-stu-id="7ceee-104">Shell.TileVertically method</span></span>

<span data-ttu-id="7ceee-105">Kachelt alle Fenster auf dem Desktop vertikal.</span><span class="sxs-lookup"><span data-stu-id="7ceee-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="7ceee-106">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und nebeneinander **Fenster** nebeneinander auswählen.</span><span class="sxs-lookup"><span data-stu-id="7ceee-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Vertically**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ceee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ceee-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileVertically()
```


```VB

Shell.TileVertically() As Integer
```





## <a name="parameters"></a><span data-ttu-id="7ceee-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ceee-108">Parameters</span></span>

<span data-ttu-id="7ceee-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7ceee-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="7ceee-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ceee-110">Examples</span></span>

<span data-ttu-id="7ceee-111">Im folgenden Beispiel wird **tilevertikal** verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ceee-111">The following example shows **TileVertically** in use.</span></span> <span data-ttu-id="7ceee-112">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7ceee-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7ceee-113">JScript</span><span class="sxs-lookup"><span data-stu-id="7ceee-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



<span data-ttu-id="7ceee-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="7ceee-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7ceee-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7ceee-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7ceee-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7ceee-116">Requirements</span></span>



| <span data-ttu-id="7ceee-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ceee-117">Requirement</span></span> | <span data-ttu-id="7ceee-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7ceee-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ceee-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ceee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7ceee-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ceee-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7ceee-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ceee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7ceee-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7ceee-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7ceee-123">Header</span><span class="sxs-lookup"><span data-stu-id="7ceee-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ceee-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ceee-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7ceee-125">IDL</span><span class="sxs-lookup"><span data-stu-id="7ceee-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ceee-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ceee-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7ceee-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7ceee-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ceee-128"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7ceee-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




