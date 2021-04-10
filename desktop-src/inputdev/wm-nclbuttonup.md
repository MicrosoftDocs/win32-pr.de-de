---
title: WM_NCLBUTTONUP Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer die linke Maustaste loslässt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.
ms.assetid: 0c30dcbd-a4ff-43da-bbd2-fbac1a347c11
keywords:
- Tastatur-und Maus Eingaben für WM_NCLBUTTONUP Nachricht
topic_type:
- apiref
api_name:
- WM_NCLBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15df7beefbfa411d00b5a069b68f4ef8cabdff58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040467"
---
# <a name="wm_nclbuttonup-message"></a><span data-ttu-id="0bd94-106">WM- \_ nclbuttonup-Meldung</span><span class="sxs-lookup"><span data-stu-id="0bd94-106">WM\_NCLBUTTONUP message</span></span>

<span data-ttu-id="0bd94-107">Wird gesendet, wenn der Benutzer die linke Maustaste loslässt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="0bd94-107">Posted when the user releases the left mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="0bd94-108">Diese Meldung wird an das Fenster gesendet, das den Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="0bd94-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="0bd94-109">Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.</span><span class="sxs-lookup"><span data-stu-id="0bd94-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="0bd94-110">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0bd94-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCLBUTTONUP                  0x00A2
```



## <a name="parameters"></a><span data-ttu-id="0bd94-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bd94-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bd94-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0bd94-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bd94-113">Der Treffer Test Wert, der von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion als Ergebnis der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0bd94-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="0bd94-114">Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.</span><span class="sxs-lookup"><span data-stu-id="0bd94-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="0bd94-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0bd94-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bd94-116">Eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-und y-Koordinaten des Cursors enthält.</span><span class="sxs-lookup"><span data-stu-id="0bd94-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="0bd94-117">Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="0bd94-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bd94-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bd94-118">Return value</span></span>

<span data-ttu-id="0bd94-119">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0bd94-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd94-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bd94-120">Remarks</span></span>

<span data-ttu-id="0bd94-121">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion testet den angegebenen Punkt, um die Position des Cursors zu ermitteln, und führt die entsprechende Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="0bd94-121">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to find out the location of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="0bd94-122">Falls zutreffend, sendet **defwindowproc** die [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Nachricht an das-Fenster.</span><span class="sxs-lookup"><span data-stu-id="0bd94-122">If appropriate, **DefWindowProc** sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="0bd94-123">Sie können auch die Makros [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der X-und y-Koordinaten aus *LPARAM* zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="0bd94-123">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="0bd94-124">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0bd94-124">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="0bd94-125">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="0bd94-125">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="0bd94-126">Wenn dies der Fall ist, sendet das System die WM- [**\_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="0bd94-126">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bd94-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bd94-127">Requirements</span></span>



| <span data-ttu-id="0bd94-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bd94-128">Requirement</span></span> | <span data-ttu-id="0bd94-129">Wert</span><span class="sxs-lookup"><span data-stu-id="0bd94-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd94-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0bd94-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0bd94-131">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bd94-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0bd94-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0bd94-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0bd94-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bd94-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0bd94-134">Header</span><span class="sxs-lookup"><span data-stu-id="0bd94-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bd94-135"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bd94-135"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bd94-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bd94-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="0bd94-137">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0bd94-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0bd94-138">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="0bd94-138">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="0bd94-139">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="0bd94-139">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="0bd94-140">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="0bd94-140">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="0bd94-141">**WM- \_ nchittest**</span><span class="sxs-lookup"><span data-stu-id="0bd94-141">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="0bd94-142">**WM \_ nclbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="0bd94-142">**WM\_NCLBUTTONDBLCLK**</span></span>](wm-nclbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="0bd94-143">**WM- \_ nclbuttondown**</span><span class="sxs-lookup"><span data-stu-id="0bd94-143">**WM\_NCLBUTTONDOWN**</span></span>](wm-nclbuttondown.md)
</dt> <dt>

[<span data-ttu-id="0bd94-144">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="0bd94-144">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="0bd94-145">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0bd94-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0bd94-146">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="0bd94-146">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="0bd94-147">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="0bd94-147">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0bd94-148">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="0bd94-148">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="0bd94-149">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0bd94-149">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

