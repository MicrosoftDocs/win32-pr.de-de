---
description: Wird an ein Fenster gesendet, dessen Größe, Position oder Position in der Z-Reihenfolge aufgrund eines Aufrufes der Funktion SetWindowPos oder einer anderen Fenster Verwaltungsfunktion geändert wurde.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: WM_WINDOWPOSCHANGED Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128957"
---
# <a name="wm_windowposchanged-message"></a><span data-ttu-id="57d29-103">WM- \_ windowposchge-Nachricht</span><span class="sxs-lookup"><span data-stu-id="57d29-103">WM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="57d29-104">Wird an ein Fenster gesendet, dessen Größe, Position oder Position in der Z-Reihenfolge aufgrund eines Aufrufes der Funktion [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) oder einer anderen Fenster Verwaltungsfunktion geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="57d29-104">Sent to a window whose size, position, or place in the Z order has changed as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="57d29-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="57d29-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a><span data-ttu-id="57d29-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57d29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57d29-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57d29-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57d29-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="57d29-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57d29-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57d29-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57d29-110">Ein Zeiger auf eine [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) -Struktur, die Informationen über die neue Größe und Position des Fensters enthält.</span><span class="sxs-lookup"><span data-stu-id="57d29-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57d29-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57d29-111">Return value</span></span>

<span data-ttu-id="57d29-112">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="57d29-112">Type: **LRESULT**</span></span>

<span data-ttu-id="57d29-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="57d29-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="57d29-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57d29-114">Remarks</span></span>

<span data-ttu-id="57d29-115">Standardmäßig sendet die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die [**WM- \_ Größe**](wm-size.md) und die WM-Verschiebungs Nachricht an das-Fenster. [**\_**](wm-move.md)</span><span class="sxs-lookup"><span data-stu-id="57d29-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_SIZE**](wm-size.md) and [**WM\_MOVE**](wm-move.md) messages to the window.</span></span> <span data-ttu-id="57d29-116">Die **WM- \_ Größe** und die WM-Verschiebungs Nachricht werden nicht gesendet, wenn eine Anwendung die **WM- \_ windowposchangsnachricht** verarbeitet, ohne **defwindowproc** Aufrufs. **\_**</span><span class="sxs-lookup"><span data-stu-id="57d29-116">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span> <span data-ttu-id="57d29-117">Es ist effizienter, jede verschiebe-oder Größen Änderungs Verarbeitung während der **WM- \_ windowposchge** -Nachricht auszuführen, ohne **defwindowproc** aufzurufenden.</span><span class="sxs-lookup"><span data-stu-id="57d29-117">It is more efficient to perform any move or size change processing during the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="57d29-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57d29-118">Requirements</span></span>



| <span data-ttu-id="57d29-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57d29-119">Requirement</span></span> | <span data-ttu-id="57d29-120">Wert</span><span class="sxs-lookup"><span data-stu-id="57d29-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57d29-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57d29-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57d29-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57d29-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="57d29-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57d29-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57d29-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57d29-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57d29-125">Header</span><span class="sxs-lookup"><span data-stu-id="57d29-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="57d29-126"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="57d29-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57d29-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57d29-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="57d29-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="57d29-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57d29-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="57d29-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="57d29-130">**Enddeferwindowpos**</span><span class="sxs-lookup"><span data-stu-id="57d29-130">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="57d29-131">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="57d29-131">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="57d29-132">**WINDOWPOS**</span><span class="sxs-lookup"><span data-stu-id="57d29-132">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="57d29-133">**WM \_ verschieben**</span><span class="sxs-lookup"><span data-stu-id="57d29-133">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="57d29-134">**WM- \_ Größe**</span><span class="sxs-lookup"><span data-stu-id="57d29-134">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="57d29-135">**WM- \_ windowposchanging**</span><span class="sxs-lookup"><span data-stu-id="57d29-135">**WM\_WINDOWPOSCHANGING**</span></span>](wm-windowposchanging.md)
</dt> <dt>

<span data-ttu-id="57d29-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="57d29-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57d29-137">Windows</span><span class="sxs-lookup"><span data-stu-id="57d29-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
