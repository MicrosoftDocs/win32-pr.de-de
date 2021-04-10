---
title: SBM_GETRANGE Meldung (Winuser. h)
description: Die SBM \_ -GetRange-Nachricht wird gesendet, um die minimalen und maximalen Positionswerte für das ScrollBar-Steuerelement abzurufen.
ms.assetid: 661a9491-3bf6-4685-aea0-c5e4126313af
keywords:
- Windows-Steuerelemente für SBM_GETRANGE Meldung
topic_type:
- apiref
api_name:
- SBM_GETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8ca47e0474152a9771d2787c4a039fb2c868b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956880"
---
# <a name="sbm_getrange-message"></a><span data-ttu-id="d7d0c-104">SBM- \_ GetRange-Nachricht</span><span class="sxs-lookup"><span data-stu-id="d7d0c-104">SBM\_GETRANGE message</span></span>

<span data-ttu-id="d7d0c-105">Die **SBM- \_ GetRange** -Nachricht wird gesendet, um die minimalen und maximalen Positionswerte für das ScrollBar-Steuerelement abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-105">The **SBM\_GETRANGE** message is sent to retrieve the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="d7d0c-106">Anwendungen sollten diese Nachricht nicht direkt senden.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-106">Applications should not send this message directly.</span></span> <span data-ttu-id="d7d0c-107">Stattdessen sollten Sie die [**getscrollrange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-107">Instead, they should use the [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) function.</span></span> <span data-ttu-id="d7d0c-108">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="d7d0c-109">Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die **getscrollrange** -Funktion ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7d0c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7d0c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7d0c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7d0c-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7d0c-112">Ein Zeiger auf eine Variable, die die minimale Bild Lauf Position empfängt.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-112">Pointer to a variable that receives the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="d7d0c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7d0c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7d0c-114">Ein Zeiger auf eine Variable, die die maximale Scrollposition empfängt.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-114">Pointer to a variable that receives the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7d0c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7d0c-115">Return value</span></span>

<span data-ttu-id="d7d0c-116">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d7d0c-116">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7d0c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7d0c-117">Requirements</span></span>



| <span data-ttu-id="d7d0c-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7d0c-118">Requirement</span></span> | <span data-ttu-id="d7d0c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d7d0c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d0c-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7d0c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d0c-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7d0c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d7d0c-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7d0c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d0c-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7d0c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d7d0c-124">Header</span><span class="sxs-lookup"><span data-stu-id="d7d0c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7d0c-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="d7d0c-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7d0c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7d0c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7d0c-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d7d0c-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d7d0c-128">**SBM- \_ GetPos**</span><span class="sxs-lookup"><span data-stu-id="d7d0c-128">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="d7d0c-129">**SBM- \_ SetPos**</span><span class="sxs-lookup"><span data-stu-id="d7d0c-129">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="d7d0c-130">**SBM-über \_ Tragung**</span><span class="sxs-lookup"><span data-stu-id="d7d0c-130">**SBM\_SETRANGE**</span></span>](sbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="d7d0c-131">**SBM- \_ abzeichnende**</span><span class="sxs-lookup"><span data-stu-id="d7d0c-131">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

