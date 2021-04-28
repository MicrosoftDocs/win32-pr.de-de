---
description: 'IShellDispatch4.ToggleDesktop-Methode: Zeigt den Desktop an oder blendet diesen aus.'
title: IShellDispatch4.ToggleDesktop-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 60199e18-b8da-48a6-b316-e7f07ff44b78
ms.openlocfilehash: b635408ed8a44b8bb0d27e52c167470f80f61b18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116818"
---
# <a name="ishelldispatch4toggledesktop-method"></a><span data-ttu-id="a6063-103">IShellDispatch4.ToggleDesktop-Methode</span><span class="sxs-lookup"><span data-stu-id="a6063-103">IShellDispatch4.ToggleDesktop method</span></span>

<span data-ttu-id="a6063-104">Zeigt den Desktop an oder blendet den Desktop aus.</span><span class="sxs-lookup"><span data-stu-id="a6063-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6063-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6063-105">Syntax</span></span>


```JScript
IShellDispatch4.ToggleDesktop()
```


```VB

IShellDispatch4.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="a6063-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6063-106">Parameters</span></span>

<span data-ttu-id="a6063-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a6063-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6063-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6063-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a6063-109">JScript</span><span class="sxs-lookup"><span data-stu-id="a6063-109">JScript</span></span>

<span data-ttu-id="a6063-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a6063-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a6063-111">VB</span><span class="sxs-lookup"><span data-stu-id="a6063-111">VB</span></span>

<span data-ttu-id="a6063-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a6063-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6063-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6063-113">Remarks</span></span>

<span data-ttu-id="a6063-114">Diese Methode hat die gleiche Auswirkung wie die Schaltfläche **Desktop anzeigen** auf der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="a6063-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="a6063-115">Sie blendet entweder alle geöffneten Fenster aus, um den Desktop anzuzeigen, oder sie blendet den Desktop aus, indem alle geöffneten Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a6063-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="a6063-116">Die **ToggleDesktop-Methode** zeigt keine Benutzeroberfläche an, sie ruft lediglich die Umschaltaktion auf.</span><span class="sxs-lookup"><span data-stu-id="a6063-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="a6063-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6063-117">Examples</span></span>

<span data-ttu-id="a6063-118">Die folgenden Beispiele zeigen die ordnungsgemäße Verwendung von **ToggleDesktop** für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a6063-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a6063-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="a6063-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="a6063-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="a6063-120">VBScript:</span></span>


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



<span data-ttu-id="a6063-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a6063-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a6063-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6063-122">Requirements</span></span>



| <span data-ttu-id="a6063-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6063-123">Requirement</span></span> | <span data-ttu-id="a6063-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a6063-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6063-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6063-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a6063-126">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6063-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="a6063-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6063-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a6063-128">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6063-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a6063-129">Header</span><span class="sxs-lookup"><span data-stu-id="a6063-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6063-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a6063-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a6063-131">Idl</span><span class="sxs-lookup"><span data-stu-id="a6063-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6063-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6063-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a6063-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a6063-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6063-134"><dt>Shell32.dll (Version 6.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a6063-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




