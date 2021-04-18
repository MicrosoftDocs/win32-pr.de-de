---
title: BM_SETSTATE Meldung (Winuser. h)
description: Legt den Hervorhebungs Zustand einer Schaltfläche fest. Der Hervorhebungs Zustand gibt an, ob die Schaltfläche hervorgehoben wird, als ob der Benutzer Sie gedrückt hätte. Sie können diese Nachricht explizit senden oder das SetState-Makro der Schaltfläche verwenden \_ .
ms.assetid: 675ebe8d-b381-46ca-b328-ebe9f25d864a
keywords:
- Windows-Steuerelemente für BM_SETSTATE Meldung
topic_type:
- apiref
api_name:
- BM_SETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9b60231980f406b0aeb499d724dc6aa7025513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339320"
---
# <a name="bm_setstate-message"></a><span data-ttu-id="97a58-106">BM- \_ SetState-Nachricht</span><span class="sxs-lookup"><span data-stu-id="97a58-106">BM\_SETSTATE message</span></span>

<span data-ttu-id="97a58-107">Legt den Hervorhebungs Zustand einer Schaltfläche fest.</span><span class="sxs-lookup"><span data-stu-id="97a58-107">Sets the highlight state of a button.</span></span> <span data-ttu-id="97a58-108">Der Hervorhebungs Zustand gibt an, ob die Schaltfläche hervorgehoben wird, als ob der Benutzer Sie gedrückt hätte.</span><span class="sxs-lookup"><span data-stu-id="97a58-108">The highlight state indicates whether the button is highlighted as if the user had pushed it.</span></span> <span data-ttu-id="97a58-109">Sie können diese Nachricht explizit senden oder das [**\_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) -Makro der Schaltfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="97a58-109">You can send this message explicitly or use the [**Button\_SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="97a58-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="97a58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97a58-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97a58-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97a58-112">Ein **boolescher** Wert, der angibt, ob die Schaltfläche markiert ist.</span><span class="sxs-lookup"><span data-stu-id="97a58-112">A **BOOL** that specifies whether the button is highlighted.</span></span> <span data-ttu-id="97a58-113">Durch den Wert **true** wird die Schaltfläche hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="97a58-113">A value of **TRUE** highlights the button.</span></span> <span data-ttu-id="97a58-114">Der Wert **false** entfernt alle Hervorhebungen.</span><span class="sxs-lookup"><span data-stu-id="97a58-114">A value of **FALSE** removes any highlighting.</span></span>

</dd> <dt>

<span data-ttu-id="97a58-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97a58-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97a58-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="97a58-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97a58-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97a58-117">Return value</span></span>

<span data-ttu-id="97a58-118">Diese Meldung gibt immer 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="97a58-118">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="97a58-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="97a58-119">Remarks</span></span>

<span data-ttu-id="97a58-120">Die Hervorhebung wirkt sich nur auf die Darstellung einer Schaltfläche aus.</span><span class="sxs-lookup"><span data-stu-id="97a58-120">Highlighting affects only the appearance of a button.</span></span> <span data-ttu-id="97a58-121">Dies hat keine Auswirkung auf den Status des Kontrollkästchens oder des Kontrollkästchens.</span><span class="sxs-lookup"><span data-stu-id="97a58-121">It has no effect on the check state of a radio button or check box.</span></span>

<span data-ttu-id="97a58-122">Eine Schaltfläche wird automatisch hervorgehoben, wenn der Benutzer den Cursor darüber positioniert und die linke Maustaste gedrückt hält.</span><span class="sxs-lookup"><span data-stu-id="97a58-122">A button is automatically highlighted when the user positions the cursor over it and presses and holds the left mouse button.</span></span> <span data-ttu-id="97a58-123">Die Hervorhebung wird entfernt, wenn der Benutzer die Maustaste loslässt.</span><span class="sxs-lookup"><span data-stu-id="97a58-123">The highlighting is removed when the user releases the mouse button.</span></span>

## <a name="requirements"></a><span data-ttu-id="97a58-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97a58-124">Requirements</span></span>



| <span data-ttu-id="97a58-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97a58-125">Requirement</span></span> | <span data-ttu-id="97a58-126">Wert</span><span class="sxs-lookup"><span data-stu-id="97a58-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a58-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97a58-127">Minimum supported client</span></span><br/> | <span data-ttu-id="97a58-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97a58-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="97a58-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97a58-129">Minimum supported server</span></span><br/> | <span data-ttu-id="97a58-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97a58-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="97a58-131">Header</span><span class="sxs-lookup"><span data-stu-id="97a58-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="97a58-132"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="97a58-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97a58-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97a58-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="97a58-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="97a58-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="97a58-135">**BM \_ GetState**</span><span class="sxs-lookup"><span data-stu-id="97a58-135">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="97a58-136">**BM- \_ setcheck**</span><span class="sxs-lookup"><span data-stu-id="97a58-136">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





