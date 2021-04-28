---
description: 'IShellDispatch.ShutdownWindows-Methode: Zeigt das Dialogfeld Windows herunterfahren an. Dies ist identisch mit dem Klicken auf das Startmenü und dem Auswählen von Herunterfahren.'
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
title: IShellDispatch.ShutdownWindows-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5146e17d17ba0f082ad2d80f91ae05c176cf44ed
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100468"
---
# <a name="ishelldispatchshutdownwindows-method"></a><span data-ttu-id="50fdb-104">IShellDispatch.ShutdownWindows-Methode</span><span class="sxs-lookup"><span data-stu-id="50fdb-104">IShellDispatch.ShutdownWindows method</span></span>

<span data-ttu-id="50fdb-105">Zeigt das **Dialogfeld Windows herunterfahren** an.</span><span class="sxs-lookup"><span data-stu-id="50fdb-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="50fdb-106">Dies ist identisch mit dem Klicken auf das **Startmenü** und dem Auswählen **von Herunterfahren.**</span><span class="sxs-lookup"><span data-stu-id="50fdb-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="50fdb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="50fdb-107">Syntax</span></span>


```JScript
IShellDispatch.ShutdownWindows()
```


```VB

IShellDispatch.ShutdownWindows()
```





## <a name="parameters"></a><span data-ttu-id="50fdb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="50fdb-108">Parameters</span></span>

<span data-ttu-id="50fdb-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="50fdb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50fdb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50fdb-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="50fdb-111">JScript</span><span class="sxs-lookup"><span data-stu-id="50fdb-111">JScript</span></span>

<span data-ttu-id="50fdb-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="50fdb-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="50fdb-113">VB</span><span class="sxs-lookup"><span data-stu-id="50fdb-113">VB</span></span>

<span data-ttu-id="50fdb-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="50fdb-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50fdb-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50fdb-115">Remarks</span></span>

<span data-ttu-id="50fdb-116">Diese Methode wird implementiert und über die [**Shell.ShutdownWindows-Methode aufgerufen.**](shell-shutdownwindows.md)</span><span class="sxs-lookup"><span data-stu-id="50fdb-116">This method is implemented and accessed through the [**Shell.ShutdownWindows**](shell-shutdownwindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="50fdb-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50fdb-117">Examples</span></span>

<span data-ttu-id="50fdb-118">Das folgende Beispiel zeigt die Verwendung von **ShutdownWindows** in JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="50fdb-118">The following example shows the use of **ShutdownWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="50fdb-119">Jscript:</span><span class="sxs-lookup"><span data-stu-id="50fdb-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="50fdb-120">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="50fdb-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.ShutdownWindows

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="50fdb-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="50fdb-121">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="50fdb-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50fdb-122">Requirements</span></span>



| <span data-ttu-id="50fdb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50fdb-123">Requirement</span></span> | <span data-ttu-id="50fdb-124">Wert</span><span class="sxs-lookup"><span data-stu-id="50fdb-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50fdb-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50fdb-125">Minimum supported client</span></span><br/> | <span data-ttu-id="50fdb-126">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50fdb-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="50fdb-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50fdb-127">Minimum supported server</span></span><br/> | <span data-ttu-id="50fdb-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50fdb-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="50fdb-129">Header</span><span class="sxs-lookup"><span data-stu-id="50fdb-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="50fdb-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="50fdb-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="50fdb-131">Idl</span><span class="sxs-lookup"><span data-stu-id="50fdb-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50fdb-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="50fdb-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="50fdb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="50fdb-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50fdb-134"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="50fdb-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




