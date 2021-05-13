---
description: 'Shell.ToggleDesktop-Methode: Zeigt den Desktop an oder blendet den Desktop aus.'
title: Shell.ToggleDesktop-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: BD07F7F2-A588-4189-95F4-3A8E2905E8F5
ms.openlocfilehash: 472f6141b8aaed47ac05c8eaf670a0d039ce5561
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841011"
---
# <a name="shelltoggledesktop-method"></a><span data-ttu-id="c0b01-103">Shell.ToggleDesktop-Methode</span><span class="sxs-lookup"><span data-stu-id="c0b01-103">Shell.ToggleDesktop method</span></span>

<span data-ttu-id="c0b01-104">Zeigt den Desktop an oder blendet den Desktop aus.</span><span class="sxs-lookup"><span data-stu-id="c0b01-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b01-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0b01-105">Syntax</span></span>


```JScript
Shell.ToggleDesktop()
```


```VB

Shell.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="c0b01-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0b01-106">Parameters</span></span>

<span data-ttu-id="c0b01-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c0b01-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0b01-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0b01-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c0b01-109">JScript</span><span class="sxs-lookup"><span data-stu-id="c0b01-109">JScript</span></span>

<span data-ttu-id="c0b01-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c0b01-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="c0b01-111">VB</span><span class="sxs-lookup"><span data-stu-id="c0b01-111">VB</span></span>

<span data-ttu-id="c0b01-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c0b01-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0b01-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c0b01-113">Remarks</span></span>

<span data-ttu-id="c0b01-114">Diese Methode hat die gleiche Wirkung wie die **Schaltfläche Desktop** anzeigen auf der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="c0b01-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="c0b01-115">Sie blendet entweder alle geöffneten Fenster aus, um den Desktop einblenden, oder sie blendet den Desktop aus, indem alle geöffneten Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c0b01-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="c0b01-116">Die **ToggleDesktop-Methode** zeigt keine Benutzeroberfläche an, sondern ruft lediglich die Umschaltaktion auf.</span><span class="sxs-lookup"><span data-stu-id="c0b01-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="c0b01-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0b01-117">Examples</span></span>

<span data-ttu-id="c0b01-118">Die folgenden Beispiele zeigen die ordnungsgemäße Verwendung von **ToggleDesktop** für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c0b01-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c0b01-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="c0b01-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="c0b01-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="c0b01-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="c0b01-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c0b01-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c0b01-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0b01-122">Requirements</span></span>



| <span data-ttu-id="c0b01-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0b01-123">Requirement</span></span> | <span data-ttu-id="c0b01-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c0b01-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b01-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c0b01-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b01-126">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0b01-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="c0b01-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c0b01-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b01-128">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c0b01-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c0b01-129">Header</span><span class="sxs-lookup"><span data-stu-id="c0b01-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0b01-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b01-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c0b01-131">Idl</span><span class="sxs-lookup"><span data-stu-id="c0b01-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0b01-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0b01-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c0b01-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c0b01-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0b01-134"><dt>Shell32.dll (Version 6.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c0b01-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




