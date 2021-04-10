---
title: Benachrichtigungs Code für NM_CUSTOMDRAW (Rebar) (kommctrl. h)
description: Wird vom Info leisten-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3ba9bb59-f297-4af1-a9a9-d8789def5bde
keywords:
- Windows-Steuerelemente für die NM_CUSTOMDRAW (Info Leiste)
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
ms.openlocfilehash: 329f3e9abfb20dbca8cebd3a6bf02673ad00f904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106623"
---
# <a name="nm_customdraw-rebar-notification-code"></a><span data-ttu-id="36cb1-105">NM \_ customdraw-Benachrichtigungs Code (Info)</span><span class="sxs-lookup"><span data-stu-id="36cb1-105">NM\_CUSTOMDRAW (rebar) notification code</span></span>

<span data-ttu-id="36cb1-106">Wird vom Info leisten-Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="36cb1-106">Sent by the rebar control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="36cb1-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="36cb1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="36cb1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="36cb1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36cb1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36cb1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36cb1-110">Ein Zeiger auf eine [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="36cb1-110">Pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="36cb1-111">Der **dwitemspec** -Member dieser Struktur enthält den Bezeichner des gezeichneten Bands.</span><span class="sxs-lookup"><span data-stu-id="36cb1-111">The **dwItemSpec** member of this structure contains the identifier of the band being drawn.</span></span> <span data-ttu-id="36cb1-112">Der **litemlparam** -Member dieser Struktur enthält das *LPARAM* -Element des Bands, das gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="36cb1-112">The **lItemlParam** member of this structure contains the *lParam* of the band being drawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36cb1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36cb1-113">Return value</span></span>

<span data-ttu-id="36cb1-114">Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab.</span><span class="sxs-lookup"><span data-stu-id="36cb1-114">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="36cb1-115">Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt.</span><span class="sxs-lookup"><span data-stu-id="36cb1-115">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="36cb1-116">Sie müssen einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="36cb1-116">You must return one of the following values.</span></span>



| <span data-ttu-id="36cb1-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="36cb1-117">Return code</span></span>                                                                                            | <span data-ttu-id="36cb1-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36cb1-118">Description</span></span>                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36cb1-119"><dt>**cdrf \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="36cb1-119"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="36cb1-120">Das Steuerelement zeichnet sich selbst auf.</span><span class="sxs-lookup"><span data-stu-id="36cb1-120">The control will draw itself.</span></span> <span data-ttu-id="36cb1-121">Es werden keine zusätzlichen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungen für diesen Zeichnungs Kreis gesendet.</span><span class="sxs-lookup"><span data-stu-id="36cb1-121">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) notifications for this paint cycle.</span></span> <span data-ttu-id="36cb1-122">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="36cb1-122">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="36cb1-123"><dt>**cdrf \_ notiteyitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="36cb1-123"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="36cb1-124">Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="36cb1-124">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="36cb1-125">Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="36cb1-125">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="36cb1-126">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="36cb1-126">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="36cb1-127"><dt>**cdrf \_ notifyposterase**</dt></span><span class="sxs-lookup"><span data-stu-id="36cb1-127"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="36cb1-128">Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="36cb1-128">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="36cb1-129">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="36cb1-129">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="36cb1-130"><dt>**cdrf \_ notifypostpaint**</dt></span><span class="sxs-lookup"><span data-stu-id="36cb1-130"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="36cb1-131">Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="36cb1-131">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="36cb1-132">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="36cb1-132">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                               |
| <dl> <span data-ttu-id="36cb1-133"><dt>**cdrf \_ notifysubitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="36cb1-133"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="36cb1-134">Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="36cb1-134">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="36cb1-135">Er sendet vor und nach dem Zeichnen von Elementen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="36cb1-135">It will send [NM\_CUSTOMDRAW](nm-customdraw.md) notification codes before and after drawing items.</span></span> <span data-ttu-id="36cb1-136">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="36cb1-136">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                           |
| <dl> <span data-ttu-id="36cb1-137"><dt>**cdrf \_ newFont**</dt></span><span class="sxs-lookup"><span data-stu-id="36cb1-137"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="36cb1-138">Die Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart.</span><span class="sxs-lookup"><span data-stu-id="36cb1-138">The application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="36cb1-139">Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="36cb1-139">For more information about changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="36cb1-140">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="36cb1-140">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="36cb1-141"><dt>**cdrf \_ skipdefault**</dt></span><span class="sxs-lookup"><span data-stu-id="36cb1-141"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="36cb1-142">Die Anwendung hat das Element manuell gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="36cb1-142">The application drew the item manually.</span></span> <span data-ttu-id="36cb1-143">Das-Steuerelement zeichnet das Element nicht.</span><span class="sxs-lookup"><span data-stu-id="36cb1-143">The control will not draw the item.</span></span> <span data-ttu-id="36cb1-144">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="36cb1-144">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="36cb1-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36cb1-145">Requirements</span></span>



| <span data-ttu-id="36cb1-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36cb1-146">Requirement</span></span> | <span data-ttu-id="36cb1-147">Wert</span><span class="sxs-lookup"><span data-stu-id="36cb1-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36cb1-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36cb1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="36cb1-149">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36cb1-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36cb1-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36cb1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="36cb1-151">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36cb1-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36cb1-152">Header</span><span class="sxs-lookup"><span data-stu-id="36cb1-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="36cb1-153"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="36cb1-153"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cb1-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36cb1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cb1-155">Verwenden benutzerdefinierter zeichnen</span><span class="sxs-lookup"><span data-stu-id="36cb1-155">Using Custom Draw</span></span>](custom-draw.md)
</dt> </dl>

 

 





