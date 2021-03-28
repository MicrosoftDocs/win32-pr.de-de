---
description: Alle Fenster auf dem Desktop werden kaskadiert. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und kaskadierte Fenster auswählen.
ms.assetid: f73d2066-4626-455b-8ee6-f7004cc9e699
title: Shell. cascadewindows-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 751182ec53e0495021f4a6e2fad355c2c700ad66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529417"
---
# <a name="shellcascadewindows-method"></a><span data-ttu-id="bb4d9-104">Shell. cascadewindows-Methode</span><span class="sxs-lookup"><span data-stu-id="bb4d9-104">Shell.CascadeWindows method</span></span>

<span data-ttu-id="bb4d9-105">Alle Fenster auf dem Desktop werden kaskadiert.</span><span class="sxs-lookup"><span data-stu-id="bb4d9-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="bb4d9-106">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und **kaskadierte Fenster** auswählen.</span><span class="sxs-lookup"><span data-stu-id="bb4d9-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade Windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb4d9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb4d9-107">Syntax</span></span>


```JScript
Shell.CascadeWindows()
```


```VB

Shell.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="bb4d9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb4d9-108">Parameters</span></span>

<span data-ttu-id="bb4d9-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bb4d9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb4d9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb4d9-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="bb4d9-111">JScript</span><span class="sxs-lookup"><span data-stu-id="bb4d9-111">JScript</span></span>

<span data-ttu-id="bb4d9-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bb4d9-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="bb4d9-113">VB</span><span class="sxs-lookup"><span data-stu-id="bb4d9-113">VB</span></span>

<span data-ttu-id="bb4d9-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bb4d9-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="bb4d9-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bb4d9-115">Examples</span></span>

<span data-ttu-id="bb4d9-116">Im folgenden Beispiel werden **caskadetten-Fenster** verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb4d9-116">The following example shows **CascadeWindows** in use.</span></span> <span data-ttu-id="bb4d9-117">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb4d9-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bb4d9-118">JScript</span><span class="sxs-lookup"><span data-stu-id="bb4d9-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="bb4d9-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="bb4d9-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="bb4d9-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bb4d9-120">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bb4d9-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bb4d9-121">Requirements</span></span>



| <span data-ttu-id="bb4d9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb4d9-122">Requirement</span></span> | <span data-ttu-id="bb4d9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="bb4d9-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb4d9-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb4d9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bb4d9-125">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb4d9-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bb4d9-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb4d9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bb4d9-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb4d9-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb4d9-128">Header</span><span class="sxs-lookup"><span data-stu-id="bb4d9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb4d9-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb4d9-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bb4d9-130">IDL</span><span class="sxs-lookup"><span data-stu-id="bb4d9-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb4d9-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb4d9-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bb4d9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bb4d9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb4d9-133"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="bb4d9-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




