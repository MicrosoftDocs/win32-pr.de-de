---
description: 'Zeigt das Dialogfeld Suchergebnisse: Computer an. Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.'
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257
title: Ishelldispatch. findcomputer-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ad928b6860a85126a714a08f3bc3df9d4aff67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978112"
---
# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="fb027-104">Ishelldispatch. findcomputer-Methode</span><span class="sxs-lookup"><span data-stu-id="fb027-104">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="fb027-105">Zeigt das Dialogfeld **Suchergebnisse: Computer** an.</span><span class="sxs-lookup"><span data-stu-id="fb027-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="fb027-106">Im Dialogfeld wird das Ergebnis der Suche nach einem angegebenen Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fb027-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb027-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb027-107">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="fb027-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb027-108">Parameters</span></span>

<span data-ttu-id="fb027-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fb027-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb027-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb027-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fb027-111">JScript</span><span class="sxs-lookup"><span data-stu-id="fb027-111">JScript</span></span>

<span data-ttu-id="fb027-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fb027-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="fb027-113">VB</span><span class="sxs-lookup"><span data-stu-id="fb027-113">VB</span></span>

<span data-ttu-id="fb027-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fb027-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb027-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb027-115">Remarks</span></span>

<span data-ttu-id="fb027-116">Diese Methode wird implementiert und über die [**Shell. findcomputer**](shell-findcomputer.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="fb027-116">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="fb027-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb027-117">Examples</span></span>

<span data-ttu-id="fb027-118">In den folgenden Beispielen wird die Verwendung von **findcomputer** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fb027-118">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="fb027-119">JScript</span><span class="sxs-lookup"><span data-stu-id="fb027-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="fb027-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="fb027-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="fb027-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="fb027-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="fb027-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="fb027-122">Requirements</span></span>



| <span data-ttu-id="fb027-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb027-123">Requirement</span></span> | <span data-ttu-id="fb027-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fb027-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb027-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb027-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fb027-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb027-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fb027-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb027-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fb027-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb027-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fb027-129">Header</span><span class="sxs-lookup"><span data-stu-id="fb027-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb027-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb027-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="fb027-131">IDL</span><span class="sxs-lookup"><span data-stu-id="fb027-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb027-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb027-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="fb027-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fb027-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb027-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="fb027-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




