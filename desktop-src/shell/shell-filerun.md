---
description: Zeigt das Dialogfeld "ausführen" für den Benutzer an. Diese Methode hat denselben Effekt wie das Klicken auf das Startmenü und das Auswählen von ausführen.
ms.assetid: bb984777-e09f-41e6-8359-51c5291654f7
title: Shell. filerun-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ebccf11ea21fdd4ceba2563a6110c1eb2494947b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980656"
---
# <a name="shellfilerun-method"></a><span data-ttu-id="17139-104">Shell. filerun-Methode</span><span class="sxs-lookup"><span data-stu-id="17139-104">Shell.FileRun method</span></span>

<span data-ttu-id="17139-105">Zeigt das Dialogfeld " **Ausführen** " für den Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="17139-105">Displays the **Run** dialog to the user.</span></span> <span data-ttu-id="17139-106">Diese Methode hat denselben Effekt wie das Klicken auf das **Startmenü** und das Auswählen von **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="17139-106">This method has the same effect as clicking the **Start** menu and selecting **Run**.</span></span>

## <a name="syntax"></a><span data-ttu-id="17139-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="17139-107">Syntax</span></span>


```JScript
Shell.FileRun()
```


```VB

Shell.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="17139-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="17139-108">Parameters</span></span>

<span data-ttu-id="17139-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="17139-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17139-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17139-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="17139-111">JScript</span><span class="sxs-lookup"><span data-stu-id="17139-111">JScript</span></span>

<span data-ttu-id="17139-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="17139-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="17139-113">VB</span><span class="sxs-lookup"><span data-stu-id="17139-113">VB</span></span>

<span data-ttu-id="17139-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="17139-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="17139-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17139-115">Examples</span></span>

<span data-ttu-id="17139-116">Das folgende Beispiel zeigt die Verwendung von **filerun** .</span><span class="sxs-lookup"><span data-stu-id="17139-116">The following example shows **FileRun** in use.</span></span> <span data-ttu-id="17139-117">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17139-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="17139-118">JScript</span><span class="sxs-lookup"><span data-stu-id="17139-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FileRun();
    }
</script>
```



<span data-ttu-id="17139-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="17139-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="17139-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="17139-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="17139-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="17139-121">Requirements</span></span>



| <span data-ttu-id="17139-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17139-122">Requirement</span></span> | <span data-ttu-id="17139-123">Wert</span><span class="sxs-lookup"><span data-stu-id="17139-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17139-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17139-124">Minimum supported client</span></span><br/> | <span data-ttu-id="17139-125">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17139-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="17139-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17139-126">Minimum supported server</span></span><br/> | <span data-ttu-id="17139-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17139-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="17139-128">Header</span><span class="sxs-lookup"><span data-stu-id="17139-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="17139-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17139-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="17139-130">IDL</span><span class="sxs-lookup"><span data-stu-id="17139-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17139-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17139-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="17139-132">DLL</span><span class="sxs-lookup"><span data-stu-id="17139-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17139-133"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="17139-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




