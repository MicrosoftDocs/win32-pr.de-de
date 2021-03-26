---
description: Zeigt das Dialogfeld Datum und Uhrzeit an. Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von Datum/Uhrzeit anpassen.
ms.assetid: D4B949F6-5508-4624-9706-491184703DC6
title: Ishelldispatch. setTime-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c9e687ea89cad4715aeacf72a2a33792fba9f7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863143"
---
# <a name="ishelldispatchsettime-method"></a><span data-ttu-id="01b8f-104">Ishelldispatch. setTime-Methode</span><span class="sxs-lookup"><span data-stu-id="01b8f-104">IShellDispatch.SetTime method</span></span>

<span data-ttu-id="01b8f-105">Zeigt das Dialogfeld **Datum und Uhrzeit** an.</span><span class="sxs-lookup"><span data-stu-id="01b8f-105">Displays the **Date and Time** dialog box.</span></span> <span data-ttu-id="01b8f-106">Diese Methode hat denselben Effekt wie das Klicken mit der rechten Maustaste auf die Uhr im Statusbereich der Taskleiste und das Auswählen von **Datum/Uhrzeit anpassen**.</span><span class="sxs-lookup"><span data-stu-id="01b8f-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust date/time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="01b8f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="01b8f-107">Syntax</span></span>


```JScript
IShellDispatch.SetTime()
```


```VB

IShellDispatch.SetTime()
```





## <a name="parameters"></a><span data-ttu-id="01b8f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="01b8f-108">Parameters</span></span>

<span data-ttu-id="01b8f-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="01b8f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="01b8f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01b8f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="01b8f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="01b8f-111">JScript</span></span>

<span data-ttu-id="01b8f-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="01b8f-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="01b8f-113">VB</span><span class="sxs-lookup"><span data-stu-id="01b8f-113">VB</span></span>

<span data-ttu-id="01b8f-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="01b8f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01b8f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01b8f-115">Remarks</span></span>

<span data-ttu-id="01b8f-116">Diese Methode wird implementiert und über die [**Shell. setTime**](shell-settime.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="01b8f-116">This method is implemented and accessed through the [**Shell.SetTime**](shell-settime.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="01b8f-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01b8f-117">Examples</span></span>

<span data-ttu-id="01b8f-118">In den folgenden Beispielen wird die Verwendung von **setTime** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="01b8f-118">The following examples show the use of **SetTime** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="01b8f-119">JScript</span><span class="sxs-lookup"><span data-stu-id="01b8f-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.SetTime();
    }
</script>
```



<span data-ttu-id="01b8f-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="01b8f-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.SetTime
 
        set objShell = nothing
    end function
```



<span data-ttu-id="01b8f-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="01b8f-121">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.SetTime
 
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="01b8f-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="01b8f-122">Requirements</span></span>



| <span data-ttu-id="01b8f-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01b8f-123">Requirement</span></span> | <span data-ttu-id="01b8f-124">Wert</span><span class="sxs-lookup"><span data-stu-id="01b8f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b8f-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01b8f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="01b8f-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01b8f-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="01b8f-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01b8f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="01b8f-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01b8f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="01b8f-129">Header</span><span class="sxs-lookup"><span data-stu-id="01b8f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="01b8f-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="01b8f-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="01b8f-131">IDL</span><span class="sxs-lookup"><span data-stu-id="01b8f-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01b8f-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01b8f-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="01b8f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="01b8f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01b8f-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="01b8f-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




