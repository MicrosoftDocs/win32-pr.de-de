---
description: Die WM \_ syncpaint-Meldung wird zum Synchronisieren der Zeichnung verwendet, während Verknüpfungen unabhängiger GUI-Threads vermieden werden.
ms.assetid: 4446be4e-e0b9-46ce-95b2-bea876348c25
title: WM_SYNCPAINT Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5602e867af9b7ce467e8979c9f341758414ad287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994550"
---
# <a name="wm_syncpaint-message"></a><span data-ttu-id="01c37-103">WM \_ syncpaint-Meldung</span><span class="sxs-lookup"><span data-stu-id="01c37-103">WM\_SYNCPAINT message</span></span>

<span data-ttu-id="01c37-104">Die **WM \_ syncpaint** -Meldung wird zum Synchronisieren der Zeichnung verwendet, während Verknüpfungen unabhängiger GUI-Threads vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="01c37-104">The **WM\_SYNCPAINT** message is used to synchronize painting while avoiding linking independent GUI threads.</span></span>

<span data-ttu-id="01c37-105">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="01c37-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="01c37-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="01c37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01c37-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="01c37-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01c37-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="01c37-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="01c37-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="01c37-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="01c37-110">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="01c37-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01c37-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01c37-111">Return value</span></span>

<span data-ttu-id="01c37-112">Eine Anwendung gibt 0 (null) zurück, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="01c37-112">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="01c37-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01c37-113">Remarks</span></span>

<span data-ttu-id="01c37-114">Wenn ein Fenster ausgeblendet, angezeigt, verschoben oder vergrößert wurde, kann das System feststellen, dass es erforderlich ist, eine **WM \_ syncpaint** -Meldung an die Fenster der obersten Ebene anderer Threads zu senden.</span><span class="sxs-lookup"><span data-stu-id="01c37-114">When a window has been hidden, shown, moved, or sized, the system may determine that it is necessary to send a **WM\_SYNCPAINT** message to the top-level windows of other threads.</span></span> <span data-ttu-id="01c37-115">Anwendungen müssen für die Verarbeitung **WM \_ syncpaint** an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  übergeben.</span><span class="sxs-lookup"><span data-stu-id="01c37-115">Applications must pass **WM\_SYNCPAINT** to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  for processing.</span></span> <span data-ttu-id="01c37-116">Die **defwindowproc** -Funktion sendet eine [**WM \_ ncpaint**](wm-ncpaint.md) -Meldung an die Fenster Prozedur, wenn der Fensterrahmen gezeichnet werden muss, und sendet eine [**WM \_ erasebkgnd**](../winmsg/wm-erasebkgnd.md) -Meldung, wenn der Fenster Hintergrund gelöscht werden muss.</span><span class="sxs-lookup"><span data-stu-id="01c37-116">The **DefWindowProc** function will send a [**WM\_NCPAINT**](wm-ncpaint.md) message to the window procedure if the window frame must be painted and send a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message if the window background must be erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c37-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="01c37-117">Requirements</span></span>



| <span data-ttu-id="01c37-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01c37-118">Requirement</span></span> | <span data-ttu-id="01c37-119">Wert</span><span class="sxs-lookup"><span data-stu-id="01c37-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c37-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01c37-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01c37-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01c37-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="01c37-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01c37-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01c37-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01c37-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="01c37-124">Header</span><span class="sxs-lookup"><span data-stu-id="01c37-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="01c37-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="01c37-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c37-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="01c37-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c37-127">Übersicht über das Zeichnen und zeichnen</span><span class="sxs-lookup"><span data-stu-id="01c37-127">Painting and Drawing Overview</span></span>](painting-and-drawing.md)
</dt> <dt>

[<span data-ttu-id="01c37-128">Zeichnen und Zeichnen von Nachrichten</span><span class="sxs-lookup"><span data-stu-id="01c37-128">Painting and Drawing Messages</span></span>](painting-and-drawing-messages.md)
</dt> <dt>

[<span data-ttu-id="01c37-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="01c37-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="01c37-130">**Getdcex**</span><span class="sxs-lookup"><span data-stu-id="01c37-130">**GetDCEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdcex)
</dt> <dt>

[<span data-ttu-id="01c37-131">**GetWindowDC**</span><span class="sxs-lookup"><span data-stu-id="01c37-131">**GetWindowDC**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)
</dt> <dt>

[<span data-ttu-id="01c37-132">**WM- \_ Paint**</span><span class="sxs-lookup"><span data-stu-id="01c37-132">**WM\_PAINT**</span></span>](wm-paint.md)
</dt> </dl>

 

 
