---
description: 'Shell.ShowBrowserBar-Methode: Zeigt eine Browserleiste an.'
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Shell.ShowBrowserBar-Methode (Shldisp.h)
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
ms.openlocfilehash: d19cd5b98ce39470860cc481ab05e4bb41adc9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083724"
---
# <a name="shellshowbrowserbar-method"></a><span data-ttu-id="cadae-103">Shell.ShowBrowserBar-Methode</span><span class="sxs-lookup"><span data-stu-id="cadae-103">Shell.ShowBrowserBar method</span></span>

<span data-ttu-id="cadae-104">Zeigt eine Browserleiste an.</span><span class="sxs-lookup"><span data-stu-id="cadae-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="cadae-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cadae-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="cadae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cadae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cadae-107">*sCLSID* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cadae-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadae-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cadae-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cadae-109">Eine **Zeichenfolge,** die die Zeichenfolgenform der CLSID der anzuzeigenden Browserleiste enthält.</span><span class="sxs-lookup"><span data-stu-id="cadae-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="cadae-110">Das Objekt muss als Explorer-Balkenobjekt mit einer CATID \_ InfoBand-Komponentenkategorie registriert werden.</span><span class="sxs-lookup"><span data-stu-id="cadae-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="cadae-111">Weitere Informationen finden Sie unter [Erstellen von benutzerdefinierten Explorer-Balken, Toolbändern und Desk-Bändern.](band-objects.md)</span><span class="sxs-lookup"><span data-stu-id="cadae-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="cadae-112">*vShow* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="cadae-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cadae-113">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="cadae-113">Type: **Variant**</span></span>

<span data-ttu-id="cadae-114">Legen Sie auf **TRUE fest,** um die Browserleiste oder **FALSE zum** Ausblenden der Leiste zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="cadae-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cadae-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cadae-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cadae-116">JScript</span><span class="sxs-lookup"><span data-stu-id="cadae-116">JScript</span></span>

<span data-ttu-id="cadae-117">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="cadae-117">Type: **Variant\***</span></span>

<span data-ttu-id="cadae-118">Gibt **true zurück,** wenn erfolgreich; andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="cadae-118">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="cadae-119">VB</span><span class="sxs-lookup"><span data-stu-id="cadae-119">VB</span></span>

<span data-ttu-id="cadae-120">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="cadae-120">Type: **Variant\***</span></span>

<span data-ttu-id="cadae-121">Gibt **true zurück,** wenn erfolgreich; andernfalls **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="cadae-121">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cadae-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cadae-122">Remarks</span></span>

<span data-ttu-id="cadae-123">Sie können eine der standardmäßigen Explorer-Balken anzeigen, indem Sie den *sCLSID-Parameter* auf die CLSID dieser Explorer-Leiste festlegen.</span><span class="sxs-lookup"><span data-stu-id="cadae-123">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="cadae-124">Die standardmäßigen Explorer-Balken und ihre CLSID-Zeichenfolgen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cadae-124">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="cadae-125">Explorer-Leiste</span><span class="sxs-lookup"><span data-stu-id="cadae-125">Explorer Bar</span></span> | <span data-ttu-id="cadae-126">CLSID-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cadae-126">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="cadae-127">Favoriten</span><span class="sxs-lookup"><span data-stu-id="cadae-127">Favorites</span></span>    | <span data-ttu-id="cadae-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="cadae-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="cadae-129">Ordner</span><span class="sxs-lookup"><span data-stu-id="cadae-129">Folders</span></span>      | <span data-ttu-id="cadae-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="cadae-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="cadae-131">Verlauf</span><span class="sxs-lookup"><span data-stu-id="cadae-131">History</span></span>      | <span data-ttu-id="cadae-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="cadae-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="cadae-133">Suche</span><span class="sxs-lookup"><span data-stu-id="cadae-133">Search</span></span>       | <span data-ttu-id="cadae-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="cadae-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="cadae-135">Diese Methode ist derzeit in Microsoft Visual Basic nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cadae-135">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="cadae-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cadae-136">Examples</span></span>

<span data-ttu-id="cadae-137">In den folgenden Beispielen wird die Verwendung von **Shell.ShowBrowserBar** zum Anzeigen der Browserleiste **Favoriten** gezeigt.</span><span class="sxs-lookup"><span data-stu-id="cadae-137">The following examples show the use of **Shell.ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="cadae-138">Die Verwendung wird für JScript und VBScript angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cadae-138">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="cadae-139">Jscript:</span><span class="sxs-lookup"><span data-stu-id="cadae-139">JScript:</span></span>


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



<span data-ttu-id="cadae-140">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="cadae-140">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="cadae-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cadae-141">Requirements</span></span>



| <span data-ttu-id="cadae-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cadae-142">Requirement</span></span> | <span data-ttu-id="cadae-143">Wert</span><span class="sxs-lookup"><span data-stu-id="cadae-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cadae-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cadae-144">Minimum supported client</span></span><br/> | <span data-ttu-id="cadae-145">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cadae-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cadae-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cadae-146">Minimum supported server</span></span><br/> | <span data-ttu-id="cadae-147">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cadae-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="cadae-148">Header</span><span class="sxs-lookup"><span data-stu-id="cadae-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="cadae-149"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="cadae-149"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="cadae-150">Idl</span><span class="sxs-lookup"><span data-stu-id="cadae-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cadae-151"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="cadae-151"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="cadae-152">DLL</span><span class="sxs-lookup"><span data-stu-id="cadae-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cadae-153"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="cadae-153"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
