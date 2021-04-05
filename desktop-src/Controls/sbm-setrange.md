---
title: SBM_SETRANGE Meldung (Winuser. h)
description: Die SBM \_ -SetRange-Nachricht wird gesendet, um die minimalen und maximalen Positionswerte für das ScrollBar-Steuerelement festzulegen.
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- Windows-Steuerelemente für SBM_SETRANGE Meldung
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859204"
---
# <a name="sbm_setrange-message"></a><span data-ttu-id="bbf89-104">SBM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="bbf89-104">SBM\_SETRANGE message</span></span>

<span data-ttu-id="bbf89-105">Die **SBM- \_ SetRange** -Nachricht wird gesendet, um die minimalen und maximalen Positionswerte für das ScrollBar-Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bbf89-105">The **SBM\_SETRANGE** message is sent to set the minimum and maximum position values for the scroll bar control.</span></span>

<span data-ttu-id="bbf89-106">Anwendungen sollten diese Nachricht nicht direkt senden.</span><span class="sxs-lookup"><span data-stu-id="bbf89-106">Applications should not send this message directly.</span></span> <span data-ttu-id="bbf89-107">Stattdessen sollten Sie die [**setscrollrange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbf89-107">Instead, they should use the [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) function.</span></span> <span data-ttu-id="bbf89-108">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bbf89-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="bbf89-109">Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Meldungen reagieren, damit die Funktion **setscrollrange** ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bbf89-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollRange** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="bbf89-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbf89-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbf89-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bbf89-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf89-112">Gibt die minimale Bild Lauf Position an.</span><span class="sxs-lookup"><span data-stu-id="bbf89-112">Specifies the minimum scrolling position.</span></span>

</dd> <dt>

<span data-ttu-id="bbf89-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbf89-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbf89-114">Gibt die maximale Scrollposition an.</span><span class="sxs-lookup"><span data-stu-id="bbf89-114">Specifies the maximum scrolling position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbf89-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbf89-115">Return value</span></span>

<span data-ttu-id="bbf89-116">**ComCtl32.dll Version 5,0**: Wenn sich die Position des Bild Lauf Felds geändert hat, ist der Rückgabewert die vorherige Position des Bild Lauf Felds. Andernfalls ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="bbf89-116">**ComCtl32.dll version 5.0**: If the position of the scroll box changed, the return value is the previous position of the scroll box; otherwise, it is zero.</span></span>

<span data-ttu-id="bbf89-117">**ComCtl32.dll Version 6,0**: die aktuelle Position des Bild Lauf Felds, unabhängig davon, ob es geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="bbf89-117">**ComCtl32.dll version 6.0**: The current position of the scroll box, regardless of whether it has changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbf89-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbf89-118">Remarks</span></span>

<span data-ttu-id="bbf89-119">Die standardmäßigen und maximalen Positionswerte sind 0 (null).</span><span class="sxs-lookup"><span data-stu-id="bbf89-119">The default minimum and maximum position values are zero.</span></span> <span data-ttu-id="bbf89-120">Der Unterschied zwischen den Werten, die von den *wParam* -und *LPARAM* -Parametern angegeben werden, darf nicht größer sein als MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="bbf89-120">The difference between the values specified by the *wParam* and *lParam* parameters must not be greater than MAXLONG.</span></span>

<span data-ttu-id="bbf89-121">Wenn die minimalen und maximalen Positionswerte gleich sind, wird das Bild Lauf leisten-Steuerelement ausgeblendet und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bbf89-121">If the minimum and maximum position values are equal, the scroll bar control is hidden and, in effect, disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf89-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbf89-122">Requirements</span></span>



| <span data-ttu-id="bbf89-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbf89-123">Requirement</span></span> | <span data-ttu-id="bbf89-124">Wert</span><span class="sxs-lookup"><span data-stu-id="bbf89-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbf89-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bbf89-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf89-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbf89-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bbf89-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bbf89-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf89-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bbf89-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bbf89-129">Header</span><span class="sxs-lookup"><span data-stu-id="bbf89-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbf89-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bbf89-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbf89-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbf89-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="bbf89-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="bbf89-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bbf89-133">**SBM- \_ GetPos**</span><span class="sxs-lookup"><span data-stu-id="bbf89-133">**SBM\_GETPOS**</span></span>](sbm-getpos.md)
</dt> <dt>

[<span data-ttu-id="bbf89-134">**SBM- \_ GetRange**</span><span class="sxs-lookup"><span data-stu-id="bbf89-134">**SBM\_GETRANGE**</span></span>](sbm-getrange.md)
</dt> <dt>

[<span data-ttu-id="bbf89-135">**SBM- \_ SetPos**</span><span class="sxs-lookup"><span data-stu-id="bbf89-135">**SBM\_SETPOS**</span></span>](sbm-setpos.md)
</dt> <dt>

[<span data-ttu-id="bbf89-136">**SBM- \_ abzeichnende**</span><span class="sxs-lookup"><span data-stu-id="bbf89-136">**SBM\_SETRANGEREDRAW**</span></span>](sbm-setrangeredraw.md)
</dt> </dl>

 

