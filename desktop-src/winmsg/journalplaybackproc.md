---
UID: ''
title: Journalplaybackproc-Rückruffunktion
description: Gibt eine Reihe von Maus-und Tastatur Meldungen wieder, die zuvor aufgezeichnet wurden.
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
ms.openlocfilehash: 9bceede3cd6ab009aace4679dfb3d4d85bd37276
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "104390107"
---
# <a name="journalplaybackproc-function"></a><span data-ttu-id="5fbaa-103">Journalplaybackproc-Funktion</span><span class="sxs-lookup"><span data-stu-id="5fbaa-103">JournalPlaybackProc function</span></span>

## <a name="description"></a><span data-ttu-id="5fbaa-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fbaa-104">Description</span></span>

<span data-ttu-id="5fbaa-105">Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="5fbaa-106">In der Regel verwendet eine Anwendung diese Funktion, um eine Reihe von Maus-und Tastatur Meldungen wiederzugeben, die zuvor von der **journalrecordproc** -Hook-Prozedur aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-106">Typically, an application uses this function to play back a series of mouse and keyboard messages recorded previously by the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="5fbaa-107">Solange eine **journalplaybackproc** -Hook-Prozedur installiert ist, sind normale Maus-und Tastatureingaben deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-107">As long as a **JournalPlaybackProc** hook procedure is installed, regular mouse and keyboard input is disabled.</span></span>

<span data-ttu-id="5fbaa-108">Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="5fbaa-109">**Journalplaybackproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-109">**JournalPlaybackProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="5fbaa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fbaa-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="5fbaa-111">Code [in]</span><span class="sxs-lookup"><span data-stu-id="5fbaa-111">code [in]</span></span>

<span data-ttu-id="5fbaa-112">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="5fbaa-112">Type: **int**</span></span>

<span data-ttu-id="5fbaa-113">Ein Code, den die Hook-Prozedur verwendet, um zu bestimmen, wie die Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-113">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="5fbaa-114">Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="5fbaa-115">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="5fbaa-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5fbaa-116">Value</span></span> | <span data-ttu-id="5fbaa-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5fbaa-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="5fbaa-118">**HC_GETNEXT** 1</span><span class="sxs-lookup"><span data-stu-id="5fbaa-118">**HC_GETNEXT** 1</span></span> | <span data-ttu-id="5fbaa-119">Die Hook-Prozedur muss die aktuelle Maus-oder Tastatur Nachricht in die [eventmsg](/windows/desktop/api/winuser/ns-winuser-eventmsg) -Struktur kopieren, auf die durch den *LPARAM* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-119">The hook procedure must copy the current mouse or keyboard message to the [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure pointed to by the *lParam* parameter.</span></span> |
| <span data-ttu-id="5fbaa-120">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="5fbaa-120">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="5fbaa-121">Eine Anwendung hat die Funktion " [Peer Message](/windows/desktop/api/winuser/nf-winuser-peekmessagew) " aufgerufen, wobei "wremovemsg" auf " **PM_NOREMOVE**" festgelegt ist. Dies deutet darauf hin, dass die **Nachricht nach der** Verarbeitung der Verarbeitung nicht aus der Nachrichten Warteschlange</span><span class="sxs-lookup"><span data-stu-id="5fbaa-121">An application has called the [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function with wRemoveMsg set to **PM_NOREMOVE**, indicating that the message is not removed from the message queue after **PeekMessage** processing.</span></span> |
| <span data-ttu-id="5fbaa-122">**HC_NOREMOVE** 2</span><span class="sxs-lookup"><span data-stu-id="5fbaa-122">**HC_NOREMOVE** 2</span></span> | <span data-ttu-id="5fbaa-123">Die Hook-Prozedur muss darauf vorbereitet sein, die nächste Maus-oder Tastatur Nachricht in die **eventmsg** -Struktur zu kopieren, auf die von *LPARAM* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-123">The hook procedure must prepare to copy the next mouse or keyboard message to the **EVENTMSG** structure pointed to by *lParam*.</span></span> <span data-ttu-id="5fbaa-124">Beim Empfang des **HC_GETNEXT** Codes muss die Hook-Prozedur die Nachricht in die-Struktur kopieren.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-124">Upon receiving the **HC_GETNEXT** code, the hook procedure must copy the message to the structure.</span></span> |
| <span data-ttu-id="5fbaa-125">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="5fbaa-125">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="5fbaa-126">Ein System modales Dialogfeld wurde zerstört.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-126">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="5fbaa-127">Die Hook-Prozedur muss die Wiedergabe der Nachrichten fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-127">The hook procedure must resume playing back the messages.</span></span> |
| <span data-ttu-id="5fbaa-128">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="5fbaa-128">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="5fbaa-129">Ein System modales Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-129">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="5fbaa-130">Bis das Dialogfeld zerstört ist, muss die Hook-Prozedur die Wiedergabe von Nachrichten abbrechen.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-130">Until the dialog box is destroyed, the hook procedure must stop playing back messages.</span></span> |

### <a name="wparam"></a><span data-ttu-id="5fbaa-131">wParam</span><span class="sxs-lookup"><span data-stu-id="5fbaa-131">wParam</span></span>

<span data-ttu-id="5fbaa-132">Typ: **wParam**</span><span class="sxs-lookup"><span data-stu-id="5fbaa-132">Type: **WPARAM**</span></span>

<span data-ttu-id="5fbaa-133">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-133">This parameter is not used.</span></span>

### <a name="lparam"></a><span data-ttu-id="5fbaa-134">lParam</span><span class="sxs-lookup"><span data-stu-id="5fbaa-134">lParam</span></span>

<span data-ttu-id="5fbaa-135">Typ: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="5fbaa-135">Type: **LPARAM**</span></span>

<span data-ttu-id="5fbaa-136">Ein Zeiger auf eine **eventmsg** -Struktur, die eine Meldung darstellt, die von der Hook-Prozedur verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-136">A pointer to an **EVENTMSG** structure that represents a message being processed by the hook procedure.</span></span>
<span data-ttu-id="5fbaa-137">Dieser Parameter ist nur gültig, wenn der *Code* Parameter **HC_GETNEXT** ist.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-137">This parameter is valid only when the *code* parameter is **HC_GETNEXT**.</span></span>

## <a name="returns"></a><span data-ttu-id="5fbaa-138">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="5fbaa-138">Returns</span></span>

<span data-ttu-id="5fbaa-139">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5fbaa-139">Type: **LRESULT**</span></span>

<span data-ttu-id="5fbaa-140">Damit das System vor der Verarbeitung der Nachricht warten kann, muss es sich bei dem Rückgabewert um die Zeitspanne (in Takt Einheiten) handeln, die vom System gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-140">To have the system wait before processing the message, the return value must be the amount of time, in clock ticks, that the system should wait.</span></span>

<span data-ttu-id="5fbaa-141">(Dieser Wert kann berechnet werden, indem der Unterschied zwischen den Zeit Elementen in der aktuellen und der vorherigen Eingabe Nachricht berechnet wird.)</span><span class="sxs-lookup"><span data-stu-id="5fbaa-141">(This value can be computed by calculating the difference between the time members in the current and previous input messages.)</span></span>

<span data-ttu-id="5fbaa-142">Der Rückgabewert muss 0 (null) lauten, damit die Nachricht sofort verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-142">To process the message immediately, the return value should be zero.</span></span> <span data-ttu-id="5fbaa-143">Der Rückgabewert wird nur verwendet, wenn der Hook-Code **HC_GETNEXT** ist. Andernfalls wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-143">The return value is used only if the hook code is **HC_GETNEXT**; otherwise, it is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fbaa-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fbaa-144">Remarks</span></span>

<span data-ttu-id="5fbaa-145">Eine **journalplaybackproc** -Hook-Prozedur sollte eine Eingabe Nachricht in den *LPARAM* -Parameter kopieren.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-145">A **JournalPlaybackProc** hook procedure should copy an input message to The *lParam* parameter.</span></span>
<span data-ttu-id="5fbaa-146">Die Nachricht muss zuvor mit einer **journalrecordproc** -Hook-Prozedur aufgezeichnet worden sein, die die Nachricht nicht ändern sollte.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-146">The message must have been previously recorded by using a **JournalRecordProc** hook procedure, which should not modify the message.</span></span>

<span data-ttu-id="5fbaa-147">Um dieselbe Nachricht immer wieder abzurufen, kann die Hook-Prozedur mehrmals aufgerufen werden, wobei der *Code* Parameter auf **HC_GETNEXT** festgelegt ist, ohne dass ein zwischengeschalteter Aufruf von *Code* auf **HC_SKIP** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-147">To retrieve the same message over and over, the hook procedure can be called several times with the *code* parameter set to **HC_GETNEXT** without an intervening call with *code* set to **HC_SKIP**.</span></span>

<span data-ttu-id="5fbaa-148">Wenn *Code* **HC_GETNEXT** und der Rückgabewert größer als 0 (null) ist, wird das System für die durch den Rückgabewert angegebene Anzahl von Millisekunden eingestellt.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-148">If *code* is **HC_GETNEXT** and the return value is greater than zero, the system sleeps for the number of milliseconds specified by the return value.</span></span> <span data-ttu-id="5fbaa-149">Wenn das System fortgesetzt wird, wird die Hook-Prozedur erneut aufgerufen, wobei *Code* auf **HC_GETNEXT** festgelegt ist, um dieselbe Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-149">When the system continues, it calls the hook procedure again with *code* set to **HC_GETNEXT** to retrieve the same message.</span></span>
<span data-ttu-id="5fbaa-150">Der Rückgabewert dieses neuen Aufrufes **journalplaybackproc** muss NULL sein. Andernfalls wechselt das System für die Anzahl von Millisekunden, die durch den Rückgabewert angegeben wird, wieder in den Standbymodus, rufen Sie **journalplaybackproc** erneut auf, usw.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-150">The return value from this new call to **JournalPlaybackProc** should be zero; otherwise, the system will go back to sleep for the number of milliseconds specified by the return value, call **JournalPlaybackProc** again, and so on.</span></span>
<span data-ttu-id="5fbaa-151">Das System reagiert anscheinend nicht.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-151">The system will appear to be not responding.</span></span>

<span data-ttu-id="5fbaa-152">Im Gegensatz zu den meisten anderen globalen Hook-Prozeduren werden die Hook-Prozeduren **journalrecordproc** und **journalplaybackproc** immer im Kontext des Threads aufgerufen, der den Hook festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-152">Unlike most other global hook procedures, the **JournalRecordProc** and **JournalPlaybackProc** hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="5fbaa-153">Nachdem die Hook-Prozedur die Steuerung an das System zurückgegeben hat, wird die Nachricht weiterhin verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-153">After the hook procedure returns control to the system, the message continues to be processed.</span></span> <span data-ttu-id="5fbaa-154">Wenn *Code* **HC_SKIP** ist, muss die Hook-Prozedur die Rückgabe der nächsten aufgezeichneten Ereignis Nachricht beim nächsten-Befehl vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-154">If *code* is **HC_SKIP**, the hook procedure must prepare to return the next recorded event message on its next call.</span></span>

<span data-ttu-id="5fbaa-155">Installieren Sie die **journalplaybackproc** -Hook-Prozedur, indem Sie den [WH_JOURNALPLAYBACK](about-hooks.md) -Typ und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-155">Install the **JournalPlaybackProc** hook procedure by specifying the [WH_JOURNALPLAYBACK](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="5fbaa-156">Wenn der Benutzer während der Journal Wiedergabe STRG + ESC oder STRG + ALT + ENTF drückt, wird die Wiedergabe beendet, die Wiedergabe der Journal Wiedergabe Prozedur aufgehoben, und es wird eine [WM_CANCELJOURNAL](wm-canceljournal.md) Nachricht an die journalinganwendung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-156">If the user presses CTRL+ESC OR CTRL+ALT+DEL during journal playback, the system stops the playback, unhooks the journal playback procedure, and posts a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

<span data-ttu-id="5fbaa-157">Wenn die Hook-Prozedur eine Nachricht im Bereich zurückgibt, **WM_KEYFIRST** an **WM_KEYLAST**, gelten die folgenden Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="5fbaa-157">If the hook procedure returns a message in the range **WM_KEYFIRST** to **WM_KEYLAST**, the following conditions apply:</span></span>

* <span data-ttu-id="5fbaa-158">Der **paraml** -Member der **eventmsg** -Struktur gibt den Code des virtuellen Schlüssels der Taste an, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-158">The **paramL** member of the **EVENTMSG** structure specifies the virtual key code of the key that was pressed.</span></span>
* <span data-ttu-id="5fbaa-159">Der **paramh** -Member der **eventmsg** -Struktur gibt den Scancode an.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-159">The **paramH** member of the **EVENTMSG** structure specifies the scan code.</span></span>
* <span data-ttu-id="5fbaa-160">Es gibt keine Möglichkeit, eine Wiederholungs Anzahl anzugeben.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-160">There's no way to specify a repeat count.</span></span>
<span data-ttu-id="5fbaa-161">Das Ereignis wird immer zur Darstellung eines schlüsselereignisses verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fbaa-161">The event is always taken to represent one key event.</span></span>

## <a name="see-also"></a><span data-ttu-id="5fbaa-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fbaa-162">See also</span></span>

[<span data-ttu-id="5fbaa-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="5fbaa-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="5fbaa-164">Eventmsg</span><span class="sxs-lookup"><span data-stu-id="5fbaa-164">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="5fbaa-165">Journalrecordproc</span><span class="sxs-lookup"><span data-stu-id="5fbaa-165">JournalRecordProc</span></span>](journalrecordproc.md)

[<span data-ttu-id="5fbaa-166">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="5fbaa-166">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="5fbaa-167">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="5fbaa-167">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="5fbaa-168">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="5fbaa-168">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="5fbaa-169">Hooks</span><span class="sxs-lookup"><span data-stu-id="5fbaa-169">Hooks</span></span>](hooks.md)
