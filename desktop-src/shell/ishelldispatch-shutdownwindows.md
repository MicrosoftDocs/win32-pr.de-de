---
description: Zeigt das Dialogfeld Windows Herunterfahren an. Dies ist das gleiche wie beim Klicken auf das Startmenü und beim Auswählen von "Herunterfahren".
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
title: Ishelldispatch. shutdownwindows-Methode (Shldisp. h)
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
ms.openlocfilehash: 9c111e1b740857337953cdcdf81735a8c0568ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993839"
---
# <a name="ishelldispatchshutdownwindows-method"></a><span data-ttu-id="78204-104">Ishelldispatch. shutdownwindows-Methode</span><span class="sxs-lookup"><span data-stu-id="78204-104">IShellDispatch.ShutdownWindows method</span></span>

<span data-ttu-id="78204-105">Zeigt das Dialogfeld **Windows herunter** fahren an.</span><span class="sxs-lookup"><span data-stu-id="78204-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="78204-106">Dies ist das gleiche wie beim Klicken auf das **Startmenü** und beim Auswählen von " **herunter** fahren".</span><span class="sxs-lookup"><span data-stu-id="78204-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="78204-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78204-107">Syntax</span></span>


```JScript
IShellDispatch.ShutdownWindows()
```


```VB

IShellDispatch.ShutdownWindows()
```





## <a name="parameters"></a><span data-ttu-id="78204-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78204-108">Parameters</span></span>

<span data-ttu-id="78204-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="78204-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="78204-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78204-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="78204-111">JScript</span><span class="sxs-lookup"><span data-stu-id="78204-111">JScript</span></span>

<span data-ttu-id="78204-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78204-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="78204-113">VB</span><span class="sxs-lookup"><span data-stu-id="78204-113">VB</span></span>

<span data-ttu-id="78204-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78204-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78204-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78204-115">Remarks</span></span>

<span data-ttu-id="78204-116">Diese Methode ist implementiert, und der Zugriff erfolgt über die [**Shell. shutdownwindows**](shell-shutdownwindows.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="78204-116">This method is implemented and accessed through the [**Shell.ShutdownWindows**](shell-shutdownwindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="78204-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="78204-117">Examples</span></span>

<span data-ttu-id="78204-118">Das folgende Beispiel zeigt die Verwendung von **shutdownwindows** in JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="78204-118">The following example shows the use of **ShutdownWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="78204-119">JScript</span><span class="sxs-lookup"><span data-stu-id="78204-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="78204-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="78204-120">VBScript:</span></span>


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



<span data-ttu-id="78204-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="78204-121">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="78204-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="78204-122">Requirements</span></span>



| <span data-ttu-id="78204-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78204-123">Requirement</span></span> | <span data-ttu-id="78204-124">Wert</span><span class="sxs-lookup"><span data-stu-id="78204-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78204-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="78204-125">Minimum supported client</span></span><br/> | <span data-ttu-id="78204-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78204-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="78204-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="78204-127">Minimum supported server</span></span><br/> | <span data-ttu-id="78204-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="78204-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="78204-129">Header</span><span class="sxs-lookup"><span data-stu-id="78204-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="78204-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="78204-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="78204-131">IDL</span><span class="sxs-lookup"><span data-stu-id="78204-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78204-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78204-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="78204-133">DLL</span><span class="sxs-lookup"><span data-stu-id="78204-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78204-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="78204-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




