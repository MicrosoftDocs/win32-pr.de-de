---
title: LB_GETCARETINDEX Meldung (Winuser. h)
description: Ruft den Index des Elements ab, das in einem Listenfeld mit Mehrfachauswahl den Fokus hat. Das Element ist möglicherweise nicht ausgewählt.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- Windows-Steuerelemente für LB_GETCARETINDEX Meldung
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040954"
---
# <a name="lb_getcaretindex-message"></a><span data-ttu-id="49d1d-105">LB- \_ getcaretindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="49d1d-105">LB\_GETCARETINDEX message</span></span>

<span data-ttu-id="49d1d-106">Ruft den Index des Elements ab, das in einem Listenfeld mit Mehrfachauswahl den Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="49d1d-106">Retrieves the index of the item that has the focus in a multiple-selection list box.</span></span> <span data-ttu-id="49d1d-107">Das Element ist möglicherweise nicht ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="49d1d-107">The item may or may not be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="49d1d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="49d1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49d1d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49d1d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49d1d-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="49d1d-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49d1d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49d1d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49d1d-112">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="49d1d-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49d1d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49d1d-113">Return value</span></span>

<span data-ttu-id="49d1d-114">Der Rückgabewert ist der null basierte Index des fokussierten Listenfeld Elements oder 0, wenn kein Element den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="49d1d-114">The return value is the zero-based index of the focused list box item, or 0 if no item has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="49d1d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49d1d-115">Remarks</span></span>

<span data-ttu-id="49d1d-116">Diese Meldung kann auch verwendet werden, um den Index des Elements zu erhalten, das derzeit in einem Listenfeld mit einer einzelnen Auswahl ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="49d1d-116">This message can also be used to get the index of the item that is currently selected in a single-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="49d1d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49d1d-117">Requirements</span></span>



| <span data-ttu-id="49d1d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49d1d-118">Requirement</span></span> | <span data-ttu-id="49d1d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="49d1d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49d1d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49d1d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49d1d-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49d1d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="49d1d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49d1d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49d1d-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49d1d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49d1d-124">Header</span><span class="sxs-lookup"><span data-stu-id="49d1d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="49d1d-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="49d1d-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49d1d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49d1d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d1d-127">**LB- \_ setcaretindex**</span><span class="sxs-lookup"><span data-stu-id="49d1d-127">**LB\_SETCARETINDEX**</span></span>](lb-setcaretindex.md)
</dt> </dl>

 

 





