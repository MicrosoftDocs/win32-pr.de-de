---
title: WM_DPICHANGED_BEFOREPARENT Meldung (Winuser. h)
description: Für Fenster der obersten Ebene von Monitor v2 wird diese Nachricht an alle hwnds in der untergeordneten hwdn-Struktur des Fensters gesendet, das eine dpi-Änderung durchläuft. | WM_DPICHANGED_BEFOREPARENT Meldung (Winuser. h)
ms.assetid: EC8CC313-565F-451F-AE18-66F3B63303CE
keywords:
- WM_DPICHANGED_BEFOREPARENT Message High dpi
topic_type:
- apiref
api_name:
- WM_DPICHANGED_BEFOREPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16641916cb16b789f2349a53b09dbd2af5f520f3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961504"
---
# <a name="wm_dpichanged_beforeparent-message"></a><span data-ttu-id="5b41e-105">WM- \_ dpichanged- \_ Meldung "beforeparent"</span><span class="sxs-lookup"><span data-stu-id="5b41e-105">WM\_DPICHANGED\_BEFOREPARENT message</span></span>

<span data-ttu-id="5b41e-106">Für Fenster der obersten Ebene von [Monitor v2](dpi-awareness-context.md) wird diese Nachricht an alle hwnds in der untergeordneten hwdn-Struktur des Fensters gesendet, das eine dpi-Änderung durchläuft.</span><span class="sxs-lookup"><span data-stu-id="5b41e-106">For [Per Monitor v2](dpi-awareness-context.md) top-level windows, this message is sent to all HWNDs in the child HWDN tree of the window that is undergoing a DPI change.</span></span> <span data-ttu-id="5b41e-107">Diese Meldung tritt auf, bevor das Fenster der obersten Ebene [**WM \_ dpichanged**](wm-dpichanged.md)empfängt und die untergeordnete Struktur von unten nach oben durchläuft.</span><span class="sxs-lookup"><span data-stu-id="5b41e-107">This message occurs before the top-level window receives [**WM\_DPICHANGED**](wm-dpichanged.md), and traverses the child tree from the bottom up.</span></span>


```C++
#define WM_DPICHANGED_BEFOREPARENT       0x02E2
```



## <a name="parameters"></a><span data-ttu-id="5b41e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b41e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b41e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b41e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b41e-110">Dieser Wert wird nicht verwendet und ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5b41e-110">This value is unused and will be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5b41e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b41e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b41e-112">Dieser Wert wird nicht verwendet und ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5b41e-112">This value is unused and will be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b41e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b41e-113">Return value</span></span>

<span data-ttu-id="5b41e-114">Dieser Wert wird vom System nicht verwendet und ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5b41e-114">This value is unused and ignored by the system.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b41e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b41e-115">Remarks</span></span>

<span data-ttu-id="5b41e-116">In [defwindowproc](/windows/win32/api/winuser/nf-winuser-defwindowproca)gibt es keine Standardbehandlung für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5b41e-116">There is no default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="5b41e-117">Diese Meldung wird nur gesendet, wenn das Fenster der obersten Ebene den dpi-Kontext PMv2 hat.</span><span class="sxs-lookup"><span data-stu-id="5b41e-117">This message is only sent when the top-level window has a DPI awareness context of PMv2.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b41e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b41e-118">Requirements</span></span>



| <span data-ttu-id="5b41e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b41e-119">Requirement</span></span> | <span data-ttu-id="5b41e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5b41e-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b41e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5b41e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5b41e-122">Windows 10, Version 1703, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b41e-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5b41e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5b41e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5b41e-124">Nur Windows Server 2016 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5b41e-124">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5b41e-125">Header</span><span class="sxs-lookup"><span data-stu-id="5b41e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b41e-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b41e-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b41e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b41e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b41e-128">**WM- \_ dpichanged**</span><span class="sxs-lookup"><span data-stu-id="5b41e-128">**WM\_DPICHANGED**</span></span>](wm-dpichanged.md)
</dt> <dt>

[<span data-ttu-id="5b41e-129">**WM- \_ dpichanged nach dem über \_ geordneten Element**</span><span class="sxs-lookup"><span data-stu-id="5b41e-129">**WM\_DPICHANGED\_AFTERPARENT**</span></span>](wm-dpichanged-afterparent.md)
</dt> </dl>

 

