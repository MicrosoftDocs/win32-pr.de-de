---
title: SBM_SETRANGEREDRAW Meldung (Winuser. h)
description: Eine Anwendung sendet die SBM \_ setrangeredraw-Nachricht an ein ScrollBar-Steuerelement, um die minimalen und maximalen Positionswerte festzulegen und das Steuerelement neu zu zeichnen.
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- Windows-Steuerelemente für SBM_SETRANGEREDRAW Meldung
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040090"
---
# <a name="sbm_setrangeredraw-message"></a><span data-ttu-id="53a3a-104">SBM- \_ Nachricht "abzeichnet"</span><span class="sxs-lookup"><span data-stu-id="53a3a-104">SBM\_SETRANGEREDRAW message</span></span>

<span data-ttu-id="53a3a-105">Eine Anwendung sendet die **SBM \_ setrangeredraw** -Nachricht an ein ScrollBar-Steuerelement, um die minimalen und maximalen Positionswerte festzulegen und das Steuerelement neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="53a3a-105">An application sends the **SBM\_SETRANGEREDRAW** message to a scroll bar control to set the minimum and maximum position values and to redraw the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="53a3a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53a3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53a3a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="53a3a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53a3a-108">Gibt die minimale Bild Lauf Position an.</span><span class="sxs-lookup"><span data-stu-id="53a3a-108">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="53a3a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="53a3a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="53a3a-110">Gibt die maximale Scrollposition an.</span><span class="sxs-lookup"><span data-stu-id="53a3a-110">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53a3a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53a3a-111">Return value</span></span>

<span data-ttu-id="53a3a-112">**ComCtl32.dll Version 5,0**: Wenn sich die Position des Bild Lauf Felds geändert hat, ist der Rückgabewert die vorherige Position des Bild Lauf Felds. Andernfalls ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="53a3a-112">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="53a3a-113">**ComCtl32.dll Version 6,0**: die aktuelle Position des Bild Lauf Felds, unabhängig davon, ob es geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="53a3a-113">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="53a3a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53a3a-114">Remarks</span></span>

<span data-ttu-id="53a3a-115">Die standardmäßigen und maximalen Positionswerte sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="53a3a-115">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="53a3a-116">Der Unterschied zwischen den Werten, die von den *wParam* -und *LPARAM* -Parametern angegeben werden, darf nicht größer sein als MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="53a3a-116">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="53a3a-117">Wenn die minimalen und maximalen Positionswerte gleich sind, wird das Bild Lauf leisten-Steuerelement ausgeblendet und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="53a3a-117">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="53a3a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53a3a-118">Requirements</span></span>



| <span data-ttu-id="53a3a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53a3a-119">Requirement</span></span> | <span data-ttu-id="53a3a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="53a3a-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53a3a-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53a3a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="53a3a-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53a3a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="53a3a-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53a3a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="53a3a-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53a3a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="53a3a-125">Header</span><span class="sxs-lookup"><span data-stu-id="53a3a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="53a3a-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="53a3a-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53a3a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53a3a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="53a3a-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="53a3a-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="53a3a-129">**SBM- \_ GetPos**</span><span class="sxs-lookup"><span data-stu-id="53a3a-129">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="53a3a-130">**SBM- \_ GetRange**</span><span class="sxs-lookup"><span data-stu-id="53a3a-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="53a3a-131">**SBM- \_ SetPos**</span><span class="sxs-lookup"><span data-stu-id="53a3a-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="53a3a-132">**SBM-über \_ Tragung**</span><span class="sxs-lookup"><span data-stu-id="53a3a-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> </dl>

 

 





