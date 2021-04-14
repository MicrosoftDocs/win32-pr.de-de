---
description: Wird an eine Anwendung gesendet, wenn das IME ein Zeichen des Konvertierungs Ergebnisses erhält. Ein Fenster empfängt diese Meldung über seine WindowProc-Funktion.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: WM_IME_CHAR Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393777"
---
# <a name="wm_ime_char-message"></a><span data-ttu-id="22508-104">WM- \_ IME- \_ char-Nachricht</span><span class="sxs-lookup"><span data-stu-id="22508-104">WM\_IME\_CHAR message</span></span>

<span data-ttu-id="22508-105">Wird an eine Anwendung gesendet, wenn das IME ein Zeichen des Konvertierungs Ergebnisses erhält.</span><span class="sxs-lookup"><span data-stu-id="22508-105">Sent to an application when the IME gets a character of the conversion result.</span></span> <span data-ttu-id="22508-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="22508-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="22508-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="22508-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22508-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="22508-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="22508-109">Ein Handle für Fenster.</span><span class="sxs-lookup"><span data-stu-id="22508-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="22508-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="22508-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22508-111">**DBCS:** Ein Einzel Byte-oder Doppelbyte-Zeichen Wert.</span><span class="sxs-lookup"><span data-stu-id="22508-111">**DBCS:** A single-byte or double-byte character value.</span></span> <span data-ttu-id="22508-112">Bei einem Double-Byte-Zeichen enthält (Byte) (wParam >> 8) das führende Byte.</span><span class="sxs-lookup"><span data-stu-id="22508-112">For a double-byte character, (BYTE)(wParam >> 8) contains the lead byte.</span></span> <span data-ttu-id="22508-113">Beachten Sie, dass die Klammern erforderlich sind, da der Umwandlungs Operator eine höhere Rangfolge aufweist als der Shift-Operator.</span><span class="sxs-lookup"><span data-stu-id="22508-113">Note that the parentheses are necessary because the cast operator has higher precedence than the shift operator.</span></span>

<span data-ttu-id="22508-114">**Unicode:** Ein Unicode-Zeichen Wert.</span><span class="sxs-lookup"><span data-stu-id="22508-114">**Unicode:** A Unicode character value.</span></span>

</dd> <dt>

<span data-ttu-id="22508-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="22508-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="22508-116">Die Wiederholungs Anzahl, der Scan Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Übergangs Zustands Kennzeichen mit den unten definierten Werten.</span><span class="sxs-lookup"><span data-stu-id="22508-116">The repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, with values as defined below.</span></span>



| <span data-ttu-id="22508-117">bit</span><span class="sxs-lookup"><span data-stu-id="22508-117">Bit</span></span>   | <span data-ttu-id="22508-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="22508-118">Meaning</span></span>                                                                              |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22508-119">0-15</span><span class="sxs-lookup"><span data-stu-id="22508-119">0-15</span></span>  | <span data-ttu-id="22508-120">Wiederholungs Anzahl.</span><span class="sxs-lookup"><span data-stu-id="22508-120">Repeat count.</span></span> <span data-ttu-id="22508-121">Da das erste Byte und das zweite Byte fortlaufend sind, ist dies immer 1.</span><span class="sxs-lookup"><span data-stu-id="22508-121">Since the first byte and second byte are continuous, this is always 1.</span></span> |
| <span data-ttu-id="22508-122">16-23</span><span class="sxs-lookup"><span data-stu-id="22508-122">16-23</span></span> | <span data-ttu-id="22508-123">Scannen Sie Code nach einem kompletten asiatischen Zeichen.</span><span class="sxs-lookup"><span data-stu-id="22508-123">Scan code for a complete Asian character.</span></span>                                            |
| <span data-ttu-id="22508-124">24</span><span class="sxs-lookup"><span data-stu-id="22508-124">24</span></span>    | <span data-ttu-id="22508-125">Erweiterter Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="22508-125">Extended key.</span></span>                                                                        |
| <span data-ttu-id="22508-126">25-28</span><span class="sxs-lookup"><span data-stu-id="22508-126">25-28</span></span> | <span data-ttu-id="22508-127">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="22508-127">Not used.</span></span>                                                                            |
| <span data-ttu-id="22508-128">29</span><span class="sxs-lookup"><span data-stu-id="22508-128">29</span></span>    | <span data-ttu-id="22508-129">Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="22508-129">Context code.</span></span>                                                                        |
| <span data-ttu-id="22508-130">30</span><span class="sxs-lookup"><span data-stu-id="22508-130">30</span></span>    | <span data-ttu-id="22508-131">Vorheriger Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="22508-131">Previous key state.</span></span>                                                                  |
| <span data-ttu-id="22508-132">31</span><span class="sxs-lookup"><span data-stu-id="22508-132">31</span></span>    | <span data-ttu-id="22508-133">Übergangsstatus.</span><span class="sxs-lookup"><span data-stu-id="22508-133">Transition state.</span></span>                                                                    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22508-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22508-134">Remarks</span></span>

<span data-ttu-id="22508-135">Anders als bei der " [**WM \_ char**](../inputdev/wm-char.md) "-Meldung für ein nicht-Unicode-Fenster kann diese Meldung Doppelbyte-und Einzel Byte-Zeichen Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="22508-135">Unlike the [**WM\_CHAR**](../inputdev/wm-char.md) message for a non-Unicode window, this message can include double-byte and single-byte character values.</span></span> <span data-ttu-id="22508-136">Bei einem Unicode-Fenster ist diese Meldung mit WM char identisch \_ .</span><span class="sxs-lookup"><span data-stu-id="22508-136">For a Unicode window, this message is the same as WM\_CHAR.</span></span>

<span data-ttu-id="22508-137">Wenn bei einem nicht-Unicode-Fenster die "WM \_ IME \_ char"-Nachricht ein Doppelbyte Zeichen enthält und die Anwendung diese Nachricht an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergibt, konvertiert der IME diese Nachricht in zwei WM- \_ char-Nachrichten, die jeweils ein Byte des Doppelbyte Zeichens enthalten.</span><span class="sxs-lookup"><span data-stu-id="22508-137">For a non-Unicode window, if the WM\_IME\_CHAR message includes a double-byte character and the application passes this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the IME converts this message into two WM\_CHAR messages, each containing one byte of the double-byte character.</span></span>

## <a name="requirements"></a><span data-ttu-id="22508-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22508-138">Requirements</span></span>



| <span data-ttu-id="22508-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22508-139">Requirement</span></span> | <span data-ttu-id="22508-140">Wert</span><span class="sxs-lookup"><span data-stu-id="22508-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22508-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22508-141">Minimum supported client</span></span><br/> | <span data-ttu-id="22508-142">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22508-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="22508-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22508-143">Minimum supported server</span></span><br/> | <span data-ttu-id="22508-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22508-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="22508-145">Header</span><span class="sxs-lookup"><span data-stu-id="22508-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="22508-146"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="22508-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22508-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22508-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22508-148">Eingabemethoden-Manager</span><span class="sxs-lookup"><span data-stu-id="22508-148">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="22508-149">Eingabemethoden-Manager-Meldungen</span><span class="sxs-lookup"><span data-stu-id="22508-149">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
