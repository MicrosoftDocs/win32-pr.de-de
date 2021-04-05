---
title: EM_SETZOOM Meldung (RichEdit. h)
description: Legt das Zoomverhältnis fest. Das Verhältnis muss ein Wert zwischen 1/64 und 64 sein. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- Windows-Steuerelemente für EM_SETZOOM Meldung
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859009"
---
# <a name="em_setzoom-message"></a><span data-ttu-id="e0282-106">EM- \_ setzoom-Meldung</span><span class="sxs-lookup"><span data-stu-id="e0282-106">EM\_SETZOOM message</span></span>

<span data-ttu-id="e0282-107">Legt das Zoomverhältnis eines mehrzeiligen Bearbeitungs Steuer Elements oder eines Rich-Edit-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="e0282-107">Sets the zoom ratio for a multiline edit control or a rich edit control.</span></span> <span data-ttu-id="e0282-108">Das Verhältnis muss ein Wert zwischen 1/64 und 64 sein.</span><span class="sxs-lookup"><span data-stu-id="e0282-108">The ratio must be a value between 1/64 and 64.</span></span> <span data-ttu-id="e0282-109">Das Bearbeitungs Steuerelement muss über den erweiterten Stil des **es \_ Ex \_** -Formats verfügen, damit diese Nachricht wirksam wird. Weitere Informationen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="e0282-109">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="e0282-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0282-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0282-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0282-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0282-112">Zähler des Zoom Verhältnisses.</span><span class="sxs-lookup"><span data-stu-id="e0282-112">Numerator of the zoom ratio.</span></span>

</dd> <dt>

<span data-ttu-id="e0282-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0282-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0282-114">Der Nenner des Zoom Verhältnisses.</span><span class="sxs-lookup"><span data-stu-id="e0282-114">Denominator of the zoom ratio.</span></span> <span data-ttu-id="e0282-115">Diese Parameter können die folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e0282-115">These parameters can have the following values.</span></span>



| <span data-ttu-id="e0282-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e0282-116">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="e0282-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e0282-117">Meaning</span></span>                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <span data-ttu-id="e0282-118"><dt>**Beide 0**</dt></span><span class="sxs-lookup"><span data-stu-id="e0282-118"><dt>**Both 0**</dt></span></span> </dl>                                                                                                   | <span data-ttu-id="e0282-119">Deaktiviert das Zoomen mithilfe der EM-Datei (" **\_ setzoom** ") (das Zoomen kann weiterhin mithilfe von " [**txgetextent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)" erfolgen).</span><span class="sxs-lookup"><span data-stu-id="e0282-119">Turns off zooming by using the **EM\_SETZOOM** message (zooming may still occur using [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).</span></span><br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <span data-ttu-id="e0282-120"><dt>**1/64 < (wParam/LPARAM) < 64**</dt></span><span class="sxs-lookup"><span data-stu-id="e0282-120"><dt>**1/64 < (wParam / lParam) < 64**</dt></span></span> </dl> | <span data-ttu-id="e0282-121">Zoom Anzeige nach Zoomverhältnis Zähler/Nenner</span><span class="sxs-lookup"><span data-stu-id="e0282-121">Zooms display by the zoom ratio numerator/denominator</span></span><br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0282-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0282-122">Return value</span></span>

<span data-ttu-id="e0282-123">Wenn die neue Zoomeinstellung akzeptiert wird, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="e0282-123">If the new zoom setting is accepted, the return value is **TRUE**.</span></span>

<span data-ttu-id="e0282-124">Wenn die neue Zoomeinstellung nicht akzeptiert wird, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="e0282-124">If the new zoom setting is not accepted, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0282-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0282-125">Remarks</span></span>

<span data-ttu-id="e0282-126">**Bearbeiten:** Wird in Windows 10 1809 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0282-126">**Edit:** Supported in Windows 10 1809 and later.</span></span> <span data-ttu-id="e0282-127">Das Bearbeitungs Steuerelement muss über den erweiterten Stil des **es \_ Ex \_** -Formats verfügen, damit diese Nachricht wirksam wird. Weitere Informationen finden Sie unter [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="e0282-127">The edit control needs to have the **ES\_EX\_ZOOMABLE** extended style set, for this message to have an effect, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span> <span data-ttu-id="e0282-128">Weitere Informationen zum Bearbeitungs Steuerelement finden Sie unter [Edit Controls](about-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e0282-128">For information about the edit control, see [Edit Controls](about-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0282-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0282-129">Requirements</span></span>



| <span data-ttu-id="e0282-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0282-130">Requirement</span></span> | <span data-ttu-id="e0282-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e0282-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0282-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e0282-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e0282-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0282-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0282-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e0282-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e0282-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e0282-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0282-136">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="e0282-136">Redistributable</span></span><br/>          | <span data-ttu-id="e0282-137">Rich Edit 3,0</span><span class="sxs-lookup"><span data-stu-id="e0282-137">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="e0282-138">Header</span><span class="sxs-lookup"><span data-stu-id="e0282-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0282-139"><dt>RichEdit. h/kommctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0282-139"><dt>Richedit.h/Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0282-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0282-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0282-141">**EM \_ getzoom**</span><span class="sxs-lookup"><span data-stu-id="e0282-141">**EM\_GETZOOM**</span></span>](em-getzoom.md)
</dt> </dl>

 

 





