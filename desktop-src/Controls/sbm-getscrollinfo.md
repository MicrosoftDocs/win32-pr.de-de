---
title: SBM_GETSCROLLINFO Meldung (Winuser. h)
description: Die SBM \_ getscrollinfo-Nachricht wird gesendet, um die Parameter einer Schiebe Leiste abzurufen.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- Windows-Steuerelemente für SBM_GETSCROLLINFO Meldung
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346766"
---
# <a name="sbm_getscrollinfo-message"></a><span data-ttu-id="15bdf-104">SBM \_ getscrollinfo-Meldung</span><span class="sxs-lookup"><span data-stu-id="15bdf-104">SBM\_GETSCROLLINFO message</span></span>

<span data-ttu-id="15bdf-105">Die **SBM \_ getscrollinfo** -Nachricht wird gesendet, um die Parameter einer Schiebe Leiste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15bdf-105">The **SBM\_GETSCROLLINFO** message is sent to retrieve the parameters of a scroll bar.</span></span>

<span data-ttu-id="15bdf-106">Anwendungen sollten diese Nachricht nicht direkt senden.</span><span class="sxs-lookup"><span data-stu-id="15bdf-106">Applications should not send this message directly.</span></span> <span data-ttu-id="15bdf-107">Stattdessen sollten Sie die [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="15bdf-107">Instead, they should use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function.</span></span> <span data-ttu-id="15bdf-108">Ein Fenster empfängt diese Meldung über seine [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="15bdf-108">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span> <span data-ttu-id="15bdf-109">Anwendungen, die ein benutzerdefiniertes Bild Lauf leisten-Steuerelement implementieren, müssen auf diese Nachrichten reagieren, damit die Funktion **getscrollinfo** ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="15bdf-109">Applications which implement a custom scroll bar control must respond to these messages for the **GetScrollInfo** function to work properly.</span></span>

## <a name="parameters"></a><span data-ttu-id="15bdf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="15bdf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15bdf-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15bdf-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15bdf-112">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="15bdf-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="15bdf-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15bdf-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15bdf-114">Zeiger auf eine [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="15bdf-114">Pointer to a [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="15bdf-115">Legen Sie vor dem Aufrufen von [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)den **CBSIZE** -Member der-Struktur auf **sizeof**(**ScrollInfo**) fest, und legen Sie den fmask-Member fest, um die abzurufenden ScrollBar-Parameter anzugeben. </span><span class="sxs-lookup"><span data-stu-id="15bdf-115">Before calling [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), set the **cbSize** member of the structure to **sizeof**(**SCROLLINFO**), and set the **fMask** member to specify the scroll bar parameters to retrieve.</span></span> <span data-ttu-id="15bdf-116">Vor der Rückgabe kopiert die Meldung die angegebenen Parameter in die entsprechenden Member der Struktur.</span><span class="sxs-lookup"><span data-stu-id="15bdf-116">Before returning, the message copies the specified parameters to the appropriate members of the structure.</span></span>

<span data-ttu-id="15bdf-117">Der **fmask** -Member kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="15bdf-117">The **fMask** member can be one or more of the following values.</span></span>



| <span data-ttu-id="15bdf-118">Wert</span><span class="sxs-lookup"><span data-stu-id="15bdf-118">Value</span></span>                                                                                                                                                      | <span data-ttu-id="15bdf-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="15bdf-119">Meaning</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <span data-ttu-id="15bdf-120"><dt>**Alle SIF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="15bdf-120"><dt>**SIF\_ALL**</dt></span></span> </dl>                | <span data-ttu-id="15bdf-121">Kombination aus SIF \_ -Seite, SIF \_ -POS, SIF \_ -Bereich und SIF- \_ trackpos.</span><span class="sxs-lookup"><span data-stu-id="15bdf-121">Combination of SIF\_PAGE, SIF\_POS, SIF\_RANGE, and SIF\_TRACKPOS.</span></span><br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <span data-ttu-id="15bdf-122"><dt>**SIF- \_ Seite**</dt></span><span class="sxs-lookup"><span data-stu-id="15bdf-122"><dt>**SIF\_PAGE**</dt></span></span> </dl>             | <span data-ttu-id="15bdf-123">Kopiert die scrollseite in den nPage-Member.</span><span class="sxs-lookup"><span data-stu-id="15bdf-123">Copies the scroll page to the nPage member.</span></span><br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <span data-ttu-id="15bdf-124"><dt>**SIF \_ Torys**</dt></span><span class="sxs-lookup"><span data-stu-id="15bdf-124"><dt>**SIF\_POS**</dt></span></span> </dl>                | <span data-ttu-id="15bdf-125">Kopiert die Scrollposition in den NPOs-Member.</span><span class="sxs-lookup"><span data-stu-id="15bdf-125">Copies the scroll position to the nPos member.</span></span> <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <span data-ttu-id="15bdf-126"><dt>**SIF- \_ Bereich**</dt></span><span class="sxs-lookup"><span data-stu-id="15bdf-126"><dt>**SIF\_RANGE**</dt></span></span> </dl>          | <span data-ttu-id="15bdf-127">Kopiert den scrollbereich in die Member nmin und nmax.</span><span class="sxs-lookup"><span data-stu-id="15bdf-127">Copies the scroll range to the nMin and nMax members.</span></span> <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <span data-ttu-id="15bdf-128"><dt>**SIF- \_ trackpos**</dt></span><span class="sxs-lookup"><span data-stu-id="15bdf-128"><dt>**SIF\_TRACKPOS**</dt></span></span> </dl> | <span data-ttu-id="15bdf-129">Kopiert die aktuelle nach Verfolgungs Position des Bild Lauf Felds in den ntrackpos-Member.</span><span class="sxs-lookup"><span data-stu-id="15bdf-129">Copies the current scroll box tracking position to the nTrackPos member.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15bdf-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15bdf-130">Return value</span></span>

<span data-ttu-id="15bdf-131">Wenn die Nachricht Werte abgerufen hat, ist der Rückgabewert " **true**". Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="15bdf-131">If the message retrieved any values, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="15bdf-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15bdf-132">Remarks</span></span>

<span data-ttu-id="15bdf-133">Die Nachrichten, die die Position der Scrollleiste, [**WM \_ HScroll**](wm-hscroll.md) und [**WM \_ VScroll**](wm-vscroll.md)angeben, stellen nur 16 Bits an Positionsdaten bereit.</span><span class="sxs-lookup"><span data-stu-id="15bdf-133">The messages that indicate scroll bar position, [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md), provide only 16 bits of position data.</span></span> <span data-ttu-id="15bdf-134">Die [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur, die von **SBM \_ getscrollinfo**, [**SBM \_ setScrollInfo**](sbm-setscrollinfo.md), [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)und [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) verwendet wird, stellt jedoch 32 Bits der Positions leisten Positionsdaten bereit.</span><span class="sxs-lookup"><span data-stu-id="15bdf-134">However, the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure used by **SBM\_GETSCROLLINFO**, [**SBM\_SETSCROLLINFO**](sbm-setscrollinfo.md), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), and [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) provides 32 bits of scroll bar position data.</span></span> <span data-ttu-id="15bdf-135">Sie können diese Nachrichten und Funktionen bei der Verarbeitung der " **WM \_ HScroll** "-oder " **WM \_ VScroll** "-Meldungen zum Abrufen von 32-Bit-Scrollleisten-Positionsdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="15bdf-135">You can use these messages and functions while processing either the **WM\_HSCROLL** or **WM\_VSCROLL** messages to obtain 32-bit scroll bar position data.</span></span>

<span data-ttu-id="15bdf-136">Um die 32-Bit-Position des Bild Lauf Felds (Ziehpunkt) während eines SB- \_ thumbrequest-Anforderungs Codes in einer [**WM \_ HScroll**](wm-hscroll.md) -oder [**WM \_ VScroll**](wm-vscroll.md) -Nachricht abzurufen, senden Sie **SBM \_ getscrollinfo** mit dem SIF \_ trackpos-Wert im **fmask** -Member der [**ScrollInfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="15bdf-136">To get the 32-bit position of the scroll box (thumb) during a SB\_THUMBTRACK request code in a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message, send **SBM\_GETSCROLLINFO** with the SIF\_TRACKPOS value in the **fMask** member of the [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) structure.</span></span> <span data-ttu-id="15bdf-137">Die Meldung gibt die nach Verfolgungs Position des Bild Lauf Felds im **ntrackpos** -Member der **ScrollInfo** -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="15bdf-137">The message returns the tracking position of the scroll box in the **nTrackPos** member of the **SCROLLINFO** structure.</span></span> <span data-ttu-id="15bdf-138">Dadurch können Sie die Position des Bild Lauf Felds beim Verschieben durch den Benutzer erhalten.</span><span class="sxs-lookup"><span data-stu-id="15bdf-138">This allows you to get the position of the scroll box as the user moves it.</span></span> <span data-ttu-id="15bdf-139">Alternativ können Sie die [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) -Funktion verwenden, um dieselben Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15bdf-139">Alternatively, you can use the [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) function to get the same information.</span></span>

## <a name="requirements"></a><span data-ttu-id="15bdf-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15bdf-140">Requirements</span></span>



| <span data-ttu-id="15bdf-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15bdf-141">Requirement</span></span> | <span data-ttu-id="15bdf-142">Wert</span><span class="sxs-lookup"><span data-stu-id="15bdf-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15bdf-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15bdf-143">Minimum supported client</span></span><br/> | <span data-ttu-id="15bdf-144">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15bdf-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="15bdf-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15bdf-145">Minimum supported server</span></span><br/> | <span data-ttu-id="15bdf-146">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15bdf-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15bdf-147">Header</span><span class="sxs-lookup"><span data-stu-id="15bdf-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="15bdf-148"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="15bdf-148"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15bdf-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15bdf-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="15bdf-150">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="15bdf-150">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="15bdf-151">**Getscrollinfo**</span><span class="sxs-lookup"><span data-stu-id="15bdf-151">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="15bdf-152">**SBM \_ setScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="15bdf-152">**SBM\_SETSCROLLINFO**</span></span>](sbm-setscrollinfo.md)
</dt> <dt>

[<span data-ttu-id="15bdf-153">**ScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="15bdf-153">**SCROLLINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[<span data-ttu-id="15bdf-154">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="15bdf-154">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

