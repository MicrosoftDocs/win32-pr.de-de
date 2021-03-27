---
description: Minimiert alle Fenster auf dem Desktop.
ms.assetid: 3af98a16-27d1-4c93-ac72-7c9e24e68c23
title: Shell. minimizeall-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 55b615cfed8813f5567b13d58648fef36aaedda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980624"
---
# <a name="shellminimizeall-method"></a><span data-ttu-id="2c8f2-103">Shell. minimizeall-Methode</span><span class="sxs-lookup"><span data-stu-id="2c8f2-103">Shell.MinimizeAll method</span></span>

<span data-ttu-id="2c8f2-104">Minimiert alle Fenster auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-104">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="2c8f2-105">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von "alle Fenster auf älteren Systemen **minimieren** " oder das Klicken auf das Symbol " **Desktop anzeigen** " im Bereich "Schnellstart" der Taskleiste in Windows 2000 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-105">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8f2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c8f2-106">Syntax</span></span>


```JScript
iRetVal = Shell.MinimizeAll()
```


```VB

Shell.MinimizeAll() As Integer
```





## <a name="parameters"></a><span data-ttu-id="2c8f2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c8f2-107">Parameters</span></span>

<span data-ttu-id="2c8f2-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="2c8f2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c8f2-109">Examples</span></span>

<span data-ttu-id="2c8f2-110">Das folgende Beispiel zeigt **minimizeall** in Verwendung.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-110">The following example shows **MinimizeAll** in use.</span></span> <span data-ttu-id="2c8f2-111">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2c8f2-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2c8f2-112">JScript</span><span class="sxs-lookup"><span data-stu-id="2c8f2-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="2c8f2-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="2c8f2-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="2c8f2-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2c8f2-114">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2c8f2-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="2c8f2-115">Requirements</span></span>



| <span data-ttu-id="2c8f2-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c8f2-116">Requirement</span></span> | <span data-ttu-id="2c8f2-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2c8f2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8f2-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c8f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8f2-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c8f2-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2c8f2-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c8f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8f2-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c8f2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2c8f2-122">Header</span><span class="sxs-lookup"><span data-stu-id="2c8f2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c8f2-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c8f2-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2c8f2-124">IDL</span><span class="sxs-lookup"><span data-stu-id="2c8f2-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c8f2-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c8f2-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2c8f2-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2c8f2-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c8f2-127"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="2c8f2-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8f2-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2c8f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8f2-129">**Shell**</span><span class="sxs-lookup"><span data-stu-id="2c8f2-129">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="2c8f2-130">**Undominimizeall**</span><span class="sxs-lookup"><span data-stu-id="2c8f2-130">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




