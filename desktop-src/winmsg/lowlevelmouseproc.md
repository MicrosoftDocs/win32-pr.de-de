---
UID: ''
title: Lowlevelmousproc-Rückruffunktion
description: Das System ruft diese Funktion jedes Mal auf, wenn ein neues Mauseingabe Ereignis in einer Thread Eingabe Warteschlange gepostet wird.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2020
ms.locfileid: "104039793"
---
# <a name="lowlevelmouseproc-function"></a><span data-ttu-id="cb95e-103">Lowlevelmousproc-Funktion</span><span class="sxs-lookup"><span data-stu-id="cb95e-103">LowLevelMouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="cb95e-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb95e-104">Description</span></span>

<span data-ttu-id="cb95e-105">Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb95e-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="cb95e-106">Das System ruft diese Funktion jedes Mal auf, wenn ein neues Mauseingabe Ereignis in einer Thread Eingabe Warteschlange gepostet wird.</span><span class="sxs-lookup"><span data-stu-id="cb95e-106">The system calls this function every time a new mouse input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="cb95e-107">Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="cb95e-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="cb95e-108">**Lowlevelmouseproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="cb95e-108">**LowLevelMouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="cb95e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb95e-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="cb95e-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="cb95e-110">nCode [in]</span></span>

<span data-ttu-id="cb95e-111">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="cb95e-111">Type: **int**</span></span>

<span data-ttu-id="cb95e-112">Ein Code, den die Hook-Prozedur verwendet, um zu bestimmen, wie die Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="cb95e-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="cb95e-113">Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cb95e-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="cb95e-114">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="cb95e-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="cb95e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cb95e-115">Value</span></span> | <span data-ttu-id="cb95e-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb95e-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="cb95e-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="cb95e-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="cb95e-118">Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Maus Meldung.</span><span class="sxs-lookup"><span data-stu-id="cb95e-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="cb95e-119">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="cb95e-119">wParam [in]</span></span>

<span data-ttu-id="cb95e-120">Typ: **wParam**</span><span class="sxs-lookup"><span data-stu-id="cb95e-120">Type: **WPARAM**</span></span>

<span data-ttu-id="cb95e-121">Der Bezeichner der Maus Nachricht.</span><span class="sxs-lookup"><span data-stu-id="cb95e-121">The identifier of the mouse message.</span></span>
<span data-ttu-id="cb95e-122">Dieser Parameter kann eine der folgenden Meldungen sein: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) oder [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span><span class="sxs-lookup"><span data-stu-id="cb95e-122">This parameter can be one of the following messages: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) or [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="cb95e-123">LParam [in]</span><span class="sxs-lookup"><span data-stu-id="cb95e-123">lParam [in]</span></span>

<span data-ttu-id="cb95e-124">Typ: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="cb95e-124">Type: **LPARAM**</span></span>

<span data-ttu-id="cb95e-125">Ein Zeiger auf eine [msllhuokstruct](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cb95e-125">A pointer to an [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="cb95e-126">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="cb95e-126">Returns</span></span>

<span data-ttu-id="cb95e-127">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="cb95e-127">Type: **LRESULT**</span></span>

<span data-ttu-id="cb95e-128">Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cb95e-128">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="cb95e-129">Wenn *nCode* größer als oder gleich 0 (null) ist und die Hook-Prozedur die Nachricht nicht verarbeitet hat, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_MOUSE_LL](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.</span><span class="sxs-lookup"><span data-stu-id="cb95e-129">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="cb95e-130">Wenn die Hook-Prozedur die Nachricht verarbeitet hat, kann Sie einen Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an den Rest der Hook-Kette oder der Zielfenster Prozedur übergibt.</span><span class="sxs-lookup"><span data-stu-id="cb95e-130">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb95e-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb95e-131">Remarks</span></span>

<span data-ttu-id="cb95e-132">Eine Anwendung installiert die Hook-Prozedur, indem Sie den **WH_MOUSE_LL** Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="cb95e-132">An application installs the hook procedure by specifying the **WH_MOUSE_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="cb95e-133">Dieser Hook wird im Kontext des Threads aufgerufen, der ihn installiert hat.</span><span class="sxs-lookup"><span data-stu-id="cb95e-133">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="cb95e-134">Der-Befehl wird aufgerufen, indem eine Nachricht an den Thread gesendet wird, der den Hook installiert hat.</span><span class="sxs-lookup"><span data-stu-id="cb95e-134">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="cb95e-135">Der Thread, der den Hook installiert hat, muss daher über eine Nachrichten Schleife verfügen.</span><span class="sxs-lookup"><span data-stu-id="cb95e-135">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="cb95e-136">Die Mauseingabe kann aus dem lokalen Mauszeiger oder aus Aufrufen der [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) -Funktion stammen.</span><span class="sxs-lookup"><span data-stu-id="cb95e-136">The mouse input can come from the local mouse driver or from calls to the [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) function.</span></span>
<span data-ttu-id="cb95e-137">Wenn die Eingabe aus einem **mouse_event** aufgerufen wird, wurde die Eingabe "eingefügt".</span><span class="sxs-lookup"><span data-stu-id="cb95e-137">If the input comes from a call to **mouse_event**, the input was "injected".</span></span>
<span data-ttu-id="cb95e-138">Allerdings wird der **WH_MOUSE_LL** Hook nicht in einen anderen Prozess eingefügt.</span><span class="sxs-lookup"><span data-stu-id="cb95e-138">However, the **WH_MOUSE_LL** hook is not injected into another process.</span></span>
<span data-ttu-id="cb95e-139">Stattdessen schaltet der Kontext zum Prozess zurück, der den Hook installiert hat, und wird im ursprünglichen Kontext aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cb95e-139">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="cb95e-140">Anschließend wechselt der Kontext zurück zu der Anwendung, die das Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="cb95e-140">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="cb95e-141">Die Hook-Prozedur sollte eine Nachricht in kürzerer Zeit **als der im** folgenden Registrierungsschlüssel angegebene Dateneintrag verarbeiten: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="cb95e-141">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="cb95e-142">Der Wert ist in Millisekunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="cb95e-142">The value is in milliseconds.</span></span>
<span data-ttu-id="cb95e-143">Wenn für die Hook-Prozedur ein Timeout eintritt, übergibt das System die Nachricht an den nächsten Hook.</span><span class="sxs-lookup"><span data-stu-id="cb95e-143">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="cb95e-144">Allerdings wird der Hook unter Windows 7 und höher automatisch entfernt, ohne aufgerufen zu werden.</span><span class="sxs-lookup"><span data-stu-id="cb95e-144">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="cb95e-145">Es gibt keine Möglichkeit, dass die Anwendung weiß, ob der Hook entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="cb95e-145">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="cb95e-146">**Hinweis:**  Debughooks können diesen Typ von Maus Hooks mit niedriger Ebene nicht verfolgen.</span><span class="sxs-lookup"><span data-stu-id="cb95e-146">**Note:**  Debug hooks cannot track this type of low level mouse hooks.</span></span>
<span data-ttu-id="cb95e-147">Wenn die Anwendung Low-Level-Hooks verwenden muss, sollte Sie die Hooks in einem dedizierten Thread ausführen, der die Arbeit an einen Arbeits Thread übergibt und dann sofort zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="cb95e-147">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="cb95e-148">In den meisten Fällen, in denen die Anwendung Low-Level-Hooks verwenden muss, sollte Sie stattdessen unformatierte Eingaben überwachen.</span><span class="sxs-lookup"><span data-stu-id="cb95e-148">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="cb95e-149">Dies liegt daran, dass die Eingabe von Rohdaten die Maus-und Tastatur Meldungen, die auf andere Threads abzielen, effektiver als auf Low-Level-Hooks abzielen können.</span><span class="sxs-lookup"><span data-stu-id="cb95e-149">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="cb95e-150">Weitere Informationen zur [roheingabe finden](/windows/desktop/inputdev/raw-input)Sie unter unformatierte Eingaben.</span><span class="sxs-lookup"><span data-stu-id="cb95e-150">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="cb95e-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb95e-151">See also</span></span>

[<span data-ttu-id="cb95e-152">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="cb95e-152">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="cb95e-153">mouse_event</span><span class="sxs-lookup"><span data-stu-id="cb95e-153">mouse_event</span></span>](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[<span data-ttu-id="cb95e-154">Kbdlltuokstruct</span><span class="sxs-lookup"><span data-stu-id="cb95e-154">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="cb95e-155">Msllhuokstruct</span><span class="sxs-lookup"><span data-stu-id="cb95e-155">MSLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[<span data-ttu-id="cb95e-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="cb95e-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="cb95e-157">WM_LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="cb95e-157">WM_LBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-lbuttondown)

[<span data-ttu-id="cb95e-158">WM_LBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="cb95e-158">WM_LBUTTONUP</span></span>](/windows/desktop/inputdev/wm-lbuttonup)

[<span data-ttu-id="cb95e-159">WM_MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="cb95e-159">WM_MOUSEMOVE</span></span>](/windows/desktop/inputdev/wm-mousemove)

[<span data-ttu-id="cb95e-160">WM_MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="cb95e-160">WM_MOUSEWHEEL</span></span>](/windows/desktop/inputdev/wm-mousewheel)

[<span data-ttu-id="cb95e-161">WM_RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="cb95e-161">WM_RBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-rbuttondown)

[<span data-ttu-id="cb95e-162">WM_RBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="cb95e-162">WM_RBUTTONUP</span></span>](/windows/desktop/inputdev/wm-rbuttonup)

[<span data-ttu-id="cb95e-163">Hooks</span><span class="sxs-lookup"><span data-stu-id="cb95e-163">Hooks</span></span>](hooks.md)

[<span data-ttu-id="cb95e-164">Informationen zu Hooks</span><span class="sxs-lookup"><span data-stu-id="cb95e-164">About Hooks</span></span>](about-hooks.md)
