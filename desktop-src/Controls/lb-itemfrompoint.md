---
title: LB_ITEMFROMPOINT Meldung (Winuser. h)
description: Ruft den NULL basierten Index des Elements ab, das dem angegebenen Punkt in einem Listenfeld am nächsten liegt.
ms.assetid: 5739eccb-e708-4ddb-ac97-d3e6c6120842
keywords:
- Windows-Steuerelemente für LB_ITEMFROMPOINT Meldung
topic_type:
- apiref
api_name:
- LB_ITEMFROMPOINT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c4f06b9de8e6580c81c7faf7ddb8c287a148b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743024"
---
# <a name="lb_itemfrompoint-message"></a><span data-ttu-id="9f419-104">LB- \_ itemfrompoint-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9f419-104">LB\_ITEMFROMPOINT message</span></span>

<span data-ttu-id="9f419-105">Ruft den NULL basierten Index des Elements ab, das dem angegebenen Punkt in einem Listenfeld am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="9f419-105">Gets the zero-based index of the item nearest the specified point in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f419-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f419-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f419-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f419-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f419-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="9f419-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9f419-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f419-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f419-110">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt die x-Koordinate eines Punkts relativ zur oberen linken Ecke des Client Bereichs des Listen Felds an.</span><span class="sxs-lookup"><span data-stu-id="9f419-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the x-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

<span data-ttu-id="9f419-111">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt die y-Koordinate eines Punkts relativ zur oberen linken Ecke des Client Bereichs des Listen Felds an.</span><span class="sxs-lookup"><span data-stu-id="9f419-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the y-coordinate of a point, relative to the upper-left corner of the client area of the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f419-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f419-112">Return value</span></span>

<span data-ttu-id="9f419-113">Der Rückgabewert enthält den Index des nächstgelegenen Elements im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9f419-113">The return value contains the index of the nearest item in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span> <span data-ttu-id="9f419-114">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist 0 (null), wenn sich der angegebene Punkt im Client Bereich des Listen Felds befindet, oder eines, wenn es außerhalb des Client Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="9f419-114">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is zero if the specified point is in the client area of the list box, or one if it is outside the client area.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f419-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f419-115">Requirements</span></span>



| <span data-ttu-id="9f419-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f419-116">Requirement</span></span> | <span data-ttu-id="9f419-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9f419-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f419-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f419-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9f419-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f419-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9f419-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f419-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9f419-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f419-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f419-122">Header</span><span class="sxs-lookup"><span data-stu-id="9f419-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f419-123"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9f419-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f419-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f419-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f419-125">**Makelparam**</span><span class="sxs-lookup"><span data-stu-id="9f419-125">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

