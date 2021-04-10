---
UID: ''
title: Journalrecordproc-Rückruffunktion
description: Die Funktion zeichnet Meldungen auf, die das System aus der System Meldungs Warteschlange entfernt.
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
ms.openlocfilehash: bc255441ca82c86542dd8dd4729564122df6c719
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "103948535"
---
# <a name="journalrecordproc-function"></a><span data-ttu-id="e84a2-103">Journalrecordproc-Funktion</span><span class="sxs-lookup"><span data-stu-id="e84a2-103">JournalRecordProc function</span></span>

## <a name="description"></a><span data-ttu-id="e84a2-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e84a2-104">Description</span></span>

<span data-ttu-id="e84a2-105">Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e84a2-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="e84a2-106">Die Funktion zeichnet Meldungen auf, die das System aus der System Meldungs Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="e84a2-106">The function records messages the system removes from the system message queue.</span></span>
<span data-ttu-id="e84a2-107">Später kann eine Anwendung eine [journalplaybackproc](journalplaybackproc.md) -Hook-Prozedur verwenden, um die Nachrichten wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="e84a2-107">Later, an application can use a [JournalPlaybackProc](journalplaybackproc.md) hook procedure to play back the messages.</span></span>

<span data-ttu-id="e84a2-108">Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="e84a2-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="e84a2-109">**Journalrecordproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="e84a2-109">**JournalRecordProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="e84a2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e84a2-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="e84a2-111">Code [in]</span><span class="sxs-lookup"><span data-stu-id="e84a2-111">code [in]</span></span>

<span data-ttu-id="e84a2-112">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="e84a2-112">Type: **int**</span></span>

<span data-ttu-id="e84a2-113">Gibt an, wie die Nachricht verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e84a2-113">Specifies how to process the message.</span></span>
<span data-ttu-id="e84a2-114">Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e84a2-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="e84a2-115">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="e84a2-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="e84a2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e84a2-116">Value</span></span> | <span data-ttu-id="e84a2-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e84a2-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="e84a2-118">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="e84a2-118">**HC_ACTION** 0</span></span> | <span data-ttu-id="e84a2-119">Der *LPARAM* -Parameter ist ein Zeiger auf eine [eventmsg](/windows/desktop/api/winuser/ns-winuser-eventmsg) -Struktur, die Informationen zu einer Nachricht enthält, die aus der System Warteschlange entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="e84a2-119">The *lParam* parameter is a pointer to an [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure containing information about a message removed from the system queue.</span></span> <span data-ttu-id="e84a2-120">Die Hook-Prozedur muss den Inhalt der Struktur aufzeichnen, indem Sie Sie in einen Puffer oder eine Datei kopieren.</span><span class="sxs-lookup"><span data-stu-id="e84a2-120">The hook procedure must record the contents of the structure by copying them to a buffer or file.</span></span> |
| <span data-ttu-id="e84a2-121">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="e84a2-121">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="e84a2-122">Ein System modales Dialogfeld wurde zerstört.</span><span class="sxs-lookup"><span data-stu-id="e84a2-122">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="e84a2-123">Die Hook-Prozedur muss die Aufzeichnung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="e84a2-123">The hook procedure must resume recording.</span></span> |
| <span data-ttu-id="e84a2-124">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="e84a2-124">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="e84a2-125">Ein System modales Dialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e84a2-125">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="e84a2-126">Die Hook-Prozedur muss die Aufzeichnung anhalten, bis das Dialogfeld zerstört ist.</span><span class="sxs-lookup"><span data-stu-id="e84a2-126">Until the dialog box is destroyed, the hook procedure must stop recording.</span></span> |

### <a name="wparam"></a><span data-ttu-id="e84a2-127">wParam</span><span class="sxs-lookup"><span data-stu-id="e84a2-127">wParam</span></span>

<span data-ttu-id="e84a2-128">Typ: **wParam**</span><span class="sxs-lookup"><span data-stu-id="e84a2-128">Type: **WPARAM**</span></span>

<span data-ttu-id="e84a2-129">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e84a2-129">This parameter is not used.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="e84a2-130">LParam [in]</span><span class="sxs-lookup"><span data-stu-id="e84a2-130">lParam [in]</span></span>

<span data-ttu-id="e84a2-131">Typ: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="e84a2-131">Type: **LPARAM**</span></span>

<span data-ttu-id="e84a2-132">Ein Zeiger auf eine **eventmsg** -Struktur, die die zu zeichnenden Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="e84a2-132">A pointer to an **EVENTMSG** structure that contains the message to be recorded.</span></span>

## <a name="returns"></a><span data-ttu-id="e84a2-133">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="e84a2-133">Returns</span></span>

<span data-ttu-id="e84a2-134">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="e84a2-134">Type: **LRESULT**</span></span>

<span data-ttu-id="e84a2-135">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e84a2-135">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="e84a2-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e84a2-136">Remarks</span></span>

<span data-ttu-id="e84a2-137">Eine **journalrecordproc** -Hook-Prozedur muss die Nachrichten kopieren, aber nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="e84a2-137">A **JournalRecordProc** hook procedure must copy but not modify the messages.</span></span>
<span data-ttu-id="e84a2-138">Nachdem die Hook-Prozedur die Steuerung an das System zurückgegeben hat, wird die Nachricht weiterhin verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="e84a2-138">After the hook procedure returns control to the system, the message continues to be processed.</span></span>

<span data-ttu-id="e84a2-139">Installieren Sie die **journalrecordproc** -Hook-Prozedur, indem Sie den [WH_JOURNALRECORD](about-hooks.md) -Typ und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angeben.</span><span class="sxs-lookup"><span data-stu-id="e84a2-139">Install the **JournalRecordProc** hook procedure by specifying the [WH_JOURNALRECORD](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="e84a2-140">Eine **journalrecordproc** -Hook-Prozedur muss nicht in einer Dynamic Link Library Leben.</span><span class="sxs-lookup"><span data-stu-id="e84a2-140">A **JournalRecordProc** hook procedure does not need to live in a dynamic-link library.</span></span>
<span data-ttu-id="e84a2-141">Eine **journalrecordproc** -Hook-Prozedur kann in der Anwendung selbst leben.</span><span class="sxs-lookup"><span data-stu-id="e84a2-141">A **JournalRecordProc** hook procedure can live in the application itself.</span></span>

<span data-ttu-id="e84a2-142">Im Gegensatz zu den meisten anderen globalen Hook-Prozeduren werden die Hook-Prozeduren **journalrecordproc** und [journalplaybackproc](journalplaybackproc.md) immer im Kontext des Threads aufgerufen, der den Hook festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="e84a2-142">Unlike most other global hook procedures, the **JournalRecordProc** and [JournalPlaybackProc](journalplaybackproc.md) hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="e84a2-143">Eine Anwendung, die eine **journalrecordproc** -Hook-Prozedur installiert hat, sollte den [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) Code des virtuellen Schlüssels überwachen (der in den meisten Tastaturen als STRG + unt-Schlüsselkombination implementiert ist).</span><span class="sxs-lookup"><span data-stu-id="e84a2-143">An application that has installed a **JournalRecordProc** hook procedure should watch for the [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) virtual key code (which is implemented as the CTRL+BREAK key combination on most keyboards).</span></span>
<span data-ttu-id="e84a2-144">Dieser virtuelle Schlüsselcode sollte von der Anwendung als Signal interpretiert werden, dass der Benutzer die Journal Aufzeichnung anhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="e84a2-144">This virtual key code should be interpreted by the application as a signal that the user wishes to stop journal recording.</span></span>
<span data-ttu-id="e84a2-145">Die Anwendung sollte Antworten, indem Sie die Aufzeichnungs Sequenz beendet und die **journalrecordproc** -Hook-Prozedur entfernt.</span><span class="sxs-lookup"><span data-stu-id="e84a2-145">The application should respond by ending the recording sequence and removing the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="e84a2-146">Das Entfernen ist wichtig.</span><span class="sxs-lookup"><span data-stu-id="e84a2-146">Removal is important.</span></span>
<span data-ttu-id="e84a2-147">Dadurch wird verhindert, dass eine Journal Anwendung das System sperrt, indem es in einer Hook-Prozedur hängt.</span><span class="sxs-lookup"><span data-stu-id="e84a2-147">It prevents a journaling application from locking up the system by hanging inside a hook procedure.</span></span>

<span data-ttu-id="e84a2-148">Diese Rolle als Signal zum Anhalten der Journl-Aufzeichnung bedeutet, dass die Tastenkombination STRG + UNTBR nicht selbst aufgezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e84a2-148">This role as a signal to stop journl recording means that a CTRL+BREAK key combination cannot itself be recorded.</span></span>
<span data-ttu-id="e84a2-149">Da die Tastenkombination STRG + C keine Rolle spielt, kann Sie aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="e84a2-149">Since the CTRL+C key combination has no such role as a journaling signal, it can be recorded.</span></span>
<span data-ttu-id="e84a2-150">Es gibt zwei weitere Tastenkombinationen, die nicht aufgezeichnet werden können: STRG + ESC und STRG + ALT + ENTF.</span><span class="sxs-lookup"><span data-stu-id="e84a2-150">There are two other key combinations that cannot be recorded: CTRL+ESC and CTRL+ALT+DEL.</span></span>
<span data-ttu-id="e84a2-151">Diese beiden Tastenkombinationen bewirken, dass das System alle journalingaktivitäten beendet (aufzeichnen oder Wiedergabe), alle journalhooks entfernt und eine [WM_CANCELJOURNAL](wm-canceljournal.md) Nachricht in der Journal Anwendung sendet.</span><span class="sxs-lookup"><span data-stu-id="e84a2-151">Those two key combinations cause the system to stop all journaling activities (record or playback), remove all journaling hooks, and post a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

## <a name="see-also"></a><span data-ttu-id="e84a2-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e84a2-152">See also</span></span>

[<span data-ttu-id="e84a2-153">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="e84a2-153">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="e84a2-154">Eventmsg</span><span class="sxs-lookup"><span data-stu-id="e84a2-154">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="e84a2-155">Journalplaybackproc</span><span class="sxs-lookup"><span data-stu-id="e84a2-155">JournalPlaybackProc</span></span>](journalplaybackproc.md)

[<span data-ttu-id="e84a2-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="e84a2-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="e84a2-157">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="e84a2-157">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="e84a2-158">Hooks</span><span class="sxs-lookup"><span data-stu-id="e84a2-158">Hooks</span></span>](hooks.md)
