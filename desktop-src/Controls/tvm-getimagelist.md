---
title: TVM_GETIMAGELIST Meldung (kommstrg. h)
description: Ruft das Handle für die normale oder Zustands Bildliste ab, die einem Strukturansicht-Steuerelement zugeordnet ist. Sie können diese Nachricht explizit oder mithilfe des TreeView \_ GetImageList-Makros senden.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- Windows-Steuerelemente für TVM_GETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743392"
---
# <a name="tvm_getimagelist-message"></a><span data-ttu-id="2917f-105">TVM \_ GetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="2917f-105">TVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="2917f-106">Ruft das Handle für die normale oder Zustands Bildliste ab, die einem Strukturansicht-Steuerelement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2917f-106">Retrieves the handle to the normal or state image list associated with a tree-view control.</span></span> <span data-ttu-id="2917f-107">Sie können diese Nachricht explizit oder mithilfe des [**TreeView \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="2917f-107">You can send this message explicitly or by using the [**TreeView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2917f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2917f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2917f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2917f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2917f-110">Typ der abzurufenden Bildliste.</span><span class="sxs-lookup"><span data-stu-id="2917f-110">Type of image list to retrieve.</span></span> <span data-ttu-id="2917f-111">Dieser Parameter kann einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="2917f-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="2917f-112">Wert</span><span class="sxs-lookup"><span data-stu-id="2917f-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="2917f-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2917f-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="2917f-114"><dt>**tvsil \_ Normal**</dt></span><span class="sxs-lookup"><span data-stu-id="2917f-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="2917f-115">Gibt die normale Bildliste an, die ausgewählte, nicht ausgewählte und Überlagerungs Bilder für die Elemente eines Strukturansicht-Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="2917f-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="2917f-116"><dt>**tvsil- \_ Status**</dt></span><span class="sxs-lookup"><span data-stu-id="2917f-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="2917f-117">Gibt die Status Bild Liste an.</span><span class="sxs-lookup"><span data-stu-id="2917f-117">Indicates the state image list.</span></span> <span data-ttu-id="2917f-118">Sie können Zustands Bilder verwenden, um Anwendungs definierte Element Zustände anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2917f-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="2917f-119">Links neben dem ausgewählten oder nicht ausgewählten Bild eines Elements wird ein Status Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2917f-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2917f-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2917f-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2917f-121">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2917f-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2917f-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2917f-122">Return value</span></span>

<span data-ttu-id="2917f-123">Gibt ein HIMAGELIST-Handle für die angegebene Bildliste zurück.</span><span class="sxs-lookup"><span data-stu-id="2917f-123">Returns an HIMAGELIST handle to the specified image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="2917f-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2917f-124">Requirements</span></span>



| <span data-ttu-id="2917f-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2917f-125">Requirement</span></span> | <span data-ttu-id="2917f-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2917f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2917f-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2917f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2917f-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2917f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2917f-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2917f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2917f-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2917f-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2917f-131">Header</span><span class="sxs-lookup"><span data-stu-id="2917f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2917f-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2917f-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2917f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2917f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2917f-134">**TVM \_ SetImageList**</span><span class="sxs-lookup"><span data-stu-id="2917f-134">**TVM\_SETIMAGELIST**</span></span>](tvm-setimagelist.md)
</dt> </dl>

 

 





