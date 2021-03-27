---
description: Die WM- \_ ncpaint-Meldung wird an ein Fenster gesendet, wenn Ihr Frame gezeichnet werden muss.
ms.assetid: d8a2a8b9-2c5d-484c-be09-67eb33de67c0
title: WM_NCPAINT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f6c2e211f3dc1602821b0197d295f940606c262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864316"
---
# <a name="wm_ncpaint-message"></a><span data-ttu-id="50d03-103">WM- \_ ncpaint-Meldung</span><span class="sxs-lookup"><span data-stu-id="50d03-103">WM\_NCPAINT message</span></span>

<span data-ttu-id="50d03-104">Die **WM- \_ ncpaint** -Meldung wird an ein Fenster gesendet, wenn Ihr Frame gezeichnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="50d03-104">The **WM\_NCPAINT** message is sent to a window when its frame must be painted.</span></span>

<span data-ttu-id="50d03-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="50d03-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="50d03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50d03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d03-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50d03-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50d03-108">Ein Handle für den Aktualisierungs Bereich des Fensters.</span><span class="sxs-lookup"><span data-stu-id="50d03-108">A handle to the update region of the window.</span></span> <span data-ttu-id="50d03-109">Der Aktualisierungs Bereich wird auf den Fensterrahmen zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="50d03-109">The update region is clipped to the window frame.</span></span>

</dd> <dt>

<span data-ttu-id="50d03-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50d03-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50d03-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="50d03-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d03-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50d03-112">Return value</span></span>

<span data-ttu-id="50d03-113">Eine Anwendung gibt 0 (null) zurück, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="50d03-113">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="50d03-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50d03-114">Remarks</span></span>

<span data-ttu-id="50d03-115">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion zeichnet den Fensterrahmen.</span><span class="sxs-lookup"><span data-stu-id="50d03-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function paints the window frame.</span></span>

<span data-ttu-id="50d03-116">Eine Anwendung kann die **WM- \_ ncpaint** -Nachricht abfangen und ihren eigenen benutzerdefinierten Fensterrahmen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="50d03-116">An application can intercept the **WM\_NCPAINT** message and paint its own custom window frame.</span></span> <span data-ttu-id="50d03-117">Der Clippingbereich für ein Fenster ist immer rechteckig, auch wenn die Form des Frames geändert wird.</span><span class="sxs-lookup"><span data-stu-id="50d03-117">The clipping region for a window is always rectangular, even if the shape of the frame is altered.</span></span>

<span data-ttu-id="50d03-118">Der *wParam* -Wert kann wie im folgenden Beispiel an [**getdcex**](/windows/desktop/api/Winuser/nf-winuser-getdcex) übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="50d03-118">The *wParam* value can be passed to [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) as in the following example.</span></span>


```C++
case WM_NCPAINT:
{
    HDC hdc;
    hdc = GetDCEx(hwnd, (HRGN)wParam, DCX_WINDOW|DCX_INTERSECTRGN);
    // Paint into this DC 
    ReleaseDC(hwnd, hdc);
}
```



## <a name="requirements"></a><span data-ttu-id="50d03-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="50d03-119">Requirements</span></span>



| <span data-ttu-id="50d03-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50d03-120">Requirement</span></span> | <span data-ttu-id="50d03-121">Wert</span><span class="sxs-lookup"><span data-stu-id="50d03-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50d03-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50d03-122">Minimum supported client</span></span><br/> | <span data-ttu-id="50d03-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50d03-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="50d03-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50d03-124">Minimum supported server</span></span><br/> | <span data-ttu-id="50d03-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50d03-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50d03-126">Header</span><span class="sxs-lookup"><span data-stu-id="50d03-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="50d03-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="50d03-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50d03-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="50d03-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d03-129">Übersicht über das Zeichnen und zeichnen</span><span class="sxs-lookup"><span data-stu-id="50d03-129">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="50d03-130">Zeichnen und Zeichnen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="50d03-130">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="50d03-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="50d03-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="50d03-132">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="50d03-132">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="50d03-133">**WM- \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="50d03-133">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> <dt>

[<span data-ttu-id="50d03-134">**Getdcex**</span><span class="sxs-lookup"><span data-stu-id="50d03-134">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> </dl>

 

 
