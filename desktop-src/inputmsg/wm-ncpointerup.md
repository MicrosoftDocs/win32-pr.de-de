---
title: WM_NCPOINTERUP Meldung
description: Wird gepostet, wenn ein Zeiger, der den Kontakt über den nicht-Client Bereich eines Fensters hergestellt hat, den Kontakt unterbricht.
ms.assetid: 4bdc11da-227c-4be1-bf0b-99704caa1322
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_NCPOINTERUP Nachricht
topic_type:
- apiref
api_name:
- WM_NCPOINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a875814b51558c20de47eeee525f6dd35f716fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742576"
---
# <a name="wm_ncpointerup-message"></a><span data-ttu-id="29ec3-104">WM_NCPOINTERUP Meldung</span><span class="sxs-lookup"><span data-stu-id="29ec3-104">WM_NCPOINTERUP message</span></span>

<span data-ttu-id="29ec3-105">Wird gepostet, wenn ein Zeiger, der den Kontakt über den nicht-Client Bereich eines Fensters hergestellt hat, den Kontakt unterbricht.</span><span class="sxs-lookup"><span data-stu-id="29ec3-105">Posted when a pointer that made contact over the non-client area of a window breaks contact.</span></span> <span data-ttu-id="29ec3-106">Die Nachricht bezieht sich auf das Fenster, über das der Zeiger Kontakt herstellt, und der Zeiger ist an diesem Punkt implizit im Fenster erfasst, sodass das Fenster weiterhin Eingaben für den Zeiger empfängt, bis der Kontakt unterbrochen wird, einschließlich der **WM_NCPOINTERUP** Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="29ec3-106">The message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact, including the **WM_NCPOINTERUP** notification.</span></span>

<span data-ttu-id="29ec3-107">Wenn ein Fenster diesen Zeiger aufgezeichnet hat, wird diese Meldung nicht gepostet.</span><span class="sxs-lookup"><span data-stu-id="29ec3-107">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="29ec3-108">Stattdessen wird ein [**WM_POINTERUP**](wm-pointerup.md) an das Fenster gesendet, das diesen Zeiger aufgezeichnet hat.</span><span class="sxs-lookup"><span data-stu-id="29ec3-108">Instead, a [**WM_POINTERUP**](wm-pointerup.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="29ec3-109">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="29ec3-109">\[!Important\]</span></span>  
> <span data-ttu-id="29ec3-110">Desktop-Apps sollten dpi-fähig sein.</span><span class="sxs-lookup"><span data-stu-id="29ec3-110">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="29ec3-111">Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen.</span><span class="sxs-lookup"><span data-stu-id="29ec3-111">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="29ec3-112">Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="29ec3-112">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="29ec3-113">Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="29ec3-113">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUP               0x0243
```



## <a name="parameters"></a><span data-ttu-id="29ec3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="29ec3-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29ec3-115">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29ec3-115">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29ec3-116">Enthält den Zeiger Bezeichner und zusätzliche Informationen.</span><span class="sxs-lookup"><span data-stu-id="29ec3-116">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="29ec3-117">Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="29ec3-117">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="29ec3-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Zeiger Bezeichner</span><span class="sxs-lookup"><span data-stu-id="29ec3-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="29ec3-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): Treffer Test Wert, der von der Verarbeitung der [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="29ec3-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="29ec3-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29ec3-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29ec3-121">Enthält die Punktposition des Zeigers.</span><span class="sxs-lookup"><span data-stu-id="29ec3-121">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="29ec3-122">Da der Zeiger über einen nicht trivialen Bereich eine Verbindung mit dem Gerät herstellen kann, kann es sein, dass diese Punktposition eine Vereinfachung eines komplexeren Zeiger Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="29ec3-122">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="29ec3-123">Wenn möglich, sollte eine Anwendung anstelle der Punktposition die gesamten Zeiger Bereichs Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="29ec3-123">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="29ec3-124">Verwenden Sie die folgenden Makros zum Abrufen der physischen Bildschirm Koordinaten des Punkts.</span><span class="sxs-lookup"><span data-stu-id="29ec3-124">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="29ec3-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(LPARAM): die X-Koordinate (horizontal Punkt).</span><span class="sxs-lookup"><span data-stu-id="29ec3-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="29ec3-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(LPARAM): die Y-Koordinate (vertikal Punkt).</span><span class="sxs-lookup"><span data-stu-id="29ec3-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29ec3-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29ec3-127">Return value</span></span>

<span data-ttu-id="29ec3-128">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="29ec3-128">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="29ec3-129">Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="29ec3-129">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="29ec3-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29ec3-130">Remarks</span></span>

<span data-ttu-id="29ec3-131">Wenn die Anwendung diese Nachricht nicht verarbeitet, kann [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) eine oder mehrere System Aktionen ausführen, je nachdem, welches Treffer Testergebnis in der Nachricht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="29ec3-131">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="29ec3-132">In der Regel sollten Anwendungen diese Nachricht nicht verarbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="29ec3-132">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="29ec3-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29ec3-133">Requirements</span></span>



| <span data-ttu-id="29ec3-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29ec3-134">Requirement</span></span> | <span data-ttu-id="29ec3-135">Wert</span><span class="sxs-lookup"><span data-stu-id="29ec3-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29ec3-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="29ec3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="29ec3-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29ec3-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="29ec3-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="29ec3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="29ec3-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="29ec3-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="29ec3-140">Header</span><span class="sxs-lookup"><span data-stu-id="29ec3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="29ec3-141"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="29ec3-141"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ec3-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29ec3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ec3-143">Meldungen</span><span class="sxs-lookup"><span data-stu-id="29ec3-143">Messages</span></span>](messages.md)
</dt> </dl>

 

