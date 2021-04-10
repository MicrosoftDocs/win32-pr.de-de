---
title: EM_SETMARGINS Meldung (Winuser. h)
description: Legt die Breite des linken und rechten Rands für ein Bearbeitungs Steuerelement fest. Die Meldung zeichnet das Steuerelement neu, um die neuen Ränder widerzuspiegeln. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 23eb6c9e-3cf9-4c90-b33e-8da84034b49b
keywords:
- Windows-Steuerelemente für EM_SETMARGINS Meldung
topic_type:
- apiref
api_name:
- EM_SETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c68f3394234a6f86b3c5ff69622b86e61afc556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956641"
---
# <a name="em_setmargins-message"></a><span data-ttu-id="d3812-106">EM- \_ setMargin-Meldung</span><span class="sxs-lookup"><span data-stu-id="d3812-106">EM\_SETMARGINS message</span></span>

<span data-ttu-id="d3812-107">Legt die Breite des linken und rechten Rands für ein Bearbeitungs Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="d3812-107">Sets the widths of the left and right margins for an edit control.</span></span> <span data-ttu-id="d3812-108">Die Meldung zeichnet das Steuerelement neu, um die neuen Ränder widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="d3812-108">The message redraws the control to reflect the new margins.</span></span> <span data-ttu-id="d3812-109">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="d3812-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3812-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3812-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3812-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3812-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3812-112">Die festzulegenden Ränder.</span><span class="sxs-lookup"><span data-stu-id="d3812-112">The margins to set.</span></span> <span data-ttu-id="d3812-113">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d3812-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="d3812-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d3812-114">Value</span></span>                                                                                                                                                            | <span data-ttu-id="d3812-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d3812-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EC_LEFTMARGIN"></span><span id="ec_leftmargin"></span><dl> <span data-ttu-id="d3812-116"><dt>**EC- \_ LeftMargin**</dt></span><span class="sxs-lookup"><span data-stu-id="d3812-116"><dt>**EC\_LEFTMARGIN**</dt></span></span> </dl>    | <span data-ttu-id="d3812-117">Legt den linken Rand fest.</span><span class="sxs-lookup"><span data-stu-id="d3812-117">Sets the left margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="EC_RIGHTMARGIN"></span><span id="ec_rightmargin"></span><dl> <span data-ttu-id="d3812-118"><dt>**EC- \_ RightMargin**</dt></span><span class="sxs-lookup"><span data-stu-id="d3812-118"><dt>**EC\_RIGHTMARGIN**</dt></span></span> </dl> | <span data-ttu-id="d3812-119">Legt den rechten Rand fest.</span><span class="sxs-lookup"><span data-stu-id="d3812-119">Sets the right margin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="EC_USEFONTINFO"></span><span id="ec_usefontinfo"></span><dl> <span data-ttu-id="d3812-120"><dt>**EC \_ usefontinfo**</dt></span><span class="sxs-lookup"><span data-stu-id="d3812-120"><dt>**EC\_USEFONTINFO**</dt></span></span> </dl> | <span data-ttu-id="d3812-121">**Rich Edit-Steuerelemente:** Legt den linken und rechten Rand auf eine schmale Breite fest, die mithilfe der Textmetrik der aktuellen Schriftart des Steuer Elements berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="d3812-121">**Rich edit controls:** Sets the left and right margins to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="d3812-122">Wenn für das Steuerelement keine Schriftart festgelegt wurde, werden die Ränder auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3812-122">If no font has been set for the control, the margins are set to zero.</span></span> <span data-ttu-id="d3812-123">Der *LPARAM* -Parameter wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d3812-123">The *lParam* parameter is ignored.</span></span> <br/> <span data-ttu-id="d3812-124">Steuer **Elemente bearbeiten:** Der Wert " **EC \_ usefontinfo** " kann nicht im *wParam* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3812-124">**Edit controls:** The **EC\_USEFONTINFO** value cannot be used in the *wParam* parameter.</span></span> <span data-ttu-id="d3812-125">Sie kann nur im *LPARAM* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3812-125">It can only be used in the *lParam* parameter.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d3812-126">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3812-126">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3812-127">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die neue Breite des linken Rands in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="d3812-127">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the new width of the left margin, in pixels.</span></span> <span data-ttu-id="d3812-128">Dieser Wert wird ignoriert, wenn der **EC- \_ LeftMargin** von *wParam* nicht eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d3812-128">This value is ignored if *wParam* does not include **EC\_LEFTMARGIN**.</span></span>

<span data-ttu-id="d3812-129">**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 3,0 und höher:** Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) kann den Wert des **EC- \_ usefontinfo** angeben, um den linken Rand auf eine schmale Breite festzulegen, die mithilfe der Textmetrik der aktuellen Schriftart des Steuer Elements berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="d3812-129">**Edit controls and Rich Edit 3.0 and later:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the left margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="d3812-130">Wenn für das Steuerelement keine Schriftart festgelegt wurde, wird der Rand auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3812-130">If no font has been set for the control, the margin is set to zero.</span></span>

<span data-ttu-id="d3812-131">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die neue Breite des rechten Rands in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="d3812-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the new width of the right margin, in pixels.</span></span> <span data-ttu-id="d3812-132">Dieser Wert wird ignoriert, wenn *wParam* den **EC- \_ RightMargin** nicht einschließt.</span><span class="sxs-lookup"><span data-stu-id="d3812-132">This value is ignored if *wParam* does not include **EC\_RIGHTMARGIN**.</span></span>

<span data-ttu-id="d3812-133">**Bearbeitungs Steuerelemente und umfangreiche Bearbeitung 3,0 und höher:** Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) kann den Wert des **EC- \_ usefontinfo** angeben, um den rechten Rand auf eine schmale Breite festzulegen, die mithilfe der Textmetrik der aktuellen Schriftart des Steuer Elements berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="d3812-133">**Edit controls and Rich Edit 3.0 and later:** The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) can specify the **EC\_USEFONTINFO** value to set the right margin to a narrow width calculated using the text metrics of the control's current font.</span></span> <span data-ttu-id="d3812-134">Wenn für das Steuerelement keine Schriftart festgelegt wurde, wird der Rand auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3812-134">If no font has been set for the control, the margin is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3812-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3812-135">Return value</span></span>

<span data-ttu-id="d3812-136">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d3812-136">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3812-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3812-137">Remarks</span></span>

<span data-ttu-id="d3812-138">Steuer **Elemente bearbeiten:** Sie können " **EC \_ usefontinfo** " nicht im *wParam* -Parameter verwenden, aber Sie können es im *LPARAM* -Parameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="d3812-138">**Edit controls:** You cannot use **EC\_USEFONTINFO** in the *wParam* parameter, but you can use it in the *lParam* parameter.</span></span>

<span data-ttu-id="d3812-139">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d3812-139">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="d3812-140">Alle Rich Edit-Versionen unterstützen die Verwendung von " **EC \_ usefontinfo** " im *wParam* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="d3812-140">All rich edit versions support the use of **EC\_USEFONTINFO** in the *wParam* parameter.</span></span> <span data-ttu-id="d3812-141">Allerdings unterstützt nur Microsoft Rich Edit 3,0 und höher die Verwendung von " **EC \_ usefontinfo** " im *LPARAM* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="d3812-141">However, only Microsoft Rich Edit 3.0 and later support the use of **EC\_USEFONTINFO** in the *lParam* parameter.</span></span> <span data-ttu-id="d3812-142">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="d3812-142">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3812-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3812-143">Requirements</span></span>



| <span data-ttu-id="d3812-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3812-144">Requirement</span></span> | <span data-ttu-id="d3812-145">Wert</span><span class="sxs-lookup"><span data-stu-id="d3812-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3812-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3812-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d3812-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3812-147">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d3812-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3812-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d3812-149">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3812-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3812-150">Header</span><span class="sxs-lookup"><span data-stu-id="d3812-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3812-151"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d3812-151"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3812-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3812-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3812-153">**EM- \_ getMargin**</span><span class="sxs-lookup"><span data-stu-id="d3812-153">**EM\_GETMARGINS**</span></span>](em-getmargins.md)
</dt> </dl>

 

