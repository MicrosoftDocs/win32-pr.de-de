---
title: SBM_SETPOS Meldung (Winuser. h)
description: Die SBM- \_ SetPos-Nachricht wird gesendet, um die Position des Bild Lauf Felds (Thumb) festzulegen, und, falls angefordert, die Schiebe Leiste neu gezeichnet, um die neue Position des Bild Lauf Felds widerzuspiegeln.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- Windows-Steuerelemente für SBM_SETPOS Meldung
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479155"
---
# <a name="sbm_setpos-message"></a><span data-ttu-id="519ed-104">SBM- \_ SetPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="519ed-104">SBM\_SETPOS message</span></span>

<span data-ttu-id="519ed-105">Die **SBM- \_ SetPos** -Nachricht wird gesendet, um die Position des Bild Lauf Felds (Thumb) festzulegen, und, falls angefordert, die Schiebe Leiste neu gezeichnet, um die neue Position des Bild Lauf Felds widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="519ed-105">The **SBM\_SETPOS** message is sent to set the position of the scroll box (thumb) and, if requested, redraw the scroll bar to reflect the new position of the scroll box.</span></span>

<span data-ttu-id="519ed-106">Anwendungen sollten diese Nachricht nicht direkt senden.</span><span class="sxs-lookup"><span data-stu-id="519ed-106">Applications should not send this message directly.</span></span> <span data-ttu-id="519ed-107">Stattdessen sollten Sie die [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="519ed-107">Instead, they should use the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span> <span data-ttu-id="519ed-108">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="519ed-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="519ed-109">Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **setscrollpos** -Funktion ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="519ed-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollPos** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="519ed-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="519ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="519ed-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="519ed-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="519ed-112">Gibt die neue Position des Bild Lauf Felds an.</span><span class="sxs-lookup"><span data-stu-id="519ed-112">Specifies the new position of the scroll box.</span></span> <span data-ttu-id="519ed-113">Er muss innerhalb des scrollbereichs liegen.</span><span class="sxs-lookup"><span data-stu-id="519ed-113">It must be within the scrolling range.</span></span> <span data-ttu-id="519ed-114">Wenn dieser Parameter außerhalb des scrollbereichs liegt, wird der Wert auf den nächstgelegenen gültigen Wert aufgerundet.</span><span class="sxs-lookup"><span data-stu-id="519ed-114">If this parameter is outside of the scrolling range, the value is rounded up or down to the nearest valid value.</span></span>

</dd> <dt>

<span data-ttu-id="519ed-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="519ed-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="519ed-116">Gibt an, ob die Schiebe Leiste neu gezeichnet werden soll, um die neue Position des Bild Lauf Felds widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="519ed-116">Specifies whether the scroll bar should be redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="519ed-117">Wenn dieser Parameter **true** ist, wird die Scrollleiste neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="519ed-117">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="519ed-118">Wenn der Wert **false** ist, wird die Scrollleiste nicht neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="519ed-118">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="519ed-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="519ed-119">Return value</span></span>

<span data-ttu-id="519ed-120">**ComCtl32.dll Version 5,0**: Wenn sich die Position des Bild Lauf Felds geändert hat, ist der Rückgabewert die vorherige Position des Bild Lauf Felds. Andernfalls ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="519ed-120">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="519ed-121">**ComCtl32.dll Version 6,0**: die aktuelle Position des Bild Lauf Felds, unabhängig davon, ob es geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="519ed-121">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="519ed-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="519ed-122">Remarks</span></span>

<span data-ttu-id="519ed-123">Wenn das Schiebe leisten-Steuerelement durch einen nachfolgenden Rückruf einer anderen Funktion neu gezeichnet wird, ist das Festlegen des *LPARAM* -Parameters auf **false** nützlich.</span><span class="sxs-lookup"><span data-stu-id="519ed-123">If the scroll bar control is redrawn by a subsequent call to another function, setting the *lParam* parameter to **FALSE** is useful.</span></span>

## <a name="requirements"></a><span data-ttu-id="519ed-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="519ed-124">Requirements</span></span>



| <span data-ttu-id="519ed-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="519ed-125">Requirement</span></span> | <span data-ttu-id="519ed-126">Wert</span><span class="sxs-lookup"><span data-stu-id="519ed-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="519ed-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="519ed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="519ed-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="519ed-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="519ed-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="519ed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="519ed-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="519ed-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="519ed-131">Header</span><span class="sxs-lookup"><span data-stu-id="519ed-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="519ed-132"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="519ed-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="519ed-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="519ed-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="519ed-134">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="519ed-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="519ed-135">**SBM- \_ GetPos**</span><span class="sxs-lookup"><span data-stu-id="519ed-135">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="519ed-136">**SBM- \_ GetRange**</span><span class="sxs-lookup"><span data-stu-id="519ed-136">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="519ed-137">**SBM-über \_ Tragung**</span><span class="sxs-lookup"><span data-stu-id="519ed-137">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="519ed-138">**SBM- \_ abzeichnende**</span><span class="sxs-lookup"><span data-stu-id="519ed-138">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

