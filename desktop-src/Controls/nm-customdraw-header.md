---
title: NM_CUSTOMDRAW (Header)-Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Header Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- Windows-Steuerelemente für die NM_CUSTOMDRAW (Kopfzeile)
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
ms.openlocfilehash: 89d6b35503aebed221da6cec212c6dbf614061f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344725"
---
# <a name="nm_customdraw-header-notification-code"></a><span data-ttu-id="325bd-105">NM- \_ customdraw-Benachrichtigungs Code (Header)</span><span class="sxs-lookup"><span data-stu-id="325bd-105">NM\_CUSTOMDRAW (header) notification code</span></span>

<span data-ttu-id="325bd-106">Wird von einem Header Steuerelement gesendet, um das übergeordnete Fenster über Zeichnungsvorgänge zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="325bd-106">Sent by a header control to notify its parent window about drawing operations.</span></span> <span data-ttu-id="325bd-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="325bd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="325bd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="325bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="325bd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="325bd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="325bd-110">Ein Zeiger auf eine [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="325bd-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="325bd-111">Der **dwitemspec** -Member dieser Struktur enthält den Index des Elements, das gezeichnet wird, und der **litemlparam** -Member dieser Struktur enthält den *LPARAM*-Wert des Elements.</span><span class="sxs-lookup"><span data-stu-id="325bd-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="325bd-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="325bd-112">Return value</span></span>

<span data-ttu-id="325bd-113">Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab.</span><span class="sxs-lookup"><span data-stu-id="325bd-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="325bd-114">Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt.</span><span class="sxs-lookup"><span data-stu-id="325bd-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="325bd-115">Sie müssen einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="325bd-115">You must return one of the following values.</span></span>



| <span data-ttu-id="325bd-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="325bd-116">Return code</span></span>                                                                                            | <span data-ttu-id="325bd-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="325bd-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="325bd-118"><dt>**cdrf \_ DODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="325bd-118"><dt>**CDRF\_DODEFAULT**</dt></span></span> </dl>         | <span data-ttu-id="325bd-119">Das Steuerelement zeichnet sich selbst auf.</span><span class="sxs-lookup"><span data-stu-id="325bd-119">The control will draw itself.</span></span> <span data-ttu-id="325bd-120">Es werden keine zusätzlichen [nm \_ customdraw](nm-customdraw.md) -Nachrichten für diesen Zeichnungs Kreis gesendet.</span><span class="sxs-lookup"><span data-stu-id="325bd-120">It will not send any additional [NM\_CUSTOMDRAW](nm-customdraw.md) messages for this paint cycle.</span></span> <span data-ttu-id="325bd-121">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="325bd-121">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="325bd-122"><dt>**cdrf \_ notiteyitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="325bd-122"><dt>**CDRF\_NOTIFYITEMDRAW**</dt></span></span> </dl>    | <span data-ttu-id="325bd-123">Das-Steuerelement benachrichtigt das übergeordnete Element über alle Element bezogenen Zeichnungsvorgänge.</span><span class="sxs-lookup"><span data-stu-id="325bd-123">The control will notify the parent of any item-related drawing operations.</span></span> <span data-ttu-id="325bd-124">Er sendet \_ vor und nach dem Zeichnen von Elementen nm customdraw-Benachrichtigungs Codes.</span><span class="sxs-lookup"><span data-stu-id="325bd-124">It will send NM\_CUSTOMDRAW notification codes before and after drawing items.</span></span> <span data-ttu-id="325bd-125">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="325bd-125">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="325bd-126"><dt>**cdrf \_ notifyposterase**</dt></span><span class="sxs-lookup"><span data-stu-id="325bd-126"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl>   | <span data-ttu-id="325bd-127">Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="325bd-127">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="325bd-128">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="325bd-128">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="325bd-129"><dt>**cdrf \_ notifypostpaint**</dt></span><span class="sxs-lookup"><span data-stu-id="325bd-129"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl>   | <span data-ttu-id="325bd-130">Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="325bd-130">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="325bd-131">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="325bd-131">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="325bd-132"><dt>**cdrf \_ notifysubitemdraw**</dt></span><span class="sxs-lookup"><span data-stu-id="325bd-132"><dt>**CDRF\_NOTIFYSUBITEMDRAW**</dt></span></span> </dl> | <span data-ttu-id="325bd-133">[Allgemeine Steuerelement Versionen](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="325bd-133">[Common Control Versions](common-control-versions.md).</span></span> <span data-ttu-id="325bd-134">Das-Steuerelement benachrichtigt das übergeordnete Element, wenn ein Listen Ansichts-Unterelement gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="325bd-134">The control will notify the parent when a list-view subitem is being drawn.</span></span> <span data-ttu-id="325bd-135">Dies tritt auf, wenn **dwdrawstage** dem CDDs- \_ präpaint gleicht.</span><span class="sxs-lookup"><span data-stu-id="325bd-135">This occurs when **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="325bd-136"><dt>**cdrf \_ newFont**</dt></span><span class="sxs-lookup"><span data-stu-id="325bd-136"><dt>**CDRF\_NEWFONT**</dt></span></span> </dl>           | <span data-ttu-id="325bd-137">Ihre Anwendung hat eine neue Schriftart für das Element angegeben. das-Steuerelement verwendet die neue Schriftart.</span><span class="sxs-lookup"><span data-stu-id="325bd-137">Your application specified a new font for the item; the control will use the new font.</span></span> <span data-ttu-id="325bd-138">Weitere Informationen zum Ändern von Schriftarten finden Sie unter [Ändern von Schriftarten und Farben](custom-draw.md).</span><span class="sxs-lookup"><span data-stu-id="325bd-138">For more information on changing fonts, see [Changing fonts and colors](custom-draw.md).</span></span> <span data-ttu-id="325bd-139">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="325bd-139">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/> |
| <dl> <span data-ttu-id="325bd-140"><dt>**cdrf \_ skipdefault**</dt></span><span class="sxs-lookup"><span data-stu-id="325bd-140"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="325bd-141">Die Anwendung hat das Element manuell gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="325bd-141">Your application drew the item manually.</span></span> <span data-ttu-id="325bd-142">Das-Steuerelement zeichnet das Element nicht.</span><span class="sxs-lookup"><span data-stu-id="325bd-142">The control will not draw the item.</span></span> <span data-ttu-id="325bd-143">Dies tritt auf, wenn **dwdrawstage** auf CDDs \_ itemprepaint zugreift.</span><span class="sxs-lookup"><span data-stu-id="325bd-143">This occurs when **dwDrawStage** equals CDDS\_ITEMPREPAINT.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="325bd-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="325bd-144">Remarks</span></span>

<span data-ttu-id="325bd-145">Weitere Informationen finden [Sie unter Verwenden von benutzerdefiniertem zeichnen](custom-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="325bd-145">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="325bd-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="325bd-146">Requirements</span></span>



| <span data-ttu-id="325bd-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="325bd-147">Requirement</span></span> | <span data-ttu-id="325bd-148">Wert</span><span class="sxs-lookup"><span data-stu-id="325bd-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="325bd-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="325bd-149">Minimum supported client</span></span><br/> | <span data-ttu-id="325bd-150">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="325bd-150">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="325bd-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="325bd-151">Minimum supported server</span></span><br/> | <span data-ttu-id="325bd-152">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="325bd-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="325bd-153">Header</span><span class="sxs-lookup"><span data-stu-id="325bd-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="325bd-154"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="325bd-154"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





