---
title: Benachrichtigungs Code für NM_CUSTOMDRAW (Strukturansicht) (kommctrl. h)
description: Wird von einem Strukturansicht-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: eafe2427-20eb-4f3b-9407-bece897ffe16
keywords:
- NM_CUSTOMDRAW (Strukturansicht) Windows-Steuerelemente für Benachrichtigungs Code
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
ms.openlocfilehash: 2bb3f7b44748c2ac9c5b9651c079a8b90df0c508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858652"
---
# <a name="nm_customdraw-tree-view-notification-code"></a><span data-ttu-id="0fdc6-105">NM \_ customdraw (Strukturansicht)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="0fdc6-105">NM\_CUSTOMDRAW (tree view) notification code</span></span>

<span data-ttu-id="0fdc6-106">Wird von einem Strukturansicht-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-106">Sent by a tree-view control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="0fdc6-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0fdc6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fdc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fdc6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fdc6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fdc6-110">Ein Zeiger auf eine [**nmtvcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält und empfängt.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-110">Pointer to an [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure that contains and receives information about the drawing operation.</span></span> <span data-ttu-id="0fdc6-111">Der **dwitemspec** -Member des **nmcd** -Members dieser Struktur enthält das Handle des Elements, das gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-111">The **dwItemSpec** member of the **nmcd** member of this structure contains the handle of the item being drawn.</span></span> <span data-ttu-id="0fdc6-112">Der **litemlparam** -Member des **nmcd** -Members dieser Struktur enthält den *LPARAM* -Element des Elements, das gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-112">The **lItemlParam** member of the **nmcd** member of this structure contains the *lParam* of the item being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fdc6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fdc6-113">Return value</span></span>

<span data-ttu-id="0fdc6-114">Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="0fdc6-115">Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="0fdc6-116">Sie müssen einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-116">You must return one of the following values.</span></span>



| <span data-ttu-id="0fdc6-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0fdc6-117">Return code</span></span>                                                                                            | <span data-ttu-id="0fdc6-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fdc6-118">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0fdc6-119"><dt>**cdrf \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="0fdc6-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="0fdc6-120">Das-Steuerelement zeichnet sich selbst.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-120">The control draws itself.</span></span> <span data-ttu-id="0fdc6-121">Es werden keine zusätzlichen nm- [ \_ customdraw](nm-customdraw.md) -Codes für diesen Zeichnungs Kreis gesendet.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-121">It does not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) codes for this paint cycle.</span></span> <span data-ttu-id="0fdc6-122">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="0fdc6-123"><dt>**cdrf \_ notiteyitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="0fdc6-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="0fdc6-124">Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-124">The control notifies the parent of any item-related drawing operations.</span></span> <span data-ttu-id="0fdc6-125">Es sendet [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes vor und nach dem Zeichnen von Elementen.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-125">It sends [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="0fdc6-126">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                |
| <dl> <span data-ttu-id="0fdc6-127"><dt>**cdrf \_ notifyposterase**</dt></span><span class="sxs-lookup"><span data-stu-id="0fdc6-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="0fdc6-128">Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements. Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-128">The control notifies the parent after erasing an item.This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="0fdc6-129"><dt>**cdrf \_ notifypostpaint**</dt></span><span class="sxs-lookup"><span data-stu-id="0fdc6-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="0fdc6-130">Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-130">The control notifies the parent after painting an item.</span></span> <span data-ttu-id="0fdc6-131">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="0fdc6-132"><dt>**cdrf \_ notifysubitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="0fdc6-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | [<span data-ttu-id="0fdc6-133">Version 4,71.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-133">Version 4.71.</span></span>](common-control-versions.md) <span data-ttu-id="0fdc6-134">Das-Steuerelement benachrichtigt das übergeordnete Element, wenn ein Listen Ansichts Unterelement gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-134">The control notifies the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="0fdc6-135">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="0fdc6-136"><dt>**cdrf \_ newFont**</dt></span><span class="sxs-lookup"><span data-stu-id="0fdc6-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="0fdc6-137">Ihre Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="0fdc6-138">Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="0fdc6-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="0fdc6-139">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="0fdc6-140"><dt>**cdrf \_ skipdefault**</dt></span><span class="sxs-lookup"><span data-stu-id="0fdc6-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="0fdc6-141">Die Anwendung hat das Element manuell gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-141">Your application drew the item manually.</span></span> <span data-ttu-id="0fdc6-142">Das-Steuerelement zeichnet das Element nicht.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-142">The control will not draw the item.</span></span> <span data-ttu-id="0fdc6-143">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="0fdc6-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fdc6-144">Remarks</span></span>

[<span data-ttu-id="0fdc6-145">Version 5,80.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-145">Version 5.80.</span></span>](common-control-versions.md) <span data-ttu-id="0fdc6-146">Wenn Sie die Schriftart ändern, indem Sie [**cdrf \_ newFont**](cdrf-constants.md)zurückgeben, wird im Strukturansicht-Steuerelement möglicherweise der abgeschnittene Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-146">If you change the font by returning [**CDRF\_NEWFONT**](cdrf-constants.md), the tree-view control might display clipped text.</span></span> <span data-ttu-id="0fdc6-147">Dieses Verhalten ist aus Gründen der Abwärtskompatibilität mit früheren Versionen der allgemeinen Steuerelemente erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-147">This behavior is necessary for backward compatibility with earlier versions of the common controls.</span></span> <span data-ttu-id="0fdc6-148">Wenn Sie die Schriftart eines Strukturansicht-Steuer Elements ändern möchten, erhalten Sie bessere Ergebnisse, wenn Sie eine ccm- [**\_ setVersion**](ccm-setversion.md) -Nachricht mit dem *wParam* -Wert 5 senden, bevor Sie dem Steuerelement Elemente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0fdc6-148">If you want to change the font of a tree-view control, you will get better results if you send a [**CCM\_SETVERSION**](ccm-setversion.md) message with the *wParam* value set to 5 before adding any items to the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fdc6-149">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fdc6-149">Requirements</span></span>



| <span data-ttu-id="0fdc6-150">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fdc6-150">Requirement</span></span> | <span data-ttu-id="0fdc6-151">Wert</span><span class="sxs-lookup"><span data-stu-id="0fdc6-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fdc6-152">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fdc6-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0fdc6-153">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fdc6-153">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0fdc6-154">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fdc6-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0fdc6-155">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fdc6-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0fdc6-156">Header</span><span class="sxs-lookup"><span data-stu-id="0fdc6-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fdc6-157"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fdc6-157"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fdc6-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fdc6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fdc6-159">Verwenden benutzerdefinierter zeichnen</span><span class="sxs-lookup"><span data-stu-id="0fdc6-159">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





