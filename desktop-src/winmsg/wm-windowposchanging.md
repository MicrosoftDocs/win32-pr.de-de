---
description: Wird an ein Fenster gesendet, dessen Größe, Position oder Position in der Z-Reihenfolge im Ergebnis eines Aufrufes der Funktion SetWindowPos oder einer anderen Fenster Verwaltungsfunktion geändert wird.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: WM_WINDOWPOSCHANGING Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758461"
---
# <a name="wm_windowposchanging-message"></a><span data-ttu-id="375ae-103">WM- \_ windowposchanging-Meldung</span><span class="sxs-lookup"><span data-stu-id="375ae-103">WM\_WINDOWPOSCHANGING message</span></span>

<span data-ttu-id="375ae-104">Wird an ein Fenster gesendet, dessen Größe, Position oder Position in der Z-Reihenfolge im Ergebnis eines Aufrufes der Funktion [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) oder einer anderen Fenster Verwaltungsfunktion geändert wird.</span><span class="sxs-lookup"><span data-stu-id="375ae-104">Sent to a window whose size, position, or place in the Z order is about to change as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="375ae-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="375ae-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a><span data-ttu-id="375ae-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="375ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="375ae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="375ae-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="375ae-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="375ae-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="375ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="375ae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="375ae-110">Ein Zeiger auf eine [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) -Struktur, die Informationen über die neue Größe und Position des Fensters enthält.</span><span class="sxs-lookup"><span data-stu-id="375ae-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="375ae-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="375ae-111">Return value</span></span>

<span data-ttu-id="375ae-112">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="375ae-112">Type: **LRESULT**</span></span>

<span data-ttu-id="375ae-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="375ae-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="375ae-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="375ae-114">Remarks</span></span>

<span data-ttu-id="375ae-115">Bei einem Fenster mit dem [**\_ über**](window-styles.md) Lapp enden oder dem **WS- \_ dicken Frame** -Stil sendet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die [**WM \_ getminmaxinfo**](wm-getminmaxinfo.md) -Meldung an das Fenster.</span><span class="sxs-lookup"><span data-stu-id="375ae-115">For a window with the [**WS\_OVERLAPPED**](window-styles.md) or **WS\_THICKFRAME** style, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_GETMINMAXINFO**](wm-getminmaxinfo.md) message to the window.</span></span> <span data-ttu-id="375ae-116">Dies geschieht, um die neue Größe und Position des Fensters zu überprüfen und die Client Stile [CS \_ bytealignclient](about-window-classes.md) und CS \_ bytealignwindow zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="375ae-116">This is done to validate the new size and position of the window and to enforce the [CS\_BYTEALIGNCLIENT](about-window-classes.md) and CS\_BYTEALIGNWINDOW client styles.</span></span> <span data-ttu-id="375ae-117">Wenn die WM- **\_ windowposchanging** -Nachricht nicht an die **defwindowproc** -Funktion übergeben wird, kann eine Anwendung diese Standardeinstellungen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="375ae-117">By not passing the **WM\_WINDOWPOSCHANGING** message to the **DefWindowProc** function, an application can override these defaults.</span></span>

<span data-ttu-id="375ae-118">Während diese Nachricht verarbeitet wird, wirkt sich das Ändern aller Werte in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) auf die neue Größe, Position oder Position des Fensters in der Z-Reihenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="375ae-118">While this message is being processed, modifying any of the values in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) affects the window's new size, position, or place in the Z order.</span></span> <span data-ttu-id="375ae-119">Eine Anwendung kann Änderungen am Fenster verhindern, indem die entsprechenden Bits im **Flags** -Member von **Windows POS** festgelegt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="375ae-119">An application can prevent changes to the window by setting or clearing the appropriate bits in the **flags** member of **WINDOWPOS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="375ae-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="375ae-120">Requirements</span></span>



| <span data-ttu-id="375ae-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="375ae-121">Requirement</span></span> | <span data-ttu-id="375ae-122">Wert</span><span class="sxs-lookup"><span data-stu-id="375ae-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="375ae-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="375ae-123">Minimum supported client</span></span><br/> | <span data-ttu-id="375ae-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="375ae-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="375ae-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="375ae-125">Minimum supported server</span></span><br/> | <span data-ttu-id="375ae-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="375ae-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="375ae-127">Header</span><span class="sxs-lookup"><span data-stu-id="375ae-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="375ae-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="375ae-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="375ae-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="375ae-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="375ae-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="375ae-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="375ae-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="375ae-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="375ae-132">**Enddeferwindowpos**</span><span class="sxs-lookup"><span data-stu-id="375ae-132">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="375ae-133">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="375ae-133">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="375ae-134">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="375ae-134">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="375ae-135">**WM \_ getminmaxinfo**</span><span class="sxs-lookup"><span data-stu-id="375ae-135">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md)
</dt> <dt>

[<span data-ttu-id="375ae-136">**WM \_ verschieben**</span><span class="sxs-lookup"><span data-stu-id="375ae-136">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="375ae-137">**WM- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="375ae-137">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="375ae-138">**WM-Windows-Server \_**</span><span class="sxs-lookup"><span data-stu-id="375ae-138">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="375ae-139">**Licher**</span><span class="sxs-lookup"><span data-stu-id="375ae-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="375ae-140">Windows</span><span class="sxs-lookup"><span data-stu-id="375ae-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
