---
description: Legt den Auswahl Zustand eines Elements in der Ansicht fest.
title: Shellfolderview. SelectItem-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: d44633983075cdf22581bce05cfb7c073f422084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217690"
---
# <a name="shellfolderviewselectitem-method"></a><span data-ttu-id="58c04-103">Shellfolderview. SelectItem-Methode</span><span class="sxs-lookup"><span data-stu-id="58c04-103">ShellFolderView.SelectItem method</span></span>

<span data-ttu-id="58c04-104">Legt den Auswahl Zustand eines Elements in der Ansicht fest.</span><span class="sxs-lookup"><span data-stu-id="58c04-104">Sets the selection state of an item in the view.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c04-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58c04-105">Syntax</span></span>


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a><span data-ttu-id="58c04-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="58c04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58c04-107">*vitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58c04-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c04-108">Typ: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="58c04-108">Type: \**Variant\** _</span></span>

<span data-ttu-id="58c04-109">Das [_ *folderItem* \*](folderitem.md) -Objekt, für das der Auswahl Zustand festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="58c04-109">The [_ *FolderItem*\*](folderitem.md) object for which the selection state will be set.</span></span>

</dd> <dt>

<span data-ttu-id="58c04-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58c04-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58c04-111">Type: **Integer**</span><span class="sxs-lookup"><span data-stu-id="58c04-111">Type: **Integer**</span></span>

<span data-ttu-id="58c04-112">Ein Satz von Flags, die den neuen Auswahl Zustand angeben.</span><span class="sxs-lookup"><span data-stu-id="58c04-112">A set of flags that indicate the new selection state.</span></span> <span data-ttu-id="58c04-113">Dabei kann es sich um einen oder mehrere der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="58c04-113">This can be one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="58c04-114"> (0)</span><span class="sxs-lookup"><span data-stu-id="58c04-114">(0)</span></span>


</dt> <dd>

<span data-ttu-id="58c04-115">Deaktivieren Sie das Element.</span><span class="sxs-lookup"><span data-stu-id="58c04-115">Deselect the item.</span></span>

</dd> <dt>



 <span data-ttu-id="58c04-116">(1)</span><span class="sxs-lookup"><span data-stu-id="58c04-116">(1)</span></span>


</dt> <dd>

<span data-ttu-id="58c04-117">Wählen Sie das Element aus.</span><span class="sxs-lookup"><span data-stu-id="58c04-117">Select the item.</span></span>

</dd> <dt>



 <span data-ttu-id="58c04-118">(3)</span><span class="sxs-lookup"><span data-stu-id="58c04-118">(3)</span></span>


</dt> <dd>

<span data-ttu-id="58c04-119">Versetzen Sie das Element in den Bearbeitungsmodus.</span><span class="sxs-lookup"><span data-stu-id="58c04-119">Put the item in edit mode.</span></span>

</dd> <dt>



 <span data-ttu-id="58c04-120">(4)</span><span class="sxs-lookup"><span data-stu-id="58c04-120">(4)</span></span>


</dt> <dd>

<span data-ttu-id="58c04-121">Deaktivieren Sie alle Elemente außer dem angegebenen Element.</span><span class="sxs-lookup"><span data-stu-id="58c04-121">Deselect all but the specified item.</span></span>

</dd> <dt>



 <span data-ttu-id="58c04-122">(8)</span><span class="sxs-lookup"><span data-stu-id="58c04-122">(8)</span></span>


</dt> <dd>

<span data-ttu-id="58c04-123">Stellen Sie sicher, dass das Element in der Ansicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="58c04-123">Ensure the item is displayed in the view.</span></span>

</dd> <dt>



 <span data-ttu-id="58c04-124">(16)</span><span class="sxs-lookup"><span data-stu-id="58c04-124">(16)</span></span>


</dt> <dd>

<span data-ttu-id="58c04-125">Gibt dem Element den Fokus.</span><span class="sxs-lookup"><span data-stu-id="58c04-125">Give the item the focus.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58c04-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58c04-126">Return value</span></span>

<span data-ttu-id="58c04-127">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="58c04-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58c04-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58c04-128">Remarks</span></span>

<span data-ttu-id="58c04-129">[**FocusedItem**](shellfolderview-focuseditem.md) kann nur auf dem lokalen System aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="58c04-129">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="58c04-130">Es funktioniert nicht, wenn es auf einer Webseite über HTTP oder UNC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58c04-130">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="58c04-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58c04-131">Examples</span></span>

<span data-ttu-id="58c04-132">Das folgende Beispiel zeigt die ordnungsgemäße Verwendung dieser Methode in JScript Embedded in HTML.</span><span class="sxs-lookup"><span data-stu-id="58c04-132">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="58c04-133">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="58c04-133">Requirements</span></span>



| <span data-ttu-id="58c04-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58c04-134">Requirement</span></span> | <span data-ttu-id="58c04-135">Wert</span><span class="sxs-lookup"><span data-stu-id="58c04-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58c04-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58c04-136">Minimum supported client</span></span><br/> | <span data-ttu-id="58c04-137">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58c04-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="58c04-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58c04-138">Minimum supported server</span></span><br/> | <span data-ttu-id="58c04-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58c04-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="58c04-140">Header</span><span class="sxs-lookup"><span data-stu-id="58c04-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="58c04-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="58c04-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="58c04-142">IDL</span><span class="sxs-lookup"><span data-stu-id="58c04-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="58c04-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="58c04-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="58c04-144">DLL</span><span class="sxs-lookup"><span data-stu-id="58c04-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58c04-145"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="58c04-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




