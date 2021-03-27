---
description: Der Computer wird von seiner Docking Station eingelesen. Dies ist das gleiche wie beim Klicken auf das Startmenü und beim Auswählen von ausgelösten PCs, wenn Ihr Computer diesen Befehl unterstützt.
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: Shell. ejectpc-Methode (Shldisp. h)
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
ms.openlocfilehash: 355d75b2ffaca9c9f90e66fbc535333a84bfa45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979905"
---
# <a name="shellejectpc-method"></a><span data-ttu-id="0c559-104">Shell. ejectpc-Methode</span><span class="sxs-lookup"><span data-stu-id="0c559-104">Shell.EjectPC method</span></span>

<span data-ttu-id="0c559-105">Der Computer wird von seiner Docking Station eingelesen.</span><span class="sxs-lookup"><span data-stu-id="0c559-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="0c559-106">Dies ist das gleiche wie beim Klicken auf das **Startmenü** und beim Auswählen von **ausgelösten PCs**, wenn Ihr Computer diesen Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0c559-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c559-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c559-107">Syntax</span></span>


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="0c559-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c559-108">Parameters</span></span>

<span data-ttu-id="0c559-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0c559-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c559-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c559-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0c559-111">JScript</span><span class="sxs-lookup"><span data-stu-id="0c559-111">JScript</span></span>

<span data-ttu-id="0c559-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0c559-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="0c559-113">VB</span><span class="sxs-lookup"><span data-stu-id="0c559-113">VB</span></span>

<span data-ttu-id="0c559-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0c559-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="0c559-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c559-115">Examples</span></span>

<span data-ttu-id="0c559-116">Im folgenden Beispiel wird **ejectpc** verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c559-116">The following example shows **EjectPC** in use.</span></span> <span data-ttu-id="0c559-117">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c559-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0c559-118">JScript</span><span class="sxs-lookup"><span data-stu-id="0c559-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



<span data-ttu-id="0c559-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="0c559-119">VBScript:</span></span>


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



<span data-ttu-id="0c559-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="0c559-120">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0c559-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0c559-121">Requirements</span></span>



| <span data-ttu-id="0c559-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c559-122">Requirement</span></span> | <span data-ttu-id="0c559-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0c559-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c559-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c559-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0c559-125">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c559-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0c559-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c559-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0c559-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c559-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0c559-128">Header</span><span class="sxs-lookup"><span data-stu-id="0c559-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c559-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c559-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0c559-130">IDL</span><span class="sxs-lookup"><span data-stu-id="0c559-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0c559-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c559-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0c559-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0c559-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c559-133"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="0c559-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




