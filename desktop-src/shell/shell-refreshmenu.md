---
description: Erfahren Sie mehr über die Shell.RefreshMenu-Methode, die den Inhalt des Startmenü. Wird nur mit Systemen vor Windows XP verwendet.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Shell.RefreshMenu-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 90020cd128f5cbc585bd7bc9ab33a8a81c745f8e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404533"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="bf7a8-104">Shell.RefreshMenu-Methode</span><span class="sxs-lookup"><span data-stu-id="bf7a8-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="bf7a8-105">Aktualisiert den Inhalt des **Startmenüs.**</span><span class="sxs-lookup"><span data-stu-id="bf7a8-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="bf7a8-106">Wird nur mit Systemen vor Windows XP verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf7a8-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7a8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf7a8-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="bf7a8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf7a8-108">Parameters</span></span>

<span data-ttu-id="bf7a8-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bf7a8-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf7a8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf7a8-110">Remarks</span></span>

<span data-ttu-id="bf7a8-111">Die von **RefreshMenu** zur Verfügung stellten Funktionen werden unter Windows XP oder höher automatisch verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="bf7a8-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="bf7a8-112">Rufen Sie diese Methode unter diesem Betriebssystem nicht auf.</span><span class="sxs-lookup"><span data-stu-id="bf7a8-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="bf7a8-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bf7a8-113">Examples</span></span>

<span data-ttu-id="bf7a8-114">Im folgenden Beispiel wird **RefreshMenu** verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf7a8-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="bf7a8-115">Die richtige Verwendung wird für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bf7a8-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bf7a8-116">Jscript:</span><span class="sxs-lookup"><span data-stu-id="bf7a8-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="bf7a8-117">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="bf7a8-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="bf7a8-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bf7a8-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bf7a8-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bf7a8-119">Requirements</span></span>



| <span data-ttu-id="bf7a8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf7a8-120">Requirement</span></span> | <span data-ttu-id="bf7a8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bf7a8-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7a8-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf7a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7a8-123">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf7a8-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bf7a8-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf7a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7a8-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf7a8-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bf7a8-126">Header</span><span class="sxs-lookup"><span data-stu-id="bf7a8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf7a8-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="bf7a8-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bf7a8-128">Idl</span><span class="sxs-lookup"><span data-stu-id="bf7a8-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bf7a8-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="bf7a8-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bf7a8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bf7a8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf7a8-131"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="bf7a8-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




