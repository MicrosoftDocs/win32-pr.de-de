---
description: 'IShellDispatch2.ShowBrowserBar-Methode: Zeigt eine Browserleiste an.'
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: IShellDispatch2.ShowBrowserBar-Methode (Shldisp.h)
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
ms.openlocfilehash: 7143b55ae59c8fca845d256ddc1f79e69672364b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116938"
---
# <a name="ishelldispatch2showbrowserbar-method"></a><span data-ttu-id="a3024-103">IShellDispatch2.ShowBrowserBar-Methode</span><span class="sxs-lookup"><span data-stu-id="a3024-103">IShellDispatch2.ShowBrowserBar method</span></span>

<span data-ttu-id="a3024-104">Zeigt eine Browserleiste an.</span><span class="sxs-lookup"><span data-stu-id="a3024-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3024-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3024-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="a3024-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3024-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3024-107">*sCLSID* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a3024-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3024-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a3024-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a3024-109">Eine **Zeichenfolge,** die die Zeichenfolgenform der CLSID der anzuzeigenden Browserleiste enthält.</span><span class="sxs-lookup"><span data-stu-id="a3024-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="a3024-110">Das Objekt muss als Explorer-Balkenobjekt mit einer CATID \_ InfoBand-Komponentenkategorie registriert werden.</span><span class="sxs-lookup"><span data-stu-id="a3024-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="a3024-111">Weitere Informationen finden Sie unter [Erstellen von benutzerdefinierten Explorer-Balken, Toolbändern und Desk-Bändern.](band-objects.md)</span><span class="sxs-lookup"><span data-stu-id="a3024-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3024-112">*vShow* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a3024-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3024-113">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="a3024-113">Type: **Variant**</span></span>

<span data-ttu-id="a3024-114">Legen Sie diese Einstellung auf **TRUE** fest, um die Browserleiste anzuzeigen, oder **auf FALSE,** um sie auszublenden.</span><span class="sxs-lookup"><span data-stu-id="a3024-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3024-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3024-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a3024-116">JScript</span><span class="sxs-lookup"><span data-stu-id="a3024-116">JScript</span></span>

<span data-ttu-id="a3024-117">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="a3024-117">Type: **Variant\***</span></span>

<span data-ttu-id="a3024-118">Gibt **true** zurück, wenn erfolgreich. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a3024-118">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="a3024-119">VB</span><span class="sxs-lookup"><span data-stu-id="a3024-119">VB</span></span>

<span data-ttu-id="a3024-120">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="a3024-120">Type: **Variant\***</span></span>

<span data-ttu-id="a3024-121">Gibt **true** zurück, wenn erfolgreich. andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="a3024-121">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3024-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3024-122">Remarks</span></span>

<span data-ttu-id="a3024-123">Diese Methode wird implementiert und über die [**Shell.ShowBrowserBar-Methode**](./shell-showbrowserbar.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a3024-123">This method is implemented and accessed through the [**Shell.ShowBrowserBar**](./shell-showbrowserbar.md) method.</span></span>

<span data-ttu-id="a3024-124">Sie können eine der Standard-Explorer-Balken anzeigen, indem Sie den *sCLSID-Parameter* auf die CLSID dieser Explorer-Leiste festlegen.</span><span class="sxs-lookup"><span data-stu-id="a3024-124">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="a3024-125">Die standardmäßigen Explorer-Balken und ihre CLSID-Zeichenfolgen sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a3024-125">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="a3024-126">Explorer-Leiste</span><span class="sxs-lookup"><span data-stu-id="a3024-126">Explorer Bar</span></span> | <span data-ttu-id="a3024-127">CLSID-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a3024-127">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="a3024-128">Favoriten</span><span class="sxs-lookup"><span data-stu-id="a3024-128">Favorites</span></span>    | <span data-ttu-id="a3024-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="a3024-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="a3024-130">Ordner</span><span class="sxs-lookup"><span data-stu-id="a3024-130">Folders</span></span>      | <span data-ttu-id="a3024-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="a3024-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="a3024-132">Verlauf</span><span class="sxs-lookup"><span data-stu-id="a3024-132">History</span></span>      | <span data-ttu-id="a3024-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="a3024-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="a3024-134">Suche</span><span class="sxs-lookup"><span data-stu-id="a3024-134">Search</span></span>       | <span data-ttu-id="a3024-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="a3024-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="a3024-136">Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a3024-136">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="a3024-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3024-137">Examples</span></span>

<span data-ttu-id="a3024-138">In den folgenden Beispielen wird die Verwendung von **ShowBrowserBar** zum Anzeigen der **Browserleiste Favoriten** gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3024-138">The following examples show the use of **ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="a3024-139">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a3024-139">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="a3024-140">Jscript:</span><span class="sxs-lookup"><span data-stu-id="a3024-140">JScript:</span></span>


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



<span data-ttu-id="a3024-141">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="a3024-141">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="a3024-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3024-142">Requirements</span></span>



| <span data-ttu-id="a3024-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3024-143">Requirement</span></span> | <span data-ttu-id="a3024-144">Wert</span><span class="sxs-lookup"><span data-stu-id="a3024-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3024-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a3024-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a3024-146">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3024-146">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3024-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a3024-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a3024-148">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a3024-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a3024-149">Header</span><span class="sxs-lookup"><span data-stu-id="a3024-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3024-150"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a3024-150"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a3024-151">Idl</span><span class="sxs-lookup"><span data-stu-id="a3024-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3024-152"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3024-152"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a3024-153">DLL</span><span class="sxs-lookup"><span data-stu-id="a3024-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3024-154"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a3024-154"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
