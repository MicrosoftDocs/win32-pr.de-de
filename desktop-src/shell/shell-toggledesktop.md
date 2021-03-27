---
description: Zeigt den Desktop an oder blendet ihn aus.
title: Shell. deggledesktop-Methode (Shldisp. h)
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
ms.openlocfilehash: 888723aeba8bd54c6ada659022286e4825e4067d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757356"
---
# <a name="shelltoggledesktop-method"></a><span data-ttu-id="1e073-103">Shell. deggledesktop-Methode</span><span class="sxs-lookup"><span data-stu-id="1e073-103">Shell.ToggleDesktop method</span></span>

<span data-ttu-id="1e073-104">Zeigt den Desktop an oder blendet ihn aus.</span><span class="sxs-lookup"><span data-stu-id="1e073-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e073-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e073-105">Syntax</span></span>


```JScript
Shell.ToggleDesktop()
```


```VB

Shell.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="1e073-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e073-106">Parameters</span></span>

<span data-ttu-id="1e073-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1e073-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e073-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e073-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1e073-109">JScript</span><span class="sxs-lookup"><span data-stu-id="1e073-109">JScript</span></span>

<span data-ttu-id="1e073-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1e073-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="1e073-111">VB</span><span class="sxs-lookup"><span data-stu-id="1e073-111">VB</span></span>

<span data-ttu-id="1e073-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1e073-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e073-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e073-113">Remarks</span></span>

<span data-ttu-id="1e073-114">Diese Methode hat dieselbe Auswirkung wie die Schaltfläche **Desktop anzeigen** auf der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="1e073-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="1e073-115">Entweder werden alle geöffneten Fenster ausgeblendet, damit der Desktop angezeigt wird, oder es wird der Desktop ausgeblendet, indem alle geöffneten Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1e073-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="1e073-116">Die Methode " **deggledesktop** " zeigt keine Benutzeroberfläche an, sondern ruft lediglich die UMSCHALT Aktion auf.</span><span class="sxs-lookup"><span data-stu-id="1e073-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="1e073-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e073-117">Examples</span></span>

<span data-ttu-id="1e073-118">Die folgenden Beispiele zeigen die ordnungsgemäße Verwendung von " **deggledesktop** " für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1e073-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1e073-119">JScript</span><span class="sxs-lookup"><span data-stu-id="1e073-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="1e073-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="1e073-120">VBScript:</span></span>


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



<span data-ttu-id="1e073-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1e073-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1e073-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1e073-122">Requirements</span></span>



| <span data-ttu-id="1e073-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e073-123">Requirement</span></span> | <span data-ttu-id="1e073-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1e073-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e073-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e073-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1e073-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e073-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="1e073-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e073-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1e073-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e073-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1e073-129">Header</span><span class="sxs-lookup"><span data-stu-id="1e073-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e073-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e073-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1e073-131">IDL</span><span class="sxs-lookup"><span data-stu-id="1e073-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e073-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e073-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1e073-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1e073-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e073-134"><dt>Shell32.dll (Version 6,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1e073-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




