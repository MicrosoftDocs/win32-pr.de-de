---
title: EM_SCROLLCARET Meldung (Winuser. h)
description: Führt einen Bildlauf in einem Bearbeitungs Steuerelement durch. Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.
ms.assetid: 7a33034d-9369-49f8-a881-0c1d2cedff6a
keywords:
- Windows-Steuerelemente für EM_SCROLLCARET Meldung
topic_type:
- apiref
api_name:
- EM_SCROLLCARET
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa9f4bd69605f5e8fad36a683c9be2894546cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106263"
---
# <a name="em_scrollcaret-message"></a><span data-ttu-id="477cc-105">EM \_ scrollcaret-Meldung</span><span class="sxs-lookup"><span data-stu-id="477cc-105">EM\_SCROLLCARET message</span></span>

<span data-ttu-id="477cc-106">Führt einen Bildlauf in einem Bearbeitungs Steuerelement durch.</span><span class="sxs-lookup"><span data-stu-id="477cc-106">Scrolls the caret into view in an edit control.</span></span> <span data-ttu-id="477cc-107">Sie können diese Nachricht entweder an ein Bearbeitungs Steuerelement oder ein Rich Edit-Steuerelement senden.</span><span class="sxs-lookup"><span data-stu-id="477cc-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="477cc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="477cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="477cc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="477cc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="477cc-110">Dieser Parameter ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="477cc-110">This parameter is reserved.</span></span> <span data-ttu-id="477cc-111">Er sollte auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="477cc-111">It should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="477cc-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="477cc-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="477cc-113">Dieser Parameter ist reserviert.</span><span class="sxs-lookup"><span data-stu-id="477cc-113">This parameter is reserved.</span></span> <span data-ttu-id="477cc-114">Er sollte auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="477cc-114">It should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="477cc-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="477cc-115">Return value</span></span>

<span data-ttu-id="477cc-116">Der Rückgabewert ist nicht sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="477cc-116">The return value is not meaningful.</span></span>

## <a name="remarks"></a><span data-ttu-id="477cc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="477cc-117">Remarks</span></span>

<span data-ttu-id="477cc-118">Umfassende **Bearbeitung:** Wird in Microsoft Rich Edit 1,0 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="477cc-118">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="477cc-119">Informationen zur Kompatibilität von Rich-Edit-Versionen mit den verschiedenen Systemversionen finden Sie unter Informationen [zu Rich Edit](about-rich-edit-controls.md)-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="477cc-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="477cc-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="477cc-120">Requirements</span></span>



| <span data-ttu-id="477cc-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="477cc-121">Requirement</span></span> | <span data-ttu-id="477cc-122">Wert</span><span class="sxs-lookup"><span data-stu-id="477cc-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="477cc-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="477cc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="477cc-124">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="477cc-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="477cc-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="477cc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="477cc-126">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="477cc-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="477cc-127">Header</span><span class="sxs-lookup"><span data-stu-id="477cc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="477cc-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="477cc-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="477cc-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="477cc-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="477cc-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="477cc-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="477cc-131">**EM- \_ linescroll**</span><span class="sxs-lookup"><span data-stu-id="477cc-131">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="477cc-132">**EM- \_ Scroll**</span><span class="sxs-lookup"><span data-stu-id="477cc-132">**EM\_SCROLL**</span></span>](em-scroll.md)
</dt> <dt>

[<span data-ttu-id="477cc-133">**WM- \_ VScroll**</span><span class="sxs-lookup"><span data-stu-id="477cc-133">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

 





