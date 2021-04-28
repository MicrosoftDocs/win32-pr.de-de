---
description: 'IShellDispatch.Explore-Methode: Öffnet einen angegebenen Ordner in einem Windows-Explorer Fenster.'
ms.assetid: DB434D02-56B2-4e8f-9E43-BBF47C7BE377
title: IShellDispatch.Explore-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e693985cf7d8d83bd5a00595c42cd4427b0ebd5b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100558"
---
# <a name="ishelldispatchexplore-method"></a><span data-ttu-id="52408-103">IShellDispatch.Explore-Methode</span><span class="sxs-lookup"><span data-stu-id="52408-103">IShellDispatch.Explore method</span></span>

<span data-ttu-id="52408-104">Öffnet einen angegebenen Ordner in einem Windows-Explorer Fenster.</span><span class="sxs-lookup"><span data-stu-id="52408-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="52408-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52408-105">Syntax</span></span>


```JScript
IShellDispatch.Explore(
  vDir
)
```


```VB

IShellDispatch.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="52408-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52408-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52408-107">*vDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="52408-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52408-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="52408-108">Type: **Variant**</span></span>

<span data-ttu-id="52408-109">Der anzuzeigende Ordner.</span><span class="sxs-lookup"><span data-stu-id="52408-109">The folder to be displayed.</span></span> <span data-ttu-id="52408-110">Dies kann eine Zeichenfolge sein, die den Pfad des Ordners oder einen der [**ShellSpecialFolderConstants-Werte angibt.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="52408-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="52408-111">Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="52408-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="52408-112">In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52408-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52408-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52408-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="52408-114">JScript</span><span class="sxs-lookup"><span data-stu-id="52408-114">JScript</span></span>

<span data-ttu-id="52408-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="52408-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="52408-116">VB</span><span class="sxs-lookup"><span data-stu-id="52408-116">VB</span></span>

<span data-ttu-id="52408-117">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="52408-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="52408-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52408-118">Remarks</span></span>

<span data-ttu-id="52408-119">Diese Methode wird implementiert und über die [**Shell.Explore-Methode**](shell-explore.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="52408-119">This method is implemented and accessed through the [**Shell.Explore**](shell-explore.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="52408-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52408-120">Examples</span></span>

<span data-ttu-id="52408-121">Die folgenden Beispiele zeigen die Verwendung von **Explore** in JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="52408-121">The following examples show the use of **Explore** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="52408-122">Jscript:</span><span class="sxs-lookup"><span data-stu-id="52408-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Explore("C:\\");
    }
</script>
```



<span data-ttu-id="52408-123">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="52408-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="52408-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="52408-124">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="52408-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52408-125">Requirements</span></span>



| <span data-ttu-id="52408-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52408-126">Requirement</span></span> | <span data-ttu-id="52408-127">Wert</span><span class="sxs-lookup"><span data-stu-id="52408-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52408-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="52408-128">Minimum supported client</span></span><br/> | <span data-ttu-id="52408-129">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52408-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="52408-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="52408-130">Minimum supported server</span></span><br/> | <span data-ttu-id="52408-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="52408-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="52408-132">Header</span><span class="sxs-lookup"><span data-stu-id="52408-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="52408-133"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="52408-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="52408-134">Idl</span><span class="sxs-lookup"><span data-stu-id="52408-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52408-135"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="52408-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="52408-136">DLL</span><span class="sxs-lookup"><span data-stu-id="52408-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52408-137"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="52408-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




