---
title: Benachrichtigungs Code für NM_CUSTOMDRAW (QuickInfo) (kommstrg. h)
description: Wird von einem ToolTip-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 82939901-baed-452b-85bf-3c0c01e1f5df
keywords:
- NM_CUSTOMDRAW (QuickInfo)-Windows-Steuerelemente
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
ms.openlocfilehash: 9ce1047f63c8580051f7d57abf3308bde37238a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743977"
---
# <a name="nm_customdraw-tooltip-notification-code"></a><span data-ttu-id="c6183-105">NM \_ customdraw (QuickInfo)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="c6183-105">NM\_CUSTOMDRAW (tooltip) notification code</span></span>

<span data-ttu-id="c6183-106">Wird von einem ToolTip-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="c6183-106">Sent by a tooltip control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="c6183-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="c6183-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c6183-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6183-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6183-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6183-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6183-110">Ein Zeiger auf eine [**nmttcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="c6183-110">Pointer to an [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) structure that contains information about the drawing operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6183-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6183-111">Return value</span></span>

<span data-ttu-id="c6183-112">Der Wert, der von der Anwendung zurückgegeben werden kann, hängt von der aktuellen Zeichnungsphase ab.</span><span class="sxs-lookup"><span data-stu-id="c6183-112">The value that your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="c6183-113">Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt.</span><span class="sxs-lookup"><span data-stu-id="c6183-113">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="c6183-114">Sie müssen einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c6183-114">You must return one of the following values.</span></span>



| <span data-ttu-id="c6183-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c6183-115">Return code</span></span>                                                                                            | <span data-ttu-id="c6183-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6183-116">Description</span></span>                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6183-117"><dt>**cdrf \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="c6183-117"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="c6183-118">Das Steuerelement zeichnet sich selbst auf.</span><span class="sxs-lookup"><span data-stu-id="c6183-118">The control will draw itself.</span></span> <span data-ttu-id="c6183-119">Es werden keine zusätzlichen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes für diesen Zeichnungs Kreis gesendet.</span><span class="sxs-lookup"><span data-stu-id="c6183-119">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes for this paint cycle.</span></span> <span data-ttu-id="c6183-120">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="c6183-120">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="c6183-121"><dt>**cdrf \_ notiteyitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="c6183-121"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="c6183-122">Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="c6183-122">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="c6183-123">Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="c6183-123">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="c6183-124">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="c6183-124">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                            |
| <dl> <span data-ttu-id="c6183-125"><dt>**cdrf \_ notifyposterase**</dt></span><span class="sxs-lookup"><span data-stu-id="c6183-125"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="c6183-126">Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="c6183-126">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="c6183-127">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="c6183-127">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="c6183-128"><dt>**cdrf \_ notifypostpaint**</dt></span><span class="sxs-lookup"><span data-stu-id="c6183-128"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="c6183-129">Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="c6183-129">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="c6183-130">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="c6183-130">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="c6183-131"><dt>**cdrf \_ notifysubitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="c6183-131"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="c6183-132">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="c6183-132">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="c6183-133">Das-Steuerelement benachrichtigt das übergeordnete Element, wenn ein Listen Ansichts-Unterelement gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="c6183-133">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="c6183-134">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="c6183-134">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="c6183-135"><dt>**cdrf \_ newFont**</dt></span><span class="sxs-lookup"><span data-stu-id="c6183-135"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="c6183-136">Ihre Anwendung hat eine neue Schriftart für das Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="c6183-136">Your application specified a new font for the item.</span></span> <span data-ttu-id="c6183-137">Das-Steuerelement verwendet die neue Schriftart.</span><span class="sxs-lookup"><span data-stu-id="c6183-137">The control will use the new font.</span></span> <span data-ttu-id="c6183-138">Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="c6183-138">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="c6183-139">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="c6183-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="c6183-140"><dt>**cdrf \_ skipdefault**</dt></span><span class="sxs-lookup"><span data-stu-id="c6183-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="c6183-141">Die Anwendung hat das Element manuell gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c6183-141">Your application drew the item manually.</span></span> <span data-ttu-id="c6183-142">Das-Steuerelement zeichnet das Element nicht.</span><span class="sxs-lookup"><span data-stu-id="c6183-142">The control will not draw the item.</span></span> <span data-ttu-id="c6183-143">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="c6183-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="c6183-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6183-144">Requirements</span></span>



| <span data-ttu-id="c6183-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6183-145">Requirement</span></span> | <span data-ttu-id="c6183-146">Wert</span><span class="sxs-lookup"><span data-stu-id="c6183-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6183-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6183-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c6183-148">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6183-148">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6183-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6183-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c6183-150">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6183-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6183-151">Header</span><span class="sxs-lookup"><span data-stu-id="c6183-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6183-152"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6183-152"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6183-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6183-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6183-154">Verwenden benutzerdefinierter zeichnen</span><span class="sxs-lookup"><span data-stu-id="c6183-154">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





