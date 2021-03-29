---
description: Stellt alle Desktop Fenster in dem Zustand wieder her, in dem Sie sich vor dem letzten minimizeall-Befehl befanden.
ms.assetid: 32BDE544-C4FF-4a64-99AF-F8960AEC4690
title: Ishelldispatch. undominimizeall-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1b11fdd7a0a82a11baa20b0f3a63a31a8a46b701
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527332"
---
# <a name="ishelldispatchundominimizeall-method"></a><span data-ttu-id="af9e5-103">Ishelldispatch. undominimizeall-Methode</span><span class="sxs-lookup"><span data-stu-id="af9e5-103">IShellDispatch.UndoMinimizeALL method</span></span>

<span data-ttu-id="af9e5-104">Stellt alle Desktop Fenster in dem Zustand wieder her, in dem Sie sich vor dem letzten [**minimizeall**](shell-minimizeall.md) -Befehl befanden.</span><span class="sxs-lookup"><span data-stu-id="af9e5-104">Restores all desktop windows to the state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="af9e5-105">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Taskleiste und das Auswählen von " **alle Fenster minimieren** (auf älteren Systemen)" oder ein zweites klicken auf das Symbol " **Desktop anzeigen** " in der Taskleiste.</span><span class="sxs-lookup"><span data-stu-id="af9e5-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** (on older systems) or a second clicking of the **Show Desktop** icon in the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9e5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="af9e5-106">Syntax</span></span>


```JScript
IShellDispatch.UndoMinimizeALL()
```


```VB

IShellDispatch.UndoMinimizeALL()
```





## <a name="parameters"></a><span data-ttu-id="af9e5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="af9e5-107">Parameters</span></span>

<span data-ttu-id="af9e5-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="af9e5-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="af9e5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af9e5-109">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="af9e5-110">JScript</span><span class="sxs-lookup"><span data-stu-id="af9e5-110">JScript</span></span>

<span data-ttu-id="af9e5-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="af9e5-111">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="af9e5-112">VB</span><span class="sxs-lookup"><span data-stu-id="af9e5-112">VB</span></span>

<span data-ttu-id="af9e5-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="af9e5-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af9e5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af9e5-114">Remarks</span></span>

<span data-ttu-id="af9e5-115">Diese Methode ist implementiert, und der Zugriff darauf erfolgt über die [**Shell. undominimizeall**](./shell-undominimizeall.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="af9e5-115">This method is implemented and accessed through the [**Shell.UndoMinimizeAll**](./shell-undominimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="af9e5-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af9e5-116">Examples</span></span>

<span data-ttu-id="af9e5-117">In den folgenden Beispielen wird die Verwendung von **undominimizeall** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="af9e5-117">The following examples show the use of **UndoMinimizeALL** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="af9e5-118">JScript</span><span class="sxs-lookup"><span data-stu-id="af9e5-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="af9e5-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="af9e5-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="af9e5-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="af9e5-120">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="af9e5-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="af9e5-121">Requirements</span></span>



| <span data-ttu-id="af9e5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af9e5-122">Requirement</span></span> | <span data-ttu-id="af9e5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="af9e5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af9e5-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="af9e5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="af9e5-125">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af9e5-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="af9e5-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="af9e5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="af9e5-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="af9e5-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="af9e5-128">Header</span><span class="sxs-lookup"><span data-stu-id="af9e5-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="af9e5-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af9e5-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="af9e5-130">IDL</span><span class="sxs-lookup"><span data-stu-id="af9e5-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af9e5-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="af9e5-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="af9e5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="af9e5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af9e5-133"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="af9e5-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
