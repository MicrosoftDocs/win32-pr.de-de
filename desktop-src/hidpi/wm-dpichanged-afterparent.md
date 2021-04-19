---
title: WM_DPICHANGED_AFTERPARENT Meldung (Winuser. h)
description: Für Fenster der obersten Ebene von Monitor v2 wird diese Nachricht an alle hwnds in der untergeordneten hwdn-Struktur des Fensters gesendet, das eine dpi-Änderung durchläuft. | WM_DPICHANGED_AFTERPARENT Meldung (Winuser. h)
ms.assetid: FEA1BF07-55B6-4584-ABD3-340515831E0A
keywords:
- WM_DPICHANGED_AFTERPARENT Message High dpi
topic_type:
- apiref
api_name:
- WM_DPICHANGED_AFTERPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cc76602662cefba42f62bd3ed85913ade40f15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106357209"
---
# <a name="wm_dpichanged_afterparent-message"></a><span data-ttu-id="00790-105">WM-dpichanged-nach-über \_ \_ geordnete Nachricht</span><span class="sxs-lookup"><span data-stu-id="00790-105">WM\_DPICHANGED\_AFTERPARENT message</span></span>

<span data-ttu-id="00790-106">Für Fenster der obersten Ebene von [Monitor v2](dpi-awareness-context.md) wird diese Nachricht an alle hwnds in der untergeordneten hwdn-Struktur des Fensters gesendet, das eine dpi-Änderung durchläuft.</span><span class="sxs-lookup"><span data-stu-id="00790-106">For [Per Monitor v2](dpi-awareness-context.md) top-level windows, this message is sent to all HWNDs in the child HWDN tree of the window that is undergoing a DPI change.</span></span> <span data-ttu-id="00790-107">Diese Meldung tritt auf, nachdem das Fenster der obersten Ebene [**WM \_ dpichanged**](wm-dpichanged.md)empfängt und die untergeordnete Struktur von oben nach unten durchläuft.</span><span class="sxs-lookup"><span data-stu-id="00790-107">This message occurs after the top-level window receives [**WM\_DPICHANGED**](wm-dpichanged.md), and traverses the child tree from the top down.</span></span>


```C++
#define WM_DPICHANGED_AFTERPARENT       0x02E3
```



## <a name="parameters"></a><span data-ttu-id="00790-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="00790-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00790-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="00790-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00790-110">Dieser Wert wird nicht verwendet und ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="00790-110">This value is unused and will be zero.</span></span>

</dd> <dt>

<span data-ttu-id="00790-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00790-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00790-112">Dieser Wert wird nicht verwendet und ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="00790-112">This value is unused and will be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00790-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00790-113">Return value</span></span>

<span data-ttu-id="00790-114">Dieser Wert wird vom System nicht verwendet und ignoriert.</span><span class="sxs-lookup"><span data-stu-id="00790-114">This value is unused and ignored by the system.</span></span>

## <a name="remarks"></a><span data-ttu-id="00790-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00790-115">Remarks</span></span>

<span data-ttu-id="00790-116">In [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)gibt es keine Standardbehandlung für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="00790-116">There is no default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="00790-117">Diese Meldung wird nur gesendet, wenn das Fenster der obersten Ebene den dpi-Kontext PMv2 hat.</span><span class="sxs-lookup"><span data-stu-id="00790-117">This message is only sent when the top-level window has a DPI awareness context of PMv2.</span></span>

## <a name="requirements"></a><span data-ttu-id="00790-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00790-118">Requirements</span></span>



| <span data-ttu-id="00790-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00790-119">Requirement</span></span> | <span data-ttu-id="00790-120">Wert</span><span class="sxs-lookup"><span data-stu-id="00790-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00790-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00790-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00790-122">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00790-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="00790-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00790-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00790-124">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="00790-124">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="00790-125">Header</span><span class="sxs-lookup"><span data-stu-id="00790-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="00790-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="00790-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00790-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00790-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00790-128">**WM- \_ dpichanged**</span><span class="sxs-lookup"><span data-stu-id="00790-128">**WM\_DPICHANGED**</span></span>](wm-dpichanged.md)
</dt> <dt>

[<span data-ttu-id="00790-129">**WM \_ dpichanged \_ beforeparent**</span><span class="sxs-lookup"><span data-stu-id="00790-129">**WM\_DPICHANGED\_BEFOREPARENT**</span></span>](wm-dpichanged-beforeparent.md)
</dt> </dl>

 

