---
title: WM_NCMBUTTONUP Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer die mittlere Maustaste loslässt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.
ms.assetid: 93335e46-c72b-4139-9785-67ce2a6bcb4a
keywords:
- Tastatur-und Maus Eingaben für WM_NCMBUTTONUP Nachricht
topic_type:
- apiref
api_name:
- WM_NCMBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a890c79f6835dc0f44257fc1adf5d00b976a87c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341789"
---
# <a name="wm_ncmbuttonup-message"></a><span data-ttu-id="23b72-106">WM- \_ ncmbuttonup-Meldung</span><span class="sxs-lookup"><span data-stu-id="23b72-106">WM\_NCMBUTTONUP message</span></span>

<span data-ttu-id="23b72-107">Wird gesendet, wenn der Benutzer die mittlere Maustaste loslässt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="23b72-107">Posted when the user releases the middle mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="23b72-108">Diese Meldung wird an das Fenster gesendet, das den Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="23b72-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="23b72-109">Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.</span><span class="sxs-lookup"><span data-stu-id="23b72-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="23b72-110">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="23b72-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMBUTTONUP                  0x00A8
```



## <a name="parameters"></a><span data-ttu-id="23b72-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="23b72-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23b72-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23b72-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23b72-113">Der Treffer Test Wert, der von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion als Ergebnis der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="23b72-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="23b72-114">Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.</span><span class="sxs-lookup"><span data-stu-id="23b72-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="23b72-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23b72-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23b72-116">Eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-und y-Koordinaten des Cursors enthält.</span><span class="sxs-lookup"><span data-stu-id="23b72-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="23b72-117">Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="23b72-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23b72-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23b72-118">Return value</span></span>

<span data-ttu-id="23b72-119">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="23b72-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="23b72-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23b72-120">Remarks</span></span>

<span data-ttu-id="23b72-121">Sie können auch die Makros [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der X-und y-Koordinaten aus *LPARAM* zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="23b72-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="23b72-122">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="23b72-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="23b72-123">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="23b72-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="23b72-124">Wenn dies der Fall ist, sendet das System die WM- [**\_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="23b72-124">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="23b72-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23b72-125">Requirements</span></span>



| <span data-ttu-id="23b72-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23b72-126">Requirement</span></span> | <span data-ttu-id="23b72-127">Wert</span><span class="sxs-lookup"><span data-stu-id="23b72-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23b72-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23b72-128">Minimum supported client</span></span><br/> | <span data-ttu-id="23b72-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23b72-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="23b72-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23b72-130">Minimum supported server</span></span><br/> | <span data-ttu-id="23b72-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23b72-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="23b72-132">Header</span><span class="sxs-lookup"><span data-stu-id="23b72-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="23b72-133"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23b72-133"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23b72-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23b72-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="23b72-135">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="23b72-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="23b72-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="23b72-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="23b72-137">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="23b72-137">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="23b72-138">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="23b72-138">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="23b72-139">**WM- \_ nchittest**</span><span class="sxs-lookup"><span data-stu-id="23b72-139">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="23b72-140">**WM \_ ncmbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="23b72-140">**WM\_NCMBUTTONDBLCLK**</span></span>](wm-ncmbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="23b72-141">**WM \_ ncmbuttondown**</span><span class="sxs-lookup"><span data-stu-id="23b72-141">**WM\_NCMBUTTONDOWN**</span></span>](wm-ncmbuttondown.md)
</dt> <dt>

[<span data-ttu-id="23b72-142">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="23b72-142">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="23b72-143">**Licher**</span><span class="sxs-lookup"><span data-stu-id="23b72-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="23b72-144">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="23b72-144">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="23b72-145">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="23b72-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="23b72-146">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="23b72-146">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="23b72-147">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="23b72-147">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

