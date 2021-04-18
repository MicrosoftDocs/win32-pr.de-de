---
title: WM_NCPOINTERUPDATE Meldung
description: Wird bereitgestellt, um ein Update für einen Zeiger bereitzustellen, der den Kontakt über den nicht-Client Bereich eines Fensters hergestellt hat, oder wenn ein nicht erfasster Kontakt, der sich im nicht-Client Bereich eines Fensters bewegt, verschoben wird
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704caa1322
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_NCPOINTERUPDATE Nachricht
topic_type:
- apiref
api_name:
- WM_NCPOINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 09ef5fd6f3b7378a963be4278f1fabdf0f6ab351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391789"
---
# <a name="wm_ncpointerupdate-message"></a><span data-ttu-id="36be3-104">WM_NCPOINTERUPDATE Meldung</span><span class="sxs-lookup"><span data-stu-id="36be3-104">WM_NCPOINTERUPDATE message</span></span>

<span data-ttu-id="36be3-105">Wird bereitgestellt, um ein Update für einen Zeiger bereitzustellen, der den Kontakt über den nicht-Client Bereich eines Fensters hergestellt hat, oder wenn ein nicht erfasster Kontakt, der sich im nicht-Client Bereich eines Fensters bewegt, verschoben wird</span><span class="sxs-lookup"><span data-stu-id="36be3-105">Posted to provide an update on a pointer that made contact over the non-client area of a window or when a hovering uncaptured contact moves over the non-client area of a window.</span></span> <span data-ttu-id="36be3-106">Während der Mauszeiger bewegt wird, wird die Nachricht auf das Fenster ausgerichtet, über das sich der Zeiger befindet.</span><span class="sxs-lookup"><span data-stu-id="36be3-106">While the pointer is hovering, the message targets whichever window the pointer happens to be over.</span></span> <span data-ttu-id="36be3-107">Während sich der Mauszeiger auf der-Oberfläche befindet, wird der Zeiger implizit in dem Fenster erfasst, über das der Zeiger den Kontakt hergestellt hat, und dieses Fenster empfängt weiterhin Eingaben für den Zeiger, bis der Kontakt unterbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="36be3-107">While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="36be3-108">Wenn ein Fenster diesen Zeiger aufgezeichnet hat, wird diese Meldung nicht gepostet.</span><span class="sxs-lookup"><span data-stu-id="36be3-108">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="36be3-109">Stattdessen wird ein [**WM_POINTERUPDATE**](wm-pointerupdate.md) an das Fenster gesendet, das diesen Zeiger aufgezeichnet hat.</span><span class="sxs-lookup"><span data-stu-id="36be3-109">Instead, a [**WM_POINTERUPDATE**](wm-pointerupdate.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="36be3-110">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="36be3-110">\[!Important\]</span></span>  
> <span data-ttu-id="36be3-111">Desktop-Apps sollten dpi-fähig sein.</span><span class="sxs-lookup"><span data-stu-id="36be3-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="36be3-112">Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen.</span><span class="sxs-lookup"><span data-stu-id="36be3-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="36be3-113">Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="36be3-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="36be3-114">Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="36be3-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUPDATE                 0x0241
```



## <a name="parameters"></a><span data-ttu-id="36be3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="36be3-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36be3-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36be3-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36be3-117">Enthält den Zeiger Bezeichner und zusätzliche Informationen.</span><span class="sxs-lookup"><span data-stu-id="36be3-117">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="36be3-118">Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="36be3-118">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="36be3-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Zeiger Bezeichner</span><span class="sxs-lookup"><span data-stu-id="36be3-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="36be3-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): Treffer Test Wert, der von der Verarbeitung der [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) Nachricht zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="36be3-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="36be3-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36be3-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36be3-122">Enthält die Punktposition des Zeigers.</span><span class="sxs-lookup"><span data-stu-id="36be3-122">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="36be3-123">Da der Zeiger über einen nicht trivialen Bereich eine Verbindung mit dem Gerät herstellen kann, kann es sein, dass diese Punktposition eine Vereinfachung eines komplexeren Zeiger Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="36be3-123">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="36be3-124">Wenn möglich, sollte eine Anwendung anstelle der Punktposition die gesamten Zeiger Bereichs Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="36be3-124">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="36be3-125">Verwenden Sie die folgenden Makros zum Abrufen der physischen Bildschirm Koordinaten des Punkts.</span><span class="sxs-lookup"><span data-stu-id="36be3-125">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="36be3-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(LPARAM): die X-Koordinate (horizontal Punkt).</span><span class="sxs-lookup"><span data-stu-id="36be3-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="36be3-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(LPARAM): die Y-Koordinate (vertikal Punkt).</span><span class="sxs-lookup"><span data-stu-id="36be3-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36be3-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36be3-128">Return value</span></span>

<span data-ttu-id="36be3-129">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="36be3-129">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="36be3-130">Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="36be3-130">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="36be3-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36be3-131">Remarks</span></span>

<span data-ttu-id="36be3-132">Wenn die Anwendung diese Nachricht nicht verarbeitet, kann [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) eine oder mehrere System Aktionen ausführen, je nachdem, welches Treffer Testergebnis in der Nachricht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="36be3-132">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="36be3-133">In der Regel sollten Anwendungen diese Nachricht nicht verarbeiten müssen.</span><span class="sxs-lookup"><span data-stu-id="36be3-133">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="36be3-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36be3-134">Requirements</span></span>



| <span data-ttu-id="36be3-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36be3-135">Requirement</span></span> | <span data-ttu-id="36be3-136">Wert</span><span class="sxs-lookup"><span data-stu-id="36be3-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36be3-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="36be3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="36be3-138">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36be3-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="36be3-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="36be3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="36be3-140">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="36be3-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="36be3-141">Header</span><span class="sxs-lookup"><span data-stu-id="36be3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="36be3-142"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="36be3-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36be3-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36be3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36be3-144">Meldungen</span><span class="sxs-lookup"><span data-stu-id="36be3-144">Messages</span></span>](messages.md)
</dt> </dl>

 

