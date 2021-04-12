---
title: LB_SETSEL Meldung (Winuser. h)
description: Wählt ein Element in einem Listenfeld mit Mehrfachauswahl aus und führt ggf. einen Bildlauf in der Ansicht durch.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- Windows-Steuerelemente für LB_SETSEL Meldung
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478537"
---
# <a name="lb_setsel-message"></a><span data-ttu-id="da4e8-104">LB-Aktivität \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="da4e8-104">LB\_SETSEL message</span></span>

<span data-ttu-id="da4e8-105">Wählt ein Element in einem Listenfeld mit Mehrfachauswahl aus und führt ggf. einen Bildlauf in der Ansicht durch.</span><span class="sxs-lookup"><span data-stu-id="da4e8-105">Selects an item in a multiple-selection list box and, if necessary, scrolls the item into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="da4e8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da4e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da4e8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da4e8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da4e8-108">Gibt an, wie die Auswahl festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="da4e8-108">Specifies how to set the selection.</span></span> <span data-ttu-id="da4e8-109">Wenn dieser Parameter **true** ist, wird das Element ausgewählt und hervorgehoben. Wenn der Wert **false** ist, wird die Hervorhebung entfernt, und das Element wird nicht mehr ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="da4e8-109">If this parameter is **TRUE**, the item is selected and highlighted; if it is **FALSE**, the highlight is removed and the item is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="da4e8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da4e8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da4e8-111">Gibt den NULL basierten Index des festzulegenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="da4e8-111">Specifies the zero-based index of the item to set.</span></span> <span data-ttu-id="da4e8-112">Wenn dieser Parameter-1 ist, wird die Auswahl in Abhängigkeit vom Wert von *wParam* hinzugefügt oder aus allen Elementen entfernt, und es erfolgt kein Bildlauf.</span><span class="sxs-lookup"><span data-stu-id="da4e8-112">If this parameter is -1, the selection is added to or removed from all items, depending on the value of *wParam*, and no scrolling occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da4e8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da4e8-113">Return value</span></span>

<span data-ttu-id="da4e8-114">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="da4e8-114">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="da4e8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da4e8-115">Remarks</span></span>

<span data-ttu-id="da4e8-116">Verwenden Sie diese Meldung nur für Listenfelder mit Mehrfachauswahl.</span><span class="sxs-lookup"><span data-stu-id="da4e8-116">Use this message only with multiple-selection list boxes.</span></span>

## <a name="requirements"></a><span data-ttu-id="da4e8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da4e8-117">Requirements</span></span>



| <span data-ttu-id="da4e8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da4e8-118">Requirement</span></span> | <span data-ttu-id="da4e8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="da4e8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da4e8-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da4e8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="da4e8-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da4e8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da4e8-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da4e8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="da4e8-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da4e8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da4e8-124">Header</span><span class="sxs-lookup"><span data-stu-id="da4e8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="da4e8-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="da4e8-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4e8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da4e8-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="da4e8-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="da4e8-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da4e8-128">**LB- \_ GetSEL**</span><span class="sxs-lookup"><span data-stu-id="da4e8-128">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="da4e8-129">**LB- \_ selitemrange**</span><span class="sxs-lookup"><span data-stu-id="da4e8-129">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> </dl>

 

 





