---
description: Die WM- \_ printclient-Nachricht wird an ein Fenster gesendet, um anzufordern, dass Sie den Client Bereich im angegebenen Gerätekontext (in der Regel in einem Drucker Gerätekontext) zeichnet.
ms.assetid: 8703ee74-812a-4ca2-8ee3-a3b8779739e7
title: WM_PRINTCLIENT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52aca68695964a35ab9a2c4e309cd71c2e9f7eca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980280"
---
# <a name="wm_printclient-message"></a><span data-ttu-id="208cb-103">WM- \_ printclient-Meldung</span><span class="sxs-lookup"><span data-stu-id="208cb-103">WM\_PRINTCLIENT message</span></span>

<span data-ttu-id="208cb-104">Die **WM- \_ printclient** -Nachricht wird an ein Fenster gesendet, um anzufordern, dass Sie den Client Bereich im angegebenen Gerätekontext (in der Regel in einem Drucker Gerätekontext) zeichnet.</span><span class="sxs-lookup"><span data-stu-id="208cb-104">The **WM\_PRINTCLIENT** message is sent to a window to request that it draw its client area in the specified device context, most commonly in a printer device context.</span></span>

<span data-ttu-id="208cb-105">Im Gegensatz zum [**WM- \_ Print**](wm-print.md)wird **WM \_ printclient** nicht von [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="208cb-105">Unlike [**WM\_PRINT**](wm-print.md), **WM\_PRINTCLIENT** is not processed by [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="208cb-106">Ein Fenster sollte die **WM \_ printclient** -Nachricht über eine von der Anwendung definierte [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion verarbeiten, damit es ordnungsgemäß verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="208cb-106">A window should process the **WM\_PRINTCLIENT** message through an application-defined [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function for it to be used properly.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="208cb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="208cb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="208cb-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="208cb-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="208cb-109">Ein Handle für den Gerätekontext, in dem gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="208cb-109">A handle to the device context to draw in.</span></span>

</dd> <dt>

<span data-ttu-id="208cb-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="208cb-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="208cb-111">Die Zeichnungsoptionen.</span><span class="sxs-lookup"><span data-stu-id="208cb-111">The drawing options.</span></span> <span data-ttu-id="208cb-112">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="208cb-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="208cb-113">Wert</span><span class="sxs-lookup"><span data-stu-id="208cb-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="208cb-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="208cb-114">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <span data-ttu-id="208cb-115"><dt>**PRF \_ checkvisible**</dt></span><span class="sxs-lookup"><span data-stu-id="208cb-115"><dt>**PRF\_CHECKVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="208cb-116">Zeichnet das Fenster nur, wenn es sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="208cb-116">Draws the window only if it is visible.</span></span><br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <span data-ttu-id="208cb-117"><dt>**untergeordnete Elemente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="208cb-117"><dt>**PRF\_CHILDREN**</dt></span></span> </dl>             | <span data-ttu-id="208cb-118">Zeichnet alle sichtbaren untergeordneten Fenster.</span><span class="sxs-lookup"><span data-stu-id="208cb-118">Draws all visible children windows.</span></span><br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <span data-ttu-id="208cb-119"><dt>**PRF- \_ Client**</dt></span><span class="sxs-lookup"><span data-stu-id="208cb-119"><dt>**PRF\_CLIENT**</dt></span></span> </dl>                   | <span data-ttu-id="208cb-120">Zeichnet den Client Bereich des Fensters.</span><span class="sxs-lookup"><span data-stu-id="208cb-120">Draws the client area of the window.</span></span><br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <span data-ttu-id="208cb-121"><dt>**PRF \_ erasebkgnd**</dt></span><span class="sxs-lookup"><span data-stu-id="208cb-121"><dt>**PRF\_ERASEBKGND**</dt></span></span> </dl>       | <span data-ttu-id="208cb-122">Löscht den Hintergrund vor dem Zeichnen des Fensters.</span><span class="sxs-lookup"><span data-stu-id="208cb-122">Erases the background before drawing the window.</span></span><br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <span data-ttu-id="208cb-123"><dt>**PRF- \_ nonclient**</dt></span><span class="sxs-lookup"><span data-stu-id="208cb-123"><dt>**PRF\_NONCLIENT**</dt></span></span> </dl>          | <span data-ttu-id="208cb-124">Zeichnet den nicht-Client Bereich des Fensters.</span><span class="sxs-lookup"><span data-stu-id="208cb-124">Draws the nonclient area of the window.</span></span><br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <span data-ttu-id="208cb-125"><dt>**PRF- \_ Besitzer**</dt></span><span class="sxs-lookup"><span data-stu-id="208cb-125"><dt>**PRF\_OWNED**</dt></span></span> </dl>                      | <span data-ttu-id="208cb-126">Zeichnet alle eigenen Fenster.</span><span class="sxs-lookup"><span data-stu-id="208cb-126">Draws all owned windows.</span></span><br/>                         |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="208cb-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="208cb-127">Remarks</span></span>

<span data-ttu-id="208cb-128">Diese Nachricht kann von einem Fenster auf die gleiche Weise wie bei [**WM \_ Paint**](./wm-paint.md)verarbeitet werden, mit der Ausnahme, dass [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) und [**endpaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) nicht aufgerufen werden müssen (ein Gerätekontext wird bereitgestellt) und das Fenster den gesamten Client Bereich und nicht nur den ungültigen Bereich zeichnen soll.</span><span class="sxs-lookup"><span data-stu-id="208cb-128">A window can process this message in much the same manner as [**WM\_PAINT**](./wm-paint.md), except that [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) need not be called (a device context is provided), and the window should draw its entire client area rather than just the invalid region.</span></span>

<span data-ttu-id="208cb-129">Windows, die an beliebiger Stelle im System verwendet werden können, z. b. Steuerelemente, sollten diese Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="208cb-129">Windows that can be used anywhere in the system, such as controls, should process this message.</span></span> <span data-ttu-id="208cb-130">Es ist wahrscheinlich auch für andere Fenster sinnvoll, diese Nachricht zu verarbeiten, da Sie relativ einfach zu implementieren ist.</span><span class="sxs-lookup"><span data-stu-id="208cb-130">It is probably worthwhile for other windows to process this message as well because it is relatively easy to implement.</span></span>

<span data-ttu-id="208cb-131">Die [animatewindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) -Funktion erfordert, dass das zu animierende Fenster die **WM \_ printclient** -Nachricht implementiert.</span><span class="sxs-lookup"><span data-stu-id="208cb-131">The [AnimateWindow](/windows/desktop/api/winuser/nf-winuser-animatewindow) function requires that the window being animated implements the **WM\_PRINTCLIENT** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="208cb-132">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="208cb-132">Requirements</span></span>



| <span data-ttu-id="208cb-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="208cb-133">Requirement</span></span> | <span data-ttu-id="208cb-134">Wert</span><span class="sxs-lookup"><span data-stu-id="208cb-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208cb-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="208cb-135">Minimum supported client</span></span><br/> | <span data-ttu-id="208cb-136">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="208cb-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="208cb-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="208cb-137">Minimum supported server</span></span><br/> | <span data-ttu-id="208cb-138">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="208cb-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="208cb-139">Header</span><span class="sxs-lookup"><span data-stu-id="208cb-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="208cb-140"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="208cb-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="208cb-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="208cb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="208cb-142">Übersicht über das Zeichnen und zeichnen</span><span class="sxs-lookup"><span data-stu-id="208cb-142">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="208cb-143">Zeichnen und Zeichnen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="208cb-143">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="208cb-144">**Animatewindow**</span><span class="sxs-lookup"><span data-stu-id="208cb-144">**AnimateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-animatewindow)
</dt> <dt>

[<span data-ttu-id="208cb-145">**BeginPaint**</span><span class="sxs-lookup"><span data-stu-id="208cb-145">**BeginPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-beginpaint)
</dt> <dt>

[<span data-ttu-id="208cb-146">**Endpaint auf**</span><span class="sxs-lookup"><span data-stu-id="208cb-146">**EndPaint**</span></span>](/windows/desktop/api/Winuser/nf-winuser-endpaint)
</dt> <dt>

[<span data-ttu-id="208cb-147">**WM- \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="208cb-147">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
