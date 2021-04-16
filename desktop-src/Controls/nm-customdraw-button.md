---
title: NM_CUSTOMDRAW (Schaltfläche)-Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines Schaltflächen-Steuer Elements über benutzerdefinierte Zeichnungsvorgänge auf der Schaltfläche. Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs \_ Meldung.
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- NM_CUSTOMDRAW-Schaltfläche (Schaltfläche) Windows-Steuerelemente
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
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479425"
---
# <a name="nm_customdraw-button-notification-code"></a><span data-ttu-id="e7427-105">NM \_ (Schaltfläche)-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="e7427-105">NM\_CUSTOMDRAW (button) notification code</span></span>

<span data-ttu-id="e7427-106">Benachrichtigt das übergeordnete Fenster eines Schaltflächen-Steuer Elements über benutzerdefinierte Zeichnungsvorgänge auf der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="e7427-106">Notifies the parent window of a button control about custom draw operations on the button.</span></span>

<span data-ttu-id="e7427-107">Das Schaltflächen-Steuerelement sendet diesen Benachrichtigungs Code in Form einer WM-Benachrichtigungs Meldung. [**\_**](wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="e7427-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e7427-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7427-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7427-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7427-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7427-110">Ein Zeiger auf eine [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur, die Informationen über den Zeichnungs Vorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="e7427-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="e7427-111">Der **dwitemspec** -Member dieser Struktur enthält den Index des Elements, das gezeichnet wird, und der **litemlparam** -Member dieser Struktur enthält den *LPARAM*-Wert des Elements.</span><span class="sxs-lookup"><span data-stu-id="e7427-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7427-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7427-112">Return value</span></span>

<span data-ttu-id="e7427-113">Der Wert, den die Anwendung zurückgeben kann, hängt von der aktuellen Zeichnungsphase ab.</span><span class="sxs-lookup"><span data-stu-id="e7427-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="e7427-114">Der **dwdrawstage** -Member der zugeordneten [**nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) -Struktur enthält einen Wert, der die Zeichnungsphase angibt.</span><span class="sxs-lookup"><span data-stu-id="e7427-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="e7427-115">Sie müssen einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e7427-115">You must return one of the following values.</span></span>



| <span data-ttu-id="e7427-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e7427-116">Return code</span></span>                                                                                          | <span data-ttu-id="e7427-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7427-117">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7427-118"><dt>**cdrf \_ notifyposterase**</dt></span><span class="sxs-lookup"><span data-stu-id="e7427-118"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl> | <span data-ttu-id="e7427-119">Das-Steuerelement benachrichtigt das übergeordnete Element nach dem Löschen eines Elements.</span><span class="sxs-lookup"><span data-stu-id="e7427-119">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="e7427-120">Dies kann nur verwendet werden, wenn **dwdrawstage** auf CDDs \_ preerase fest.</span><span class="sxs-lookup"><span data-stu-id="e7427-120">This can be used only if **dwDrawStage** equals CDDS\_PREERASE.</span></span><br/>                                  |
| <dl> <span data-ttu-id="e7427-121"><dt>**cdrf \_ notifypostpaint**</dt></span><span class="sxs-lookup"><span data-stu-id="e7427-121"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl> | <span data-ttu-id="e7427-122">Das-Steuerelement benachrichtigt das übergeordnete Element, nachdem ein Element gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7427-122">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="e7427-123">Dies kann nur verwendet werden, wenn **dwdrawstage** auf CDDs \_ PrePaint fest.</span><span class="sxs-lookup"><span data-stu-id="e7427-123">This can be used only if **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                 |
| <dl> <span data-ttu-id="e7427-124"><dt>**cdrf \_ skipdefault**</dt></span><span class="sxs-lookup"><span data-stu-id="e7427-124"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>     | <span data-ttu-id="e7427-125">Die Anwendung hat das Element manuell gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e7427-125">The application drew the item manually.</span></span> <span data-ttu-id="e7427-126">Das-Steuerelement zeichnet das Element nicht.</span><span class="sxs-lookup"><span data-stu-id="e7427-126">The control will not draw the item.</span></span> <span data-ttu-id="e7427-127">Dies kann verwendet werden, wenn **dwdrawstage** auf CDDs \_ preerase oder CDDs \_ PrePaint fest.</span><span class="sxs-lookup"><span data-stu-id="e7427-127">This can be used when **dwDrawStage** equals CDDS\_PREERASE or CDDS\_PREPAINT.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7427-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7427-128">Remarks</span></span>

<span data-ttu-id="e7427-129">Wenn das Schaltflächen-Steuerelement als "Besitzer zeichnen" gekennzeichnet ist \_ , wird der "nm \_ customdraw"-Benachrichtigungs Code nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="e7427-129">If the button control is marked ownerdraw (BS\_OWNERDRAW), the NM\_CUSTOMDRAW notification code is not sent.</span></span>

<span data-ttu-id="e7427-130">Weitere Informationen finden [Sie unter Verwenden von benutzerdefiniertem zeichnen](custom-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="e7427-130">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

> [!Note]  
> <span data-ttu-id="e7427-131">Zur Verwendung dieses Benachrichtigungs Codes müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="e7427-131">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="e7427-132">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e7427-132">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7427-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7427-133">Requirements</span></span>



| <span data-ttu-id="e7427-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7427-134">Requirement</span></span> | <span data-ttu-id="e7427-135">Wert</span><span class="sxs-lookup"><span data-stu-id="e7427-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7427-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7427-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e7427-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7427-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e7427-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7427-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e7427-139">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7427-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e7427-140">Header</span><span class="sxs-lookup"><span data-stu-id="e7427-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7427-141"><dt>Kommctrl. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7427-141"><dt>Commctrl.h (include Windows.h)</dt></span></span> </dl> |



 

 





