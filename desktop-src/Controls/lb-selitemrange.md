---
title: LB_SELITEMRANGE Meldung (Winuser. h)
description: Aktiviert oder deaktiviert ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit Mehrfachauswahl.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- Windows-Steuerelemente für LB_SELITEMRANGE Meldung
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040896"
---
# <a name="lb_selitemrange-message"></a><span data-ttu-id="d9533-104">LB- \_ selitemrange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d9533-104">LB\_SELITEMRANGE message</span></span>

<span data-ttu-id="d9533-105">Aktiviert oder deaktiviert ein oder mehrere aufeinander folgende Elemente in einem Listenfeld mit Mehrfachauswahl.</span><span class="sxs-lookup"><span data-stu-id="d9533-105">Selects or deselects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9533-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9533-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9533-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9533-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9533-108">" **True** ", um den Bereich von Elementen auszuwählen, oder " **false** ", um die Auswahl zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d9533-108">**TRUE** to select the range of items, or **FALSE** to deselect it.</span></span>

</dd> <dt>

<span data-ttu-id="d9533-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9533-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9533-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den NULL basierten Index des ersten Elements an, das ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9533-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the first item to select.</span></span> <span data-ttu-id="d9533-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den NULL basierten Index des letzten Elements an, das ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9533-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9533-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9533-112">Return value</span></span>

<span data-ttu-id="d9533-113">Wenn ein Fehler auftritt, ist der Rückgabewert lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d9533-113">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9533-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9533-114">Remarks</span></span>

<span data-ttu-id="d9533-115">Verwenden Sie diese Meldung nur für Listenfelder mit Mehrfachauswahl.</span><span class="sxs-lookup"><span data-stu-id="d9533-115">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="d9533-116">Diese Meldung kann einen Bereich nur innerhalb der ersten 65.536 Elemente auswählen.</span><span class="sxs-lookup"><span data-stu-id="d9533-116">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9533-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9533-117">Requirements</span></span>



| <span data-ttu-id="d9533-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9533-118">Requirement</span></span> | <span data-ttu-id="d9533-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d9533-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9533-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d9533-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d9533-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9533-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d9533-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d9533-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d9533-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d9533-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d9533-124">Header</span><span class="sxs-lookup"><span data-stu-id="d9533-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9533-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d9533-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9533-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9533-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d9533-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d9533-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d9533-128">**LB- \_ selitemrangeex**</span><span class="sxs-lookup"><span data-stu-id="d9533-128">**LB\_SELITEMRANGEEX**</span></span>](lb-selitemrangeex.md)
</dt> <dt>

[<span data-ttu-id="d9533-129">**LB- \_ Sekunden**</span><span class="sxs-lookup"><span data-stu-id="d9533-129">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> <dt>

<span data-ttu-id="d9533-130">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d9533-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d9533-131">**Makelparam**</span><span class="sxs-lookup"><span data-stu-id="d9533-131">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

