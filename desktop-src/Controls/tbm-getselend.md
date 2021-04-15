---
title: TBM_GETSELEND Meldung (kommstrg. h)
description: Ruft die Endposition des aktuellen Auswahl Bereichs in einer TrackBar ab.
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- Windows-Steuerelemente für TBM_GETSELEND Meldung
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 486d66d3e7fc2dd4d23b89cb5e9406fa81b34638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476803"
---
# <a name="tbm_getselend-message"></a><span data-ttu-id="76b07-104">TBM- \_ getselend-Nachricht</span><span class="sxs-lookup"><span data-stu-id="76b07-104">TBM\_GETSELEND message</span></span>

<span data-ttu-id="76b07-105">Ruft die Endposition des aktuellen Auswahl Bereichs in einer TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="76b07-105">Retrieves the ending position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="76b07-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="76b07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76b07-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76b07-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="76b07-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="76b07-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="76b07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76b07-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="76b07-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="76b07-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76b07-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76b07-111">Return value</span></span>

<span data-ttu-id="76b07-112">Gibt einen 32-Bit-Wert zurück, der die Endposition des aktuellen Auswahl Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="76b07-112">Returns a 32-bit value that specifies the ending position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="76b07-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76b07-113">Remarks</span></span>

<span data-ttu-id="76b07-114">Eine TrackBar kann nur dann einen Auswahlbereich haben, wenn Sie den TSB-Formatvorlagen [**\_ Bereich**](trackbar-control-styles.md) bei der Erstellung angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="76b07-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="76b07-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76b07-115">Requirements</span></span>



| <span data-ttu-id="76b07-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76b07-116">Requirement</span></span> | <span data-ttu-id="76b07-117">Wert</span><span class="sxs-lookup"><span data-stu-id="76b07-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76b07-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76b07-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76b07-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76b07-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76b07-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76b07-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76b07-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76b07-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76b07-122">Header</span><span class="sxs-lookup"><span data-stu-id="76b07-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76b07-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="76b07-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76b07-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76b07-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="76b07-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="76b07-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="76b07-126">**TBM \_ getselstart**</span><span class="sxs-lookup"><span data-stu-id="76b07-126">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="76b07-127">**TBM- \_ Sekunden**</span><span class="sxs-lookup"><span data-stu-id="76b07-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="76b07-128">**TBM- \_ setselend**</span><span class="sxs-lookup"><span data-stu-id="76b07-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="76b07-129">**TBM- \_ setselstart**</span><span class="sxs-lookup"><span data-stu-id="76b07-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





