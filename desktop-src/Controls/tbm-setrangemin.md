---
title: TBM_SETRANGEMIN Meldung (kommstrg. h)
description: Legt die minimale logische Position für den Schieberegler in einer TrackBar fest.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- Windows-Steuerelemente für TBM_SETRANGEMIN Meldung
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949411"
---
# <a name="tbm_setrangemin-message"></a><span data-ttu-id="629f1-104">TBM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="629f1-104">TBM\_SETRANGEMIN message</span></span>

<span data-ttu-id="629f1-105">Legt die minimale logische Position für den Schieberegler in einer TrackBar fest.</span><span class="sxs-lookup"><span data-stu-id="629f1-105">Sets the minimum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="629f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="629f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="629f1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="629f1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="629f1-108">Flag neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="629f1-108">Redraw flag.</span></span> <span data-ttu-id="629f1-109">Wenn dieser Parameter **true** ist, zeichnet die Nachricht die TrackBar neu, nachdem der Bereich festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="629f1-109">If this parameter is **TRUE**, the message redraws the trackbar after the range is set.</span></span> <span data-ttu-id="629f1-110">Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Bereich fest, aber die TrackBar wird nicht neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="629f1-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="629f1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="629f1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="629f1-112">Minimale Position für den Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="629f1-112">Minimum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="629f1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="629f1-113">Return value</span></span>

<span data-ttu-id="629f1-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="629f1-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="629f1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="629f1-115">Remarks</span></span>

<span data-ttu-id="629f1-116">Wenn die aktuelle Position des Schiebereglers kleiner ist als der neue Minimalwert, legt die **TBM- \_ SetRangeMin** -Meldung die Schiebereglerposition auf den neuen Minimalwert fest.</span><span class="sxs-lookup"><span data-stu-id="629f1-116">If the current slider position is less than the new minimum, the **TBM\_SETRANGEMIN** message sets the slider position to the new minimum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="629f1-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="629f1-117">Requirements</span></span>



| <span data-ttu-id="629f1-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="629f1-118">Requirement</span></span> | <span data-ttu-id="629f1-119">Wert</span><span class="sxs-lookup"><span data-stu-id="629f1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="629f1-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="629f1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="629f1-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="629f1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="629f1-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="629f1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="629f1-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="629f1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="629f1-124">Header</span><span class="sxs-lookup"><span data-stu-id="629f1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="629f1-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="629f1-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="629f1-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="629f1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="629f1-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="629f1-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="629f1-128">**TBM-über \_ Tragung**</span><span class="sxs-lookup"><span data-stu-id="629f1-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="629f1-129">**TBM-Objekt- \_ Max**</span><span class="sxs-lookup"><span data-stu-id="629f1-129">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





