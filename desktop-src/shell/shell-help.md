---
description: Zeigt das Windows-Hilfe-und Support Center an. Diese Methode hat denselben Effekt wie das Klicken auf das Startmenü und das Auswählen von Hilfe und Support.
ms.assetid: fc13fef8-dac8-4c59-936d-8da0e63e06d4
title: Shell. Help-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bfb4e9b3272355c41d13526d2e526515ff65d42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216066"
---
# <a name="shellhelp-method"></a><span data-ttu-id="b5116-104">Shell. Help-Methode</span><span class="sxs-lookup"><span data-stu-id="b5116-104">Shell.Help method</span></span>

<span data-ttu-id="b5116-105">Zeigt das Windows-Hilfe-und Support Center an.</span><span class="sxs-lookup"><span data-stu-id="b5116-105">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="b5116-106">Diese Methode hat denselben Effekt wie das Klicken auf das **Startmenü** und das Auswählen von **Hilfe und Support**.</span><span class="sxs-lookup"><span data-stu-id="b5116-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5116-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5116-107">Syntax</span></span>


```JScript
Shell.Help()
```


```VB

Shell.Help()
```





## <a name="parameters"></a><span data-ttu-id="b5116-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5116-108">Parameters</span></span>

<span data-ttu-id="b5116-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b5116-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b5116-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b5116-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b5116-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b5116-111">JScript</span></span>

<span data-ttu-id="b5116-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b5116-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b5116-113">VB</span><span class="sxs-lookup"><span data-stu-id="b5116-113">VB</span></span>

<span data-ttu-id="b5116-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b5116-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="b5116-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5116-115">Examples</span></span>

<span data-ttu-id="b5116-116">Das folgende Beispiel zeigt die verwendete **Hilfe** .</span><span class="sxs-lookup"><span data-stu-id="b5116-116">The following example shows **Help** in use.</span></span> <span data-ttu-id="b5116-117">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b5116-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b5116-118">JScript</span><span class="sxs-lookup"><span data-stu-id="b5116-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Help();
    }
</script>
```



<span data-ttu-id="b5116-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="b5116-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b5116-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b5116-120">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b5116-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b5116-121">Requirements</span></span>



| <span data-ttu-id="b5116-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5116-122">Requirement</span></span> | <span data-ttu-id="b5116-123">Wert</span><span class="sxs-lookup"><span data-stu-id="b5116-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5116-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5116-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b5116-125">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5116-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b5116-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5116-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b5116-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b5116-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b5116-128">Header</span><span class="sxs-lookup"><span data-stu-id="b5116-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5116-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5116-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b5116-130">IDL</span><span class="sxs-lookup"><span data-stu-id="b5116-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b5116-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b5116-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b5116-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b5116-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5116-133"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b5116-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




