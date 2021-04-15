---
title: WM_NCMOUSEMOVE Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, wenn der Cursor innerhalb des nicht-Client Bereichs des Fensters bewegt wird. Diese Meldung wird an das Fenster gesendet, das den Cursor enthält. Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.
ms.assetid: 49c7cde9-701c-4821-8d16-31ca3c016ed4
keywords:
- Tastatur-und Maus Eingaben für WM_NCMOUSEMOVE Nachricht
topic_type:
- apiref
api_name:
- WM_NCMOUSEMOVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65461d2e84b6185b95ac05c071f31df680450e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479179"
---
# <a name="wm_ncmousemove-message"></a><span data-ttu-id="801db-106">WM- \_ ncmouungsmeldung</span><span class="sxs-lookup"><span data-stu-id="801db-106">WM\_NCMOUSEMOVE message</span></span>

<span data-ttu-id="801db-107">Wird an ein Fenster gesendet, wenn der Cursor innerhalb des nicht-Client Bereichs des Fensters bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="801db-107">Posted to a window when the cursor is moved within the nonclient area of the window.</span></span> <span data-ttu-id="801db-108">Diese Meldung wird an das Fenster gesendet, das den Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="801db-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="801db-109">Wenn ein Fenster die Maus erfasst hat, wird diese Meldung nicht gepostet.</span><span class="sxs-lookup"><span data-stu-id="801db-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="801db-110">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="801db-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMOUSEMOVE                  0x00A0
```



## <a name="parameters"></a><span data-ttu-id="801db-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="801db-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="801db-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="801db-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="801db-113">Der Treffer Test Wert, der von der [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion als Ergebnis der Verarbeitung der [**WM- \_ nchittest**](wm-nchittest.md) -Nachricht zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="801db-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="801db-114">Eine Liste der Treffer Test Werte finden Sie unter **WM \_ nchittest**.</span><span class="sxs-lookup"><span data-stu-id="801db-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="801db-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="801db-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="801db-116">Eine [**Points**](/previous-versions//dd162808(v=vs.85)) -Struktur, die die x-und y-Koordinaten des Cursors enthält.</span><span class="sxs-lookup"><span data-stu-id="801db-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="801db-117">Die Koordinaten sind relativ zur oberen linken Ecke des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="801db-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="801db-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="801db-118">Return value</span></span>

<span data-ttu-id="801db-119">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="801db-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="801db-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="801db-120">Remarks</span></span>

<span data-ttu-id="801db-121">Wenn dies der Fall ist, sendet das System die WM- [**\_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="801db-121">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="801db-122">Sie können auch die Makros [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) verwenden, um die Werte der X-und y-Koordinaten aus *LPARAM* zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="801db-122">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="801db-123">Verwenden Sie die [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -oder [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) -Makros nicht, um die x-und y-Koordinaten der Cursorposition zu extrahieren, da diese Makros falsche Ergebnisse für Systeme mit mehreren Monitoren zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="801db-123">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="801db-124">Systeme mit mehreren Monitoren können über negative x-und y-Koordinaten verfügen, und **LoWord** und **HIWORD** behandeln die Koordinaten als nicht signierte Mengen.</span><span class="sxs-lookup"><span data-stu-id="801db-124">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="801db-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="801db-125">Requirements</span></span>



| <span data-ttu-id="801db-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="801db-126">Requirement</span></span> | <span data-ttu-id="801db-127">Wert</span><span class="sxs-lookup"><span data-stu-id="801db-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="801db-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="801db-128">Minimum supported client</span></span><br/> | <span data-ttu-id="801db-129">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="801db-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="801db-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="801db-130">Minimum supported server</span></span><br/> | <span data-ttu-id="801db-131">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="801db-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="801db-132">Header</span><span class="sxs-lookup"><span data-stu-id="801db-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="801db-133"><dt>Winuser. h (Include WINDOWSX. h)</dt></span><span class="sxs-lookup"><span data-stu-id="801db-133"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="801db-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="801db-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="801db-135">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="801db-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="801db-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="801db-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="801db-137">**GET \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="801db-137">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="801db-138">**\_Y- \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="801db-138">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="801db-139">**WM- \_ nchittest**</span><span class="sxs-lookup"><span data-stu-id="801db-139">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="801db-140">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="801db-140">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="801db-141">**Licher**</span><span class="sxs-lookup"><span data-stu-id="801db-141">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="801db-142">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="801db-142">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="801db-143">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="801db-143">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="801db-144">**Makepoints**</span><span class="sxs-lookup"><span data-stu-id="801db-144">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="801db-145">[**Punkt**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="801db-145">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

