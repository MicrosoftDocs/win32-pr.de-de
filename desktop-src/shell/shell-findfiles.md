---
description: 'Zeigt das Dialogfeld suchen: alle Dateien an. Dies ist das gleiche wie beim Klicken auf das Startmenü und anschließendes Auswählen von suchen (oder der entsprechenden Entsprechung unter Systeme vor Windows XP).'
ms.assetid: cccdd3ea-b52a-4fbe-b4c5-1efc1dd6d770
title: Shell. findfiles-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindFiles
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f3e6551dc41fd8d6a040ada8000f0b46e81a5dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217699"
---
# <a name="shellfindfiles-method"></a><span data-ttu-id="7c661-104">Shell. findfiles-Methode</span><span class="sxs-lookup"><span data-stu-id="7c661-104">Shell.FindFiles method</span></span>

<span data-ttu-id="7c661-105">Zeigt das Dialogfeld **suchen: alle Dateien** an.</span><span class="sxs-lookup"><span data-stu-id="7c661-105">Displays the **Find: All Files** dialog box.</span></span> <span data-ttu-id="7c661-106">Dies ist das gleiche wie beim Klicken auf das **Startmenü** und anschließendes Auswählen von **Suchen** (oder der entsprechenden Entsprechung unter Systeme vor Windows XP).</span><span class="sxs-lookup"><span data-stu-id="7c661-106">This is the same as clicking the **Start** menu and then selecting **Search** (or its equivalent under systems earlier than Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c661-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c661-107">Syntax</span></span>


```JScript
Shell.FindFiles()
```


```VB

Shell.FindFiles()
```





## <a name="parameters"></a><span data-ttu-id="7c661-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c661-108">Parameters</span></span>

<span data-ttu-id="7c661-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7c661-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c661-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c661-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7c661-111">JScript</span><span class="sxs-lookup"><span data-stu-id="7c661-111">JScript</span></span>

<span data-ttu-id="7c661-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7c661-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="7c661-113">VB</span><span class="sxs-lookup"><span data-stu-id="7c661-113">VB</span></span>

<span data-ttu-id="7c661-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7c661-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="7c661-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c661-115">Examples</span></span>

<span data-ttu-id="7c661-116">Das folgende Beispiel zeigt, wie **findfiles** verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7c661-116">The following example shows **FindFiles** in use.</span></span> <span data-ttu-id="7c661-117">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c661-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7c661-118">JScript</span><span class="sxs-lookup"><span data-stu-id="7c661-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindFilesJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Shell_FindFiles();
    }
</script>
```



<span data-ttu-id="7c661-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="7c661-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindFilesVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FindFiles

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7c661-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7c661-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFindFilesVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindFiles

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7c661-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7c661-121">Requirements</span></span>



| <span data-ttu-id="7c661-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c661-122">Requirement</span></span> | <span data-ttu-id="7c661-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7c661-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c661-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c661-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7c661-125">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c661-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7c661-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c661-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7c661-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c661-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7c661-128">Header</span><span class="sxs-lookup"><span data-stu-id="7c661-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c661-129"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c661-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7c661-130">IDL</span><span class="sxs-lookup"><span data-stu-id="7c661-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c661-131"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c661-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7c661-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7c661-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c661-133"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7c661-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




