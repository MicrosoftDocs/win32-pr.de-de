---
description: 'IShellDispatch.EjectPC-Methode: Wirft den Computer von seiner Andockstation aus. Dies entspricht dem Klicken auf die Startmenü und dem Auswählen von PC auswerfen, wenn Ihr Computer diesen Befehl unterstützt.'
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: IShellDispatch.EjectPC-Methode (Shldisp.h)
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
ms.openlocfilehash: ac42e1a4331a553a03bac3da50a187e06c90859c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086638"
---
# <a name="ishelldispatchejectpc-method"></a><span data-ttu-id="d4805-104">IShellDispatch.EjectPC-Methode</span><span class="sxs-lookup"><span data-stu-id="d4805-104">IShellDispatch.EjectPC method</span></span>

<span data-ttu-id="d4805-105">Wirft den Computer von seiner Andockstation aus.</span><span class="sxs-lookup"><span data-stu-id="d4805-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="d4805-106">Dies entspricht dem Klicken auf das **Startmenü** und der Auswahl von **PC auswerfen,** wenn Ihr Computer diesen Befehl unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4805-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4805-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4805-107">Syntax</span></span>


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="d4805-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4805-108">Parameters</span></span>

<span data-ttu-id="d4805-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d4805-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4805-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4805-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d4805-111">JScript</span><span class="sxs-lookup"><span data-stu-id="d4805-111">JScript</span></span>

<span data-ttu-id="d4805-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d4805-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="d4805-113">VB</span><span class="sxs-lookup"><span data-stu-id="d4805-113">VB</span></span>

<span data-ttu-id="d4805-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d4805-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4805-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4805-115">Remarks</span></span>

<span data-ttu-id="d4805-116">Diese Methode wird implementiert und über die [**Shell.EjectPC-Methode**](shell-ejectpc.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d4805-116">This method is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="d4805-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4805-117">Examples</span></span>

<span data-ttu-id="d4805-118">Die folgenden Beispiele zeigen die Verwendung von **EjectPC** in JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d4805-118">The following examples show the use of **EjectPC** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d4805-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="d4805-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



<span data-ttu-id="d4805-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="d4805-120">VBScript:</span></span>


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



<span data-ttu-id="d4805-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d4805-121">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d4805-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4805-122">Requirements</span></span>



| <span data-ttu-id="d4805-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4805-123">Requirement</span></span> | <span data-ttu-id="d4805-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d4805-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4805-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4805-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d4805-126">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4805-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d4805-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4805-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d4805-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4805-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d4805-129">Header</span><span class="sxs-lookup"><span data-stu-id="d4805-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4805-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="d4805-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d4805-131">Idl</span><span class="sxs-lookup"><span data-stu-id="d4805-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4805-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4805-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d4805-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d4805-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4805-134"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="d4805-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




