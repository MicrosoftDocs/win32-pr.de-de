---
title: TBM_SETRANGEMAX Meldung (kommstrg. h)
description: Legt die maximale logische Position für den Schieberegler in einer TrackBar fest.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- Windows-Steuerelemente für TBM_SETRANGEMAX Meldung
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475135"
---
# <a name="tbm_setrangemax-message"></a><span data-ttu-id="6179f-104">TBM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="6179f-104">TBM\_SETRANGEMAX message</span></span>

<span data-ttu-id="6179f-105">Legt die maximale logische Position für den Schieberegler in einer TrackBar fest.</span><span class="sxs-lookup"><span data-stu-id="6179f-105">Sets the maximum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6179f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6179f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6179f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6179f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6179f-108">Flag neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6179f-108">Redraw flag.</span></span> <span data-ttu-id="6179f-109">Wenn dieser Parameter **true** ist, wird die TrackBar nach dem Festlegen des Bereichs neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6179f-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="6179f-110">Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Bereich fest, aber die TrackBar wird nicht neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6179f-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="6179f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6179f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6179f-112">Maximale Position für den Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="6179f-112">Maximum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6179f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6179f-113">Return value</span></span>

<span data-ttu-id="6179f-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="6179f-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6179f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6179f-115">Remarks</span></span>

<span data-ttu-id="6179f-116">Wenn die aktuelle Schieberegler-Position größer als die neue Höchstzahl ist, legt die **TBM \_ SetRangeMax** -Meldung die Schieberegler-Position auf den neuen maximalen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="6179f-116">If the current slider position is greater than the new maximum, the **TBM\_SETRANGEMAX** message sets the slider position to the new maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6179f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6179f-117">Requirements</span></span>



| <span data-ttu-id="6179f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6179f-118">Requirement</span></span> | <span data-ttu-id="6179f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6179f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6179f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6179f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6179f-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6179f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6179f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6179f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6179f-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6179f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6179f-124">Header</span><span class="sxs-lookup"><span data-stu-id="6179f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6179f-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6179f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6179f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6179f-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6179f-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6179f-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6179f-128">**TBM-über \_ Tragung**</span><span class="sxs-lookup"><span data-stu-id="6179f-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="6179f-129">**TBM \_ -Anpassung**</span><span class="sxs-lookup"><span data-stu-id="6179f-129">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

 





