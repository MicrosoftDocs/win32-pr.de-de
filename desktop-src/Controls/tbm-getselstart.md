---
title: TBM_GETSELSTART Meldung (kommstrg. h)
description: Ruft die Anfangsposition des aktuellen Auswahl Bereichs in einer TrackBar ab.
ms.assetid: 0000df2a-c40d-40c2-b120-e5d4fe6c5016
keywords:
- Windows-Steuerelemente für TBM_GETSELSTART Meldung
topic_type:
- apiref
api_name:
- TBM_GETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af796c57adb3615241a8f5b702ff58062468509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341609"
---
# <a name="tbm_getselstart-message"></a><span data-ttu-id="8d29a-104">TBM \_ getselstart-Nachricht</span><span class="sxs-lookup"><span data-stu-id="8d29a-104">TBM\_GETSELSTART message</span></span>

<span data-ttu-id="8d29a-105">Ruft die Anfangsposition des aktuellen Auswahl Bereichs in einer TrackBar ab.</span><span class="sxs-lookup"><span data-stu-id="8d29a-105">Retrieves the starting position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d29a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d29a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d29a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d29a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8d29a-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8d29a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8d29a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d29a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8d29a-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8d29a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d29a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d29a-111">Return value</span></span>

<span data-ttu-id="8d29a-112">Gibt einen 32-Bit-Wert zurück, der die Anfangsposition des aktuellen Auswahl Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="8d29a-112">Returns a 32-bit value that specifies the starting position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d29a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d29a-113">Remarks</span></span>

<span data-ttu-id="8d29a-114">Eine TrackBar kann nur dann einen Auswahlbereich haben, wenn Sie den TSB-Formatvorlagen [**\_ Bereich**](trackbar-control-styles.md) bei der Erstellung angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="8d29a-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d29a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8d29a-115">Requirements</span></span>



| <span data-ttu-id="8d29a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8d29a-116">Requirement</span></span> | <span data-ttu-id="8d29a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8d29a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d29a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8d29a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8d29a-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d29a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d29a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8d29a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8d29a-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8d29a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d29a-122">Header</span><span class="sxs-lookup"><span data-stu-id="8d29a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d29a-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d29a-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d29a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d29a-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d29a-125">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8d29a-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8d29a-126">**TBM- \_ getselend**</span><span class="sxs-lookup"><span data-stu-id="8d29a-126">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="8d29a-127">**TBM- \_ Sekunden**</span><span class="sxs-lookup"><span data-stu-id="8d29a-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="8d29a-128">**TBM- \_ setselend**</span><span class="sxs-lookup"><span data-stu-id="8d29a-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="8d29a-129">**TBM- \_ setselstart**</span><span class="sxs-lookup"><span data-stu-id="8d29a-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





