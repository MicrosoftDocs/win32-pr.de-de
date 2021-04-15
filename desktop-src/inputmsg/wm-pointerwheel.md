---
title: WM_POINTERWHEEL Meldung
description: Wird im Fenster mit dem Vordergrund Tastaturfokus gesendet, wenn ein Mausrad gedreht wird.
ms.assetid: 6eec37da-2200-4be1-bf0b-44704caa1320
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_POINTERWHEEL Nachricht
topic_type:
- apiref
api_name:
- WM_POINTERWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ad1177b2e92e47ca40c745e6cd5f1ea2cf259215
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476137"
---
# <a name="wm_pointerwheel-message"></a><span data-ttu-id="13115-104">WM_POINTERWHEEL Meldung</span><span class="sxs-lookup"><span data-stu-id="13115-104">WM_POINTERWHEEL message</span></span>

<span data-ttu-id="13115-105">Wird im Fenster mit dem Vordergrund Tastaturfokus gesendet, wenn ein Mausrad gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="13115-105">Posted to the window with foreground keyboard focus when a scroll wheel is rotated.</span></span>

<span data-ttu-id="13115-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="13115-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="13115-107">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="13115-107">\[!Important\]</span></span>  
> <span data-ttu-id="13115-108">Desktop-Apps sollten dpi-fähig sein.</span><span class="sxs-lookup"><span data-stu-id="13115-108">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="13115-109">Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen.</span><span class="sxs-lookup"><span data-stu-id="13115-109">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="13115-110">Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="13115-110">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="13115-111">Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="13115-111">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERWHEEL            0x024E
```



## <a name="parameters"></a><span data-ttu-id="13115-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="13115-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13115-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13115-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13115-114">Enthält den Zeiger Bezeichner und das raddelta.</span><span class="sxs-lookup"><span data-stu-id="13115-114">Contains the pointer identifier and wheel delta.</span></span> <span data-ttu-id="13115-115">Verwenden Sie die folgenden Makros, um diese Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="13115-115">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="13115-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): Zeiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="13115-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier.</span></span>

<span data-ttu-id="13115-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): ein raddelta als Wert mit Vorzeichen als Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="13115-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): wheel delta as a signed short value.</span></span>

</dd> <dt>

<span data-ttu-id="13115-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13115-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13115-119">Enthält die Punktposition des Zeigers.</span><span class="sxs-lookup"><span data-stu-id="13115-119">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="13115-120">Da der Zeiger über einen nicht trivialen Bereich eine Verbindung mit dem Gerät herstellen kann, kann es sein, dass diese Punktposition eine Vereinfachung eines komplexeren Zeiger Bereichs ist.</span><span class="sxs-lookup"><span data-stu-id="13115-120">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="13115-121">Wenn möglich, sollte eine Anwendung anstelle der Punktposition die gesamten Zeiger Bereichs Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="13115-121">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="13115-122">Verwenden Sie die folgenden Makros zum Abrufen der physischen Bildschirm Koordinaten des Punkts.</span><span class="sxs-lookup"><span data-stu-id="13115-122">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="13115-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(LPARAM): die X-Koordinate (horizontal Punkt).</span><span class="sxs-lookup"><span data-stu-id="13115-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="13115-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(LPARAM): die Y-Koordinate (vertikal Punkt).</span><span class="sxs-lookup"><span data-stu-id="13115-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13115-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13115-125">Return value</span></span>

<span data-ttu-id="13115-126">Wenn die Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="13115-126">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="13115-127">Wenn die Anwendung diese Nachricht nicht verarbeitet, sollte Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="13115-127">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="13115-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13115-128">Remarks</span></span>

<span data-ttu-id="13115-129">Verwenden Sie zum Abrufen der Mausrad-schiebeeinheiten den **Input Data** -Befehl der [**POINTER_INFO**](/previous-versions/windows/desktop/api) Struktur, die durch den Aufruf der [**getpointerinfo**](/previous-versions/windows/desktop/api) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="13115-129">To retrieve the wheel scroll units, use the **inputData** filed of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure returned by calling [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span> <span data-ttu-id="13115-130">Dieses Feld enthält einen Wert mit Vorzeichen und wird in einem Vielfachen von **WHEEL_DELTA** ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="13115-130">This field contains a signed value and is expressed in a multiple of **WHEEL_DELTA**.</span></span> <span data-ttu-id="13115-131">Ein positiver Wert gibt einen Drehungs Forward an, und ein negativer Wert gibt eine Drehung rückwärts an.</span><span class="sxs-lookup"><span data-stu-id="13115-131">A positive value indicates a rotation forward and a negative value indicates a rotation backward.</span></span>

<span data-ttu-id="13115-132">Beachten Sie, dass die Radeingaben auch dann übermittelt werden können, wenn sich der Mauszeiger außerhalb des Fensters der Anwendung befindet.</span><span class="sxs-lookup"><span data-stu-id="13115-132">Note that the wheel inputs may be delivered even if the mouse cursor is located outside of application s window.</span></span> <span data-ttu-id="13115-133">Die radnachrichten werden auf eine Weise übermittelt, die den Tastatureingaben sehr ähnlich ist.</span><span class="sxs-lookup"><span data-stu-id="13115-133">The wheel messages are delivered in a way very similar to the keyboard inputs.</span></span> <span data-ttu-id="13115-134">Das Fokus Fenster der foregournd-Nachrichten Warteschlange empfängt die radnachrichten.</span><span class="sxs-lookup"><span data-stu-id="13115-134">The focus window of the foregournd message queue receives the wheel messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="13115-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13115-135">Requirements</span></span>



| <span data-ttu-id="13115-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13115-136">Requirement</span></span> | <span data-ttu-id="13115-137">Wert</span><span class="sxs-lookup"><span data-stu-id="13115-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13115-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13115-138">Minimum supported client</span></span><br/> | <span data-ttu-id="13115-139">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13115-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="13115-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13115-140">Minimum supported server</span></span><br/> | <span data-ttu-id="13115-141">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13115-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13115-142">Header</span><span class="sxs-lookup"><span data-stu-id="13115-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="13115-143"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="13115-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13115-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13115-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13115-145">Meldungen</span><span class="sxs-lookup"><span data-stu-id="13115-145">Messages</span></span>](messages.md)
</dt> </dl>

 

