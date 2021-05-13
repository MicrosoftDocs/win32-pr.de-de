---
description: Fügt dem Microsoft-Konto ein Element Active Desktop.
title: ShellUIHelper.AddDesktopComponent-Methode (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: 2edaa79bd62dcee40e4f197700d2128cb0b2070d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842461"
---
# <a name="shelluihelperadddesktopcomponent-method"></a><span data-ttu-id="86897-103">ShellUIHelper.AddDesktopComponent-Methode</span><span class="sxs-lookup"><span data-stu-id="86897-103">ShellUIHelper.AddDesktopComponent method</span></span>

<span data-ttu-id="86897-104">Fügt dem Microsoft-Konto ein Element Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="86897-104">Adds an item to the Microsoft Active Desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="86897-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="86897-105">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a><span data-ttu-id="86897-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86897-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86897-107">*sURL* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="86897-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86897-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="86897-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="86897-109">Ein **Zeichenfolgenwert,** der die URL des neuen Favoritenelements angibt.</span><span class="sxs-lookup"><span data-stu-id="86897-109">A **String** value that specifies the URL of the new favorite item.</span></span>

</dd> <dt>

<span data-ttu-id="86897-110">*sType* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="86897-110">*sType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86897-111">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="86897-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="86897-112">Ein **Zeichenfolgenwert,** der den Typ des hinzugefügten Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="86897-112">A **String** value that specifies the type of item being added.</span></span> <span data-ttu-id="86897-113">Dies kann einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="86897-113">This can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="86897-114">(Bild)</span><span class="sxs-lookup"><span data-stu-id="86897-114">(image)</span></span>


</dt> <dd>

<span data-ttu-id="86897-115">Die Komponente ist ein Bild.</span><span class="sxs-lookup"><span data-stu-id="86897-115">The component is an image.</span></span>

</dd> <dt>



 <span data-ttu-id="86897-116">(Website)</span><span class="sxs-lookup"><span data-stu-id="86897-116">(website)</span></span>


</dt> <dd>

<span data-ttu-id="86897-117">Die Komponente ist eine Website.</span><span class="sxs-lookup"><span data-stu-id="86897-117">The component is a website.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="86897-118">*Links* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="86897-118">*Left* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86897-119">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="86897-119">Type: **Variant**</span></span>

<span data-ttu-id="86897-120">Die Position des linken Rands der Komponente in Bildschirmkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="86897-120">The position of the left edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="86897-121">*Oben* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="86897-121">*Top* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86897-122">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="86897-122">Type: **Variant**</span></span>

<span data-ttu-id="86897-123">Die Position des oberen Rands der Komponente in Bildschirmkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="86897-123">The position of the top edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="86897-124">*Breite* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="86897-124">*Width* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86897-125">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="86897-125">Type: **Variant**</span></span>

<span data-ttu-id="86897-126">Die Breite der Komponente in Bildschirmeinheiten.</span><span class="sxs-lookup"><span data-stu-id="86897-126">The width of the component, in screen units.</span></span>

</dd> <dt>

<span data-ttu-id="86897-127">*Höhe* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="86897-127">*Height* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="86897-128">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="86897-128">Type: **Variant**</span></span>

<span data-ttu-id="86897-129">Die Höhe der Komponente in Bildschirmeinheiten.</span><span class="sxs-lookup"><span data-stu-id="86897-129">The height of the component, in screen units.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="86897-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86897-130">Examples</span></span>

<span data-ttu-id="86897-131">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript, das in HTML und Visual Basic eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="86897-131">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="86897-132">Jscript:</span><span class="sxs-lookup"><span data-stu-id="86897-132">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



<span data-ttu-id="86897-133">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="86897-133">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="86897-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86897-134">Requirements</span></span>



| <span data-ttu-id="86897-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86897-135">Requirement</span></span> | <span data-ttu-id="86897-136">Wert</span><span class="sxs-lookup"><span data-stu-id="86897-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86897-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86897-137">Minimum supported client</span></span><br/> | <span data-ttu-id="86897-138">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86897-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="86897-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86897-139">Minimum supported server</span></span><br/> | <span data-ttu-id="86897-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86897-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="86897-141">Header</span><span class="sxs-lookup"><span data-stu-id="86897-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="86897-142"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="86897-142"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="86897-143">DLL</span><span class="sxs-lookup"><span data-stu-id="86897-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86897-144"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="86897-144"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
