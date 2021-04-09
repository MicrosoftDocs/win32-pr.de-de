---
UID: ''
title: LowLevelKeyboardProc-Rückruffunktion
description: Das System ruft diese Funktion jedes Mal auf, wenn ein neues Tastatureingabe Ereignis in einer Thread Eingabe Warteschlange gepostet wird.
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
ms.openlocfilehash: f33acbb6888bad97a03b610c513cbaf9c3750684
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "104038712"
---
# <a name="lowlevelkeyboardproc-function"></a><span data-ttu-id="55e6a-103">LowLevelKeyboardProc-Funktion</span><span class="sxs-lookup"><span data-stu-id="55e6a-103">LowLevelKeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="55e6a-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55e6a-104">Description</span></span>

<span data-ttu-id="55e6a-105">Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="55e6a-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="55e6a-106">Das System ruft diese Funktion jedes Mal auf, wenn ein neues Tastatureingabe Ereignis in einer Thread Eingabe Warteschlange gepostet wird.</span><span class="sxs-lookup"><span data-stu-id="55e6a-106">The system calls this function every time a new keyboard input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="55e6a-107">**Hinweis:**  Wenn diese Rückruffunktion als Reaktion auf eine Änderung des Zustands eines Schlüssels aufgerufen wird, wird die Rückruffunktion aufgerufen, bevor der asynchrone Zustand des Schlüssels aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="55e6a-107">**Note:**  When this callback function is called in response to a change in the state of a key, the callback function is called before the asynchronous state of the key is updated.</span></span>
<span data-ttu-id="55e6a-108">Folglich kann der asynchrone Zustand des Schlüssels nicht durch Aufrufen von [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) innerhalb der Rückruffunktion bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="55e6a-108">Consequently, the asynchronous state of the key cannot be determined by calling [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) from within the callback function.</span></span>

<span data-ttu-id="55e6a-109">Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="55e6a-109">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="55e6a-110">**LowLevelKeyboardProc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="55e6a-110">**LowLevelKeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="55e6a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="55e6a-111">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="55e6a-112">Code [in]</span><span class="sxs-lookup"><span data-stu-id="55e6a-112">code [in]</span></span>

<span data-ttu-id="55e6a-113">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="55e6a-113">Type: **int**</span></span>

<span data-ttu-id="55e6a-114">Ein Code, den die Hook-Prozedur verwendet, um zu bestimmen, wie die Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="55e6a-114">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="55e6a-115">Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="55e6a-115">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="55e6a-116">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="55e6a-116">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="55e6a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="55e6a-117">Value</span></span> | <span data-ttu-id="55e6a-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="55e6a-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="55e6a-119">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="55e6a-119">**HC_ACTION** 0</span></span> | <span data-ttu-id="55e6a-120">Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Tastatur Meldung.</span><span class="sxs-lookup"><span data-stu-id="55e6a-120">The *wParam* and *lParam* parameters contain information about a keyboard message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="55e6a-121">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="55e6a-121">wParam [in]</span></span>

<span data-ttu-id="55e6a-122">Typ: **wParam**</span><span class="sxs-lookup"><span data-stu-id="55e6a-122">Type: **WPARAM**</span></span>

<span data-ttu-id="55e6a-123">Der Bezeichner der Tastatur Meldung.</span><span class="sxs-lookup"><span data-stu-id="55e6a-123">The identifier of the keyboard message.</span></span>
<span data-ttu-id="55e6a-124">Dieser Parameter kann eine der folgenden Meldungen sein: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)oder [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span><span class="sxs-lookup"><span data-stu-id="55e6a-124">This parameter can be one of the following messages: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown), or [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="55e6a-125">LParam [in]</span><span class="sxs-lookup"><span data-stu-id="55e6a-125">lParam [in]</span></span>

<span data-ttu-id="55e6a-126">Typ: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="55e6a-126">Type: **LPARAM**</span></span>

<span data-ttu-id="55e6a-127">Ein Zeiger auf eine [kbdllhuokstruct](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="55e6a-127">A pointer to a [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="55e6a-128">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="55e6a-128">Returns</span></span>

<span data-ttu-id="55e6a-129">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="55e6a-129">Type: **LRESULT**</span></span>

<span data-ttu-id="55e6a-130">Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="55e6a-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="55e6a-131">Wenn *nCode* größer als oder gleich 0 (null) ist und die Hook-Prozedur die Nachricht nicht verarbeitet hat, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_KEYBOARD_LL](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.</span><span class="sxs-lookup"><span data-stu-id="55e6a-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="55e6a-132">Wenn die Hook-Prozedur die Nachricht verarbeitet hat, kann Sie einen Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an den Rest der Hook-Kette oder der Zielfenster Prozedur übergibt.</span><span class="sxs-lookup"><span data-stu-id="55e6a-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="55e6a-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55e6a-133">Remarks</span></span>

<span data-ttu-id="55e6a-134">Eine Anwendung installiert die Hook-Prozedur, indem Sie den **WH_KEYBOARD_LL** Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="55e6a-134">An application installs the hook procedure by specifying the **WH_KEYBOARD_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="55e6a-135">Dieser Hook wird im Kontext des Threads aufgerufen, der ihn installiert hat.</span><span class="sxs-lookup"><span data-stu-id="55e6a-135">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="55e6a-136">Der-Befehl wird aufgerufen, indem eine Nachricht an den Thread gesendet wird, der den Hook installiert hat.</span><span class="sxs-lookup"><span data-stu-id="55e6a-136">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="55e6a-137">Der Thread, der den Hook installiert hat, muss daher über eine Nachrichten Schleife verfügen.</span><span class="sxs-lookup"><span data-stu-id="55e6a-137">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="55e6a-138">Die Tastatureingabe kann aus dem lokalen Tastaturtreiber oder aus Aufrufen der [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) -Funktion stammen.</span><span class="sxs-lookup"><span data-stu-id="55e6a-138">The keyboard input can come from the local keyboard driver or from calls to the [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) function.</span></span>
<span data-ttu-id="55e6a-139">Wenn die Eingabe aus einem **keybd_event** aufgerufen wird, wurde die Eingabe "eingefügt".</span><span class="sxs-lookup"><span data-stu-id="55e6a-139">If the input comes from a call to **keybd_event**, the input was "injected".</span></span>
<span data-ttu-id="55e6a-140">Allerdings wird der WH_KEYBOARD_LL Hook nicht in einen anderen Prozess eingefügt.</span><span class="sxs-lookup"><span data-stu-id="55e6a-140">However, the WH_KEYBOARD_LL hook is not injected into another process.</span></span>
<span data-ttu-id="55e6a-141">Stattdessen schaltet der Kontext zum Prozess zurück, der den Hook installiert hat, und wird im ursprünglichen Kontext aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="55e6a-141">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="55e6a-142">Anschließend wechselt der Kontext zurück zu der Anwendung, die das Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="55e6a-142">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="55e6a-143">Die Hook-Prozedur sollte eine Nachricht in kürzerer Zeit **als der im** folgenden Registrierungsschlüssel angegebene Dateneintrag verarbeiten: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="55e6a-143">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="55e6a-144">Der Wert ist in Millisekunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="55e6a-144">The value is in milliseconds.</span></span>
<span data-ttu-id="55e6a-145">Wenn für die Hook-Prozedur ein Timeout eintritt, übergibt das System die Nachricht an den nächsten Hook.</span><span class="sxs-lookup"><span data-stu-id="55e6a-145">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="55e6a-146">Allerdings wird der Hook unter Windows 7 und höher automatisch entfernt, ohne aufgerufen zu werden.</span><span class="sxs-lookup"><span data-stu-id="55e6a-146">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="55e6a-147">Es gibt keine Möglichkeit, dass die Anwendung weiß, ob der Hook entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="55e6a-147">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="55e6a-148">Hinweis: debughooks können diese Art von Tastatur Hooks auf niedriger Ebene nicht verfolgen.</span><span class="sxs-lookup"><span data-stu-id="55e6a-148">Note:  Debug hooks cannot track this type of low level keyboard hooks.</span></span>
<span data-ttu-id="55e6a-149">Wenn die Anwendung Low-Level-Hooks verwenden muss, sollte Sie die Hooks in einem dedizierten Thread ausführen, der die Arbeit an einen Arbeits Thread übergibt und dann sofort zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="55e6a-149">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="55e6a-150">In den meisten Fällen, in denen die Anwendung Low-Level-Hooks verwenden muss, sollte Sie stattdessen unformatierte Eingaben überwachen.</span><span class="sxs-lookup"><span data-stu-id="55e6a-150">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="55e6a-151">Dies liegt daran, dass die Eingabe von Rohdaten die Maus-und Tastatur Meldungen, die auf andere Threads abzielen, effektiver als auf Low-Level-Hooks abzielen können.</span><span class="sxs-lookup"><span data-stu-id="55e6a-151">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="55e6a-152">Weitere Informationen zur [roheingabe finden](/windows/desktop/inputdev/raw-input)Sie unter unformatierte Eingaben.</span><span class="sxs-lookup"><span data-stu-id="55e6a-152">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="55e6a-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55e6a-153">See also</span></span>

[<span data-ttu-id="55e6a-154">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="55e6a-154">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="55e6a-155">Kbdlltuokstruct</span><span class="sxs-lookup"><span data-stu-id="55e6a-155">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="55e6a-156">keybd_event</span><span class="sxs-lookup"><span data-stu-id="55e6a-156">keybd_event</span></span>](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[<span data-ttu-id="55e6a-157">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="55e6a-157">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="55e6a-158">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="55e6a-158">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="55e6a-159">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="55e6a-159">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="55e6a-160">WM_SYSKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="55e6a-160">WM_SYSKEYDOWN</span></span>](/windows/desktop/inputdev/wm-syskeydown)

[<span data-ttu-id="55e6a-161">WM_SYSKEYUP</span><span class="sxs-lookup"><span data-stu-id="55e6a-161">WM_SYSKEYUP</span></span>](/windows/desktop/inputdev/wm-syskeyup)

[<span data-ttu-id="55e6a-162">Hooks</span><span class="sxs-lookup"><span data-stu-id="55e6a-162">Hooks</span></span>](hooks.md)

[<span data-ttu-id="55e6a-163">Informationen zu Hooks</span><span class="sxs-lookup"><span data-stu-id="55e6a-163">About Hooks</span></span>](about-hooks.md)
