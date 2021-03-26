---
description: Zeigt das Fenster Hilfe und Support an. Diese Methode hat denselben Effekt wie das Klicken auf das Startmenü und das Auswählen von Hilfe und Support.
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
title: Ishelldispatch. Help-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b58bcc97748cecf6ab4064ecccf3ba5bbe190b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978097"
---
# <a name="ishelldispatchhelp-method"></a><span data-ttu-id="89be0-104">Ishelldispatch. Help-Methode</span><span class="sxs-lookup"><span data-stu-id="89be0-104">IShellDispatch.Help method</span></span>

<span data-ttu-id="89be0-105">Zeigt das Fenster Hilfe und Support an.</span><span class="sxs-lookup"><span data-stu-id="89be0-105">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="89be0-106">Diese Methode hat denselben Effekt wie das Klicken auf das **Startmenü** und das Auswählen von **Hilfe und Support**.</span><span class="sxs-lookup"><span data-stu-id="89be0-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="89be0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="89be0-107">Syntax</span></span>


```JScript
IShellDispatch.Help()
```


```VB

IShellDispatch.Help()
```





## <a name="parameters"></a><span data-ttu-id="89be0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89be0-108">Parameters</span></span>

<span data-ttu-id="89be0-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="89be0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89be0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89be0-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="89be0-111">JScript</span><span class="sxs-lookup"><span data-stu-id="89be0-111">JScript</span></span>

<span data-ttu-id="89be0-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="89be0-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="89be0-113">VB</span><span class="sxs-lookup"><span data-stu-id="89be0-113">VB</span></span>

<span data-ttu-id="89be0-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="89be0-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="89be0-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89be0-115">Remarks</span></span>

<span data-ttu-id="89be0-116">Diese Methode wird implementiert und über die [**Shell. Help**](shell-help.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="89be0-116">This method is implemented and accessed through the [**Shell.Help**](shell-help.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="89be0-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89be0-117">Examples</span></span>

<span data-ttu-id="89be0-118">In den folgenden Beispielen wird die Verwendung der **Hilfe** in JScript, VBScript und Visual Basic veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="89be0-118">The following examples show the use of **Help** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="89be0-119">JScript</span><span class="sxs-lookup"><span data-stu-id="89be0-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
    }
</script>
```



<span data-ttu-id="89be0-120">VBScript</span><span class="sxs-lookup"><span data-stu-id="89be0-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="89be0-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="89be0-121">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="89be0-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="89be0-122">Requirements</span></span>



| <span data-ttu-id="89be0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89be0-123">Requirement</span></span> | <span data-ttu-id="89be0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="89be0-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89be0-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89be0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="89be0-126">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89be0-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="89be0-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89be0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="89be0-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="89be0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="89be0-129">Header</span><span class="sxs-lookup"><span data-stu-id="89be0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="89be0-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="89be0-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="89be0-131">IDL</span><span class="sxs-lookup"><span data-stu-id="89be0-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="89be0-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="89be0-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="89be0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="89be0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89be0-134"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="89be0-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




