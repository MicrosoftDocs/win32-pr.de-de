---
title: Webviewfoldercontents. SelectItem-Methode (Shldisp. h)
description: Legt den Auswahl Zustand eines Elements in der Ansicht fest.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- SelectItem-Methode Legacy Windows-Umgebungs Features
- SelectItem-Methode Legacy-Windows-Umgebungs Features, webviewfoldercontents-Objekt
- Webviewfoldercontents-Objekt Legacy Funktionen der Windows-Umgebung, SelectItem-Methode
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
ms.openlocfilehash: e491fb27db2d6e1e9b449be4aa2924684021539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339935"
---
# <a name="webviewfoldercontentsselectitem-method"></a><span data-ttu-id="d7b83-106">Webviewfoldercontents. SelectItem-Methode</span><span class="sxs-lookup"><span data-stu-id="d7b83-106">WebViewFolderContents.SelectItem method</span></span>

<span data-ttu-id="d7b83-107">Legt den Auswahl Zustand eines Elements in der Ansicht fest.</span><span class="sxs-lookup"><span data-stu-id="d7b83-107">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7b83-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7b83-108">Syntax</span></span>


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="d7b83-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7b83-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7b83-110">*vitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7b83-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7b83-111">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="d7b83-111">Type: \**Variant\** _</span></span>

<span data-ttu-id="d7b83-112">Das [_ *folderItem* \*](../shell/folderitem.md) -Objekt, für das der Auswahl Zustand festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d7b83-112">The [_ *FolderItem*\*](../shell/folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="d7b83-113">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7b83-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7b83-114">Type: **Integer**</span><span class="sxs-lookup"><span data-stu-id="d7b83-114">Type: **Integer**</span></span>

<span data-ttu-id="d7b83-115">Ein Satz von Flags, die den neuen Auswahl Zustand angeben.</span><span class="sxs-lookup"><span data-stu-id="d7b83-115">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="d7b83-116">Dabei kann es sich um einen oder mehrere der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="d7b83-116">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="d7b83-117"> (0)</span><span class="sxs-lookup"><span data-stu-id="d7b83-117">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d7b83-118">Deaktivieren Sie das Element.</span><span class="sxs-lookup"><span data-stu-id="d7b83-118">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="d7b83-119">(1)</span><span class="sxs-lookup"><span data-stu-id="d7b83-119">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d7b83-120">Wählen Sie das Element aus.</span><span class="sxs-lookup"><span data-stu-id="d7b83-120">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="d7b83-121">(3)</span><span class="sxs-lookup"><span data-stu-id="d7b83-121">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d7b83-122">Versetzen Sie das Element in den Bearbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="d7b83-122">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="d7b83-123">(4)</span><span class="sxs-lookup"><span data-stu-id="d7b83-123">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d7b83-124">Deaktivieren Sie alle Elemente außer dem angegebenen Element.</span><span class="sxs-lookup"><span data-stu-id="d7b83-124">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="d7b83-125">(8)</span><span class="sxs-lookup"><span data-stu-id="d7b83-125">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d7b83-126">Stellen Sie sicher, dass das Element in der Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7b83-126">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="d7b83-127">(16)</span><span class="sxs-lookup"><span data-stu-id="d7b83-127">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d7b83-128">Gibt dem Element den Fokus.</span><span class="sxs-lookup"><span data-stu-id="d7b83-128">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7b83-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7b83-129">Return value</span></span>

<span data-ttu-id="d7b83-130">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d7b83-130">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d7b83-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7b83-131">Examples</span></span>

<span data-ttu-id="d7b83-132">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode für JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="d7b83-132">The following example shows the proper usage of this method for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d7b83-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7b83-133">Requirements</span></span>



| <span data-ttu-id="d7b83-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7b83-134">Requirement</span></span> | <span data-ttu-id="d7b83-135">Wert</span><span class="sxs-lookup"><span data-stu-id="d7b83-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b83-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7b83-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b83-137">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7b83-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d7b83-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7b83-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b83-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7b83-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d7b83-140">Header</span><span class="sxs-lookup"><span data-stu-id="d7b83-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7b83-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7b83-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d7b83-142">IDL</span><span class="sxs-lookup"><span data-stu-id="d7b83-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7b83-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7b83-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d7b83-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d7b83-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7b83-145"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="d7b83-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

