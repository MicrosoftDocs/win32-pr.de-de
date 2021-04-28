---
title: WebViewFolderContents.SelectItem-Methode (Shldisp.h)
description: 'WebViewFolderContents.SelectItem-Methode: Legt den Auswahlzustand eines Elements in der Ansicht fest.'
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- SelectItem-Methode – Ältere Windows-Umgebungsfeatures
- SelectItem-Methode Legacy-Windows-Umgebungsfeatures, WebViewFolderContents-Objekt
- WebViewFolderContents-Objekt Legacy-Windows-Umgebungsfeatures, SelectItem-Methode
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66e2d05c010199f05826df7ed4591e8c7c1723e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102609"
---
# <a name="webviewfoldercontentsselectitem-method"></a><span data-ttu-id="1b19c-106">WebViewFolderContents.SelectItem-Methode</span><span class="sxs-lookup"><span data-stu-id="1b19c-106">WebViewFolderContents.SelectItem method</span></span>

<span data-ttu-id="1b19c-107">Legt den Auswahlzustand eines Elements in der Ansicht fest.</span><span class="sxs-lookup"><span data-stu-id="1b19c-107">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b19c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b19c-108">Syntax</span></span>


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="1b19c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b19c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b19c-110">*vItem* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1b19c-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b19c-111">Typ: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="1b19c-111">Type: **Variant\***</span></span>

<span data-ttu-id="1b19c-112">Das [**FolderItem-Objekt,**](../shell/folderitem.md) für das der Auswahlzustand festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1b19c-112">The [**FolderItem**](../shell/folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="1b19c-113">*dwFlags* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1b19c-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b19c-114">Typ: **Ganze Zahl**</span><span class="sxs-lookup"><span data-stu-id="1b19c-114">Type: **Integer**</span></span>

<span data-ttu-id="1b19c-115">Ein Satz von Flags, die den neuen Auswahlzustand angeben.</span><span class="sxs-lookup"><span data-stu-id="1b19c-115">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="1b19c-116">Dies kann einer oder mehrere der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="1b19c-116">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="1b19c-117"> (0)</span><span class="sxs-lookup"><span data-stu-id="1b19c-117">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1b19c-118">Deaktivieren Sie das Element.</span><span class="sxs-lookup"><span data-stu-id="1b19c-118">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="1b19c-119">(1)</span><span class="sxs-lookup"><span data-stu-id="1b19c-119">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1b19c-120">Wählen Sie das Element aus.</span><span class="sxs-lookup"><span data-stu-id="1b19c-120">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="1b19c-121">(3)</span><span class="sxs-lookup"><span data-stu-id="1b19c-121">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1b19c-122">Versetzen Sie das Element in den Bearbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="1b19c-122">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="1b19c-123">(4)</span><span class="sxs-lookup"><span data-stu-id="1b19c-123">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1b19c-124">Deaktivieren Sie alle außer dem angegebenen Element.</span><span class="sxs-lookup"><span data-stu-id="1b19c-124">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="1b19c-125">(8)</span><span class="sxs-lookup"><span data-stu-id="1b19c-125">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1b19c-126">Stellen Sie sicher, dass das Element in der Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1b19c-126">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="1b19c-127">(16)</span><span class="sxs-lookup"><span data-stu-id="1b19c-127">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1b19c-128">Geben Sie dem Element den Fokus.</span><span class="sxs-lookup"><span data-stu-id="1b19c-128">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b19c-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b19c-129">Return value</span></span>

<span data-ttu-id="1b19c-130">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1b19c-130">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="1b19c-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b19c-131">Examples</span></span>

<span data-ttu-id="1b19c-132">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript, das in HTML eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="1b19c-132">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="1b19c-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b19c-133">Requirements</span></span>



| <span data-ttu-id="1b19c-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b19c-134">Requirement</span></span> | <span data-ttu-id="1b19c-135">Wert</span><span class="sxs-lookup"><span data-stu-id="1b19c-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b19c-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b19c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1b19c-137">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b19c-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1b19c-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b19c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1b19c-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b19c-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1b19c-140">Header</span><span class="sxs-lookup"><span data-stu-id="1b19c-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b19c-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="1b19c-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1b19c-142">Idl</span><span class="sxs-lookup"><span data-stu-id="1b19c-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b19c-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b19c-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1b19c-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1b19c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b19c-145"><dt>Shell32.dll (Version 4.71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1b19c-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

