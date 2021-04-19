---
description: Wird an eine Anwendung gesendet, wenn ein Benutzer die journalingaktivitäten der Anwendung abbricht. Die Nachricht wird mit einem NULL-Fenster Handle gepostet.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: WM_CANCELJOURNAL Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350341"
---
# <a name="wm_canceljournal-message"></a><span data-ttu-id="a63e8-104">WM \_ canceljournal-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a63e8-104">WM\_CANCELJOURNAL message</span></span>

<span data-ttu-id="a63e8-105">Wird an eine Anwendung gesendet, wenn ein Benutzer die journalingaktivitäten der Anwendung abbricht.</span><span class="sxs-lookup"><span data-stu-id="a63e8-105">Posted to an application when a user cancels the application's journaling activities.</span></span> <span data-ttu-id="a63e8-106">Die Nachricht wird mit einem **null** -Fenster Handle gepostet.</span><span class="sxs-lookup"><span data-stu-id="a63e8-106">The message is posted with a **NULL** window handle.</span></span>


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a><span data-ttu-id="a63e8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a63e8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a63e8-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a63e8-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a63e8-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a63e8-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="a63e8-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a63e8-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a63e8-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a63e8-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a63e8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a63e8-112">Return value</span></span>

<span data-ttu-id="a63e8-113">Typ: **void**</span><span class="sxs-lookup"><span data-stu-id="a63e8-113">Type: **void**</span></span>

<span data-ttu-id="a63e8-114">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a63e8-114">This message does not return a value.</span></span> <span data-ttu-id="a63e8-115">Sie soll aus einer-Hauptschleife einer Anwendung oder einer [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Hook-Prozedur, nicht aus einer Fenster Prozedur verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a63e8-115">It is meant to be processed from within an application's main loop or a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) hook procedure, not from a window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a63e8-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a63e8-116">Remarks</span></span>

<span data-ttu-id="a63e8-117">Journal Daten Satz-und Wiedergabe Modi sind Modi, die auf dem System angewendet werden, mit denen eine Anwendung die Benutzereingaben sequenziell aufzeichnen oder wiedergeben können.</span><span class="sxs-lookup"><span data-stu-id="a63e8-117">Journal record and playback modes are modes imposed on the system that let an application sequentially record or play back user input.</span></span> <span data-ttu-id="a63e8-118">Das System gibt diese Modi ein, wenn eine Anwendung eine [*journalrecordproc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) -oder [*journalplaybackproc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) -Hook-Prozedur installiert.</span><span class="sxs-lookup"><span data-stu-id="a63e8-118">The system enters these modes when an application installs a [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) or [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) hook procedure.</span></span> <span data-ttu-id="a63e8-119">Wenn sich das System in einem dieser Journalmodi befindet, müssen Anwendungen das Lesen von Eingaben aus der Eingabe Warteschlange durchführen.</span><span class="sxs-lookup"><span data-stu-id="a63e8-119">When the system is in either of these journaling modes, applications must take turns reading input from the input queue.</span></span> <span data-ttu-id="a63e8-120">Wenn eine Anwendung das Lesen von Eingaben beendet, während sich das System in einem journalingmodus befindet, wird die Wartezeit für andere Anwendungen erzwungen.</span><span class="sxs-lookup"><span data-stu-id="a63e8-120">If any one application stops reading input while the system is in a journaling mode, other applications are forced to wait.</span></span>

<span data-ttu-id="a63e8-121">Um ein robustes System zu gewährleisten, das nicht von einer Anwendung als nicht reaktionsfähig festgestellt werden kann, bricht das System automatisch alle journalaktivitäten ab, wenn ein Benutzer STRG + ESC oder STRG + ALT + ENTF drückt.</span><span class="sxs-lookup"><span data-stu-id="a63e8-121">To ensure a robust system, one that cannot be made unresponsive by any one application, the system automatically cancels any journaling activities when a user presses CTRL+ESC or CTRL+ALT+DEL.</span></span> <span data-ttu-id="a63e8-122">Das System entbindet dann alle Journalen Hook-Prozeduren und sendet eine **WM \_ canceljournal** -Nachricht mit einem **null** -Fenster Handle an die Anwendung, die den Journal Hook festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="a63e8-122">The system then unhooks any journaling hook procedures, and posts a **WM\_CANCELJOURNAL** message, with a **NULL** window handle, to the application that set the journaling hook.</span></span>

<span data-ttu-id="a63e8-123">Die **WM \_ canceljournal** -Nachricht weist ein Fenster Handle mit dem Wert **null** auf und kann daher nicht an eine Fenster Prozedur weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a63e8-123">The **WM\_CANCELJOURNAL** message has a **NULL** window handle, therefore it cannot be dispatched to a window procedure.</span></span> <span data-ttu-id="a63e8-124">Es gibt zwei Möglichkeiten für eine Anwendung, eine **WM \_ canceljournal** -Nachricht anzuzeigen: Wenn die Anwendung in einer eigenen Hauptschleife ausgeführt wird, muss Sie die Nachricht zwischen dem Aufrufen von [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) oder der [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Nachricht und dem Aufrufen von [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)abfangen.</span><span class="sxs-lookup"><span data-stu-id="a63e8-124">There are two ways for an application to see a **WM\_CANCELJOURNAL** message: If the application is running in its own main loop, it must catch the message between its call to [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) and its call to [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span></span> <span data-ttu-id="a63e8-125">Wenn die Anwendung nicht in einer eigenen Hauptschleife ausgeführt wird, muss Sie eine [*getmsgproc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) -Hook-Prozedur festlegen (durch Aufrufen von [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) , die den Typ " **WH \_ GetMessage** Hook" angibt), der die Nachricht überwacht.</span><span class="sxs-lookup"><span data-stu-id="a63e8-125">If the application is not running in its own main loop, it must set a [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) hook procedure (through a call to [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) specifying the **WH\_GETMESSAGE** hook type) that watches for the message.</span></span>

<span data-ttu-id="a63e8-126">Wenn eine Anwendung eine **WM- \_ canceljournal** -Nachricht sieht, kann Sie zwei Dinge annehmen: der Benutzer hat den Journal Daten Satz oder den Wiedergabemodus absichtlich abgebrochen, und das System hat bereits alle Journal Datensätze oder Wiedergabe-Hook-Prozeduren nicht eingebunden.</span><span class="sxs-lookup"><span data-stu-id="a63e8-126">When an application sees a **WM\_CANCELJOURNAL** message, it can assume two things: the user has intentionally canceled the journal record or playback mode, and the system has already unhooked any journal record or playback hook procedures.</span></span>

<span data-ttu-id="a63e8-127">Beachten Sie, dass die oben erwähnten Tastenkombinationen (STRG + ESC oder STRG + ALT + ENTF) bewirken, dass das System Journal Vorgang abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="a63e8-127">Note that the key combinations mentioned above (CTRL+ESC or CTRL+ALT+DEL) cause the system to cancel journaling.</span></span> <span data-ttu-id="a63e8-128">Wenn eine Anwendung nicht mehr reagiert, können Sie dem Benutzer eine Möglichkeit zur Wiederherstellung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="a63e8-128">If any one application is made unresponsive, they give the user a means of recovery.</span></span> <span data-ttu-id="a63e8-129">Der Code der virtuellen Taste für den [**VK \_**](../inputdev/virtual-key-codes.md) -Abbruch (in der Regel als STRG + UNTBR-Tastenkombination implementiert) ist das, was eine Anwendung, die sich im Journal Daten Satz Modus befindet, als Signal ansehen soll, dass der Benutzer die Journal Aktivität abbrechen möchte.</span><span class="sxs-lookup"><span data-stu-id="a63e8-129">The [**VK\_CANCEL**](../inputdev/virtual-key-codes.md) virtual key code (usually implemented as the CTRL+BREAK key combination) is what an application that is in journal record mode should watch for as a signal that the user wishes to cancel the journaling activity.</span></span> <span data-ttu-id="a63e8-130">Der Unterschied besteht darin, dass das Überwachen von **VK \_ Cancel** ein empfohlenes Verhalten für das journalisieren von Anwendungen ist, während STRG + ESC oder STRG + ALT + ENTF bewirkt, dass das System das Journal Vorgang unabhängig vom Verhalten einer Journalen Anwendung abbricht.</span><span class="sxs-lookup"><span data-stu-id="a63e8-130">The difference is that watching for **VK\_CANCEL** is a suggested behavior for journaling applications, whereas CTRL+ESC or CTRL+ALT+DEL cause the system to cancel journaling regardless of a journaling application's behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="a63e8-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a63e8-131">Requirements</span></span>



| <span data-ttu-id="a63e8-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a63e8-132">Requirement</span></span> | <span data-ttu-id="a63e8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="a63e8-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a63e8-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a63e8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a63e8-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a63e8-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a63e8-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a63e8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a63e8-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a63e8-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a63e8-138">Header</span><span class="sxs-lookup"><span data-stu-id="a63e8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a63e8-139"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="a63e8-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a63e8-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a63e8-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="a63e8-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a63e8-141">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="a63e8-142">[*Journalplaybackproc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a63e8-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a63e8-143">[*Journalrecordproc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a63e8-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a63e8-144">[*Getmsgproc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a63e8-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a63e8-145">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="a63e8-145">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="a63e8-146">**Licher**</span><span class="sxs-lookup"><span data-stu-id="a63e8-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a63e8-147">Hooks</span><span class="sxs-lookup"><span data-stu-id="a63e8-147">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
