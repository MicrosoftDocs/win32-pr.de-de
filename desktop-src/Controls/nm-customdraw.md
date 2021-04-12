---
title: NM_CUSTOMDRAW Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Steuer Elements über benutzerdefinierte Zeichnungsvorgänge. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- Windows-Steuerelemente für NM_CUSTOMDRAW Benachrichtigungs
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
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475156"
---
# <a name="nm_customdraw-notification-code"></a><span data-ttu-id="bb434-105">NM \_ customdraw-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="bb434-105">NM\_CUSTOMDRAW notification code</span></span>

<span data-ttu-id="bb434-106">Benachrichtigt das übergeordnete Fenster eines Steuer Elements über benutzerdefinierte Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="bb434-106">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="bb434-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="bb434-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a><span data-ttu-id="bb434-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb434-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb434-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb434-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb434-110">Ein Zeiger auf eine benutzerdefinierte Zeichnungs bezogene Struktur, die Informationen über den Zeichnungs Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="bb434-110">A pointer to a custom draw-related structure that contains information about the drawing operation.</span></span> <span data-ttu-id="bb434-111">In der folgenden Liste sind die Steuerelemente und ihre zugeordneten Strukturen angegeben.</span><span class="sxs-lookup"><span data-stu-id="bb434-111">The following list specifies the controls and their associated structures.</span></span>



| <span data-ttu-id="bb434-112">Control</span><span class="sxs-lookup"><span data-stu-id="bb434-112">Control</span></span>                     | <span data-ttu-id="bb434-113">Benutzerdefinierte Zeichnungs Struktur</span><span class="sxs-lookup"><span data-stu-id="bb434-113">Custom Draw Structure</span></span>                    |
|-----------------------------|------------------------------------------|
| <span data-ttu-id="bb434-114">Info Leiste, TrackBar und Header</span><span class="sxs-lookup"><span data-stu-id="bb434-114">Rebar, trackbar, and header</span></span> | [<span data-ttu-id="bb434-115">**Nmcustomdraw**</span><span class="sxs-lookup"><span data-stu-id="bb434-115">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| <span data-ttu-id="bb434-116">Listenansicht</span><span class="sxs-lookup"><span data-stu-id="bb434-116">List view</span></span>                   | [<span data-ttu-id="bb434-117">**Nmlvcustomdraw**</span><span class="sxs-lookup"><span data-stu-id="bb434-117">**NMLVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| <span data-ttu-id="bb434-118">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="bb434-118">Tooltip</span></span>                     | [<span data-ttu-id="bb434-119">**Nmttcustomdraw**</span><span class="sxs-lookup"><span data-stu-id="bb434-119">**NMTTCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| <span data-ttu-id="bb434-120">Strukturansicht</span><span class="sxs-lookup"><span data-stu-id="bb434-120">Tree view</span></span>                   | [<span data-ttu-id="bb434-121">**Nmtvcustomdraw**</span><span class="sxs-lookup"><span data-stu-id="bb434-121">**NMTVCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| <span data-ttu-id="bb434-122">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="bb434-122">Toolbar</span></span>                     | [<span data-ttu-id="bb434-123">**Nmtbcustomdraw**</span><span class="sxs-lookup"><span data-stu-id="bb434-123">**NMTBCUSTOMDRAW**</span></span>](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb434-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb434-124">Return value</span></span>

<span data-ttu-id="bb434-125">Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab.</span><span class="sxs-lookup"><span data-stu-id="bb434-125">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="bb434-126">Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt.</span><span class="sxs-lookup"><span data-stu-id="bb434-126">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="bb434-127">Sie müssen einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bb434-127">You must return one of the following values.</span></span>



| <span data-ttu-id="bb434-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bb434-128">Return code</span></span>                                                                                            | <span data-ttu-id="bb434-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb434-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb434-130"><dt>**cdrf \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="bb434-130"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="bb434-131">Das Steuerelement zeichnet sich selbst auf.</span><span class="sxs-lookup"><span data-stu-id="bb434-131">The control will draw itself.</span></span> <span data-ttu-id="bb434-132">Es werden keine zusätzlichen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes für diesen Zeichnungs Kreis gesendet.</span><span class="sxs-lookup"><span data-stu-id="bb434-132">It will not send additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="bb434-133">Dieses Flag kann nicht mit einem anderen Flag verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb434-133">This flag cannot be used with any other flag.</span></span> <br/>                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="bb434-134"><dt>**cdrf \_ doerase**</dt></span><span class="sxs-lookup"><span data-stu-id="bb434-134"><dt>**CDRF\_DOERASE**</dt></span></span> </dl>           | <span data-ttu-id="bb434-135">Das-Steuerelement zeichnet nur den Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="bb434-135">The control will only draw the background.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="bb434-136"><dt>**cdrf \_ newFont**</dt></span><span class="sxs-lookup"><span data-stu-id="bb434-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="bb434-137">Ihre Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart.</span><span class="sxs-lookup"><span data-stu-id="bb434-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="bb434-138">Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="bb434-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="bb434-139">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="bb434-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="bb434-140"><dt>**cdrf \_ notiteyitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="bb434-140"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="bb434-141">Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="bb434-141">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="bb434-142">Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="bb434-142">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="bb434-143">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="bb434-143">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="bb434-144"><dt>**cdrf \_ notifyposterase**</dt></span><span class="sxs-lookup"><span data-stu-id="bb434-144"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="bb434-145">Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="bb434-145">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="bb434-146">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="bb434-146">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="bb434-147"><dt>**cdrf \_ notifypostpaint**</dt></span><span class="sxs-lookup"><span data-stu-id="bb434-147"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="bb434-148">Das-Steuerelement sendet einen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Code, wenn der Zeichnungsprozess für das gesamte-Steuerelement vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="bb434-148">The control will send an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code when the painting cycle for the entire control is complete.</span></span> <span data-ttu-id="bb434-149">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="bb434-149">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="bb434-150"><dt>**cdrf \_ notifysubitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="bb434-150"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="bb434-151">Die Anwendung empfängt einen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Code, wobei **dwdrawstage** auf CDDs \_ itemprepaint \| CDDs \_ Unterelement festgelegt ist, bevor die einzelnen Listen Ansichts unter Elemente gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="bb434-151">Your application will receive an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code with **dwDrawStage** set to CDDS\_ITEMPREPAINT \| CDDS\_SUBITEM before each list-view subitem is drawn.</span></span> <span data-ttu-id="bb434-152">Anschließend können Sie Schriftart und Farbe für jedes Unterelement separat angeben oder [**cdrf \_ DODEFAULT**](cdrf-constants.md) für die Standard Verarbeitung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bb434-152">You can then specify font and color for each subitem separately or return [**CDRF\_DODEFAULT**](cdrf-constants.md) for default processing.</span></span> <span data-ttu-id="bb434-153">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="bb434-153">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="bb434-154"><dt>**cdrf \_ skipdefault**</dt></span><span class="sxs-lookup"><span data-stu-id="bb434-154"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="bb434-155">Die Anwendung hat das Element manuell gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bb434-155">Your application drew the item manually.</span></span> <span data-ttu-id="bb434-156">Das-Steuerelement zeichnet das Element nicht.</span><span class="sxs-lookup"><span data-stu-id="bb434-156">The control will not draw the item.</span></span> <span data-ttu-id="bb434-157">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="bb434-157">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="bb434-158"><dt>**cdrf \_ skippostpaint**</dt></span><span class="sxs-lookup"><span data-stu-id="bb434-158"><dt>**CDRF\_SKIPPOSTPAINT**</dt></span></span> </dl>     | <span data-ttu-id="bb434-159">Das-Steuerelement zeichnet das Fokus Rechteck nicht um ein Element.</span><span class="sxs-lookup"><span data-stu-id="bb434-159">The control will not draw the focus rectangle around an item.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="bb434-160">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb434-160">Remarks</span></span>

<span data-ttu-id="bb434-161">Derzeit unterstützen die folgenden Steuerelemente benutzerdefinierte Zeichnungsfunktionen: Header, Listenansicht, Info Leiste, Symbolleiste, QuickInfo, TrackBar und Strukturansicht.</span><span class="sxs-lookup"><span data-stu-id="bb434-161">Currently, the following controls support custom draw functionality: header, list view, rebar, toolbar, tooltip, trackbar, and tree view.</span></span> <span data-ttu-id="bb434-162">Benutzerdefiniertes Zeichnen wird auch für Schaltflächen Steuerelemente unterstützt, wenn Sie über ein Anwendungs Manifest verfügen, um sicherzustellen, dass Comctl32.dll Version 6 verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="bb434-162">Custom draw is also supported for button controls if you have an application manifest to ensure that Comctl32.dll version 6 is available.</span></span>

<span data-ttu-id="bb434-163">Wenn diese Meldung in einer Dialogfeld Prozedur behandelt wird, müssen Sie den Rückgabewert als Teil der Fenster Daten festlegen, bevor Sie " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bb434-163">If this message is handled in a dialog procedure, you must set the return value as part of the window data before returning **TRUE**.</span></span> <span data-ttu-id="bb434-164">Weitere Informationen finden Sie unter [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span><span class="sxs-lookup"><span data-stu-id="bb434-164">For more information, see [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb434-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb434-165">Requirements</span></span>



| <span data-ttu-id="bb434-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb434-166">Requirement</span></span> | <span data-ttu-id="bb434-167">Wert</span><span class="sxs-lookup"><span data-stu-id="bb434-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb434-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb434-168">Minimum supported client</span></span><br/> | <span data-ttu-id="bb434-169">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb434-169">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb434-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb434-170">Minimum supported server</span></span><br/> | <span data-ttu-id="bb434-171">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb434-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb434-172">Header</span><span class="sxs-lookup"><span data-stu-id="bb434-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb434-173"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb434-173"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb434-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb434-174">See also</span></span>

<dl> <dt>

<span data-ttu-id="bb434-175">**Licher**</span><span class="sxs-lookup"><span data-stu-id="bb434-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bb434-176">Benutzerdefiniertes Zeichnen</span><span class="sxs-lookup"><span data-stu-id="bb434-176">Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

