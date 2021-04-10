---
title: TBM_SETSELSTART Meldung (kommstrg. h)
description: Legt die logische Startposition des aktuellen Auswahl Bereichs in einer TrackBar fest. Diese Meldung wird ignoriert, wenn die TrackBar nicht über den \_ enableselrange-Stil von TB verfügt.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- Windows-Steuerelemente für TBM_SETSELSTART Meldung
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040087"
---
# <a name="tbm_setselstart-message"></a><span data-ttu-id="59945-105">TBM- \_ setselstart-Meldung</span><span class="sxs-lookup"><span data-stu-id="59945-105">TBM\_SETSELSTART message</span></span>

<span data-ttu-id="59945-106">Legt die logische Startposition des aktuellen Auswahl Bereichs in einer TrackBar fest.</span><span class="sxs-lookup"><span data-stu-id="59945-106">Sets the starting logical position of the current selection range in a trackbar.</span></span> <span data-ttu-id="59945-107">Diese Meldung wird ignoriert, wenn die TrackBar nicht über den [**\_ enableselrange**](trackbar-control-styles.md) -Stil von TB verfügt.</span><span class="sxs-lookup"><span data-stu-id="59945-107">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="59945-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="59945-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59945-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="59945-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59945-110">Flag neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="59945-110">Redraw flag.</span></span> <span data-ttu-id="59945-111">Wenn dieser Parameter **true** ist, zeichnet die Nachricht die TrackBar neu, nachdem der Auswahlbereich festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="59945-111">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="59945-112">Wenn dieser Parameter auf **false** festgelegt ist, legt die Meldung den Auswahlbereich fest, aber die TrackBar wird nicht neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="59945-112">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="59945-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="59945-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="59945-114">Anfangsposition des Auswahl Bereichs.</span><span class="sxs-lookup"><span data-stu-id="59945-114">Starting position of the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59945-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59945-115">Return value</span></span>

<span data-ttu-id="59945-116">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="59945-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="59945-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59945-117">Requirements</span></span>



| <span data-ttu-id="59945-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59945-118">Requirement</span></span> | <span data-ttu-id="59945-119">Wert</span><span class="sxs-lookup"><span data-stu-id="59945-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="59945-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="59945-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59945-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59945-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="59945-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="59945-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59945-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="59945-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="59945-124">Header</span><span class="sxs-lookup"><span data-stu-id="59945-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="59945-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="59945-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59945-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59945-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="59945-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="59945-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="59945-128">**TBM- \_ getselend**</span><span class="sxs-lookup"><span data-stu-id="59945-128">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="59945-129">**TBM \_ getselstart**</span><span class="sxs-lookup"><span data-stu-id="59945-129">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="59945-130">**TBM- \_ Sekunden**</span><span class="sxs-lookup"><span data-stu-id="59945-130">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="59945-131">**TBM- \_ setselend**</span><span class="sxs-lookup"><span data-stu-id="59945-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> </dl>

 

 





