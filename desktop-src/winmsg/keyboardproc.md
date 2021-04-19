---
UID: ''
title: Keyboardproc-Rückruffunktion
description: Das System ruft diese Funktion auf und ruft eine Message-Funktion ab, und es gibt eine zu verarbeitende Tastatur Meldung.
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
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "106342122"
---
# <a name="keyboardproc-function"></a><span data-ttu-id="5abef-103">Keyboardproc-Funktion</span><span class="sxs-lookup"><span data-stu-id="5abef-103">KeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="5abef-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5abef-104">Description</span></span>

<span data-ttu-id="5abef-105">Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5abef-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="5abef-106">Das System ruft diese Funktion immer dann auf, wenn eine Anwendung die [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) -oder die [Peer Message](/windows/desktop/api/winuser/nf-winuser-peekmessagew) -Funktion aufruft und eine Tastatur Meldung ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) oder [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) zur Verarbeitung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5abef-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a keyboard message ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) or [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) to be processed.</span></span>

<span data-ttu-id="5abef-107">Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="5abef-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="5abef-108">**Keyboardproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="5abef-108">**KeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="5abef-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5abef-109">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="5abef-110">Code [in]</span><span class="sxs-lookup"><span data-stu-id="5abef-110">code [in]</span></span>

<span data-ttu-id="5abef-111">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="5abef-111">Type: **int**</span></span>

<span data-ttu-id="5abef-112">Ein Code, den die Hook-Prozedur verwendet, um zu bestimmen, wie die Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5abef-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="5abef-113">Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5abef-113">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="5abef-114">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="5abef-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="5abef-115">Wert</span><span class="sxs-lookup"><span data-stu-id="5abef-115">Value</span></span> | <span data-ttu-id="5abef-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5abef-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="5abef-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="5abef-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="5abef-118">Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Tastatureingabe-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5abef-118">The *wParam* and *lParam* parameters contain information about a keystroke message.</span></span> |
| <span data-ttu-id="5abef-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="5abef-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="5abef-120">Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Tastatureingabe-Nachricht, und die Tastatureingabe-Nachricht wurde nicht aus der Nachrichten Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="5abef-120">The *wParam* and *lParam* parameters contain information about a keystroke message, and the keystroke message has not been removed from the message queue.</span></span> <span data-ttu-id="5abef-121">(Eine Anwendung, die die Funktion " **Peer Message** " genannt wird und das **PM_NOREMOVE** Flag angibt.)</span><span class="sxs-lookup"><span data-stu-id="5abef-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="5abef-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="5abef-122">wParam [in]</span></span>

<span data-ttu-id="5abef-123">Typ: **wParam**</span><span class="sxs-lookup"><span data-stu-id="5abef-123">Type: **WPARAM**</span></span>

<span data-ttu-id="5abef-124">Der [Code](/windows/desktop/inputdev/virtual-key-codes) für den virtuellen Schlüssel des Schlüssels, der die Tastatureingabe-Nachricht generiert hat.</span><span class="sxs-lookup"><span data-stu-id="5abef-124">The [virtual-key code](/windows/desktop/inputdev/virtual-key-codes) of the key that generated the keystroke message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="5abef-125">LParam [in]</span><span class="sxs-lookup"><span data-stu-id="5abef-125">lParam [in]</span></span>

<span data-ttu-id="5abef-126">Typ: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="5abef-126">Type: **LPARAM**</span></span>

<span data-ttu-id="5abef-127">Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das transitionstate-Flag.</span><span class="sxs-lookup"><span data-stu-id="5abef-127">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span>
<span data-ttu-id="5abef-128">Weitere Informationen zum *LPARAM* -Parameter finden Sie unter [KeyStroke-Nachrichtenflags](/windows/desktop/inputdev/about-keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="5abef-128">For more information about The *lParam* parameter, see [Keystroke Message Flags](/windows/desktop/inputdev/about-keyboard-input).</span></span>
<span data-ttu-id="5abef-129">In der folgenden Tabelle werden die Bits dieses Werts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5abef-129">The following table describes the bits of this value.</span></span>

| <span data-ttu-id="5abef-130">Bits</span><span class="sxs-lookup"><span data-stu-id="5abef-130">Bits</span></span> | <span data-ttu-id="5abef-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5abef-131">Description</span></span> |
|-------|---------|
| <span data-ttu-id="5abef-132">0-15</span><span class="sxs-lookup"><span data-stu-id="5abef-132">0-15</span></span> | <span data-ttu-id="5abef-133">Die Wiederholungs Anzahl.</span><span class="sxs-lookup"><span data-stu-id="5abef-133">The repeat count.</span></span> <span data-ttu-id="5abef-134">Der Wert gibt an, wie oft der Tastatur Schlag wiederholt wird, wenn der Benutzer die Taste gedrückt hält.</span><span class="sxs-lookup"><span data-stu-id="5abef-134">The value is the number of times the keystroke is repeated as a result of the user's holding down the key.</span></span> |
| <span data-ttu-id="5abef-135">16-23</span><span class="sxs-lookup"><span data-stu-id="5abef-135">16-23</span></span> | <span data-ttu-id="5abef-136">Der Überprüfungs Code.</span><span class="sxs-lookup"><span data-stu-id="5abef-136">The scan code.</span></span> <span data-ttu-id="5abef-137">Der Wert hängt vom OEM ab.</span><span class="sxs-lookup"><span data-stu-id="5abef-137">The value depends on the OEM.</span></span> |
| <span data-ttu-id="5abef-138">24</span><span class="sxs-lookup"><span data-stu-id="5abef-138">24</span></span> | <span data-ttu-id="5abef-139">Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. ein Funktionsschlüssel oder ein Schlüssel auf der numerischen Keypad.</span><span class="sxs-lookup"><span data-stu-id="5abef-139">Indicates whether the key is an extended key, such as a function key or a key on the numeric keypad.</span></span> <span data-ttu-id="5abef-140">Der Wert ist 1, wenn der Schlüssel ein erweiterter Schlüssel ist. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="5abef-140">The value is 1 if the key is an extended key; otherwise, it is 0.</span></span> |
| <span data-ttu-id="5abef-141">25-28</span><span class="sxs-lookup"><span data-stu-id="5abef-141">25-28</span></span> | <span data-ttu-id="5abef-142">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="5abef-142">Reserved.</span></span> |
| <span data-ttu-id="5abef-143">29</span><span class="sxs-lookup"><span data-stu-id="5abef-143">29</span></span> | <span data-ttu-id="5abef-144">Der Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="5abef-144">The context code.</span></span> <span data-ttu-id="5abef-145">Der Wert ist 1, wenn die Alt-Taste gedrückt ist. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="5abef-145">The value is 1 if the ALT key is down; otherwise, it is 0.</span></span> |
| <span data-ttu-id="5abef-146">30</span><span class="sxs-lookup"><span data-stu-id="5abef-146">30</span></span> | <span data-ttu-id="5abef-147">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="5abef-147">The previous key state.</span></span> <span data-ttu-id="5abef-148">Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird. der Wert ist 0 (null), wenn der Schlüssel aktuell ist.</span><span class="sxs-lookup"><span data-stu-id="5abef-148">The value is 1 if the key is down before the message is sent; it is 0 if the key is up.</span></span> |
| <span data-ttu-id="5abef-149">31</span><span class="sxs-lookup"><span data-stu-id="5abef-149">31</span></span> | <span data-ttu-id="5abef-150">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="5abef-150">The transition state.</span></span> <span data-ttu-id="5abef-151">Der Wert ist 0 (null), wenn der Schlüssel gedrückt wird, und 1, wenn er freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5abef-151">The value is 0 if the key is being pressed and 1 if it is being released.</span></span> |

## <a name="returns"></a><span data-ttu-id="5abef-152">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="5abef-152">Returns</span></span>

<span data-ttu-id="5abef-153">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5abef-153">Type: **LRESULT**</span></span>

<span data-ttu-id="5abef-154">Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5abef-154">If *code* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="5abef-155">Wenn *Code* größer oder gleich 0 (null) ist und die Hook-Prozedur die Nachricht nicht verarbeitet hat, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_KEYBOARD](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.</span><span class="sxs-lookup"><span data-stu-id="5abef-155">If *code* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="5abef-156">Wenn die Hook-Prozedur die Nachricht verarbeitet hat, kann Sie einen Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an den Rest der Hook-Kette oder der Zielfenster Prozedur übergibt.</span><span class="sxs-lookup"><span data-stu-id="5abef-156">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="5abef-157">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5abef-157">Remarks</span></span>

<span data-ttu-id="5abef-158">Eine Anwendung installiert die Hook-Prozedur, indem Sie den **WH_KEYBOARD** Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="5abef-158">An application installs the hook procedure by specifying the **WH_KEYBOARD** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="5abef-159">Dieser Hook kann im Kontext des Threads aufgerufen werden, der ihn installiert hat.</span><span class="sxs-lookup"><span data-stu-id="5abef-159">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="5abef-160">Der-Befehl wird aufgerufen, indem eine Nachricht an den Thread gesendet wird, der den Hook installiert hat.</span><span class="sxs-lookup"><span data-stu-id="5abef-160">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="5abef-161">Der Thread, der den Hook installiert hat, muss daher über eine Nachrichten Schleife verfügen.</span><span class="sxs-lookup"><span data-stu-id="5abef-161">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="5abef-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5abef-162">See also</span></span>

[<span data-ttu-id="5abef-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="5abef-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="5abef-164">GetMessage</span><span class="sxs-lookup"><span data-stu-id="5abef-164">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="5abef-165">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="5abef-165">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="5abef-166">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="5abef-166">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="5abef-167">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="5abef-167">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="5abef-168">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="5abef-168">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="5abef-169">Hooks</span><span class="sxs-lookup"><span data-stu-id="5abef-169">Hooks</span></span>](hooks.md)
