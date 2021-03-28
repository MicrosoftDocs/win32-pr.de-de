---
description: Der Computer wird von seiner Docking Station eingelesen. Dies ist das gleiche wie beim Klicken auf das Startmenü und beim Auswählen von ausgelösten PCs, wenn Ihr Computer diesen Befehl unterstützt.
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: Ishelldispatch. ejectpc-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d85dd8c007338dca3d68183bc9ba3fbd333195ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214874"
---
# <a name="ishelldispatchejectpc-method"></a><span data-ttu-id="b585d-104">Ishelldispatch. ejectpc-Methode</span><span class="sxs-lookup"><span data-stu-id="b585d-104">IShellDispatch.EjectPC method</span></span>

<span data-ttu-id="b585d-105">Der Computer wird von seiner Docking Station eingelesen.</span><span class="sxs-lookup"><span data-stu-id="b585d-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="b585d-106">Dies ist das gleiche wie beim Klicken auf das **Startmenü** und beim Auswählen von **ausgelösten PCs**, wenn Ihr Computer diesen Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b585d-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="b585d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b585d-107">Syntax</span></span>


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="b585d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b585d-108">Parameters</span></span>

<span data-ttu-id="b585d-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b585d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b585d-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b585d-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b585d-111">JScript</span><span class="sxs-lookup"><span data-stu-id="b585d-111">JScript</span></span>

<span data-ttu-id="b585d-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b585d-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b585d-113">VB</span><span class="sxs-lookup"><span data-stu-id="b585d-113">VB</span></span>

<span data-ttu-id="b585d-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b585d-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b585d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b585d-115">Remarks</span></span>

<span data-ttu-id="b585d-116">Diese Methode wird implementiert und über die [**Shell. ejectpc**](shell-ejectpc.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b585d-116">This method is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b585d-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b585d-117">Examples</span></span>

<span data-ttu-id="b585d-118">In den folgenden Beispielen wird die Verwendung von **ejectpc** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b585d-118">The following examples show the use of **EjectPC** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b585d-119">JScript</span><span class="sxs-lookup"><span data-stu-id="b585d-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



<span data-ttu-id="b585d-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="b585d-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="b585d-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b585d-121">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b585d-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b585d-122">Requirements</span></span>



| <span data-ttu-id="b585d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b585d-123">Requirement</span></span> | <span data-ttu-id="b585d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b585d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b585d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b585d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b585d-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b585d-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b585d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b585d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b585d-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b585d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b585d-129">Header</span><span class="sxs-lookup"><span data-stu-id="b585d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="b585d-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b585d-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b585d-131">IDL</span><span class="sxs-lookup"><span data-stu-id="b585d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b585d-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b585d-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b585d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b585d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b585d-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="b585d-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




