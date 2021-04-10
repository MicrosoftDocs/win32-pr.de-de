---
title: WM_NCMOUSEHOVER Meldung (Winuser. h)
description: Wird in einem Fenster gepostet, wenn der Cursor für den Zeitraum, der in einem vorherigen Aufruf von TrackMouseEvent angegeben ist, auf den nicht-Client Bereich des Fensters zeigt.
ms.assetid: ca1afdc2-7884-445e-b9b7-4d7dd5dcea38
keywords:
- Tastatur-und Maus Eingaben für WM_NCMOUSEHOVER Nachricht
topic_type:
- apiref
api_name:
- WM_NCMOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde2e70b04602de5936e945789007a6c5fea8542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040922"
---
# <a name="wm_ncmousehover-message"></a><span data-ttu-id="c9ca8-104">WM \_ ncmouseelhover-Meldung</span><span class="sxs-lookup"><span data-stu-id="c9ca8-104">WM\_NCMOUSEHOVER message</span></span>

<span data-ttu-id="c9ca8-105">Wird in einem Fenster gepostet, wenn der Cursor für den Zeitraum, der in einem vorherigen Aufruf von [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)angegeben ist, auf den nicht-Client Bereich des Fensters zeigt.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-105">Posted to a window when the cursor hovers over the nonclient area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="c9ca8-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSEHOVER                 0x02A0
```



## <a name="parameters"></a><span data-ttu-id="c9ca8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9ca8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ca8-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c9ca8-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9ca8-109">Der Treffer Test Wert, der von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion als Ergebnis der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-109">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="c9ca8-110">Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-110">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="c9ca8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c9ca8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c9ca8-112">Eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-und y-Koordinaten des Cursors enthält.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-112">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="c9ca8-113">Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-113">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9ca8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9ca8-114">Return value</span></span>

<span data-ttu-id="c9ca8-115">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-115">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9ca8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9ca8-116">Remarks</span></span>

<span data-ttu-id="c9ca8-117">Die Hover-Nachverfolgung wird beendet, wenn diese Meldung generiert wird.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-117">Hover tracking stops when this message is generated.</span></span> <span data-ttu-id="c9ca8-118">Die Anwendung muss [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) erneut aufrufen, wenn Sie eine weitere Nachverfolgung des Mauszeiger Verhaltens erfordert.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-118">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="c9ca8-119">Sie können auch die Makros [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der X-und y-Koordinaten aus *LPARAM* zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-119">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="c9ca8-120">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-120">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="c9ca8-121">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="c9ca8-121">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9ca8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c9ca8-122">Requirements</span></span>



| <span data-ttu-id="c9ca8-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c9ca8-123">Requirement</span></span> | <span data-ttu-id="c9ca8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c9ca8-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ca8-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c9ca8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c9ca8-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9ca8-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c9ca8-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c9ca8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c9ca8-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c9ca8-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c9ca8-129">Header</span><span class="sxs-lookup"><span data-stu-id="c9ca8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9ca8-130"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9ca8-130"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9ca8-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9ca8-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="c9ca8-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c9ca8-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c9ca8-134">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-134">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="c9ca8-135">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-135">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="c9ca8-136">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-136">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="c9ca8-137">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-137">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="c9ca8-138">**WM- \_ nchittest**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-138">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="c9ca8-139">**WM- \_ moupagehover**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-139">**WM\_MOUSEHOVER**</span></span>](wm-mousehover.md)
</dt> <dt>

<span data-ttu-id="c9ca8-140">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c9ca8-141">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="c9ca8-141">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="c9ca8-142">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c9ca8-143">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="c9ca8-143">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="c9ca8-144">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c9ca8-144">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

