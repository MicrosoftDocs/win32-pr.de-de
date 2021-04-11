---
title: LVM_SETCALLBACKMASK Meldung (kommstrg. h)
description: Ändert die Rückruf Maske für ein Listenansicht-Steuerelement. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros SetCallbackMask senden.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- Windows-Steuerelemente für LVM_SETCALLBACKMASK Meldung
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103363"
---
# <a name="lvm_setcallbackmask-message"></a><span data-ttu-id="c524b-105">LVM- \_ SetCallbackMask-Meldung</span><span class="sxs-lookup"><span data-stu-id="c524b-105">LVM\_SETCALLBACKMASK message</span></span>

<span data-ttu-id="c524b-106">Ändert die Rückruf Maske für ein Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c524b-106">Changes the callback mask for a list-view control.</span></span> <span data-ttu-id="c524b-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView-Makros \_ SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) senden.</span><span class="sxs-lookup"><span data-stu-id="c524b-107">You can send this message explicitly or by using the [**ListView\_SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c524b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c524b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c524b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c524b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c524b-110">Der Wert der Rückruf Maske.</span><span class="sxs-lookup"><span data-stu-id="c524b-110">Value of the callback mask.</span></span> <span data-ttu-id="c524b-111">Die Bits der Maske geben die Element Zustände oder-Bilder an, für die die Anwendung die aktuellen Zustandsdaten speichert.</span><span class="sxs-lookup"><span data-stu-id="c524b-111">The bits of the mask indicate the item states or images for which the application stores the current state data.</span></span> <span data-ttu-id="c524b-112">Dieser Wert kann eine beliebige Kombination der folgenden Konstanten sein:</span><span class="sxs-lookup"><span data-stu-id="c524b-112">This value can be any combination of the following constants:</span></span>



| <span data-ttu-id="c524b-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c524b-113">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="c524b-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c524b-114">Meaning</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="c524b-115"><dt>**LVIS- \_ Ausschneiden**</dt></span><span class="sxs-lookup"><span data-stu-id="c524b-115"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="c524b-116">Das Element ist für einen Ausschneide-und Einfügevorgang gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="c524b-116">The item is marked for a cut-and-paste operation.</span></span><br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="c524b-117"><dt>**LVIS wurde \_ beendet.**</dt></span><span class="sxs-lookup"><span data-stu-id="c524b-117"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="c524b-118">Das Element wird als Drag & Drop-Ziel hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="c524b-118">The item is highlighted as a drag-and-drop target.</span></span><br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="c524b-119"><dt>**LVIS \_ fokussiert**</dt></span><span class="sxs-lookup"><span data-stu-id="c524b-119"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="c524b-120">Das Element hat den Fokus.</span><span class="sxs-lookup"><span data-stu-id="c524b-120">The item has the focus.</span></span><br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="c524b-121"><dt>**LVIS \_ ausgewählt**</dt></span><span class="sxs-lookup"><span data-stu-id="c524b-121"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="c524b-122">Das Element ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c524b-122">The item is selected.</span></span> <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="c524b-123"><dt>**LVIS \_ overlaymask**</dt></span><span class="sxs-lookup"><span data-stu-id="c524b-123"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="c524b-124">Die Anwendung speichert den Abbild Listen Index des aktuellen Überlagerungs Bilds für jedes Element.</span><span class="sxs-lookup"><span data-stu-id="c524b-124">The application stores the image list index of the current overlay image for each item.</span></span><br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="c524b-125"><dt>**LVIS- \_ Status-magemask**</dt></span><span class="sxs-lookup"><span data-stu-id="c524b-125"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="c524b-126">Die Anwendung speichert den Abbild Listen Index des aktuellen Status Bilds für jedes Element.</span><span class="sxs-lookup"><span data-stu-id="c524b-126">The application stores the image list index of the current state image for each item.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="c524b-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c524b-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c524b-128">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="c524b-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c524b-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c524b-129">Return value</span></span>

<span data-ttu-id="c524b-130">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="c524b-130">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c524b-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c524b-131">Remarks</span></span>

<span data-ttu-id="c524b-132">Bei der *Rückruf Maske* eines Listenansicht-Steuer Elements handelt es sich um einen Satz von Bitflags, die die Element Zustände angeben, für die die Anwendung und nicht das Steuerelement die aktuellen Daten speichert.</span><span class="sxs-lookup"><span data-stu-id="c524b-132">The *callback mask* of a list-view control is a set of bit flags that specify the item states for which the application, rather than the control, stores the current data.</span></span> <span data-ttu-id="c524b-133">Die Rückruf Maske gilt für alle Elemente des Steuer Elements, im Gegensatz zur Rückruf Element Bezeichnung, die für ein bestimmtes Element gilt.</span><span class="sxs-lookup"><span data-stu-id="c524b-133">The callback mask applies to all of the control's items, unlike the callback item designation, which applies to a specific item.</span></span> <span data-ttu-id="c524b-134">Die Rückruf Maske ist standardmäßig 0 (null), was bedeutet, dass das Listenansicht-Steuerelement alle Element Zustandsinformationen speichert.</span><span class="sxs-lookup"><span data-stu-id="c524b-134">The callback mask is zero by default, meaning that the list-view control stores all item state information.</span></span> <span data-ttu-id="c524b-135">Nachdem Sie ein Listenansicht-Steuerelement erstellt und seine Elemente initialisiert haben, können Sie die **LVM- \_ SetCallbackMask** -Nachricht senden, um die Rückruf Maske zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c524b-135">After creating a list-view control and initializing its items, you can send the **LVM\_SETCALLBACKMASK** message to change the callback mask.</span></span> <span data-ttu-id="c524b-136">Um die aktuelle Rückruf Maske abzurufen, senden Sie die [**LVM \_ GetCallbackMask**](lvm-getcallbackmask.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c524b-136">To retrieve the current callback mask, send the [**LVM\_GETCALLBACKMASK**](lvm-getcallbackmask.md) message.</span></span>

<span data-ttu-id="c524b-137">Weitere Informationen zu Überlagerungs Bildern und Zustands Bildern finden Sie unter [Hinzufügen List-View Bildlisten](using-list-view-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c524b-137">For more information about overlay images and state images, see [Adding List-View Image Lists](using-list-view-controls.md).</span></span>

<span data-ttu-id="c524b-138">Weitere Informationen zu List-View-Rückrufen finden Sie unter [Rückruf Elemente und Rückruf Maske](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c524b-138">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c524b-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c524b-139">Requirements</span></span>



| <span data-ttu-id="c524b-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c524b-140">Requirement</span></span> | <span data-ttu-id="c524b-141">Wert</span><span class="sxs-lookup"><span data-stu-id="c524b-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c524b-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c524b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c524b-143">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c524b-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c524b-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c524b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c524b-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c524b-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c524b-146">Header</span><span class="sxs-lookup"><span data-stu-id="c524b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c524b-147"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c524b-147"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c524b-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c524b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c524b-149">**LVN \_ getdispinfo**</span><span class="sxs-lookup"><span data-stu-id="c524b-149">**LVN\_GETDISPINFO**</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





