---
description: Minimiert alle Fenster auf dem Desktop. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen der Option alle Fenster auf älteren Systemen minimieren oder klicken auf das Symbol Desktop anzeigen auf der Taskleiste.
ms.assetid: 25DD56B0-221E-44a2-9FAD-FB358ADD7FF1
title: Ishelldispatch. minimizeall-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b8b8f20ab82a6216a03d772151f852fd9c69b917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527341"
---
# <a name="ishelldispatchminimizeall-method"></a><span data-ttu-id="1798f-104">Ishelldispatch. minimizeall-Methode</span><span class="sxs-lookup"><span data-stu-id="1798f-104">IShellDispatch.MinimizeAll method</span></span>

<span data-ttu-id="1798f-105">Minimiert alle Fenster auf dem Desktop.</span><span class="sxs-lookup"><span data-stu-id="1798f-105">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="1798f-106">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen der Option alle Fenster auf älteren Systemen **minimieren** oder klicken auf das Symbol **Desktop anzeigen** auf der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="1798f-106">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon on the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="1798f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1798f-107">Syntax</span></span>


```JScript
IShellDispatch.MinimizeAll()
```


```VB

IShellDispatch.MinimizeAll()
```





## <a name="parameters"></a><span data-ttu-id="1798f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1798f-108">Parameters</span></span>

<span data-ttu-id="1798f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1798f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1798f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1798f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1798f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="1798f-111">JScript</span></span>

<span data-ttu-id="1798f-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1798f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="1798f-113">VB</span><span class="sxs-lookup"><span data-stu-id="1798f-113">VB</span></span>

<span data-ttu-id="1798f-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1798f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1798f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1798f-115">Remarks</span></span>

<span data-ttu-id="1798f-116">Diese Methode wird implementiert, und der Zugriff erfolgt über die [**Shell. minimizeall**](shell-minimizeall.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1798f-116">This method is implemented and accessed through the [**Shell.MinimizeAll**](shell-minimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="1798f-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1798f-117">Examples</span></span>

<span data-ttu-id="1798f-118">In den folgenden Beispielen wird die Verwendung von **minimizeall** für JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1798f-118">The following examples show the use of **MinimizeAll** in use for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1798f-119">JScript</span><span class="sxs-lookup"><span data-stu-id="1798f-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="1798f-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="1798f-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1798f-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1798f-121">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1798f-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1798f-122">Requirements</span></span>



| <span data-ttu-id="1798f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1798f-123">Requirement</span></span> | <span data-ttu-id="1798f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1798f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1798f-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1798f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1798f-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1798f-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1798f-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1798f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1798f-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1798f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1798f-129">Header</span><span class="sxs-lookup"><span data-stu-id="1798f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1798f-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1798f-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1798f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="1798f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1798f-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1798f-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1798f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1798f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1798f-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1798f-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1798f-135">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1798f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1798f-136">**Ishelldispatch**</span><span class="sxs-lookup"><span data-stu-id="1798f-136">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="1798f-137">**Undominimizeall**</span><span class="sxs-lookup"><span data-stu-id="1798f-137">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




