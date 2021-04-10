---
title: SBM_GETPOS Meldung (Winuser. h)
description: Die SBM- \_ GetPos-Nachricht wird gesendet, um die aktuelle Position des Bild Lauf Felds eines ScrollBar-Steuer Elements abzurufen.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- Windows-Steuerelemente für SBM_GETPOS Meldung
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956881"
---
# <a name="sbm_getpos-message"></a><span data-ttu-id="c3062-104">SBM- \_ GetPos-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c3062-104">SBM\_GETPOS message</span></span>

<span data-ttu-id="c3062-105">Die **SBM- \_ GetPos** -Nachricht wird gesendet, um die aktuelle Position des Bild Lauf Felds eines ScrollBar-Steuer Elements abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c3062-105">The **SBM\_GETPOS** message is sent to retrieve the current position of the scroll box of a scroll bar control.</span></span> <span data-ttu-id="c3062-106">Die aktuelle Position ist ein relativer Wert, der vom aktuellen scrollbereich abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="c3062-106">The current position is a relative value that depends on the current scrolling range.</span></span> <span data-ttu-id="c3062-107">Wenn der scrollbereich z. b. zwischen 0 und 100 liegt und sich das Bild Lauf Feld in der Mitte des Balkens befindet, ist die aktuelle Position 50.</span><span class="sxs-lookup"><span data-stu-id="c3062-107">For example, if the scrolling range is 0 through 100 and the scroll box is in the middle of the bar, the current position is 50.</span></span>

<span data-ttu-id="c3062-108">Anwendungen sollten diese Nachricht nicht direkt senden.</span><span class="sxs-lookup"><span data-stu-id="c3062-108">Applications should not send this message directly.</span></span> <span data-ttu-id="c3062-109">Stattdessen sollten Sie die [**getscrollpos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3062-109">Instead, they should use the [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) function.</span></span> <span data-ttu-id="c3062-110">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c3062-110">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="c3062-111">Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **getscrollpos** -Funktion ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c3062-111">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollPos** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3062-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3062-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3062-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3062-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3062-114">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c3062-114">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c3062-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3062-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3062-116">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c3062-116">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3062-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3062-117">Return value</span></span>

<span data-ttu-id="c3062-118">Der Rückgabewert ist die aktuelle Position des Bild Lauf Felds auf der Bild Lauf Leiste.</span><span class="sxs-lookup"><span data-stu-id="c3062-118">The return value is the current position of the scroll box in the scroll bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3062-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3062-119">Requirements</span></span>



| <span data-ttu-id="c3062-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3062-120">Requirement</span></span> | <span data-ttu-id="c3062-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c3062-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3062-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c3062-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c3062-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3062-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c3062-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c3062-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c3062-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c3062-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c3062-126">Header</span><span class="sxs-lookup"><span data-stu-id="c3062-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3062-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c3062-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3062-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3062-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c3062-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c3062-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c3062-130">**SBM- \_ GetRange**</span><span class="sxs-lookup"><span data-stu-id="c3062-130">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="c3062-131">**SBM- \_ SetPos**</span><span class="sxs-lookup"><span data-stu-id="c3062-131">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="c3062-132">**SBM-über \_ Tragung**</span><span class="sxs-lookup"><span data-stu-id="c3062-132">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="c3062-133">**SBM- \_ abzeichnende**</span><span class="sxs-lookup"><span data-stu-id="c3062-133">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

