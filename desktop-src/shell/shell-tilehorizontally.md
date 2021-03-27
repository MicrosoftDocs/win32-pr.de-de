---
description: Kachelt alle Fenster auf dem Desktop horizontal. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und Fenster horizontal nebeneinander auswählen.
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: Shell. tilehorizontale-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e295d0a7847afc0cb405f3ab9141e54ae424e9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216596"
---
# <a name="shelltilehorizontally-method"></a><span data-ttu-id="42a41-104">Shell. tilehorizontale-Methode</span><span class="sxs-lookup"><span data-stu-id="42a41-104">Shell.TileHorizontally method</span></span>

<span data-ttu-id="42a41-105">Kachelt alle Fenster auf dem Desktop horizontal.</span><span class="sxs-lookup"><span data-stu-id="42a41-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="42a41-106">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und **Fenster horizontal** nebeneinander auswählen.</span><span class="sxs-lookup"><span data-stu-id="42a41-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Horizontally**.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a41-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a41-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a><span data-ttu-id="42a41-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="42a41-108">Parameters</span></span>

<span data-ttu-id="42a41-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="42a41-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="42a41-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42a41-110">Examples</span></span>

<span data-ttu-id="42a41-111">Im folgenden Beispiel wird **tilehorizontin** verwendet.</span><span class="sxs-lookup"><span data-stu-id="42a41-111">The following example shows **TileHorizontally** in use.</span></span> <span data-ttu-id="42a41-112">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42a41-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="42a41-113">JScript</span><span class="sxs-lookup"><span data-stu-id="42a41-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="42a41-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="42a41-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="42a41-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="42a41-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="42a41-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="42a41-116">Requirements</span></span>



| <span data-ttu-id="42a41-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="42a41-117">Requirement</span></span> | <span data-ttu-id="42a41-118">Wert</span><span class="sxs-lookup"><span data-stu-id="42a41-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a41-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="42a41-119">Minimum supported client</span></span><br/> | <span data-ttu-id="42a41-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42a41-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="42a41-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="42a41-121">Minimum supported server</span></span><br/> | <span data-ttu-id="42a41-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="42a41-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42a41-123">Header</span><span class="sxs-lookup"><span data-stu-id="42a41-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a41-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="42a41-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="42a41-125">IDL</span><span class="sxs-lookup"><span data-stu-id="42a41-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42a41-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42a41-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="42a41-127">DLL</span><span class="sxs-lookup"><span data-stu-id="42a41-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a41-128"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="42a41-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




