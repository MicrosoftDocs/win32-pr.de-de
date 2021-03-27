---
description: Zeigt eine Browserleiste an.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Shell. showbrowserbar-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d112399e62825714b4c060aeddcb8618ff73d478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979760"
---
# <a name="shellshowbrowserbar-method"></a><span data-ttu-id="58baf-103">Shell. showbrowserbar-Methode</span><span class="sxs-lookup"><span data-stu-id="58baf-103">Shell.ShowBrowserBar method</span></span>

<span data-ttu-id="58baf-104">Zeigt eine Browserleiste an.</span><span class="sxs-lookup"><span data-stu-id="58baf-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="58baf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58baf-105">Syntax</span></span>


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="58baf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58baf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58baf-107">*sclsid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58baf-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58baf-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="58baf-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="58baf-109">Eine **Zeichen** Folge, die die Zeichen folgen Form der CLSID der anzuzeigenden Browserleiste enthält.</span><span class="sxs-lookup"><span data-stu-id="58baf-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="58baf-110">Das Objekt muss als Explorer-Balken Objekt mit der Kategorie "CATID \_ Infoband-Komponente" registriert werden.</span><span class="sxs-lookup"><span data-stu-id="58baf-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="58baf-111">Weitere Informationen finden Sie unter [Creating Custom Explorer Bars, Toolbands und Desk Bands](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="58baf-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="58baf-112">*vshow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58baf-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58baf-113">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="58baf-113">Type: **Variant**</span></span>

<span data-ttu-id="58baf-114">Legen Sie diese Einstellung auf " **true** " fest **, um die** Browserleiste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="58baf-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58baf-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58baf-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="58baf-116">JScript</span><span class="sxs-lookup"><span data-stu-id="58baf-116">JScript</span></span>

<span data-ttu-id="58baf-117">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="58baf-117">Type: \**Variant\** _</span></span>

<span data-ttu-id="58baf-118">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="58baf-118">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="58baf-119">VB</span><span class="sxs-lookup"><span data-stu-id="58baf-119">VB</span></span>

<span data-ttu-id="58baf-120">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="58baf-120">Type: \**Variant\** _</span></span>

<span data-ttu-id="58baf-121">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="58baf-121">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="58baf-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58baf-122">Remarks</span></span>

<span data-ttu-id="58baf-123">Sie können eine der Standard-Explorer-leisten anzeigen, indem Sie den *sclsid* -Parameter auf die CLSID dieser Explorer-Leiste festlegen.</span><span class="sxs-lookup"><span data-stu-id="58baf-123">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="58baf-124">Die Standard-Explorer-leisten und Ihre CLSID-Zeichen folgen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="58baf-124">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="58baf-125">Explorer-Leiste</span><span class="sxs-lookup"><span data-stu-id="58baf-125">Explorer Bar</span></span> | <span data-ttu-id="58baf-126">CLSID-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="58baf-126">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="58baf-127">Favoriten</span><span class="sxs-lookup"><span data-stu-id="58baf-127">Favorites</span></span>    | <span data-ttu-id="58baf-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="58baf-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="58baf-129">Ordner</span><span class="sxs-lookup"><span data-stu-id="58baf-129">Folders</span></span>      | <span data-ttu-id="58baf-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="58baf-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="58baf-131">Verlauf</span><span class="sxs-lookup"><span data-stu-id="58baf-131">History</span></span>      | <span data-ttu-id="58baf-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="58baf-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="58baf-133">Suchen,</span><span class="sxs-lookup"><span data-stu-id="58baf-133">Search</span></span>       | <span data-ttu-id="58baf-134">{30d02401-6a81-11D0-8274-00c04\d5ae38}</span><span class="sxs-lookup"><span data-stu-id="58baf-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="58baf-135">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="58baf-135">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="58baf-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58baf-136">Examples</span></span>

<span data-ttu-id="58baf-137">In den folgenden Beispielen wird gezeigt, wie **Shell. showbrowserbar** verwendet wird, um die **Favoriten** -Browserleiste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="58baf-137">The following examples show the use of **Shell.ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="58baf-138">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="58baf-138">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="58baf-139">JScript</span><span class="sxs-lookup"><span data-stu-id="58baf-139">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



<span data-ttu-id="58baf-140">VBScript</span><span class="sxs-lookup"><span data-stu-id="58baf-140">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="58baf-141">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="58baf-141">Requirements</span></span>



| <span data-ttu-id="58baf-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58baf-142">Requirement</span></span> | <span data-ttu-id="58baf-143">Wert</span><span class="sxs-lookup"><span data-stu-id="58baf-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58baf-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58baf-144">Minimum supported client</span></span><br/> | <span data-ttu-id="58baf-145">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58baf-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58baf-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58baf-146">Minimum supported server</span></span><br/> | <span data-ttu-id="58baf-147">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58baf-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="58baf-148">Header</span><span class="sxs-lookup"><span data-stu-id="58baf-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="58baf-149"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="58baf-149"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="58baf-150">IDL</span><span class="sxs-lookup"><span data-stu-id="58baf-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="58baf-151"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="58baf-151"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="58baf-152">DLL</span><span class="sxs-lookup"><span data-stu-id="58baf-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58baf-153"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="58baf-153"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
