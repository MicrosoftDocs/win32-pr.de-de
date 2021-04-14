---
title: LVM_GETITEMSTATE Meldung (kommstrg. h)
description: Ruft den Status eines Listen Ansichts Elements ab. Sie können diese Nachricht explizit oder mithilfe des ListView \_ GetItemState-Makros senden.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- Windows-Steuerelemente für LVM_GETITEMSTATE Meldung
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478519"
---
# <a name="lvm_getitemstate-message"></a><span data-ttu-id="dbae2-105">LVM \_ GetItemState-Nachricht</span><span class="sxs-lookup"><span data-stu-id="dbae2-105">LVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="dbae2-106">Ruft den Status eines Listen Ansichts Elements ab.</span><span class="sxs-lookup"><span data-stu-id="dbae2-106">Retrieves the state of a list-view item.</span></span> <span data-ttu-id="dbae2-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="dbae2-107">You can send this message explicitly or by using the [**ListView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dbae2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbae2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbae2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dbae2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbae2-110">Der Index des Listen Ansichts Elements.</span><span class="sxs-lookup"><span data-stu-id="dbae2-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="dbae2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dbae2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dbae2-112">Zustandsinformationen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dbae2-112">State information to retrieve.</span></span> <span data-ttu-id="dbae2-113">Dieser Parameter kann eine Kombination der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="dbae2-113">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="dbae2-114">Wert</span><span class="sxs-lookup"><span data-stu-id="dbae2-114">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="dbae2-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dbae2-115">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="dbae2-116"><dt>**LVIS- \_ Ausschneiden**</dt></span><span class="sxs-lookup"><span data-stu-id="dbae2-116"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="dbae2-117">Das Element ist für einen Ausschneide-und Einfügevorgang gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="dbae2-117">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="dbae2-118"><dt>**LVIS wurde \_ beendet.**</dt></span><span class="sxs-lookup"><span data-stu-id="dbae2-118"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="dbae2-119">Das Element wird als Drag & Drop-Ziel hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="dbae2-119">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="dbae2-120"><dt>**LVIS \_ fokussiert**</dt></span><span class="sxs-lookup"><span data-stu-id="dbae2-120"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="dbae2-121">Das Element besitzt den Fokus, sodass es von einem Standard Fokus Rechteck umgeben ist.</span><span class="sxs-lookup"><span data-stu-id="dbae2-121">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="dbae2-122">Obwohl mehr als ein Element ausgewählt werden kann, kann nur ein Element den Fokus haben.</span><span class="sxs-lookup"><span data-stu-id="dbae2-122">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="dbae2-123"><dt>**LVIS \_ ausgewählt**</dt></span><span class="sxs-lookup"><span data-stu-id="dbae2-123"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="dbae2-124">Das Element ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="dbae2-124">The item is selected.</span></span> <span data-ttu-id="dbae2-125">Die Darstellung eines ausgewählten Elements hängt davon ab, ob es den Fokus und die für die Auswahl verwendeten Systemfarben besitzt.</span><span class="sxs-lookup"><span data-stu-id="dbae2-125">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="dbae2-126"><dt>**LVIS \_ overlaymask**</dt></span><span class="sxs-lookup"><span data-stu-id="dbae2-126"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="dbae2-127">Verwenden Sie diese Maske, um den Überlagerungs Bild Index des Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dbae2-127">Use this mask to retrieve the item's overlay image index.</span></span><br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="dbae2-128"><dt>**LVIS- \_ Status-magemask**</dt></span><span class="sxs-lookup"><span data-stu-id="dbae2-128"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="dbae2-129">Verwenden Sie diese Maske, um den Status Bild Index des Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="dbae2-129">Use this mask to retrieve the item's state image index.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbae2-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dbae2-130">Return value</span></span>

<span data-ttu-id="dbae2-131">Gibt den aktuellen Zustand für das angegebene Element zurück.</span><span class="sxs-lookup"><span data-stu-id="dbae2-131">Returns the current state for the specified item.</span></span> <span data-ttu-id="dbae2-132">Die einzigen gültigen Bits im Rückgabewert entsprechen den Bits, die im *LPARAM* -Parameter festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="dbae2-132">The only valid bits in the return value are those that correspond to the bits set in the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbae2-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dbae2-133">Remarks</span></span>

<span data-ttu-id="dbae2-134">Die Zustandsinformationen eines Elements enthalten einen Satz von Bitflags und Bildlisten Indizes, die das Zustands Bild des Elements und das Überlagerungs Bild angeben.</span><span class="sxs-lookup"><span data-stu-id="dbae2-134">An item's state information includes a set of bit flags as well as image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbae2-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dbae2-135">Requirements</span></span>



| <span data-ttu-id="dbae2-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dbae2-136">Requirement</span></span> | <span data-ttu-id="dbae2-137">Wert</span><span class="sxs-lookup"><span data-stu-id="dbae2-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbae2-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dbae2-138">Minimum supported client</span></span><br/> | <span data-ttu-id="dbae2-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbae2-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dbae2-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dbae2-140">Minimum supported server</span></span><br/> | <span data-ttu-id="dbae2-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dbae2-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dbae2-142">Header</span><span class="sxs-lookup"><span data-stu-id="dbae2-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbae2-143"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbae2-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbae2-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbae2-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbae2-145">**LVM- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="dbae2-145">**LVM\_SETITEMSTATE**</span></span>](lvm-setitemstate.md)
</dt> </dl>

 

 





