---
UID: ''
title: Getmsgproc-Rückruffunktion
description: Das System ruft diese Funktion auf, wenn eine Nachrichten Funktion eine Nachricht aus einer Anwendungs Nachrichten Warteschlange abruft.
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
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "106344154"
---
# <a name="getmsgproc-function"></a><span data-ttu-id="6c3f0-103">Getmsgproc-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c3f0-103">GetMsgProc function</span></span>

## <a name="-description"></a><span data-ttu-id="6c3f0-104">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c3f0-104">-description</span></span>

<span data-ttu-id="6c3f0-105">Eine von der Anwendung definierte oder Bibliotheks definierte Rückruffunktion, die mit der [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) -Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span> <span data-ttu-id="6c3f0-106">Das System ruft diese Funktion immer dann auf, wenn die [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) -Funktion oder die [Peer Message](/windows/desktop/api/winuser/nf-winuser-peekmessagew) -Funktion eine Nachricht aus einer Anwendungs Nachrichten Warteschlange abgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-106">The system calls this function whenever the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function has retrieved a message from an application message queue.</span></span>
<span data-ttu-id="6c3f0-107">Bevor die abgerufene Nachricht an den Aufrufer zurückgegeben wird, übergibt das System die Nachricht an die Hook-Prozedur.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-107">Before returning the retrieved message to the caller, the system passes the message to the hook procedure.</span></span>

<span data-ttu-id="6c3f0-108">Der **HookProc** -Typ definiert einen Zeiger auf diese Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="6c3f0-109">**Getmsgproc** ist ein Platzhalter für den Anwendungs definierten oder Bibliotheks definierten Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-109">**GetMsgProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a><span data-ttu-id="6c3f0-110">-Parameter</span><span class="sxs-lookup"><span data-stu-id="6c3f0-110">-parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="6c3f0-111">Code [in]</span><span class="sxs-lookup"><span data-stu-id="6c3f0-111">code [in]</span></span>

<span data-ttu-id="6c3f0-112">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="6c3f0-112">Type: **int**</span></span>

<span data-ttu-id="6c3f0-113">Gibt an, ob die Hook-Prozedur die Nachricht verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-113">Specifies whether the hook procedure must process the message.</span></span>
<span data-ttu-id="6c3f0-114">Wenn *Code* **HC_ACTION** ist, muss die Hook-Prozedur die Nachricht verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-114">If *code* is **HC_ACTION**, the hook procedure must process the message.</span></span>
<span data-ttu-id="6c3f0-115">Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur die Nachricht ohne weitere Verarbeitung an die [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) -Funktion übergeben und den von **CallNextHookEx** zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-115">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>

### <a name="wparam-in"></a><span data-ttu-id="6c3f0-116">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="6c3f0-116">wParam [in]</span></span>

<span data-ttu-id="6c3f0-117">Typ: **wParam**</span><span class="sxs-lookup"><span data-stu-id="6c3f0-117">Type: **WPARAM**</span></span>

<span data-ttu-id="6c3f0-118">Gibt an, ob die Nachricht aus der Warteschlange entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-118">Specifies whether the message has been removed from the queue.</span></span>
<span data-ttu-id="6c3f0-119">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-119">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="6c3f0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="6c3f0-120">Value</span></span> | <span data-ttu-id="6c3f0-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6c3f0-121">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="6c3f0-122">**PM_NOREMOVE** 0x0000</span><span class="sxs-lookup"><span data-stu-id="6c3f0-122">**PM_NOREMOVE** 0x0000</span></span> | <span data-ttu-id="6c3f0-123">Die Nachricht wurde nicht aus der Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-123">The message has not been removed from the queue.</span></span> <span data-ttu-id="6c3f0-124">(Eine Anwendung, die die Funktion " **Peer Message** " genannt wird und das **PM_NOREMOVE** Flag angibt.)</span><span class="sxs-lookup"><span data-stu-id="6c3f0-124">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |
| <span data-ttu-id="6c3f0-125">**PM_REMOVE** 0x0001</span><span class="sxs-lookup"><span data-stu-id="6c3f0-125">**PM_REMOVE** 0x0001</span></span> | <span data-ttu-id="6c3f0-126">Die Nachricht wurde aus der Warteschlange entfernt.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-126">The message has been removed from the queue.</span></span> <span data-ttu-id="6c3f0-127">(Eine Anwendung namens **GetMessage** oder die Funktion "  **Peer Message** ", die das **PM_REMOVE** -Flag angibt.)</span><span class="sxs-lookup"><span data-stu-id="6c3f0-127">(An application called **GetMessage**, or it called the  **PeekMessage** function, specifying the **PM_REMOVE** flag.)</span></span>|

### <a name="lparam-in"></a><span data-ttu-id="6c3f0-128">LParam [in]</span><span class="sxs-lookup"><span data-stu-id="6c3f0-128">lParam [in]</span></span>

<span data-ttu-id="6c3f0-129">Typ: **LPARAM**</span><span class="sxs-lookup"><span data-stu-id="6c3f0-129">Type: **LPARAM**</span></span>

<span data-ttu-id="6c3f0-130">Ein Zeiger auf eine [msg](/windows/desktop/api/winuser/ns-winuser-msg) -Struktur, die Details über die Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-130">A pointer to an [MSG](/windows/desktop/api/winuser/ns-winuser-msg) structure that contains details about the message.</span></span>

## <a name="-returns"></a><span data-ttu-id="6c3f0-131">-Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="6c3f0-131">-returns</span></span>

<span data-ttu-id="6c3f0-132">Wenn *Code* kleiner als 0 (null) ist, muss die Hook-Prozedur den von [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)zurückgegebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-132">If *code* is less than zero, the hook procedure must return the value returned by [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span></span>

<span data-ttu-id="6c3f0-133">Wenn *Code* größer als oder gleich 0 (null) ist, wird dringend empfohlen, **CallNextHookEx** aufzurufen und den zurückgegebenen Wert zurückzugeben. Andernfalls erhalten andere Anwendungen, die [WH_GETMESSAGE](about-hooks.md) Hooks installiert haben, keine Hook-Benachrichtigungen und können sich daher fälschlicherweise Verhalten.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-133">If *code* is greater than or equal to zero, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_GETMESSAGE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="6c3f0-134">Wenn die Hook-Prozedur **CallNextHookEx** nicht aufruft, sollte der Rückgabewert 0 (null) lauten.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-134">If the hook procedure does not call **CallNextHookEx**, the return value should be zero.</span></span>

## <a name="-remarks"></a><span data-ttu-id="6c3f0-135">-Hinweise</span><span class="sxs-lookup"><span data-stu-id="6c3f0-135">-remarks</span></span>

<span data-ttu-id="6c3f0-136">Die **getmsgproc** -Hook-Prozedur kann die Nachricht überprüfen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-136">The **GetMsgProc** hook procedure can examine or modify the message.</span></span>
<span data-ttu-id="6c3f0-137">Nachdem die Hook-Prozedur die Steuerung an das System zurückgegeben hat, gibt die **GetMessage** -Funktion oder die **Peer Message** -Funktion die Nachricht zusammen mit allen Änderungen an die Anwendung zurück, die Sie ursprünglich aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-137">After the hook procedure returns control to the system, the **GetMessage** or **PeekMessage** function returns the message, along with any modifications, to the application that originally called it.</span></span>

<span data-ttu-id="6c3f0-138">Eine Anwendung installiert diese Hook-Prozedur, indem Sie den **WH_GETMESSAGE** Hooktyp und einen Zeiger auf die Hook-Prozedur in einem Aufrufen der **SetWindowsHookEx** -Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="6c3f0-138">An application installs this hook procedure by specifying the **WH_GETMESSAGE** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c3f0-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c3f0-139">See also</span></span>

[<span data-ttu-id="6c3f0-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="6c3f0-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="6c3f0-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="6c3f0-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="6c3f0-142">Meldung</span><span class="sxs-lookup"><span data-stu-id="6c3f0-142">MSG</span></span>](/windows/desktop/api/winuser/ns-winuser-msg)

[<span data-ttu-id="6c3f0-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="6c3f0-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="6c3f0-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="6c3f0-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="6c3f0-145">Hooks</span><span class="sxs-lookup"><span data-stu-id="6c3f0-145">Hooks</span></span>](hooks.md)
