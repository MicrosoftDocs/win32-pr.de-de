---
description: Öffnet einen angegebenen Ordner in einem Windows-Explorer-Fenster.
ms.assetid: a788a3c4-f316-4fae-9294-3872eee8f46a
title: Shell. explore-Methode (Shldisp. h)
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
ms.openlocfilehash: 00b597aea0121e5f87f51886e8019a1130a20584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960511"
---
# <a name="shellexplore-method"></a><span data-ttu-id="337d5-103">Shell. explore-Methode</span><span class="sxs-lookup"><span data-stu-id="337d5-103">Shell.Explore method</span></span>

<span data-ttu-id="337d5-104">Öffnet einen angegebenen Ordner in einem Windows-Explorer-Fenster.</span><span class="sxs-lookup"><span data-stu-id="337d5-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="337d5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="337d5-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="337d5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="337d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="337d5-107">*vdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="337d5-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="337d5-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="337d5-108">Type: **Variant**</span></span>

<span data-ttu-id="337d5-109">Der Ordner, der angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="337d5-109">The folder to be displayed.</span></span> <span data-ttu-id="337d5-110">Dabei kann es sich um eine Zeichenfolge handeln, die den Pfad des Ordners oder einen der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="337d5-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="337d5-111">Beachten Sie, dass die in **shellspecialfolderconstants** gefundenen Konstanten Namen in Visual Basic verfügbar sind, jedoch nicht in VBScript oder JScript.</span><span class="sxs-lookup"><span data-stu-id="337d5-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="337d5-112">In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="337d5-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="337d5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="337d5-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="337d5-114">JScript</span><span class="sxs-lookup"><span data-stu-id="337d5-114">JScript</span></span>

<span data-ttu-id="337d5-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="337d5-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="337d5-116">VB</span><span class="sxs-lookup"><span data-stu-id="337d5-116">VB</span></span>

<span data-ttu-id="337d5-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="337d5-117">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="337d5-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="337d5-118">Examples</span></span>

<span data-ttu-id="337d5-119">Das folgende **Beispiel zeigt die** Verwendung von "in Verwendung".</span><span class="sxs-lookup"><span data-stu-id="337d5-119">The following example shows **Explore** in use.</span></span> <span data-ttu-id="337d5-120">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="337d5-120">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="337d5-121">JScript</span><span class="sxs-lookup"><span data-stu-id="337d5-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



<span data-ttu-id="337d5-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="337d5-122">VBScript:</span></span>


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



<span data-ttu-id="337d5-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="337d5-123">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="337d5-124">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="337d5-124">Requirements</span></span>



| <span data-ttu-id="337d5-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="337d5-125">Requirement</span></span> | <span data-ttu-id="337d5-126">Wert</span><span class="sxs-lookup"><span data-stu-id="337d5-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="337d5-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="337d5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="337d5-128">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="337d5-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="337d5-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="337d5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="337d5-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="337d5-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="337d5-131">Header</span><span class="sxs-lookup"><span data-stu-id="337d5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="337d5-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="337d5-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="337d5-133">IDL</span><span class="sxs-lookup"><span data-stu-id="337d5-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="337d5-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="337d5-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="337d5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="337d5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="337d5-136"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="337d5-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




