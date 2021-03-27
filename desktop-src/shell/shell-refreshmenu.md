---
description: Aktualisiert den Inhalt des Start Menüs. Wird nur mit Systemen vor Windows XP verwendet.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Shell. erfrischend Menu-Methode (Shldisp. h)
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
ms.openlocfilehash: a5812312c846026f4e0c7d2a4f6a5f857a572a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979768"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="6aca1-104">Shell. erfrischend Menu-Methode</span><span class="sxs-lookup"><span data-stu-id="6aca1-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="6aca1-105">Aktualisiert den Inhalt des **Start** Menüs.</span><span class="sxs-lookup"><span data-stu-id="6aca1-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="6aca1-106">Wird nur mit Systemen vor Windows XP verwendet.</span><span class="sxs-lookup"><span data-stu-id="6aca1-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aca1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6aca1-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="6aca1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6aca1-108">Parameters</span></span>

<span data-ttu-id="6aca1-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6aca1-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="6aca1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6aca1-110">Remarks</span></span>

<span data-ttu-id="6aca1-111">Die Funktionalität, die das Aktualitäts **Menü** bereitstellt, wird automatisch unter Windows XP oder höher behandelt.</span><span class="sxs-lookup"><span data-stu-id="6aca1-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="6aca1-112">Diese Methode darf nicht unter diesem Betriebssystem aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6aca1-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="6aca1-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6aca1-113">Examples</span></span>

<span data-ttu-id="6aca1-114">Das folgende Beispiel zeigt das verwendete **aktumenü "erfrischendes Menü** ".</span><span class="sxs-lookup"><span data-stu-id="6aca1-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="6aca1-115">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6aca1-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6aca1-116">JScript</span><span class="sxs-lookup"><span data-stu-id="6aca1-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="6aca1-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="6aca1-117">VBScript:</span></span>


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



<span data-ttu-id="6aca1-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6aca1-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6aca1-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="6aca1-119">Requirements</span></span>



| <span data-ttu-id="6aca1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6aca1-120">Requirement</span></span> | <span data-ttu-id="6aca1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6aca1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aca1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6aca1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6aca1-123">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6aca1-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6aca1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6aca1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6aca1-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6aca1-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6aca1-126">Header</span><span class="sxs-lookup"><span data-stu-id="6aca1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6aca1-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aca1-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6aca1-128">IDL</span><span class="sxs-lookup"><span data-stu-id="6aca1-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6aca1-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6aca1-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6aca1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6aca1-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aca1-131"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="6aca1-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




