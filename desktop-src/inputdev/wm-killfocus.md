---
title: WM_KILLFOCUS Meldung (Winuser. h)
description: Wird sofort an ein Fenster gesendet, bevor es den Tastaturfokus verliert.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- Tastatur-und Maus Eingaben für WM_KILLFOCUS Nachricht
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040471"
---
# <a name="wm_killfocus-message"></a><span data-ttu-id="17c9c-104">WM- \_ killfocus-Meldung</span><span class="sxs-lookup"><span data-stu-id="17c9c-104">WM\_KILLFOCUS message</span></span>

<span data-ttu-id="17c9c-105">Wird sofort an ein Fenster gesendet, bevor es den Tastaturfokus verliert.</span><span class="sxs-lookup"><span data-stu-id="17c9c-105">Sent to a window immediately before it loses the keyboard focus.</span></span>


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a><span data-ttu-id="17c9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="17c9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c9c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17c9c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17c9c-108">Ein Handle für das Fenster, das den Tastaturfokus erhält.</span><span class="sxs-lookup"><span data-stu-id="17c9c-108">A handle to the window that receives the keyboard focus.</span></span> <span data-ttu-id="17c9c-109">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="17c9c-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="17c9c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17c9c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17c9c-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="17c9c-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c9c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="17c9c-112">Return value</span></span>

<span data-ttu-id="17c9c-113">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="17c9c-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c9c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17c9c-114">Remarks</span></span>

<span data-ttu-id="17c9c-115">Wenn eine Anwendung eine Einfügemarke anzeigt, sollte die Einfügemarke zu diesem Zeitpunkt zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="17c9c-115">If an application is displaying a caret, the caret should be destroyed at this point.</span></span>

<span data-ttu-id="17c9c-116">Nehmen Sie bei der Verarbeitung dieser Nachricht keine Funktionsaufrufe vor, die ein Fenster anzeigen oder aktivieren.</span><span class="sxs-lookup"><span data-stu-id="17c9c-116">While processing this message, do not make any function calls that display or activate a window.</span></span> <span data-ttu-id="17c9c-117">Dies bewirkt, dass der Thread die Steuerung übernimmt und dazu führt, dass die Anwendung nicht mehr auf Nachrichten reagiert.</span><span class="sxs-lookup"><span data-stu-id="17c9c-117">This causes the thread to yield control and can cause the application to stop responding to messages.</span></span> <span data-ttu-id="17c9c-118">Weitere Informationen finden Sie unter [Message Deadlocks](/windows/desktop/winmsg/about-messages-and-message-queues).</span><span class="sxs-lookup"><span data-stu-id="17c9c-118">For more information, see [Message Deadlocks](/windows/desktop/winmsg/about-messages-and-message-queues).</span></span>

## <a name="requirements"></a><span data-ttu-id="17c9c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="17c9c-119">Requirements</span></span>



| <span data-ttu-id="17c9c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17c9c-120">Requirement</span></span> | <span data-ttu-id="17c9c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="17c9c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c9c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17c9c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="17c9c-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17c9c-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="17c9c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17c9c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="17c9c-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="17c9c-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="17c9c-126">Header</span><span class="sxs-lookup"><span data-stu-id="17c9c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="17c9c-127"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="17c9c-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17c9c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17c9c-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="17c9c-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="17c9c-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="17c9c-130">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="17c9c-130">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[<span data-ttu-id="17c9c-131">**WM- \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="17c9c-131">**WM\_SETFOCUS**</span></span>](wm-setfocus.md)
</dt> <dt>

<span data-ttu-id="17c9c-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="17c9c-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="17c9c-133">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="17c9c-133">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

