---
description: 'Shell.Open-Methode: Öffnet den angegebenen Ordner.'
ms.assetid: 96ed9360-fb8f-4f7e-aefb-4a63ec95df07
title: Shell.Open-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 36f8914be3fce6b461e5267562e6f3ef40aa5fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104228"
---
# <a name="shellopen-method"></a><span data-ttu-id="edb21-103">Shell.Open-Methode</span><span class="sxs-lookup"><span data-stu-id="edb21-103">Shell.Open method</span></span>

<span data-ttu-id="edb21-104">Öffnet den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="edb21-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb21-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="edb21-105">Syntax</span></span>


```JScript
iRetVal = Shell.Open(
  vDir
)
```


```VB

Shell.Open( _
  ByVal vDir As Variant _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="edb21-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="edb21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb21-107">*vDir* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="edb21-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb21-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="edb21-108">Type: **Variant**</span></span>

<span data-ttu-id="edb21-109">Eine Zeichenfolge, die den Pfad des Ordners oder eines der [**ShellSpecialFolderConstants-Werte angibt.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)</span><span class="sxs-lookup"><span data-stu-id="edb21-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="edb21-110">Beachten Sie, dass die konstanten Namen in **ShellSpecialFolderConstants** in Visual Basic, aber nicht in VBScript oder JScript verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="edb21-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="edb21-111">In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edb21-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="edb21-112">Wenn *vDir* auf einen der [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) festgelegt ist und der spezielle Ordner nicht vorhanden ist, erstellt diese Funktion den Ordner.</span><span class="sxs-lookup"><span data-stu-id="edb21-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="edb21-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="edb21-113">Examples</span></span>

<span data-ttu-id="edb21-114">Im folgenden Beispiel wird **Open** in use gezeigt.</span><span class="sxs-lookup"><span data-stu-id="edb21-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="edb21-115">Die richtige Verwendung wird für JScript, VBScript und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="edb21-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="edb21-116">Jscript:</span><span class="sxs-lookup"><span data-stu-id="edb21-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objShell.Shell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="edb21-117">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="edb21-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Shell.Open("C:\\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="edb21-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="edb21-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="edb21-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edb21-119">Requirements</span></span>



| <span data-ttu-id="edb21-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edb21-120">Requirement</span></span> | <span data-ttu-id="edb21-121">Wert</span><span class="sxs-lookup"><span data-stu-id="edb21-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edb21-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="edb21-122">Minimum supported client</span></span><br/> | <span data-ttu-id="edb21-123">Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edb21-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="edb21-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="edb21-124">Minimum supported server</span></span><br/> | <span data-ttu-id="edb21-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edb21-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="edb21-126">Header</span><span class="sxs-lookup"><span data-stu-id="edb21-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="edb21-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="edb21-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="edb21-128">Idl</span><span class="sxs-lookup"><span data-stu-id="edb21-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="edb21-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="edb21-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="edb21-130">DLL</span><span class="sxs-lookup"><span data-stu-id="edb21-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edb21-131"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="edb21-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb21-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="edb21-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb21-133">**Shell**</span><span class="sxs-lookup"><span data-stu-id="edb21-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="edb21-134">**Erkunden**</span><span class="sxs-lookup"><span data-stu-id="edb21-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




