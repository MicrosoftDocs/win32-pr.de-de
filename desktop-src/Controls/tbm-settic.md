---
title: TBM_SETTIC Meldung (kommstrg. h)
description: Legt einen Teil Strich in einer TrackBar an der angegebenen logischen Position fest.
ms.assetid: 89b42cac-967e-40c7-9fab-2bd76f06f3f9
keywords:
- Windows-Steuerelemente für TBM_SETTIC Meldung
topic_type:
- apiref
api_name:
- TBM_SETTIC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a42839157125c8def28a19dd9c2ccce21d3b96c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103222"
---
# <a name="tbm_settic-message"></a><span data-ttu-id="303f4-104">TBM- \_ SetTic-Nachricht</span><span class="sxs-lookup"><span data-stu-id="303f4-104">TBM\_SETTIC message</span></span>

<span data-ttu-id="303f4-105">Legt einen Teil Strich in einer TrackBar an der angegebenen logischen Position fest.</span><span class="sxs-lookup"><span data-stu-id="303f4-105">Sets a tick mark in a trackbar at the specified logical position.</span></span>

## <a name="parameters"></a><span data-ttu-id="303f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="303f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="303f4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="303f4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="303f4-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="303f4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="303f4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="303f4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="303f4-110">Position des Teil Strichs.</span><span class="sxs-lookup"><span data-stu-id="303f4-110">Position of the tick mark.</span></span> <span data-ttu-id="303f4-111">Bei diesem Parameter kann es sich um einen beliebigen ganzzahligen Wert in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen handeln.</span><span class="sxs-lookup"><span data-stu-id="303f4-111">This parameter can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="303f4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="303f4-112">Return value</span></span>

<span data-ttu-id="303f4-113">Gibt **true** zurück, wenn der Teil Strich festgelegt ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="303f4-113">Returns **TRUE** if the tick mark is set, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="303f4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="303f4-114">Remarks</span></span>

<span data-ttu-id="303f4-115">Eine TrackBar erstellt eigene erste und letzte Teil Striche.</span><span class="sxs-lookup"><span data-stu-id="303f4-115">A trackbar creates its own first and last tick marks.</span></span> <span data-ttu-id="303f4-116">Verwenden Sie diese Meldung nicht, um den ersten und den letzten Teil Strich festzulegen.</span><span class="sxs-lookup"><span data-stu-id="303f4-116">Do not use this message to set the first and last tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="303f4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="303f4-117">Requirements</span></span>



| <span data-ttu-id="303f4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="303f4-118">Requirement</span></span> | <span data-ttu-id="303f4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="303f4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="303f4-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="303f4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="303f4-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="303f4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="303f4-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="303f4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="303f4-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="303f4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="303f4-124">Header</span><span class="sxs-lookup"><span data-stu-id="303f4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="303f4-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="303f4-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="303f4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="303f4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="303f4-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="303f4-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="303f4-128">**TBM- \_ getptics**</span><span class="sxs-lookup"><span data-stu-id="303f4-128">**TBM\_GETPTICS**</span></span>](tbm-getptics.md)
</dt> <dt>

[<span data-ttu-id="303f4-129">**TBM \_ GetTic**</span><span class="sxs-lookup"><span data-stu-id="303f4-129">**TBM\_GETTIC**</span></span>](tbm-gettic.md)
</dt> </dl>

 

 





