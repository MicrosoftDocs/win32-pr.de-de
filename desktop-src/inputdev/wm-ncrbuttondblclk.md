---
title: WM_NCRBUTTONDBLCLK Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer mit der rechten Maustaste doppelklickt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.
ms.assetid: 20d62b05-07de-49da-b160-29fa1f5067fa
keywords:
- Tastatur-und Maus Eingaben für WM_NCRBUTTONDBLCLK Nachricht
topic_type:
- apiref
api_name:
- WM_NCRBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fee33d9b31f99a00181427c9a715df792d95fe55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518329"
---
# <a name="wm_ncrbuttondblclk-message"></a><span data-ttu-id="c08f2-106">WM- \_ ncrbuttondblclk-Meldung</span><span class="sxs-lookup"><span data-stu-id="c08f2-106">WM\_NCRBUTTONDBLCLK message</span></span>

<span data-ttu-id="c08f2-107">Wird gesendet, wenn der Benutzer mit der rechten Maustaste doppelklickt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="c08f2-107">Posted when the user double-clicks the right mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="c08f2-108">Diese Meldung wird an das Fenster gesendet, das den Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="c08f2-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="c08f2-109">Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.</span><span class="sxs-lookup"><span data-stu-id="c08f2-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="c08f2-110">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c08f2-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCRBUTTONDBLCLK              0x00A6
```



## <a name="parameters"></a><span data-ttu-id="c08f2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c08f2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c08f2-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c08f2-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c08f2-113">Der Treffer Test Wert, der von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion als Ergebnis der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c08f2-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="c08f2-114">Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.</span><span class="sxs-lookup"><span data-stu-id="c08f2-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="c08f2-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c08f2-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c08f2-116">Eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-und y-Koordinaten des Cursors enthält.</span><span class="sxs-lookup"><span data-stu-id="c08f2-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="c08f2-117">Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="c08f2-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c08f2-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c08f2-118">Return value</span></span>

<span data-ttu-id="c08f2-119">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c08f2-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c08f2-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c08f2-120">Remarks</span></span>

<span data-ttu-id="c08f2-121">Ein Fenster muss nicht den **CS- \_ dblclks** -Stil aufweisen, um **WM \_ ncrbuttondblclk** -Meldungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c08f2-121">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCRBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="c08f2-122">Das System generiert eine **WM- \_ ncrbuttondblclk** -Meldung, wenn der Benutzer die Maustaste drückt, loslässt und erneut mit der rechten Maustaste im Doppelklick-Zeit Limit des Systems drückt.</span><span class="sxs-lookup"><span data-stu-id="c08f2-122">The system generates a **WM\_NCRBUTTONDBLCLK** message when the user presses, releases, and again presses the right mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="c08f2-123">Durch Doppelklicken auf die Rechte Maustaste werden tatsächlich vier Meldungen generiert [**: \_ WM ncrbuttondown**](wm-ncrbuttondown.md), [**WM \_ ncrbuttonup**](wm-ncrbuttonup.md), **WM \_ ncrbuttondblclk** und **WM \_ ncrbuttonup** .</span><span class="sxs-lookup"><span data-stu-id="c08f2-123">Double-clicking the right mouse button actually generates four messages: [**WM\_NCRBUTTONDOWN**](wm-ncrbuttondown.md), [**WM\_NCRBUTTONUP**](wm-ncrbuttonup.md), **WM\_NCRBUTTONDBLCLK**, and **WM\_NCRBUTTONUP** again.</span></span>

<span data-ttu-id="c08f2-124">Sie können auch die Makros [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der X-und y-Koordinaten aus *LPARAM* zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="c08f2-124">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="c08f2-125">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c08f2-125">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="c08f2-126">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="c08f2-126">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="c08f2-127">Wenn dies der Fall ist, sendet das System die WM- [**\_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="c08f2-127">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="c08f2-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c08f2-128">Requirements</span></span>



| <span data-ttu-id="c08f2-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c08f2-129">Requirement</span></span> | <span data-ttu-id="c08f2-130">Wert</span><span class="sxs-lookup"><span data-stu-id="c08f2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c08f2-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c08f2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c08f2-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c08f2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c08f2-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c08f2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c08f2-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c08f2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c08f2-135">Header</span><span class="sxs-lookup"><span data-stu-id="c08f2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c08f2-136"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c08f2-136"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c08f2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c08f2-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="c08f2-138">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c08f2-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c08f2-139">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c08f2-139">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c08f2-140">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="c08f2-140">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="c08f2-141">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="c08f2-141">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="c08f2-142">**WM- \_ nchittest**</span><span class="sxs-lookup"><span data-stu-id="c08f2-142">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="c08f2-143">**WM- \_ ncrbuttondown**</span><span class="sxs-lookup"><span data-stu-id="c08f2-143">**WM\_NCRBUTTONDOWN**</span></span>](wm-ncrbuttondown.md)
</dt> <dt>

[<span data-ttu-id="c08f2-144">**WM- \_ ncrbuttonup**</span><span class="sxs-lookup"><span data-stu-id="c08f2-144">**WM\_NCRBUTTONUP**</span></span>](wm-ncrbuttonup.md)
</dt> <dt>

[<span data-ttu-id="c08f2-145">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="c08f2-145">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="c08f2-146">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c08f2-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c08f2-147">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="c08f2-147">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="c08f2-148">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c08f2-148">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c08f2-149">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="c08f2-149">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="c08f2-150">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c08f2-150">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

