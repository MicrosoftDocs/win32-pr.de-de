---
title: WM_NCLBUTTONDBLCLK Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer mit der linken Maustaste doppelklickt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.
ms.assetid: fc655631-64d0-4cc5-b85e-25d274182994
keywords:
- Tastatur-und Maus Eingaben für WM_NCLBUTTONDBLCLK Nachricht
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db66edcb3b1645c6c34c72e35df53afc516dafc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103398"
---
# <a name="wm_nclbuttondblclk-message"></a><span data-ttu-id="d7765-106">WM- \_ nclbuttondblclk-Meldung</span><span class="sxs-lookup"><span data-stu-id="d7765-106">WM\_NCLBUTTONDBLCLK message</span></span>

<span data-ttu-id="d7765-107">Wird gesendet, wenn der Benutzer mit der linken Maustaste doppelklickt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="d7765-107">Posted when the user double-clicks the left mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="d7765-108">Diese Meldung wird an das Fenster gesendet, das den Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="d7765-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="d7765-109">Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.</span><span class="sxs-lookup"><span data-stu-id="d7765-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="d7765-110">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="d7765-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCLBUTTONDBLCLK              0x00A3
```



## <a name="parameters"></a><span data-ttu-id="d7765-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7765-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7765-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7765-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7765-113">Der Treffer Test Wert, der von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion als Ergebnis der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7765-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="d7765-114">Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.</span><span class="sxs-lookup"><span data-stu-id="d7765-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="d7765-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7765-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7765-116">Eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-und y-Koordinaten des Cursors enthält.</span><span class="sxs-lookup"><span data-stu-id="d7765-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="d7765-117">Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="d7765-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7765-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7765-118">Return value</span></span>

<span data-ttu-id="d7765-119">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d7765-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7765-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7765-120">Remarks</span></span>

<span data-ttu-id="d7765-121">Sie können auch die Makros [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der X-und y-Koordinaten aus *LPARAM* zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="d7765-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="d7765-122">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d7765-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="d7765-123">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="d7765-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="d7765-124">Standardmäßig testet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion den angegebenen Punkt, um die Position des Cursors zu ermitteln, und führt die entsprechende Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="d7765-124">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to find out the location of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="d7765-125">Falls zutreffend, sendet **defwindowproc** die [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Nachricht an das-Fenster.</span><span class="sxs-lookup"><span data-stu-id="d7765-125">If appropriate, **DefWindowProc** sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="d7765-126">Ein Fenster muss nicht den **CS- \_ dblclks** -Stil aufweisen, um **WM \_ nclbuttondblclk** -Meldungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d7765-126">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCLBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="d7765-127">Das System generiert eine **WM- \_ nclbuttondblclk** -Meldung, wenn der Benutzer die linke Maustaste drückt und die linke Maustaste im Doppelklick-Zeit Limit des Systems drückt.</span><span class="sxs-lookup"><span data-stu-id="d7765-127">The system generates a **WM\_NCLBUTTONDBLCLK** message when the user presses, releases, and again presses the left mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="d7765-128">Durch Doppelklicken auf die linke Maustaste werden tatsächlich vier Meldungen generiert [**: \_ WM nclbuttondown**](wm-nclbuttondown.md), [**WM \_ nclbuttonup**](wm-nclbuttonup.md), **WM \_ nclbuttondblclk** und **WM \_ nclbuttonup** .</span><span class="sxs-lookup"><span data-stu-id="d7765-128">Double-clicking the left mouse button actually generates four messages: [**WM\_NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM\_NCLBUTTONUP**](wm-nclbuttonup.md), **WM\_NCLBUTTONDBLCLK**, and **WM\_NCLBUTTONUP** again.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7765-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7765-129">Requirements</span></span>



| <span data-ttu-id="d7765-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7765-130">Requirement</span></span> | <span data-ttu-id="d7765-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d7765-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7765-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7765-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d7765-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7765-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d7765-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7765-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d7765-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7765-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d7765-136">Header</span><span class="sxs-lookup"><span data-stu-id="d7765-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7765-137"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7765-137"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7765-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7765-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7765-139">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="d7765-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d7765-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="d7765-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="d7765-141">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="d7765-141">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="d7765-142">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="d7765-142">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="d7765-143">**WM- \_ nchittest**</span><span class="sxs-lookup"><span data-stu-id="d7765-143">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="d7765-144">**WM- \_ nclbuttondown**</span><span class="sxs-lookup"><span data-stu-id="d7765-144">**WM\_NCLBUTTONDOWN**</span></span>](wm-nclbuttondown.md)
</dt> <dt>

[<span data-ttu-id="d7765-145">**WM- \_ nclbuttonup**</span><span class="sxs-lookup"><span data-stu-id="d7765-145">**WM\_NCLBUTTONUP**</span></span>](wm-nclbuttonup.md)
</dt> <dt>

[<span data-ttu-id="d7765-146">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="d7765-146">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="d7765-147">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d7765-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d7765-148">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="d7765-148">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="d7765-149">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="d7765-149">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d7765-150">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="d7765-150">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="d7765-151">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d7765-151">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

