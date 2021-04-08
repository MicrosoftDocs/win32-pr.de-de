---
title: EM_GETZOOM Meldung (RichEdit. h)
description: Ruft das aktuelle Zoomverhältnis ab. Die Zoom-Ration liegt immer zwischen 1/64 und 64. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- Windows-Steuerelemente für EM_GETZOOM Meldung
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740296"
---
# <a name="em_getzoom-message"></a><span data-ttu-id="522e2-106">EM \_ getzoom-Meldung</span><span class="sxs-lookup"><span data-stu-id="522e2-106">EM\_GETZOOM message</span></span>

<span data-ttu-id="522e2-107">Ruft das aktuelle Zoomverhältnis eines mehrzeiligen Bearbeitungs Steuer Elements oder eines Rich-Edit-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="522e2-107">Gets the current zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="522e2-108">Die Zoom-Ration liegt immer zwischen 1/64 und 64.</span><span class="sxs-lookup"><span data-stu-id="522e2-108">The zoom ration is always between 1/64 and 64.</span></span>

## <a name="parameters"></a><span data-ttu-id="522e2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="522e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="522e2-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="522e2-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="522e2-111">Empfängt den Zähler des Zoom Verhältnisses.</span><span class="sxs-lookup"><span data-stu-id="522e2-111">Receives the numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="522e2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="522e2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="522e2-113">Empfängt den Nenner des Zoom Verhältnisses.</span><span class="sxs-lookup"><span data-stu-id="522e2-113">Receives the denominator of the zoom ratio.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="522e2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="522e2-114">Return value</span></span>

<span data-ttu-id="522e2-115">Die Meldung gibt **true** zurück, wenn die Nachricht verarbeitet wird. Dies ist, wenn sowohl *wParam* als auch *LPARAM* nicht **null** sind.</span><span class="sxs-lookup"><span data-stu-id="522e2-115">The message returns **TRUE** if message is processed, which it will be if both *wParam* and *lParam* are not **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="522e2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="522e2-116">Remarks</span></span>

<span data-ttu-id="522e2-117">**Bearbeiten:** Wird in Windows 10 1809 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="522e2-117">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="522e2-118">Das Bearbeitungs Steuerelement muss über den erweiterten Stil des **es \_ Ex \_** -Formats verfügen, damit diese Nachricht wirksam wird. Weitere Informationen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="522e2-118">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="522e2-119">Weitere Informationen zum Bearbeitungs Steuerelement finden Sie unter [Edit Controls](edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="522e2-119">For information about the edit control, see [Edit Controls](edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="522e2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="522e2-120">Requirements</span></span>



| <span data-ttu-id="522e2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="522e2-121">Requirement</span></span> | <span data-ttu-id="522e2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="522e2-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="522e2-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="522e2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="522e2-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="522e2-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="522e2-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="522e2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="522e2-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="522e2-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="522e2-127">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="522e2-127">Redistributable</span></span><br/>          | <span data-ttu-id="522e2-128">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="522e2-128">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="522e2-129">Header</span><span class="sxs-lookup"><span data-stu-id="522e2-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="522e2-130"><dt>RichEdit. h/kommctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="522e2-130"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="522e2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="522e2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522e2-132">**EM- \_ setzoom**</span><span class="sxs-lookup"><span data-stu-id="522e2-132">**EM\_SETZOOM**</span></span>](em-setzoom.md)
</dt> </dl>

 

 





