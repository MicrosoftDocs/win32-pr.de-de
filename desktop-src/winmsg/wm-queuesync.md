---
description: Wird von einer computerbasierten Schulungs Anwendung (CBT) zum Trennen von Benutzereingabe Nachrichten von anderen Nachrichten gesendet, die über die Prozedur "WH \_ journalplayback" gesendet werden.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: WM_QUEUESYNC Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348027"
---
# <a name="wm_queuesync-message"></a><span data-ttu-id="22a70-103">WM \_ queuesync-Meldung</span><span class="sxs-lookup"><span data-stu-id="22a70-103">WM\_QUEUESYNC message</span></span>

<span data-ttu-id="22a70-104">Wird von einer computerbasierten Schulungs Anwendung (CBT) zum Trennen von Benutzereingabe Nachrichten von anderen Nachrichten gesendet, die über die Prozedur " [**WH \_ journalplayback**](about-hooks.md) " gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="22a70-104">Sent by a computer-based training (CBT) application to separate user-input messages from other messages sent through the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure.</span></span>


```C++
#define WM_QUEUESYNC                    0x0023
```



## <a name="parameters"></a><span data-ttu-id="22a70-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="22a70-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a70-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22a70-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22a70-107">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22a70-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="22a70-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22a70-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22a70-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22a70-109">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22a70-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22a70-110">Return value</span></span>

<span data-ttu-id="22a70-111">Typ: **void**</span><span class="sxs-lookup"><span data-stu-id="22a70-111">Type: **void**</span></span>

<span data-ttu-id="22a70-112">Eine CBT-Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="22a70-112">A CBT application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="22a70-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22a70-113">Remarks</span></span>

<span data-ttu-id="22a70-114">Wenn eine CBT-Anwendung die " [**WH \_ journalplayback**](about-hooks.md) "-Prozedur verwendet, sind die erste und die letzte Nachricht **WM \_ queuesync**.</span><span class="sxs-lookup"><span data-stu-id="22a70-114">Whenever a CBT application uses the [**WH\_JOURNALPLAYBACK**](about-hooks.md) procedure, the first and last messages are **WM\_QUEUESYNC**.</span></span> <span data-ttu-id="22a70-115">Dies ermöglicht es der CBT-Anwendung, vom Benutzer initiierte Nachrichten abzufangen und zu untersuchen, ohne dies für Ereignisse zu tun, die Sie sendet.</span><span class="sxs-lookup"><span data-stu-id="22a70-115">This allows the CBT application to intercept and examine user-initiated messages without doing so for events that it sends.</span></span>

<span data-ttu-id="22a70-116">Wenn eine Anwendung ein **null** -Fenster Handle angibt, wird die Meldung in der Nachrichten Warteschlange des aktiven Fensters gepostet.</span><span class="sxs-lookup"><span data-stu-id="22a70-116">If an application specifies a **NULL** window handle, the message is posted to the message queue of the active window.</span></span>

## <a name="requirements"></a><span data-ttu-id="22a70-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22a70-117">Requirements</span></span>



| <span data-ttu-id="22a70-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22a70-118">Requirement</span></span> | <span data-ttu-id="22a70-119">Wert</span><span class="sxs-lookup"><span data-stu-id="22a70-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a70-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22a70-120">Minimum supported client</span></span><br/> | <span data-ttu-id="22a70-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22a70-121">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="22a70-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22a70-122">Minimum supported server</span></span><br/> | <span data-ttu-id="22a70-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22a70-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="22a70-124">Header</span><span class="sxs-lookup"><span data-stu-id="22a70-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="22a70-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="22a70-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22a70-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22a70-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="22a70-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="22a70-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="22a70-128">[*Journalplaybackproc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22a70-128">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="22a70-129">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="22a70-129">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="22a70-130">**Licher**</span><span class="sxs-lookup"><span data-stu-id="22a70-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="22a70-131">Hooks</span><span class="sxs-lookup"><span data-stu-id="22a70-131">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
