---
description: Zeigt das Dialogfeld Windows Herunterfahren an. Dies ist das gleiche wie beim Klicken auf das Startmenü und beim Auswählen von "Herunterfahren".
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: Shell. shutdownwindows-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 804a1e211e191206d20f83d85dee2202492bfd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216598"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="567f7-104">Shell. shutdownwindows-Methode</span><span class="sxs-lookup"><span data-stu-id="567f7-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="567f7-105">Zeigt das Dialogfeld **Windows herunter** fahren an.</span><span class="sxs-lookup"><span data-stu-id="567f7-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="567f7-106">Dies ist das gleiche wie beim Klicken auf das **Startmenü** und beim Auswählen von " **herunter** fahren".</span><span class="sxs-lookup"><span data-stu-id="567f7-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="567f7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="567f7-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="567f7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="567f7-108">Parameters</span></span>

<span data-ttu-id="567f7-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="567f7-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="567f7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="567f7-110">Examples</span></span>

<span data-ttu-id="567f7-111">Im folgenden Beispiel wird die Verwendung von **shutdownwindows** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="567f7-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="567f7-112">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="567f7-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="567f7-113">JScript</span><span class="sxs-lookup"><span data-stu-id="567f7-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="567f7-114">VBScript</span><span class="sxs-lookup"><span data-stu-id="567f7-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="567f7-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="567f7-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="567f7-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="567f7-116">Requirements</span></span>



| <span data-ttu-id="567f7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="567f7-117">Requirement</span></span> | <span data-ttu-id="567f7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="567f7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="567f7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="567f7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="567f7-120">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="567f7-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="567f7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="567f7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="567f7-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="567f7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="567f7-123">Header</span><span class="sxs-lookup"><span data-stu-id="567f7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="567f7-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="567f7-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="567f7-125">IDL</span><span class="sxs-lookup"><span data-stu-id="567f7-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="567f7-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="567f7-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="567f7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="567f7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="567f7-128"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="567f7-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




