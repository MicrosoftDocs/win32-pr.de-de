---
description: 'Shell.Explore-Methode: Öffnet einen angegebenen Ordner in einem Windows-Explorer Fenster.'
ms.assetid: a788a3c4-f316-4fae-9294-3872eee8f46a
title: Shell.Explore-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9ec1756ad6743c5bbac36f56087e6f3820cbb624
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104328"
---
# <a name="shellexplore-method"></a><span data-ttu-id="8c47d-103">Shell.Explore-Methode</span><span class="sxs-lookup"><span data-stu-id="8c47d-103">Shell.Explore method</span></span>

<span data-ttu-id="8c47d-104">Öffnet einen angegebenen Ordner in einem Windows-Explorer Fenster.</span><span class="sxs-lookup"><span data-stu-id="8c47d-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c47d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c47d-105">Syntax</span></span>


```JScript
Shell.Explore(
  vDir
)
```


```VB

Shell.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="8c47d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c47d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c47d-107">*vDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8c47d-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c47d-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="8c47d-108">Type: **Variant**</span></span>

<span data-ttu-id="8c47d-109">Der anzuzeigende Ordner.</span><span class="sxs-lookup"><span data-stu-id="8c47d-109">The folder to be displayed.</span></span> <span data-ttu-id="8c47d-110">Dies kann eine Zeichenfolge sein, die den Pfad des Ordners oder einen der [**ShellSpecialFolderConstants-Werte**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) angibt.</span><span class="sxs-lookup"><span data-stu-id="8c47d-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="8c47d-111">Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8c47d-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="8c47d-112">In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c47d-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c47d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8c47d-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="8c47d-114">JScript</span><span class="sxs-lookup"><span data-stu-id="8c47d-114">JScript</span></span>

<span data-ttu-id="8c47d-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8c47d-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="8c47d-116">VB</span><span class="sxs-lookup"><span data-stu-id="8c47d-116">VB</span></span>

<span data-ttu-id="8c47d-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8c47d-117">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="8c47d-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c47d-118">Examples</span></span>

<span data-ttu-id="8c47d-119">Das folgende Beispiel zeigt **Explore** in use (In Verwendung untersuchen).</span><span class="sxs-lookup"><span data-stu-id="8c47d-119">The following example shows **Explore** in use.</span></span> <span data-ttu-id="8c47d-120">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c47d-120">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8c47d-121">Jscript:</span><span class="sxs-lookup"><span data-stu-id="8c47d-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



<span data-ttu-id="8c47d-122">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="8c47d-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="8c47d-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8c47d-123">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8c47d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c47d-124">Requirements</span></span>



| <span data-ttu-id="8c47d-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c47d-125">Requirement</span></span> | <span data-ttu-id="8c47d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8c47d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c47d-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c47d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8c47d-128">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c47d-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8c47d-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c47d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8c47d-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c47d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8c47d-131">Header</span><span class="sxs-lookup"><span data-stu-id="8c47d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c47d-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="8c47d-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8c47d-133">Idl</span><span class="sxs-lookup"><span data-stu-id="8c47d-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8c47d-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="8c47d-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8c47d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8c47d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c47d-136"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="8c47d-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




