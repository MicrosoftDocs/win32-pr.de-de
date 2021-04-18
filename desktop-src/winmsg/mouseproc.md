---
UID: ''
title: Mousproc-Rückruffunktion
description: Das System ruft diese Funktion auf, wenn eine Anwendung eine Nachrichten Funktion aufruft und eine zu verarbeitende Maus Nachricht vorhanden ist.
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/11/2020
ms.locfileid: "106338654"
---
# <a name="mouseproc-function"></a><span data-ttu-id="bcbf5-103">Mousproc-Funktion</span><span class="sxs-lookup"><span data-stu-id="bcbf5-103">MouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="bcbf5-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bcbf5-104">Description</span></span>

<span data-ttu-id="bcbf5-105">Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="bcbf5-106">Das System ruft diese Funktion immer dann auf, wenn eine Anwendung die [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) -oder die [Peer Message](/windows/desktop/api/winuser/nf-winuser-peekmessagew) -Funktion aufruft und eine zu verarbeitende Maus Nachricht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a mouse message to be processed.</span></span>

<span data-ttu-id="bcbf5-107">Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="bcbf5-108">**Mouseproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-108">**MouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="bcbf5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcbf5-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="bcbf5-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="bcbf5-110">nCode [in]</span></span>

<span data-ttu-id="bcbf5-111">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="bcbf5-111">Type: **int**</span></span>

<span data-ttu-id="bcbf5-112">Ein Code, den die Hook-Prozedur verwendet, um zu bestimmen, wie die Nachricht verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-112">A code that the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="bcbf5-113">Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="bcbf5-114">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="bcbf5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="bcbf5-115">Value</span></span> | <span data-ttu-id="bcbf5-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bcbf5-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="bcbf5-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="bcbf5-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="bcbf5-118">Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Maus Meldung.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |
| <span data-ttu-id="bcbf5-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="bcbf5-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="bcbf5-120">Der *wParam* -Parameter und der *LPARAM* -Parameter enthalten Informationen über eine Maus Meldung, und die Maus Nachricht wurde nicht aus der Nachrichten Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-120">The *wParam* and *lParam* parameters contain information about a mouse message, and the mouse message has not been removed from the message queue.</span></span> <span data-ttu-id="bcbf5-121">(Eine Anwendung, die die Funktion " **Peer Message** " genannt wird und das **PM_NOREMOVE** Flag angibt.)</span><span class="sxs-lookup"><span data-stu-id="bcbf5-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="bcbf5-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="bcbf5-122">wParam [in]</span></span>

<span data-ttu-id="bcbf5-123">Typ: **wParam**</span><span class="sxs-lookup"><span data-stu-id="bcbf5-123">Type: **WPARAM**</span></span>

<span data-ttu-id="bcbf5-124">Der Bezeichner der Maus Nachricht.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-124">The identifier of the mouse message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="bcbf5-125">LParam [in]</span><span class="sxs-lookup"><span data-stu-id="bcbf5-125">lParam [in]</span></span>

<span data-ttu-id="bcbf5-126">Typ: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="bcbf5-126">Type: **LPARAM**</span></span>

<span data-ttu-id="bcbf5-127">Ein Zeiger auf eine [mouethuokstruct](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-127">A pointer to a [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="bcbf5-128">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="bcbf5-128">Returns</span></span>

<span data-ttu-id="bcbf5-129">Typ: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="bcbf5-129">Type: **LRESULT**</span></span>

<span data-ttu-id="bcbf5-130">Wenn *nCode* kleiner als 0 (null) ist, muss die Hook-Prozedur den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="bcbf5-131">Wenn *nCode* größer als oder gleich 0 (null) ist und die Hook-Prozedur die Nachricht nicht verarbeitet hat, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_MOUSE](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="bcbf5-132">Wenn die Hook-Prozedur die Nachricht verarbeitet hat, kann Sie einen Wert ungleich 0 (null) zurückgeben, um zu verhindern, dass das System die Nachricht an die Zielfenster Prozedur übergibt.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcbf5-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcbf5-133">Remarks</span></span>

<span data-ttu-id="bcbf5-134">Eine Anwendung installiert die Hook-Prozedur, indem Sie den WH_MOUSE Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-134">An application installs the hook procedure by specifying the WH_MOUSE hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="bcbf5-135">Die Hook-Prozedur darf keine [WH_JOURNALPLAYBACK](about-hooks.md) Rückruffunktion installieren.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-135">The hook procedure must not install a [WH_JOURNALPLAYBACK](about-hooks.md) callback function.</span></span>

<span data-ttu-id="bcbf5-136">Dieser Hook kann im Kontext des Threads aufgerufen werden, der ihn installiert hat.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-136">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="bcbf5-137">Der-Befehl wird aufgerufen, indem eine Nachricht an den Thread gesendet wird, der den Hook installiert hat.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-137">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="bcbf5-138">Der Thread, der den Hook installiert hat, muss daher über eine Nachrichten Schleife verfügen.</span><span class="sxs-lookup"><span data-stu-id="bcbf5-138">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="bcbf5-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcbf5-139">See also</span></span>

[<span data-ttu-id="bcbf5-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="bcbf5-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="bcbf5-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="bcbf5-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="bcbf5-142">Mouselhuokstruct</span><span class="sxs-lookup"><span data-stu-id="bcbf5-142">MOUSEHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[<span data-ttu-id="bcbf5-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="bcbf5-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="bcbf5-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="bcbf5-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="bcbf5-145">Hooks</span><span class="sxs-lookup"><span data-stu-id="bcbf5-145">Hooks</span></span>](hooks.md)

[<span data-ttu-id="bcbf5-146">Informationen zu Hooks</span><span class="sxs-lookup"><span data-stu-id="bcbf5-146">About Hooks</span></span>](about-hooks.md)
