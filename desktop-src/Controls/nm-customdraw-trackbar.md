---
title: NM_CUSTOMDRAW (TrackBar)-Benachrichtigungs Code (kommctrl. h)
description: Wird von einem TrackBar-Steuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- NM_CUSTOMDRAW (TrackBar)-Benachrichtigungs Code Windows-Steuerelemente
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68ebbffd531fb44e2491d72954ce111db208f2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106622"
---
# <a name="nm_customdraw-trackbar-notification-code"></a><span data-ttu-id="dc74b-105">NM \_ (TrackBar)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="dc74b-105">NM\_CUSTOMDRAW (trackbar) notification code</span></span>

<span data-ttu-id="dc74b-106">Wird von einem TrackBar-Steuerelement gesendet, um die übergeordneten Fenster über Zeichnungsvorgänge zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="dc74b-106">Sent by a trackbar control to notify its parent windows about drawing operations.</span></span> <span data-ttu-id="dc74b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="dc74b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="dc74b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc74b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc74b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc74b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc74b-110">Ein Zeiger auf eine [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="dc74b-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="dc74b-111">Der **dwitemspec** -Member dieser Struktur enthält einen der [benutzerdefinierten zeichnen-Werte](custom-draw-values.md) , der angibt, welcher Teil des Steuer Elements gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="dc74b-111">The **dwItemSpec** member of this structure will contain one of the [Custom Draw Values](custom-draw-values.md) that indicates which part of the control is being drawn.</span></span> <span data-ttu-id="dc74b-112">TrackBar-Steuerelemente fügen die folgenden Werte in den **dwitemspec** -Member dieser-Struktur ein, um den Teil des zu zeichnenden Steuer Elements zu identifizieren:</span><span class="sxs-lookup"><span data-stu-id="dc74b-112">Trackbar controls insert the following values into the **dwItemSpec** member of this structure to identify the portion of the control being drawn:</span></span>



| <span data-ttu-id="dc74b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="dc74b-113">Value</span></span>                                                                                                                                                      | <span data-ttu-id="dc74b-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dc74b-114">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="dc74b-115"><dt>**TBCD- \_ Kanal**</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-115"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="dc74b-116">Gibt den Kanal an, entlang dem der Ziehpunkt des TrackBar-Steuer Elements bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="dc74b-116">Identifies the channel that the trackbar control's thumb marker slides along.</span></span> <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="dc74b-117"><dt>**TBCD- \_ Thumb**</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-117"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="dc74b-118">Identifiziert den Zieh Punkt Marker des TrackBar-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="dc74b-118">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="dc74b-119">Dies ist der Teil des-Steuer Elements, den der Benutzer verschiebt.</span><span class="sxs-lookup"><span data-stu-id="dc74b-119">This is the portion of the control that the user moves.</span></span> <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="dc74b-120"><dt>**TBCD- \_ tik**</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-120"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="dc74b-121">Identifiziert die Inkrement-Teil Striche, die entlang der Kante des TrackBar-Steuer Elements angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dc74b-121">Identifies the increment tick marks that appear along the edge of the trackbar control.</span></span> <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc74b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc74b-122">Return value</span></span>

<span data-ttu-id="dc74b-123">Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab.</span><span class="sxs-lookup"><span data-stu-id="dc74b-123">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="dc74b-124">Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt.</span><span class="sxs-lookup"><span data-stu-id="dc74b-124">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="dc74b-125">Sie müssen einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dc74b-125">You must return one of the following values.</span></span>



| <span data-ttu-id="dc74b-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dc74b-126">Return code</span></span>                                                                                            | <span data-ttu-id="dc74b-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc74b-127">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc74b-128"><dt>**cdrf \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-128"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="dc74b-129">Das Steuerelement zeichnet sich selbst auf.</span><span class="sxs-lookup"><span data-stu-id="dc74b-129">The control will draw itself.</span></span> <span data-ttu-id="dc74b-130">Es werden keine zusätzlichen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes für diesen Zeichnungs Kreis gesendet.</span><span class="sxs-lookup"><span data-stu-id="dc74b-130">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="dc74b-131">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="dc74b-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="dc74b-132"><dt>**cdrf \_ notiteyitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-132"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="dc74b-133">Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="dc74b-133">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="dc74b-134">Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="dc74b-134">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="dc74b-135">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="dc74b-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                         |
| <dl> <span data-ttu-id="dc74b-136"><dt>**cdrf \_ notifyposterase**</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-136"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="dc74b-137">Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="dc74b-137">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="dc74b-138">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="dc74b-138">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="dc74b-139"><dt>**cdrf \_ notifypostpaint**</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-139"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="dc74b-140">Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="dc74b-140">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="dc74b-141">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="dc74b-141">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="dc74b-142"><dt>**cdrf \_ notifysubitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-142"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="dc74b-143">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="dc74b-143">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="dc74b-144">Das-Steuerelement benachrichtigt das übergeordnete Element, wenn ein Listen Ansichts-Unterelement gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="dc74b-144">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="dc74b-145">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="dc74b-145">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="dc74b-146"><dt>**cdrf \_ newFont**</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-146"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="dc74b-147">Ihre Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart.</span><span class="sxs-lookup"><span data-stu-id="dc74b-147">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="dc74b-148">Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="dc74b-148">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="dc74b-149">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="dc74b-149">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="dc74b-150"><dt>**cdrf \_ skipdefault**</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-150"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="dc74b-151">Die Anwendung hat das Element manuell gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dc74b-151">Your application drew the item manually.</span></span> <span data-ttu-id="dc74b-152">Das-Steuerelement zeichnet das Element nicht.</span><span class="sxs-lookup"><span data-stu-id="dc74b-152">The control will not draw the item.</span></span> <span data-ttu-id="dc74b-153">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="dc74b-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="dc74b-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc74b-154">Requirements</span></span>



| <span data-ttu-id="dc74b-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc74b-155">Requirement</span></span> | <span data-ttu-id="dc74b-156">Wert</span><span class="sxs-lookup"><span data-stu-id="dc74b-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc74b-157">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc74b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="dc74b-158">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc74b-158">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc74b-159">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc74b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="dc74b-160">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc74b-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc74b-161">Header</span><span class="sxs-lookup"><span data-stu-id="dc74b-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc74b-162"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc74b-162"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc74b-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc74b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc74b-164">Verwenden benutzerdefinierter zeichnen</span><span class="sxs-lookup"><span data-stu-id="dc74b-164">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





