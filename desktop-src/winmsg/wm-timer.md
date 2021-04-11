---
description: Wird in der Meldungs Warteschlange des Installations Threads gepostet, wenn ein Timer abläuft. Die Nachricht wird von der getMessage-Funktion oder der Peer Message-Funktion gepostet.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: WM_TIMER Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c99db67c9c9b3419e477ccd0a78133df453a7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217512"
---
# <a name="wm_timer-message"></a><span data-ttu-id="6f8ee-104">WM-Zeit Geber \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="6f8ee-104">WM\_TIMER message</span></span>

<span data-ttu-id="6f8ee-105">Wird in der Meldungs Warteschlange des Installations Threads gepostet, wenn ein Timer abläuft.</span><span class="sxs-lookup"><span data-stu-id="6f8ee-105">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="6f8ee-106">Die Nachricht wird von der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion oder der [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Funktion gepostet.</span><span class="sxs-lookup"><span data-stu-id="6f8ee-106">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span>


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a><span data-ttu-id="6f8ee-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f8ee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f8ee-108">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f8ee-108">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f8ee-109">Der timerbezeichner.</span><span class="sxs-lookup"><span data-stu-id="6f8ee-109">The timer identifier.</span></span>

</dd> <dt>

<span data-ttu-id="6f8ee-110">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f8ee-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f8ee-111">Ein Zeiger auf eine Anwendungs definierte Rückruffunktion, die bei der Installation des Timers an die [**SETTIMER**](/windows/win32/api/winuser/nf-winuser-settimer) -Funktion übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="6f8ee-111">A pointer to an application-defined callback function that was passed to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function when the timer was installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f8ee-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f8ee-112">Return value</span></span>

<span data-ttu-id="6f8ee-113">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6f8ee-113">Type: **LRESULT**</span></span>

<span data-ttu-id="6f8ee-114">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="6f8ee-114">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f8ee-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f8ee-115">Remarks</span></span>

<span data-ttu-id="6f8ee-116">Sie können die Nachricht verarbeiten, indem Sie **einen \_ WM** -Zeit Geber Fall in der Fenster Prozedur bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6f8ee-116">You can process the message by providing a **WM\_TIMER** case in the window procedure.</span></span> <span data-ttu-id="6f8ee-117">Andernfalls ruft [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) die [*timerproc*](/windows/win32/api/winuser/nc-winuser-timerproc) -Rückruffunktion auf, die im [**Aufrufen der Funktion "-Funktion"**](/windows/win32/api/winuser/nf-winuser-settimer) angegeben ist, die zum Installieren des Timers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f8ee-117">Otherwise, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) will call the [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) callback function specified in the call to the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function used to install the timer.</span></span>

<span data-ttu-id="6f8ee-118">Die WM-Zeit Geber Nachricht ist eine Nachricht mit niedriger Priorität. **\_**</span><span class="sxs-lookup"><span data-stu-id="6f8ee-118">The **WM\_TIMER** message is a low-priority message.</span></span> <span data-ttu-id="6f8ee-119">Die Funktionen [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) und [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) stellen diese Nachricht nur dann bereit, wenn sich keine anderen Nachrichten mit höherer Priorität in der Nachrichten Warteschlange des Threads befinden.</span><span class="sxs-lookup"><span data-stu-id="6f8ee-119">The [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) functions post this message only when no other higher-priority messages are in the thread's message queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f8ee-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f8ee-120">Requirements</span></span>



| <span data-ttu-id="6f8ee-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f8ee-121">Requirement</span></span> | <span data-ttu-id="6f8ee-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6f8ee-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f8ee-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f8ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6f8ee-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f8ee-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6f8ee-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f8ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6f8ee-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f8ee-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6f8ee-127">Header</span><span class="sxs-lookup"><span data-stu-id="6f8ee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f8ee-128"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6f8ee-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f8ee-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f8ee-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="6f8ee-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6f8ee-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6f8ee-131">**GetMessage**</span><span class="sxs-lookup"><span data-stu-id="6f8ee-131">**GetMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[<span data-ttu-id="6f8ee-132">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="6f8ee-132">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[<span data-ttu-id="6f8ee-133">**Ziel**</span><span class="sxs-lookup"><span data-stu-id="6f8ee-133">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[<span data-ttu-id="6f8ee-134">**Timerproc**</span><span class="sxs-lookup"><span data-stu-id="6f8ee-134">**TimerProc**</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

<span data-ttu-id="6f8ee-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="6f8ee-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6f8ee-136">Timer</span><span class="sxs-lookup"><span data-stu-id="6f8ee-136">Timers</span></span>](timers.md)
</dt> </dl>

 

 
