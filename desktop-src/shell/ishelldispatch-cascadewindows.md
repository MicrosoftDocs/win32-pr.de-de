---
description: Alle Fenster auf dem Desktop werden kaskadiert. Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und kaskadierte Fenster auswählen.
ms.assetid: 6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78
title: Ishelldispatch. cascadewindows-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4252e4df579bc73e9f082630f9f98b83e3b57f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130100"
---
# <a name="ishelldispatchcascadewindows-method"></a><span data-ttu-id="de875-104">Ishelldispatch. cascadewindows-Methode</span><span class="sxs-lookup"><span data-stu-id="de875-104">IShellDispatch.CascadeWindows method</span></span>

<span data-ttu-id="de875-105">Alle Fenster auf dem Desktop werden kaskadiert.</span><span class="sxs-lookup"><span data-stu-id="de875-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="de875-106">Diese Methode hat denselben Effekt, wenn Sie mit der rechten Maustaste auf die Taskleiste klicken und **kaskadierte Fenster** auswählen.</span><span class="sxs-lookup"><span data-stu-id="de875-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="de875-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="de875-107">Syntax</span></span>


```JScript
IShellDispatch.CascadeWindows()
```


```VB

IShellDispatch.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="de875-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de875-108">Parameters</span></span>

<span data-ttu-id="de875-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="de875-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de875-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de875-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="de875-111">JScript</span><span class="sxs-lookup"><span data-stu-id="de875-111">JScript</span></span>

<span data-ttu-id="de875-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="de875-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="de875-113">VB</span><span class="sxs-lookup"><span data-stu-id="de875-113">VB</span></span>

<span data-ttu-id="de875-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="de875-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de875-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de875-115">Remarks</span></span>

<span data-ttu-id="de875-116">Diese Methode wird implementiert und über die [**Shell. cascadewindows**](shell-cascadewindows.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="de875-116">This method is implemented and accessed through the [**Shell.CascadeWindows**](shell-cascadewindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="de875-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de875-117">Examples</span></span>

<span data-ttu-id="de875-118">In den folgenden Beispielen wird die Verwendung von **caskadetten-Fenstern** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="de875-118">The following examples show the use of **CascadeWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="de875-119">JScript</span><span class="sxs-lookup"><span data-stu-id="de875-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="de875-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="de875-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="de875-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="de875-121">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="de875-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="de875-122">Requirements</span></span>



| <span data-ttu-id="de875-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de875-123">Requirement</span></span> | <span data-ttu-id="de875-124">Wert</span><span class="sxs-lookup"><span data-stu-id="de875-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de875-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de875-125">Minimum supported client</span></span><br/> | <span data-ttu-id="de875-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de875-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="de875-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de875-127">Minimum supported server</span></span><br/> | <span data-ttu-id="de875-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de875-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="de875-129">Header</span><span class="sxs-lookup"><span data-stu-id="de875-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="de875-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de875-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="de875-131">IDL</span><span class="sxs-lookup"><span data-stu-id="de875-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de875-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="de875-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="de875-133">DLL</span><span class="sxs-lookup"><span data-stu-id="de875-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de875-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="de875-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




