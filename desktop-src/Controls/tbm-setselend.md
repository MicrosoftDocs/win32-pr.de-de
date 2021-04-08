---
title: TBM_SETSELEND Meldung (kommstrg. h)
description: Legt die logische Endposition des aktuellen Auswahl Bereichs in einer TrackBar fest. Diese Meldung wird ignoriert, wenn die TrackBar nicht über den \_ enableselrange-Stil von TB verfügt.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- Windows-Steuerelemente für TBM_SETSELEND Meldung
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146446df4daf8e8ac7c0f3499149ba0f46940880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102862"
---
# <a name="tbm_setselend-message"></a><span data-ttu-id="ea526-105">TBM- \_ setselend-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ea526-105">TBM\_SETSELEND message</span></span>

<span data-ttu-id="ea526-106">Legt die logische Endposition des aktuellen Auswahl Bereichs in einer TrackBar fest.</span><span class="sxs-lookup"><span data-stu-id="ea526-106">Sets the ending logical position of the current selection range in a trackbar.</span></span> <span data-ttu-id="ea526-107">Diese Meldung wird ignoriert, wenn die TrackBar nicht über den [**\_ enableselrange**](trackbar-control-styles.md) -Stil von TB verfügt.</span><span class="sxs-lookup"><span data-stu-id="ea526-107">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea526-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea526-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea526-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea526-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea526-110">Flag neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="ea526-110">Redraw flag.</span></span> <span data-ttu-id="ea526-111">Wenn dieser Parameter **true** ist, zeichnet die Nachricht die TrackBar neu, nachdem der Auswahlbereich festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ea526-111">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="ea526-112">Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Auswahlbereich fest, aber die TrackBar wird nicht neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ea526-112">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="ea526-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea526-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea526-114">Endende logische Position des Auswahl Bereichs.</span><span class="sxs-lookup"><span data-stu-id="ea526-114">Ending logical position of the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea526-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea526-115">Return value</span></span>

<span data-ttu-id="ea526-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ea526-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea526-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea526-117">Requirements</span></span>



| <span data-ttu-id="ea526-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea526-118">Requirement</span></span> | <span data-ttu-id="ea526-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ea526-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea526-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea526-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ea526-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea526-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea526-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea526-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ea526-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea526-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea526-124">Header</span><span class="sxs-lookup"><span data-stu-id="ea526-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea526-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea526-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea526-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea526-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ea526-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ea526-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ea526-128">**TBM- \_ getselend**</span><span class="sxs-lookup"><span data-stu-id="ea526-128">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="ea526-129">**TBM \_ getselstart**</span><span class="sxs-lookup"><span data-stu-id="ea526-129">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="ea526-130">**TBM- \_ Sekunden**</span><span class="sxs-lookup"><span data-stu-id="ea526-130">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="ea526-131">**TBM- \_ setselstart**</span><span class="sxs-lookup"><span data-stu-id="ea526-131">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





