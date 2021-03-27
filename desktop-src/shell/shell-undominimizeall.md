---
description: Stellt alle Desktop Fenster in dem Zustand wieder her, in dem Sie vor dem letzten minimizeall-Befehl standen.
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: Shell. undominimizeall-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a5010e4ac6b4fca42689f7c80db50c55ab2cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216595"
---
# <a name="shellundominimizeall-method"></a><span data-ttu-id="3ae02-103">Shell. undominimizeall-Methode</span><span class="sxs-lookup"><span data-stu-id="3ae02-103">Shell.UndoMinimizeALL method</span></span>

<span data-ttu-id="3ae02-104">Stellt alle Desktop Fenster in dem Zustand wieder her, in dem Sie vor dem letzten [**minimizeall**](shell-minimizeall.md) -Befehl standen.</span><span class="sxs-lookup"><span data-stu-id="3ae02-104">Restores all desktop windows to the same state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="3ae02-105">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von "alle Fenster auf älteren Systemen **minimieren** " oder ein zweites klicken auf das Symbol " **Desktop anzeigen** " im Bereich "Schnellstart" der Taskleiste in Windows 2000 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3ae02-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** on older systems or a second clicking of the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae02-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ae02-106">Syntax</span></span>


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a><span data-ttu-id="3ae02-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ae02-107">Parameters</span></span>

<span data-ttu-id="3ae02-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3ae02-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="3ae02-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ae02-109">Examples</span></span>

<span data-ttu-id="3ae02-110">Das folgende Beispiel zeigt die Verwendung von **undominimizeall** .</span><span class="sxs-lookup"><span data-stu-id="3ae02-110">The following example shows **UndoMinimizeALL** in use.</span></span> <span data-ttu-id="3ae02-111">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3ae02-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3ae02-112">JScript</span><span class="sxs-lookup"><span data-stu-id="3ae02-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="3ae02-113">VBScript</span><span class="sxs-lookup"><span data-stu-id="3ae02-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3ae02-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3ae02-114">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3ae02-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3ae02-115">Requirements</span></span>



| <span data-ttu-id="3ae02-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3ae02-116">Requirement</span></span> | <span data-ttu-id="3ae02-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3ae02-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae02-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3ae02-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae02-119">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ae02-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3ae02-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3ae02-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae02-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3ae02-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3ae02-122">Header</span><span class="sxs-lookup"><span data-stu-id="3ae02-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ae02-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ae02-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3ae02-124">IDL</span><span class="sxs-lookup"><span data-stu-id="3ae02-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ae02-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ae02-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3ae02-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3ae02-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ae02-127"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="3ae02-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




