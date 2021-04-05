---
title: TBM_CLEARSEL Meldung (kommstrg. h)
description: Löscht den aktuellen Auswahlbereich in einer TrackBar.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- Windows-Steuerelemente für TBM_CLEARSEL Meldung
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d2474f3978dc80b2611bd6b454c45e515ee159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859327"
---
# <a name="tbm_clearsel-message"></a><span data-ttu-id="cf930-104">TBM- \_ ClearSEL-Meldung</span><span class="sxs-lookup"><span data-stu-id="cf930-104">TBM\_CLEARSEL message</span></span>

<span data-ttu-id="cf930-105">Löscht den aktuellen Auswahlbereich in einer TrackBar.</span><span class="sxs-lookup"><span data-stu-id="cf930-105">Clears the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf930-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf930-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf930-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf930-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf930-108">Flag neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="cf930-108">Redraw flag.</span></span> <span data-ttu-id="cf930-109">Wenn dieser Parameter **true** ist, wird die TrackBar nach dem Löschen der Auswahl neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cf930-109">If this parameter is **TRUE**, the trackbar is redrawn after the selection is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="cf930-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf930-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cf930-111">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="cf930-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf930-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf930-112">Return value</span></span>

<span data-ttu-id="cf930-113">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="cf930-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf930-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf930-114">Remarks</span></span>

<span data-ttu-id="cf930-115">Eine TrackBar kann nur dann einen Auswahlbereich haben, wenn Sie den TSB-Formatvorlagen [**\_ Bereich**](trackbar-control-styles.md) bei der Erstellung angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="cf930-115">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf930-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf930-116">Requirements</span></span>



| <span data-ttu-id="cf930-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf930-117">Requirement</span></span> | <span data-ttu-id="cf930-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cf930-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf930-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf930-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf930-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf930-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cf930-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf930-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf930-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf930-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf930-123">Header</span><span class="sxs-lookup"><span data-stu-id="cf930-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf930-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf930-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf930-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf930-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="cf930-126">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cf930-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cf930-127">**TBM- \_ Sekunden**</span><span class="sxs-lookup"><span data-stu-id="cf930-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="cf930-128">**TBM- \_ setselend**</span><span class="sxs-lookup"><span data-stu-id="cf930-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="cf930-129">**TBM- \_ setselstart**</span><span class="sxs-lookup"><span data-stu-id="cf930-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





