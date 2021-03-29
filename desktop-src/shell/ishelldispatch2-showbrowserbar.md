---
description: Zeigt eine Browserleiste an.
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: IShellDispatch2. showbrowserbar-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e1df729401dd12b8221ba98a3b81ea65569113e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978016"
---
# <a name="ishelldispatch2showbrowserbar-method"></a><span data-ttu-id="ac5b5-103">IShellDispatch2. showbrowserbar-Methode</span><span class="sxs-lookup"><span data-stu-id="ac5b5-103">IShellDispatch2.ShowBrowserBar method</span></span>

<span data-ttu-id="ac5b5-104">Zeigt eine Browserleiste an.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac5b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac5b5-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="ac5b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac5b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac5b5-107">*sclsid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac5b5-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5b5-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="ac5b5-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="ac5b5-109">Eine **Zeichen** Folge, die die Zeichen folgen Form der CLSID der anzuzeigenden Browserleiste enthält.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="ac5b5-110">Das Objekt muss als Explorer-Balken Objekt mit der Kategorie "CATID \_ Infoband-Komponente" registriert werden.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="ac5b5-111">Weitere Informationen finden Sie unter [Creating Custom Explorer Bars, Toolbands und Desk Bands](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ac5b5-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="ac5b5-112">*vshow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac5b5-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac5b5-113">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ac5b5-113">Type: **Variant**</span></span>

<span data-ttu-id="ac5b5-114">Legen Sie diese Einstellung auf " **true** " fest **, um die** Browserleiste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac5b5-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac5b5-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ac5b5-116">JScript</span><span class="sxs-lookup"><span data-stu-id="ac5b5-116">JScript</span></span>

<span data-ttu-id="ac5b5-117">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="ac5b5-117">Type: \**Variant\** _</span></span>

<span data-ttu-id="ac5b5-118">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-118">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="ac5b5-119">VB</span><span class="sxs-lookup"><span data-stu-id="ac5b5-119">VB</span></span>

<span data-ttu-id="ac5b5-120">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="ac5b5-120">Type: \**Variant\** _</span></span>

<span data-ttu-id="ac5b5-121">Gibt _ *true*\* zurück, wenn erfolgreich; andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-121">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac5b5-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac5b5-122">Remarks</span></span>

<span data-ttu-id="ac5b5-123">Diese Methode wird implementiert und über die [**Shell. showbrowserbar**](./shell-showbrowserbar.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-123">This method is implemented and accessed through the [**Shell.ShowBrowserBar**](./shell-showbrowserbar.md) method.</span></span>

<span data-ttu-id="ac5b5-124">Sie können eine der Standard-Explorer-leisten anzeigen, indem Sie den *sclsid* -Parameter auf die CLSID dieser Explorer-Leiste festlegen.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-124">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="ac5b5-125">Die Standard-Explorer-leisten und Ihre CLSID-Zeichen folgen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ac5b5-125">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="ac5b5-126">Explorer-Leiste</span><span class="sxs-lookup"><span data-stu-id="ac5b5-126">Explorer Bar</span></span> | <span data-ttu-id="ac5b5-127">CLSID-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ac5b5-127">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="ac5b5-128">Favoriten</span><span class="sxs-lookup"><span data-stu-id="ac5b5-128">Favorites</span></span>    | <span data-ttu-id="ac5b5-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="ac5b5-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="ac5b5-130">Ordner</span><span class="sxs-lookup"><span data-stu-id="ac5b5-130">Folders</span></span>      | <span data-ttu-id="ac5b5-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="ac5b5-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="ac5b5-132">Verlauf</span><span class="sxs-lookup"><span data-stu-id="ac5b5-132">History</span></span>      | <span data-ttu-id="ac5b5-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="ac5b5-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="ac5b5-134">Suchen,</span><span class="sxs-lookup"><span data-stu-id="ac5b5-134">Search</span></span>       | <span data-ttu-id="ac5b5-135">{30d02401-6a81-11D0-8274-00c04\d5ae38}</span><span class="sxs-lookup"><span data-stu-id="ac5b5-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="ac5b5-136">Diese Methode ist zurzeit nicht in Microsoft Visual Basic verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-136">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="ac5b5-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac5b5-137">Examples</span></span>

<span data-ttu-id="ac5b5-138">In den folgenden Beispielen wird gezeigt, wie Sie **showbrowserbar** verwenden, um die **Favoriten** -Browserleiste anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-138">The following examples show the use of **ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="ac5b5-139">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac5b5-139">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="ac5b5-140">JScript</span><span class="sxs-lookup"><span data-stu-id="ac5b5-140">JScript:</span></span>


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



<span data-ttu-id="ac5b5-141">VBScript</span><span class="sxs-lookup"><span data-stu-id="ac5b5-141">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ac5b5-142">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ac5b5-142">Requirements</span></span>



| <span data-ttu-id="ac5b5-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac5b5-143">Requirement</span></span> | <span data-ttu-id="ac5b5-144">Wert</span><span class="sxs-lookup"><span data-stu-id="ac5b5-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac5b5-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ac5b5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ac5b5-146">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac5b5-146">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac5b5-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ac5b5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ac5b5-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ac5b5-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ac5b5-149">Header</span><span class="sxs-lookup"><span data-stu-id="ac5b5-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac5b5-150"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac5b5-150"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ac5b5-151">IDL</span><span class="sxs-lookup"><span data-stu-id="ac5b5-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac5b5-152"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac5b5-152"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ac5b5-153">DLL</span><span class="sxs-lookup"><span data-stu-id="ac5b5-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac5b5-154"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ac5b5-154"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
