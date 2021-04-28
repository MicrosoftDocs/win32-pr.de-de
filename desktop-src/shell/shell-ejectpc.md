---
description: 'Shell.EjectPC-Methode: Wirft den Computer aus seiner Andockstation aus. Dies entspricht dem Klicken auf das Startmenü und dem Auswählen von Eject PC, wenn Ihr Computer diesen Befehl unterstützt.'
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: Shell.EjectPC-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5ec08aaa82d2f752fa06537434adede86b9d5a3a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104348"
---
# <a name="shellejectpc-method"></a><span data-ttu-id="f6e9a-104">Shell.EjectPC-Methode</span><span class="sxs-lookup"><span data-stu-id="f6e9a-104">Shell.EjectPC method</span></span>

<span data-ttu-id="f6e9a-105">Wirft den Computer aus seiner Andockstation.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="f6e9a-106">Dies entspricht dem Klicken auf das **Startmenü** und dem Auswählen von **Eject PC**, wenn Ihr Computer diesen Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e9a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6e9a-107">Syntax</span></span>


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="f6e9a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6e9a-108">Parameters</span></span>

<span data-ttu-id="f6e9a-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6e9a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6e9a-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f6e9a-111">JScript</span><span class="sxs-lookup"><span data-stu-id="f6e9a-111">JScript</span></span>

<span data-ttu-id="f6e9a-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f6e9a-113">VB</span><span class="sxs-lookup"><span data-stu-id="f6e9a-113">VB</span></span>

<span data-ttu-id="f6e9a-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="f6e9a-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6e9a-115">Examples</span></span>

<span data-ttu-id="f6e9a-116">Im folgenden Beispiel wird **EjectPC** verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-116">The following example shows **EjectPC** in use.</span></span> <span data-ttu-id="f6e9a-117">Die richtige Verwendung wird für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f6e9a-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f6e9a-118">Jscript:</span><span class="sxs-lookup"><span data-stu-id="f6e9a-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



<span data-ttu-id="f6e9a-119">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="f6e9a-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f6e9a-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f6e9a-120">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f6e9a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6e9a-121">Requirements</span></span>



| <span data-ttu-id="f6e9a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6e9a-122">Requirement</span></span> | <span data-ttu-id="f6e9a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f6e9a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e9a-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6e9a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f6e9a-125">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6e9a-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f6e9a-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6e9a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f6e9a-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f6e9a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f6e9a-128">Header</span><span class="sxs-lookup"><span data-stu-id="f6e9a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6e9a-129"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f6e9a-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f6e9a-130">Idl</span><span class="sxs-lookup"><span data-stu-id="f6e9a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6e9a-131"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6e9a-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f6e9a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f6e9a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6e9a-133"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="f6e9a-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




