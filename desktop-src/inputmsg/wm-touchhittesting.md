---
title: WM_TOUCHHITTESTING Meldung
description: Wird an ein Fenster in einem Touchscreen gesendet, um das wahrscheinlichste Berührungs Ziel zu ermitteln.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- Eingabe Meldungen und Benachrichtigungen der WM_TOUCHHITTESTING Nachricht
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104558"
---
# <a name="wm_touchhittesting-message"></a><span data-ttu-id="34537-104">WM_TOUCHHITTESTING Meldung</span><span class="sxs-lookup"><span data-stu-id="34537-104">WM_TOUCHHITTESTING message</span></span>

<span data-ttu-id="34537-105">Wird an ein Fenster in einem Touchscreen gesendet, um das wahrscheinlichste Berührungs Ziel zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="34537-105">Sent to a window on a touch down in order to determine the most probable touch target.</span></span>

> <span data-ttu-id="34537-106">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="34537-106">\[!Important\]</span></span>  
> <span data-ttu-id="34537-107">Desktop-Apps sollten dpi-fähig sein.</span><span class="sxs-lookup"><span data-stu-id="34537-107">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="34537-108">Wenn Ihre APP nicht dpi-fähig ist, können Bildschirm Koordinaten, die in Zeiger Nachrichten und zugehörigen Strukturen enthalten sind, aufgrund der dpi-Virtualisierung ungenau erscheinen.</span><span class="sxs-lookup"><span data-stu-id="34537-108">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="34537-109">Die dpi-Virtualisierung bietet Unterstützung für die automatische Skalierung für Anwendungen, die nicht mit dpi-Werten kompatibel sind und standardmäßig aktiv sind (Benutzer können Sie deaktivieren).</span><span class="sxs-lookup"><span data-stu-id="34537-109">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="34537-110">Weitere Informationen finden Sie unter [Schreiben von High-dpi-Win32-Anwendungen](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="34537-110">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a><span data-ttu-id="34537-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="34537-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34537-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34537-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34537-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34537-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="34537-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34537-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34537-115">Ein Zeiger auf die [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) Struktur, die die Daten des Berührungs Kontakt Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="34537-115">Pointer to the [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) structure that holds the touch contact area data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34537-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="34537-116">Return value</span></span>

<span data-ttu-id="34537-117">Wenn sich ein oder mehrere Elemente im Touch-Kontaktbereich befinden, sollte eine Anwendung das Ergebnis von [**packtouchhittestingproximityevaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="34537-117">If one or more elements are within the touch contact area, an application should return the result of [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span></span>

<span data-ttu-id="34537-118">Wenn sich keine Elemente im Touch-Kontaktbereich befinden, sollte eine Anwendung den Wert von **Score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) auf [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) festlegen und [**packtouchhittestingproximityevaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) aufrufen, um den LRESULT-Rückgabewert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="34537-118">If no elements are within the touch contact area, an application should set the value of **score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) to [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) and call [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) to get the LRESULT return value.</span></span>

<span data-ttu-id="34537-119">Wenn die Anwendung diese Nachricht nicht verarbeitet, muss Sie [**defwindowproc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="34537-119">If the application does not process this message, it must call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="34537-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="34537-120">Remarks</span></span>

<span data-ttu-id="34537-121">Diese Meldung wird an Windows gesendet, die über die [**registertouchhittestingwindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) -Funktion registriert werden.</span><span class="sxs-lookup"><span data-stu-id="34537-121">This message is sent to windows that register through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="34537-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="34537-122">Requirements</span></span>



| <span data-ttu-id="34537-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="34537-123">Requirement</span></span> | <span data-ttu-id="34537-124">Wert</span><span class="sxs-lookup"><span data-stu-id="34537-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34537-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="34537-125">Minimum supported client</span></span><br/> | <span data-ttu-id="34537-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34537-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="34537-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="34537-127">Minimum supported server</span></span><br/> | <span data-ttu-id="34537-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="34537-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="34537-129">Header</span><span class="sxs-lookup"><span data-stu-id="34537-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="34537-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="34537-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34537-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34537-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34537-132">Meldungen</span><span class="sxs-lookup"><span data-stu-id="34537-132">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="34537-133">**Treffer Treffer Test-Ergebnisse**</span><span class="sxs-lookup"><span data-stu-id="34537-133">**Touch Hit Testing Scores**</span></span>](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

