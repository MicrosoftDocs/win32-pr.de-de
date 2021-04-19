---
title: WM_NCXBUTTONDOWN Meldung (Winuser. h)
description: Wird gesendet, wenn der Benutzer die erste oder zweite X-Schaltfläche drückt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.
ms.assetid: 72744c98-1898-4548-bd10-61ad53eeab15
keywords:
- Tastatur-und Maus Eingaben für WM_NCXBUTTONDOWN Nachricht
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd615b1e30e013f23097cdc7a8ca7c22c338684a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342206"
---
# <a name="wm_ncxbuttondown-message"></a><span data-ttu-id="c5ba3-106">WM- \_ ncxbuttondown-Meldung</span><span class="sxs-lookup"><span data-stu-id="c5ba3-106">WM\_NCXBUTTONDOWN message</span></span>

<span data-ttu-id="c5ba3-107">Wird gesendet, wenn der Benutzer die erste oder zweite X-Schaltfläche drückt, während sich der Cursor im nicht-Client Bereich eines Fensters befindet.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-107">Posted when the user presses the first or second X button while the cursor is in the nonclient area of a window.</span></span> <span data-ttu-id="c5ba3-108">Diese Meldung wird an das Fenster gesendet, das den Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="c5ba3-109">Wenn ein Fenster die Maus erfasst hat, wird diese Meldung *nicht* gepostet.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-109">If a window has captured the mouse, this message is *not* posted.</span></span>

<span data-ttu-id="c5ba3-110">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCXBUTTONDOWN                0x00AB
```



## <a name="parameters"></a><span data-ttu-id="c5ba3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5ba3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ba3-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5ba3-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ba3-113">Das nieder wertige Wort gibt den Treffer Testwert an, der von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion aus der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function from processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="c5ba3-114">Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span> <span data-ttu-id="c5ba3-115">Das höchst wertige Wort gibt an, welche Schaltfläche gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-115">The high-order word indicates which button was pressed.</span></span> <span data-ttu-id="c5ba3-116">Dieses Argument einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-116">It can be one of the following values.</span></span>



| <span data-ttu-id="c5ba3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c5ba3-117">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="c5ba3-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c5ba3-118">Meaning</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="c5ba3-119"><dt>**XButton1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c5ba3-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="c5ba3-120">Die erste X-Taste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-120">The first X button was pressed.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="c5ba3-121"><dt>**XButton2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="c5ba3-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="c5ba3-122">Die zweite X-Taste wurde gedrückt.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-122">The second X button was pressed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c5ba3-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5ba3-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5ba3-124">Ein Zeiger auf eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-und y-Koordinaten des Cursors enthält.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-124">A pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="c5ba3-125">Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-125">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ba3-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5ba3-126">Return value</span></span>

<span data-ttu-id="c5ba3-127">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-127">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="c5ba3-128">Weitere Informationen zum Verarbeiten des Rückgabewerts finden Sie im Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="c5ba3-128">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ba3-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5ba3-129">Remarks</span></span>

<span data-ttu-id="c5ba3-130">Verwenden Sie den folgenden Code, um die Informationen im *wParam* -Parameter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-130">Use the following code to get the information in the *wParam* parameter.</span></span>


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



<span data-ttu-id="c5ba3-131">Sie können auch den folgenden Code verwenden, um die x-und y-Koordinaten von *LPARAM* zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="c5ba3-131">You can also use the following code to get the x- and y-coordinates from *lParam*:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="c5ba3-132">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-132">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="c5ba3-133">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-133">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="c5ba3-134">Standardmäßig testet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion den angegebenen Punkt, um die Position des Cursors abzurufen, und führt die entsprechende Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-134">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to get the position of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="c5ba3-135">Bei Bedarf wird die WM- [**\_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Nachricht an das Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-135">If appropriate, it sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="c5ba3-136">Im Gegensatz zu den Nachrichten [**WM \_ nclbuttondown**](wm-nclbuttondown.md), [**WM \_ ncmbuttondown**](wm-ncmbuttondown.md)und [**WM \_ ncrbuttondown**](wm-ncrbuttondown.md) sollte eine Anwendung bei der Verarbeitung von dieser Nachricht **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-136">Unlike the [**WM\_NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM\_NCMBUTTONDOWN**](wm-ncmbuttondown.md), and [**WM\_NCRBUTTONDOWN**](wm-ncrbuttondown.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="c5ba3-137">Auf diese Weise kann Software, die diese Meldung auf Windows-Systemen vor Windows 2000 simuliert, ermitteln, ob die Fenster Prozedur die Nachricht verarbeitet hat oder [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) aufgerufen hat, um Sie zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c5ba3-137">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ba3-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5ba3-138">Requirements</span></span>



| <span data-ttu-id="c5ba3-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5ba3-139">Requirement</span></span> | <span data-ttu-id="c5ba3-140">Wert</span><span class="sxs-lookup"><span data-stu-id="c5ba3-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ba3-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5ba3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ba3-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c5ba3-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5ba3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ba3-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c5ba3-145">Header</span><span class="sxs-lookup"><span data-stu-id="c5ba3-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ba3-146"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5ba3-146"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ba3-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5ba3-147">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5ba3-148">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-148">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c5ba3-149">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-149">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="c5ba3-150">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-150">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="c5ba3-151">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-151">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="c5ba3-152">**WM- \_ nchittest**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-152">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="c5ba3-153">**WM \_ ncxbuttondblclk**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-153">**WM\_NCXBUTTONDBLCLK**</span></span>](wm-ncxbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="c5ba3-154">**WM- \_ ncxbuttonup**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-154">**WM\_NCXBUTTONUP**</span></span>](wm-ncxbuttonup.md)
</dt> <dt>

[<span data-ttu-id="c5ba3-155">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-155">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="c5ba3-156">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5ba3-157">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="c5ba3-157">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="c5ba3-158">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-158">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c5ba3-159">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="c5ba3-159">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="c5ba3-160">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5ba3-160">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

