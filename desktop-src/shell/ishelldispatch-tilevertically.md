---
description: Kachelt alle Fenster auf dem Desktop vertikal. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und Fenster nebeneinander anzeigen auswählen.
ms.assetid: 63CB7E20-48E6-4cfe-B0BA-0D28A7B151BD
title: Ishelldispatch. tilevertikal-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 42f98ae99814495029c67d41b05e86182c6b8b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978080"
---
# <a name="ishelldispatchtilevertically-method"></a><span data-ttu-id="72c74-104">Ishelldispatch. tilevertikal-Methode</span><span class="sxs-lookup"><span data-stu-id="72c74-104">IShellDispatch.TileVertically method</span></span>

<span data-ttu-id="72c74-105">Kachelt alle Fenster auf dem Desktop vertikal.</span><span class="sxs-lookup"><span data-stu-id="72c74-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="72c74-106">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und **Fenster nebeneinander anzeigen** auswählen.</span><span class="sxs-lookup"><span data-stu-id="72c74-106">This method has the same effect as right-clicking the taskbar and selecting **Show windows side by side**.</span></span>

## <a name="syntax"></a><span data-ttu-id="72c74-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="72c74-107">Syntax</span></span>


```JScript
IShellDispatch.TileVertically()
```


```VB

IShellDispatch.TileVertically()
```





## <a name="parameters"></a><span data-ttu-id="72c74-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="72c74-108">Parameters</span></span>

<span data-ttu-id="72c74-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="72c74-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72c74-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72c74-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="72c74-111">JScript</span><span class="sxs-lookup"><span data-stu-id="72c74-111">JScript</span></span>

<span data-ttu-id="72c74-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="72c74-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="72c74-113">VB</span><span class="sxs-lookup"><span data-stu-id="72c74-113">VB</span></span>

<span data-ttu-id="72c74-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="72c74-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="72c74-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72c74-115">Remarks</span></span>

<span data-ttu-id="72c74-116">Diese Methode wird implementiert und über die [**Shell. tilevertikal**](shell-tilevertically.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="72c74-116">This method is implemented and accessed through the [**Shell.TileVertically**](shell-tilevertically.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="72c74-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72c74-117">Examples</span></span>

<span data-ttu-id="72c74-118">In den folgenden Beispielen wird die Verwendung von **tilevertikal** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="72c74-118">The following examples show the use of **TileVertically** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="72c74-119">JScript</span><span class="sxs-lookup"><span data-stu-id="72c74-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.TileVertically();
    }
</script>
```



<span data-ttu-id="72c74-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="72c74-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="72c74-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="72c74-121">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="72c74-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="72c74-122">Requirements</span></span>



| <span data-ttu-id="72c74-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72c74-123">Requirement</span></span> | <span data-ttu-id="72c74-124">Wert</span><span class="sxs-lookup"><span data-stu-id="72c74-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72c74-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72c74-125">Minimum supported client</span></span><br/> | <span data-ttu-id="72c74-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72c74-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="72c74-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72c74-127">Minimum supported server</span></span><br/> | <span data-ttu-id="72c74-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72c74-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="72c74-129">Header</span><span class="sxs-lookup"><span data-stu-id="72c74-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="72c74-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72c74-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="72c74-131">IDL</span><span class="sxs-lookup"><span data-stu-id="72c74-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72c74-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72c74-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="72c74-133">DLL</span><span class="sxs-lookup"><span data-stu-id="72c74-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72c74-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="72c74-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




