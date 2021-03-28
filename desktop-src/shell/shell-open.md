---
description: Öffnet den angegebenen Ordner.
ms.assetid: 96ed9360-fb8f-4f7e-aefb-4a63ec95df07
title: Shell. Open-Methode (Shldisp. h)
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
ms.openlocfilehash: 3572f48a7b129500c38c3c0227ba479ecb775067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866144"
---
# <a name="shellopen-method"></a><span data-ttu-id="3bbeb-103">Shell. Open-Methode</span><span class="sxs-lookup"><span data-stu-id="3bbeb-103">Shell.Open method</span></span>

<span data-ttu-id="3bbeb-104">Öffnet den angegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="3bbeb-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bbeb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bbeb-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="3bbeb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bbeb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bbeb-107">*vdir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3bbeb-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bbeb-108">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="3bbeb-108">Type: **Variant**</span></span>

<span data-ttu-id="3bbeb-109">Eine Zeichenfolge, die den Pfad des Ordners oder einen der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Werte angibt.</span><span class="sxs-lookup"><span data-stu-id="3bbeb-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="3bbeb-110">Beachten Sie, dass die in **shellspecialfolderconstants** gefundenen Konstanten Namen in Visual Basic verfügbar sind, jedoch nicht in VBScript oder JScript.</span><span class="sxs-lookup"><span data-stu-id="3bbeb-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="3bbeb-111">In diesen Fällen müssen die numerischen Werte an ihrer Stelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3bbeb-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="3bbeb-112">Wenn *vdir* auf eine der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) festgelegt ist und der spezielle Ordner nicht vorhanden ist, erstellt diese Funktion den Ordner.</span><span class="sxs-lookup"><span data-stu-id="3bbeb-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3bbeb-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3bbeb-113">Examples</span></span>

<span data-ttu-id="3bbeb-114">Das folgende Beispiel zeigt **Open** in use.</span><span class="sxs-lookup"><span data-stu-id="3bbeb-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="3bbeb-115">Die richtige Verwendung wird für JScript, VBScript und Visual Basic angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bbeb-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3bbeb-116">JScript</span><span class="sxs-lookup"><span data-stu-id="3bbeb-116">JScript:</span></span>


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



<span data-ttu-id="3bbeb-117">VBScript</span><span class="sxs-lookup"><span data-stu-id="3bbeb-117">VBScript:</span></span>


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



<span data-ttu-id="3bbeb-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3bbeb-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3bbeb-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3bbeb-119">Requirements</span></span>



| <span data-ttu-id="3bbeb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bbeb-120">Requirement</span></span> | <span data-ttu-id="3bbeb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="3bbeb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bbeb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3bbeb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3bbeb-123">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bbeb-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3bbeb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3bbeb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3bbeb-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3bbeb-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3bbeb-126">Header</span><span class="sxs-lookup"><span data-stu-id="3bbeb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bbeb-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bbeb-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3bbeb-128">IDL</span><span class="sxs-lookup"><span data-stu-id="3bbeb-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3bbeb-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3bbeb-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3bbeb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3bbeb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bbeb-131"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="3bbeb-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bbeb-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3bbeb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bbeb-133">**Shell**</span><span class="sxs-lookup"><span data-stu-id="3bbeb-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="3bbeb-134">**Erkunden**</span><span class="sxs-lookup"><span data-stu-id="3bbeb-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




