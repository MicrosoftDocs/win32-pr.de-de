---
description: Zeigt das Dialogfeld Datums-und Uhrzeit Eigenschaften an. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von Datum/Uhrzeit anpassen.
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: Shell. setTime-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b610effe87bd9e4ab33a6e8396e90f79e7bbbe9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979761"
---
# <a name="shellsettime-method"></a><span data-ttu-id="c9cde-104">Shell. setTime-Methode</span><span class="sxs-lookup"><span data-stu-id="c9cde-104">Shell.SetTime method</span></span>

<span data-ttu-id="c9cde-105">Zeigt das Dialogfeld **Datums-und Uhrzeit Eigenschaften** an.</span><span class="sxs-lookup"><span data-stu-id="c9cde-105">Displays the **Date and Time Properties** dialog box.</span></span> <span data-ttu-id="c9cde-106">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von **Datum/Uhrzeit anpassen**.</span><span class="sxs-lookup"><span data-stu-id="c9cde-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust Date/Time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cde-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9cde-107">Syntax</span></span>


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a><span data-ttu-id="c9cde-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9cde-108">Parameters</span></span>

<span data-ttu-id="c9cde-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c9cde-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="c9cde-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9cde-110">Examples</span></span>

<span data-ttu-id="c9cde-111">Im folgenden Beispiel wird die Verwendung von **setTime** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c9cde-111">The following example shows **SetTime** in use.</span></span> <span data-ttu-id="c9cde-112">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9cde-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c9cde-113">JScript</span><span class="sxs-lookup"><span data-stu-id="c9cde-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



<span data-ttu-id="c9cde-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="c9cde-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c9cde-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c9cde-115">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c9cde-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c9cde-116">Requirements</span></span>



| <span data-ttu-id="c9cde-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9cde-117">Requirement</span></span> | <span data-ttu-id="c9cde-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c9cde-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9cde-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9cde-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c9cde-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9cde-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c9cde-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9cde-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c9cde-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9cde-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c9cde-123">Header</span><span class="sxs-lookup"><span data-stu-id="c9cde-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9cde-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9cde-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c9cde-125">IDL</span><span class="sxs-lookup"><span data-stu-id="c9cde-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9cde-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9cde-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c9cde-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c9cde-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9cde-128"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c9cde-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




