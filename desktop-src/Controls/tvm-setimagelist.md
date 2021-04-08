---
title: TVM_SETIMAGELIST Meldung (kommstrg. h)
description: Legt die normale oder Zustands Bildliste für ein Strukturansicht-Steuerelement fest und zeichnet das Steuerelement mithilfe der neuen Bilder neu. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ SetImageList-Makros senden.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- Windows-Steuerelemente für TVM_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741553"
---
# <a name="tvm_setimagelist-message"></a><span data-ttu-id="59450-105">TVM \_ SetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="59450-105">TVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="59450-106">Legt die normale oder Zustands Bildliste für ein Strukturansicht-Steuerelement fest und zeichnet das Steuerelement mithilfe der neuen Bilder neu.</span><span class="sxs-lookup"><span data-stu-id="59450-106">Sets the normal or state image list for a tree-view control and redraws the control using the new images.</span></span> <span data-ttu-id="59450-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="59450-107">You can send this message explicitly or by using the [**TreeView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="59450-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="59450-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59450-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59450-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59450-110">Typ der festzulegenden Bildliste.</span><span class="sxs-lookup"><span data-stu-id="59450-110">Type of image list to set.</span></span> <span data-ttu-id="59450-111">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="59450-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="59450-112">Wert</span><span class="sxs-lookup"><span data-stu-id="59450-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="59450-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="59450-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="59450-114"><dt>**tvsil \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="59450-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="59450-115">Gibt die normale Bildliste an, die ausgewählte, nicht ausgewählte und Überlagerungs Bilder für die Elemente eines Strukturansicht-Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="59450-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="59450-116"><dt>**tvsil- \_ Status**</dt></span><span class="sxs-lookup"><span data-stu-id="59450-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="59450-117">Gibt die Status Bild Liste an.</span><span class="sxs-lookup"><span data-stu-id="59450-117">Indicates the state image list.</span></span> <span data-ttu-id="59450-118">Sie können Zustands Bilder verwenden, um Anwendungs definierte Element Zustände anzugeben.</span><span class="sxs-lookup"><span data-stu-id="59450-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="59450-119">Links neben dem ausgewählten oder nicht ausgewählten Bild eines Elements wird ein Status Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="59450-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="59450-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59450-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59450-121">Handle für die Bildliste.</span><span class="sxs-lookup"><span data-stu-id="59450-121">Handle to the image list.</span></span> <span data-ttu-id="59450-122">Wenn *LPARAM* den Wert **null** hat, entfernt die Meldung die angegebene Bildliste aus dem Strukturansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="59450-122">If *lParam* is **NULL**, the message removes the specified image list from the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59450-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59450-123">Return value</span></span>

<span data-ttu-id="59450-124">Gibt ggf. das Handle für die vorherige Bildliste zurück, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="59450-124">Returns the handle to the previous image list, if any, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="59450-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59450-125">Remarks</span></span>

<span data-ttu-id="59450-126">Das Strukturansicht-Steuerelement zerstört nicht die mit dieser Meldung angegebene Bildliste.</span><span class="sxs-lookup"><span data-stu-id="59450-126">The tree-view control will not destroy the image list specified with this message.</span></span> <span data-ttu-id="59450-127">Die Anwendung muss die Bildliste zerstören, wenn Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="59450-127">Your application must destroy the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="59450-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59450-128">Requirements</span></span>



| <span data-ttu-id="59450-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59450-129">Requirement</span></span> | <span data-ttu-id="59450-130">Wert</span><span class="sxs-lookup"><span data-stu-id="59450-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59450-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59450-131">Minimum supported client</span></span><br/> | <span data-ttu-id="59450-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59450-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59450-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59450-133">Minimum supported server</span></span><br/> | <span data-ttu-id="59450-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59450-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59450-135">Header</span><span class="sxs-lookup"><span data-stu-id="59450-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="59450-136"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="59450-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59450-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59450-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59450-138">**TVM \_ GetImageList**</span><span class="sxs-lookup"><span data-stu-id="59450-138">**TVM\_GETIMAGELIST**</span></span>](tvm-getimagelist.md)
</dt> </dl>

 

 





