---
title: WM_SETCURSOR Meldung (Winuser. h)
description: Wird an ein Fenster gesendet, wenn die Maus bewirkt, dass der Cursor innerhalb eines Fensters bewegt wird und die Maus Eingaben nicht aufgezeichnet werden.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040696"
---
# <a name="wm_setcursor-message"></a><span data-ttu-id="a607d-104">WM- \_ SetCursor-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a607d-104">WM\_SETCURSOR message</span></span>

<span data-ttu-id="a607d-105">Wird an ein Fenster gesendet, wenn die Maus bewirkt, dass der Cursor innerhalb eines Fensters bewegt wird und die Maus Eingaben nicht aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a607d-105">Sent to a window if the mouse causes the cursor to move within a window and mouse input is not captured.</span></span>


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a><span data-ttu-id="a607d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a607d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a607d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a607d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a607d-108">Ein Handle für das Fenster, das den Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="a607d-108">A handle to the window that contains the cursor.</span></span>

</dd> <dt>

<span data-ttu-id="a607d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a607d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a607d-110">Das nieder wertige Wort von *LPARAM* gibt das Treffer Testergebnis für die Cursorposition an.</span><span class="sxs-lookup"><span data-stu-id="a607d-110">The low-order word of *lParam* specifies the hit-test result for the cursor position.</span></span> <span data-ttu-id="a607d-111">Mögliche Werte finden Sie in den Rückgabe Werten für [WM_NCHITTEST](../inputdev/wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="a607d-111">See the return values for [WM_NCHITTEST](../inputdev/wm-nchittest.md) for possible values.</span></span>

<span data-ttu-id="a607d-112">Das hochwertige Wort *LPARAM* gibt die Maus Fenster Meldung an, die dieses Ereignis ausgelöst hat, z. b. [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span><span class="sxs-lookup"><span data-stu-id="a607d-112">The high-order word of *lParam* specifies the mouse window message which triggered this event, such as [WM_MOUSEMOVE](../inputdev/wm-mousemove.md).</span></span> <span data-ttu-id="a607d-113">Wenn das Fenster in den Menü Modus wechselt, ist dieser Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a607d-113">When the window enters menu mode, this value is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a607d-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a607d-114">Return value</span></span>

<span data-ttu-id="a607d-115">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie " **true** " zurückgeben, um die weitere Verarbeitung anzuhalten, oder " **false** ".</span><span class="sxs-lookup"><span data-stu-id="a607d-115">If an application processes this message, it should return **TRUE** to halt further processing or **FALSE** to continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="a607d-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a607d-116">Remarks</span></span>

<span data-ttu-id="a607d-117">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) -Funktion übergibt die **WM- \_ SetCursor** -Nachricht vor der Verarbeitung an ein übergeordnetes Fenster.</span><span class="sxs-lookup"><span data-stu-id="a607d-117">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) function passes the **WM\_SETCURSOR** message to a parent window before processing.</span></span> <span data-ttu-id="a607d-118">Wenn das übergeordnete Fenster **true** zurückgibt, wird die weitere Verarbeitung angehalten.</span><span class="sxs-lookup"><span data-stu-id="a607d-118">If the parent window returns **TRUE**, further processing is halted.</span></span> <span data-ttu-id="a607d-119">Durch das übergeben der Nachricht an das übergeordnete Fenster eines Fensters erhält das übergeordnete Fenster Steuerelement über die Cursor Einstellung in einem untergeordneten Fenster.</span><span class="sxs-lookup"><span data-stu-id="a607d-119">Passing the message to a window's parent window gives the parent window control over the cursor's setting in a child window.</span></span> <span data-ttu-id="a607d-120">Die **defwindowproc** -Funktion verwendet diese Meldung auch, um den Cursor auf einen Pfeil festzulegen, wenn er sich nicht im Client Bereich befindet, oder an den registrierten Klassen Cursor, wenn er sich im Client Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="a607d-120">The **DefWindowProc** function also uses this message to set the cursor to an arrow if it is not in the client area, or to the registered class cursor if it is in the client area.</span></span> <span data-ttu-id="a607d-121">Wenn das nieder wertige Wort des *LPARAM* -Parameters **HTError** und das hochwertige Wort *LPARAM* angibt, dass eine der Maustasten gedrückt ist, ruft **defwindowproc** die [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="a607d-121">If the low-order word of the *lParam* parameter is **HTERROR** and the high-order word of *lParam* specifies that one of the mouse buttons is pressed, **DefWindowProc** calls the [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a607d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a607d-122">Requirements</span></span>



| <span data-ttu-id="a607d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a607d-123">Requirement</span></span> | <span data-ttu-id="a607d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a607d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a607d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a607d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a607d-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a607d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a607d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a607d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a607d-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a607d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a607d-129">Header</span><span class="sxs-lookup"><span data-stu-id="a607d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a607d-130"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a607d-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a607d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a607d-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="a607d-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a607d-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a607d-133">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="a607d-133">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

<span data-ttu-id="a607d-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a607d-134">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a607d-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a607d-135">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a607d-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="a607d-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a607d-137">Cursor</span><span class="sxs-lookup"><span data-stu-id="a607d-137">Cursors</span></span>](cursors.md)
</dt> </dl>

 

