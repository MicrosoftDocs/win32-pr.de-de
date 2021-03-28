---
description: 'Zeigt das Dialogfeld Suchergebnisse: Computer an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.'
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360
title: Shell. findcomputer-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3824eeb98bfac11e007d1bf7dd9f89153a7b73ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980641"
---
# <a name="shellfindcomputer-method"></a><span data-ttu-id="de575-104">Shell. findcomputer-Methode</span><span class="sxs-lookup"><span data-stu-id="de575-104">Shell.FindComputer method</span></span>

<span data-ttu-id="de575-105">Zeigt das Dialogfeld **Suchergebnisse: Computer** an.</span><span class="sxs-lookup"><span data-stu-id="de575-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="de575-106">Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="de575-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="de575-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="de575-107">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="de575-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de575-108">Parameters</span></span>

<span data-ttu-id="de575-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="de575-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de575-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de575-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="de575-111">JScript</span><span class="sxs-lookup"><span data-stu-id="de575-111">JScript</span></span>

<span data-ttu-id="de575-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="de575-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="de575-113">VB</span><span class="sxs-lookup"><span data-stu-id="de575-113">VB</span></span>

<span data-ttu-id="de575-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="de575-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="de575-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de575-115">Examples</span></span>

<span data-ttu-id="de575-116">Das folgende Beispiel zeigt, wie **findcomputer** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="de575-116">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="de575-117">Das Ergebnis dieses Codes ist das gleiche wie beim Drücken der **Start** Schaltfläche, beim Klicken auf **Suchen**, beim Klicken auf die Option **Drucker, Computer oder Personen** und anschließendes Klicken **auf einen Computer im Netzwerk**.</span><span class="sxs-lookup"><span data-stu-id="de575-117">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="de575-118">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="de575-118">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="de575-119">JScript</span><span class="sxs-lookup"><span data-stu-id="de575-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="de575-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="de575-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="de575-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="de575-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="de575-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="de575-122">Requirements</span></span>



| <span data-ttu-id="de575-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de575-123">Requirement</span></span> | <span data-ttu-id="de575-124">Wert</span><span class="sxs-lookup"><span data-stu-id="de575-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de575-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de575-125">Minimum supported client</span></span><br/> | <span data-ttu-id="de575-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de575-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="de575-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de575-127">Minimum supported server</span></span><br/> | <span data-ttu-id="de575-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de575-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="de575-129">Header</span><span class="sxs-lookup"><span data-stu-id="de575-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="de575-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="de575-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="de575-131">IDL</span><span class="sxs-lookup"><span data-stu-id="de575-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de575-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="de575-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="de575-133">DLL</span><span class="sxs-lookup"><span data-stu-id="de575-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de575-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="de575-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




