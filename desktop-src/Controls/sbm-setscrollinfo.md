---
title: SBM_SETSCROLLINFO Meldung (Winuser. h)
description: Die SBM- \_ setScrollInfo-Nachricht wird gesendet, um die Parameter einer Schiebe Leiste festzulegen.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- Windows-Steuerelemente für SBM_SETSCROLLINFO Meldung
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345494"
---
# <a name="sbm_setscrollinfo-message"></a><span data-ttu-id="c12a6-104">SBM- \_ setScrollInfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="c12a6-104">SBM\_SETSCROLLINFO message</span></span>

<span data-ttu-id="c12a6-105">Die **SBM- \_ setScrollInfo** -Nachricht wird gesendet, um die Parameter einer Schiebe Leiste festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c12a6-105">The **SBM\_SETSCROLLINFO** message is sent to set the parameters of a scroll bar.</span></span>

<span data-ttu-id="c12a6-106">Anwendungen sollten diese Nachricht nicht direkt senden.</span><span class="sxs-lookup"><span data-stu-id="c12a6-106">Applications should not send this message directly.</span></span> <span data-ttu-id="c12a6-107">Stattdessen sollten Sie die [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="c12a6-107">Instead, they should use the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) function.</span></span> <span data-ttu-id="c12a6-108">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c12a6-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="c12a6-109">Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Nachrichten reagieren, damit die Funktion **setScrollInfo** ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c12a6-109">Applications which implement a custom scroll bar control must respond to these messages for the **SetScrollInfo** function to function properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="c12a6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c12a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c12a6-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c12a6-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c12a6-112">Gibt an, ob die Schiebe Leiste neu gezeichnet wird, um die neue Position des Bild Lauf Felds widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="c12a6-112">Specifies whether the scroll bar is redrawn to reflect the new scroll box position.</span></span> <span data-ttu-id="c12a6-113">Wenn dieser Parameter **true** ist, wird die Scrollleiste neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c12a6-113">If this parameter is **TRUE**, the scroll bar is redrawn.</span></span> <span data-ttu-id="c12a6-114">Wenn der Wert **false** ist, wird die Scrollleiste nicht neu gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c12a6-114">If it is **FALSE**, the scroll bar is not redrawn.</span></span>

</dd> <dt>

<span data-ttu-id="c12a6-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c12a6-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c12a6-116">Zeiger auf eine [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c12a6-116">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="c12a6-117">Legen Sie vor dem Aufrufen von [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)den **CBSIZE** -Member der-Struktur auf **sizeof**(**ScrollInfo**) fest, legen Sie den **fmask** -Member fest, um die festzulegenden Parameter anzugeben, und geben Sie die neuen Parameterwerte in den entsprechenden Membern an.</span><span class="sxs-lookup"><span data-stu-id="c12a6-117">Before calling [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), set the **fMask** member to indicate the parameters to set, and specify the new parameter values in the appropriate members.</span></span>

<span data-ttu-id="c12a6-118">Der **fmask** -Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c12a6-118">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="c12a6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c12a6-119">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="c12a6-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c12a6-120">Meaning</span></span>                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <span data-ttu-id="c12a6-121"><dt>**SIF \_ DisableNoScroll**</dt></span><span class="sxs-lookup"><span data-stu-id="c12a6-121"><dt>**SIF\_DISABLENOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="c12a6-122">Deaktiviert die Schiebe Leiste, anstatt Sie zu entfernen, wenn die neuen Parameter der Scrollleiste die Bild Lauf Leiste unnötig machen.</span><span class="sxs-lookup"><span data-stu-id="c12a6-122">Disables the scroll bar instead of removing it, if the scroll bar's new parameters make the scroll bar unnecessary.</span></span><br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="c12a6-123"><dt>**SIF- \_ Seite**</dt></span><span class="sxs-lookup"><span data-stu-id="c12a6-123"><dt>**SIF\_PAGE**</dt></span></span> </dl>                                  | <span data-ttu-id="c12a6-124">Legt die scrollseite auf den im **nPage** -Member angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c12a6-124">Sets the scroll page to the value specified in the **nPage** member.</span></span><br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="c12a6-125"><dt>**SIF \_ Torys**</dt></span><span class="sxs-lookup"><span data-stu-id="c12a6-125"><dt>**SIF\_POS**</dt></span></span> </dl>                                     | <span data-ttu-id="c12a6-126">Legt die Scrollposition auf den im **NPOs** -Member angegebenen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c12a6-126">Sets the scroll position to the value specified in the **nPos** member.</span></span> <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="c12a6-127"><dt>**SIF- \_ Bereich**</dt></span><span class="sxs-lookup"><span data-stu-id="c12a6-127"><dt>**SIF\_RANGE**</dt></span></span> </dl>                               | <span data-ttu-id="c12a6-128">Legt den scrollbereich auf den Wert fest, der in den **nmin** -und **nmax** -Membern angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="c12a6-128">Sets the scroll range to the value specified in the **nMin** and **nMax** members.</span></span> <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c12a6-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c12a6-129">Return value</span></span>

<span data-ttu-id="c12a6-130">Der Rückgabewert ist die aktuelle Position des Bild Lauf Felds.</span><span class="sxs-lookup"><span data-stu-id="c12a6-130">The return value is the current position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="c12a6-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c12a6-131">Remarks</span></span>

<span data-ttu-id="c12a6-132">Die Nachrichten, die die Position der Scrollleiste, [**WM \_ HScroll**](wm-hscroll.md) und [**WM \_ VScroll**](wm-vscroll.md)angeben, stellen nur 16 Bits an Positionsdaten bereit.</span><span class="sxs-lookup"><span data-stu-id="c12a6-132">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="c12a6-133">Die [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur, die von [**SBM \_ getscrollinfo**](sbm-getscrollinfo.md), **SBM \_ setScrollInfo**, [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)und [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) verwendet wird, stellt jedoch 32 Bits der Positions leisten Positionsdaten bereit.</span><span class="sxs-lookup"><span data-stu-id="c12a6-133">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by [**SBM\_GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM\_SETSCROLLINFO**, [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="c12a6-134">Sie können diese Nachrichten und Funktionen bei der Verarbeitung der " **WM \_ HScroll** "-oder " **WM \_ VScroll** "-Meldungen zum Abrufen von 32-Bit-Scrollleisten-Positionsdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="c12a6-134">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c12a6-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c12a6-135">Requirements</span></span>



| <span data-ttu-id="c12a6-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c12a6-136">Requirement</span></span> | <span data-ttu-id="c12a6-137">Wert</span><span class="sxs-lookup"><span data-stu-id="c12a6-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c12a6-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c12a6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c12a6-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c12a6-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c12a6-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c12a6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c12a6-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c12a6-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c12a6-142">Header</span><span class="sxs-lookup"><span data-stu-id="c12a6-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c12a6-143"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c12a6-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c12a6-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c12a6-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="c12a6-145">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c12a6-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c12a6-146">**Getscrollinfo**</span><span class="sxs-lookup"><span data-stu-id="c12a6-146">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="c12a6-147">**SBM \_ getscrollinfo**</span><span class="sxs-lookup"><span data-stu-id="c12a6-147">**SBM\_GETSCROLLINFO**</span></span>](sbm-getscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="c12a6-148">**ScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="c12a6-148">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="c12a6-149">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="c12a6-149">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

