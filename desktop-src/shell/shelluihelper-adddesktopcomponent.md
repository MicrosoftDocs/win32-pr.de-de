---
description: Fügt dem Microsoft Active Desktop ein Element hinzu.
title: Shelluihelper. adddesktopcomponent-Methode (Exdisp. h)
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
ms.openlocfilehash: d5234a0b43ea25c8ac931dc14ec90f7a6696ddfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980592"
---
# <a name="shelluihelperadddesktopcomponent-method"></a><span data-ttu-id="73be8-103">Shelluihelper. adddesktopcomponent-Methode</span><span class="sxs-lookup"><span data-stu-id="73be8-103">ShellUIHelper.AddDesktopComponent method</span></span>

<span data-ttu-id="73be8-104">Fügt dem Microsoft Active Desktop ein Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="73be8-104">Adds an item to the Microsoft Active Desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="73be8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73be8-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="73be8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="73be8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73be8-107">*sUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73be8-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73be8-108">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="73be8-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="73be8-109">Ein **Zeichen** folgen Wert, der die URL des neuen bevorzugten Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="73be8-109">A **String** value that specifies the URL of the new favorite item.</span></span>

</dd> <dt>

<span data-ttu-id="73be8-110">*sType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73be8-110">*sType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73be8-111">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="73be8-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="73be8-112">Ein **Zeichen** folgen Wert, der den Typ des hinzugefügten Elements angibt.</span><span class="sxs-lookup"><span data-stu-id="73be8-112">A **String** value that specifies the type of item being added.</span></span> <span data-ttu-id="73be8-113">Dies kann einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="73be8-113">This can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="73be8-114">Klang</span><span class="sxs-lookup"><span data-stu-id="73be8-114">(image)</span></span>


</dt> <dd>

<span data-ttu-id="73be8-115">Die Komponente ist ein Bild.</span><span class="sxs-lookup"><span data-stu-id="73be8-115">The component is an image.</span></span>

</dd> <dt>



 <span data-ttu-id="73be8-116">Website</span><span class="sxs-lookup"><span data-stu-id="73be8-116">(website)</span></span>


</dt> <dd>

<span data-ttu-id="73be8-117">Die Komponente ist eine Website.</span><span class="sxs-lookup"><span data-stu-id="73be8-117">The component is a website.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="73be8-118">*Links* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="73be8-118">*Left* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73be8-119">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="73be8-119">Type: **Variant**</span></span>

<span data-ttu-id="73be8-120">Die Position des linken Rands der Komponente in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="73be8-120">The position of the left edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="73be8-121">Nach *oben* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="73be8-121">*Top* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73be8-122">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="73be8-122">Type: **Variant**</span></span>

<span data-ttu-id="73be8-123">Die Position des oberen Rands der Komponente in Bildschirm Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="73be8-123">The position of the top edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="73be8-124">*Breite* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="73be8-124">*Width* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73be8-125">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="73be8-125">Type: **Variant**</span></span>

<span data-ttu-id="73be8-126">Die Breite der Komponente in Bildschirm Einheiten.</span><span class="sxs-lookup"><span data-stu-id="73be8-126">The width of the component, in screen units.</span></span>

</dd> <dt>

<span data-ttu-id="73be8-127">*Höhe* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="73be8-127">*Height* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="73be8-128">Typ: **Variant**</span><span class="sxs-lookup"><span data-stu-id="73be8-128">Type: **Variant**</span></span>

<span data-ttu-id="73be8-129">Die Höhe der Komponente in Bildschirm Einheiten.</span><span class="sxs-lookup"><span data-stu-id="73be8-129">The height of the component, in screen units.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="73be8-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73be8-130">Examples</span></span>

<span data-ttu-id="73be8-131">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript Embedded in HTML und Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="73be8-131">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="73be8-132">JScript</span><span class="sxs-lookup"><span data-stu-id="73be8-132">JScript:</span></span>


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



<span data-ttu-id="73be8-133">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="73be8-133">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="73be8-134">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="73be8-134">Requirements</span></span>



| <span data-ttu-id="73be8-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73be8-135">Requirement</span></span> | <span data-ttu-id="73be8-136">Wert</span><span class="sxs-lookup"><span data-stu-id="73be8-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73be8-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73be8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="73be8-138">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73be8-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="73be8-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73be8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="73be8-140">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73be8-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="73be8-141">Header</span><span class="sxs-lookup"><span data-stu-id="73be8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="73be8-142"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="73be8-142"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="73be8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="73be8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73be8-144"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="73be8-144"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
