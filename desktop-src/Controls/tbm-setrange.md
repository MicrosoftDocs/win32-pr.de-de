---
title: TBM_SETRANGE Meldung (kommstrg. h)
description: Legt den Bereich der minimalen und maximalen logischen Positionen für den Schieberegler in einer TrackBar fest.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- Windows-Steuerelemente für TBM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040359"
---
# <a name="tbm_setrange-message"></a><span data-ttu-id="7274c-104">TBM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="7274c-104">TBM\_SETRANGE message</span></span>

<span data-ttu-id="7274c-105">Legt den Bereich der minimalen und maximalen logischen Positionen für den Schieberegler in einer TrackBar fest.</span><span class="sxs-lookup"><span data-stu-id="7274c-105">Sets the range of minimum and maximum logical positions for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7274c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7274c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7274c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7274c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7274c-108">Flag neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="7274c-108">Redraw flag.</span></span> <span data-ttu-id="7274c-109">Wenn dieser Parameter **true** ist, wird die TrackBar nach dem Festlegen des Bereichs neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7274c-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="7274c-110">Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Bereich fest, aber die TrackBar wird nicht neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7274c-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="7274c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7274c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7274c-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die minimale Position für den Schieberegler an, und das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die maximale Position an.</span><span class="sxs-lookup"><span data-stu-id="7274c-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum position for the slider, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7274c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7274c-113">Return value</span></span>

<span data-ttu-id="7274c-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="7274c-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7274c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7274c-115">Remarks</span></span>

<span data-ttu-id="7274c-116">Wenn sich die aktuelle Position des Schiebereglers außerhalb des neuen Bereichs befindet, legt die **TBM- \_ SetRange** -Nachricht die Schiebereglerposition auf den neuen maximalen oder minimalen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="7274c-116">If the current slider position is outside the new range, the **TBM\_SETRANGE** message sets the slider position to the new maximum or minimum value.</span></span>

<span data-ttu-id="7274c-117">Da diese Nachricht 2 16-Bit-ganz Zahl Werte ohne Vorzeichen annimmt, liegt der maximale Bereich, den diese Meldung angeben kann, zwischen 0 und 65.535.</span><span class="sxs-lookup"><span data-stu-id="7274c-117">Because this message takes two 16-bit unsigned integer values, the maximum range that this message can specify is from 0 to 65,535.</span></span> <span data-ttu-id="7274c-118">Um größere Bereichs Werte anzugeben, verwenden Sie die TBM-Nachrichten " [**TBM \_**](tbm-setrangemin.md) " und " [**TBM \_**](tbm-setrangemax.md) ".</span><span class="sxs-lookup"><span data-stu-id="7274c-118">To specify larger range values, use the [**TBM\_SETRANGEMIN**](tbm-setrangemin.md) and [**TBM\_SETRANGEMAX**](tbm-setrangemax.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="7274c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7274c-119">Requirements</span></span>



| <span data-ttu-id="7274c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7274c-120">Requirement</span></span> | <span data-ttu-id="7274c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7274c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7274c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7274c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7274c-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7274c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7274c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7274c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7274c-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7274c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7274c-126">Header</span><span class="sxs-lookup"><span data-stu-id="7274c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7274c-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="7274c-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7274c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7274c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="7274c-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7274c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7274c-130">**TBM-Objekt- \_ Max**</span><span class="sxs-lookup"><span data-stu-id="7274c-130">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> <dt>

[<span data-ttu-id="7274c-131">**TBM \_ -Anpassung**</span><span class="sxs-lookup"><span data-stu-id="7274c-131">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

