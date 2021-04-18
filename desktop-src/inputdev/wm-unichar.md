---
title: WM_UNICHAR Meldung (Winuser. h)
description: Die WM \_ UNICHAR-Nachricht kann von einer Anwendung verwendet werden, um Eingaben für andere Fenster bereitzustellen.
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- Tastatur-und Maus Eingaben für WM_UNICHAR Nachricht
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340335"
---
# <a name="wm_unichar-message"></a><span data-ttu-id="0c659-104">WM \_ UNICHAR-Nachricht</span><span class="sxs-lookup"><span data-stu-id="0c659-104">WM\_UNICHAR message</span></span>

<span data-ttu-id="0c659-105">Die **WM \_ UNICHAR** -Nachricht kann von einer Anwendung verwendet werden, um Eingaben für andere Fenster bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0c659-105">The **WM\_UNICHAR** message can be used by an application to post input to other windows.</span></span> <span data-ttu-id="0c659-106">Diese Meldung enthält den Zeichencode der Taste, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="0c659-106">This message contains the character code of the key that was pressed.</span></span> <span data-ttu-id="0c659-107">(Testen Sie, ob eine Ziel-APP **WM- \_ UNICHAR** -Nachrichten verarbeiten kann, indem Sie die Nachricht mit *wParam* auf **Unicode \_ nochar** senden.)</span><span class="sxs-lookup"><span data-stu-id="0c659-107">(Test whether a target app can process **WM\_UNICHAR** messages by sending the message with *wParam* set to **UNICODE\_NOCHAR**.)</span></span>


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a><span data-ttu-id="0c659-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c659-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c659-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c659-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c659-110">Der Zeichencode des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="0c659-110">The character code of the key.</span></span>

<span data-ttu-id="0c659-111">Wenn *wParam* eine **Unicode \_** -Datei ist und die Anwendung diese Nachricht verarbeitet, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0c659-111">If *wParam* is **UNICODE\_NOCHAR** and the application processes this message, then return **TRUE**.</span></span> <span data-ttu-id="0c659-112">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion gibt **false** zurück (Standard).</span><span class="sxs-lookup"><span data-stu-id="0c659-112">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function will return **FALSE** (the default).</span></span>

<span data-ttu-id="0c659-113">Wenn *wParam* nicht der **Unicode \_**-Wert ist, wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0c659-113">If *wParam* is not **UNICODE\_NOCHAR**, return **FALSE**.</span></span> <span data-ttu-id="0c659-114">Der Unicode-  [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sendet eine [**WM \_ char**](wm-char.md) -Nachricht mit denselben Parametern, und die ANSI **defwindowproc** -Funktion postet entweder eine oder zwei **WM \_ char** -Nachrichten mit den entsprechenden ANSI-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0c659-114">The Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posts a [**WM\_CHAR**](wm-char.md) message with the same parameters and the ANSI **DefWindowProc** function posts either one or two **WM\_CHAR** messages with the corresponding ANSI character(s).</span></span>

</dd> <dt>

<span data-ttu-id="0c659-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c659-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c659-116">Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c659-116">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="0c659-117">Bits</span><span class="sxs-lookup"><span data-stu-id="0c659-117">Bits</span></span>  | <span data-ttu-id="0c659-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0c659-118">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c659-119">0-15</span><span class="sxs-lookup"><span data-stu-id="0c659-119">0-15</span></span>  | <span data-ttu-id="0c659-120">Die Wiederholungs Anzahl für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0c659-120">The repeat count for the current message.</span></span> <span data-ttu-id="0c659-121">Der Wert gibt an, wie oft der Tastatur Schlag automatisch durchgeführt wird, wenn der Benutzer die Taste gedrückt hält.</span><span class="sxs-lookup"><span data-stu-id="0c659-121">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="0c659-122">Wenn die Tastatureingabe lang genug gehalten wird, werden mehrere Nachrichten gesendet.</span><span class="sxs-lookup"><span data-stu-id="0c659-122">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="0c659-123">Die Wiederholungs Anzahl ist jedoch nicht kumulativ.</span><span class="sxs-lookup"><span data-stu-id="0c659-123">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="0c659-124">16-23</span><span class="sxs-lookup"><span data-stu-id="0c659-124">16-23</span></span> | <span data-ttu-id="0c659-125">Der Überprüfungs Code.</span><span class="sxs-lookup"><span data-stu-id="0c659-125">The scan code.</span></span> <span data-ttu-id="0c659-126">Der Wert hängt vom OEM ab.</span><span class="sxs-lookup"><span data-stu-id="0c659-126">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="0c659-127">24</span><span class="sxs-lookup"><span data-stu-id="0c659-127">24</span></span>    | <span data-ttu-id="0c659-128">Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0c659-128">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="0c659-129">Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="0c659-129">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="0c659-130">25-28</span><span class="sxs-lookup"><span data-stu-id="0c659-130">25-28</span></span> | <span data-ttu-id="0c659-131">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="0c659-131">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="0c659-132">29</span><span class="sxs-lookup"><span data-stu-id="0c659-132">29</span></span>    | <span data-ttu-id="0c659-133">Der Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="0c659-133">The context code.</span></span> <span data-ttu-id="0c659-134">Der Wert ist 1, wenn die Alt-Taste gedrückt gehalten wird, während die Taste gedrückt wird. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="0c659-134">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="0c659-135">30</span><span class="sxs-lookup"><span data-stu-id="0c659-135">30</span></span>    | <span data-ttu-id="0c659-136">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="0c659-136">The previous key state.</span></span> <span data-ttu-id="0c659-137">Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird, oder wenn der Schlüssel auf "0" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0c659-137">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="0c659-138">31</span><span class="sxs-lookup"><span data-stu-id="0c659-138">31</span></span>    | <span data-ttu-id="0c659-139">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="0c659-139">The transition state.</span></span> <span data-ttu-id="0c659-140">Der Wert ist 1, wenn der Schlüssel freigegeben wird, oder der Wert ist 0, wenn die Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="0c659-140">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="0c659-141">Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="0c659-141">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c659-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c659-142">Return value</span></span>

<span data-ttu-id="0c659-143">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0c659-143">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c659-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c659-144">Remarks</span></span>

<span data-ttu-id="0c659-145">Die **WM- \_ UNICHAR** -Nachricht ähnelt [**WM \_ char**](wm-char.md), verwendet jedoch UTF (Unicode Transformation Format)-32, während **WM \_ char** UTF-16 verwendet.</span><span class="sxs-lookup"><span data-stu-id="0c659-145">The **WM\_UNICHAR** message is similar to [**WM\_CHAR**](wm-char.md), but it uses Unicode Transformation Format (UTF)-32, whereas **WM\_CHAR** uses UTF-16.</span></span>

<span data-ttu-id="0c659-146">Diese Nachricht dient zum Senden oder Bereitstellen von Unicode-Zeichen an ANSI-Fenster und kann zusätzliche Unicode-unikezeichen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0c659-146">This message is designed to send or post Unicode characters to ANSI windows and can handle Unicode Supplementary Plane characters.</span></span>

<span data-ttu-id="0c659-147">Da es nicht notwendigerweise eine 1:1-Entsprechung zwischen den gedrückten Schlüsseln und Zeichen Nachrichten gibt, sind die Informationen im höherwertigen Wort des *LPARAM* -Parameters für Anwendungen in der Regel nicht nützlich.</span><span class="sxs-lookup"><span data-stu-id="0c659-147">Because there is not necessarily a one-to-one correspondence between keys pressed and character messages generated, the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="0c659-148">Die Informationen im höherwertigen Wort gelten nur für die letzte [**WM- \_ KeyDown**](wm-keydown.md) -Nachricht, die vor der Bereitstellung der **WM \_ UNICHAR** -Nachricht steht.</span><span class="sxs-lookup"><span data-stu-id="0c659-148">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_UNICHAR** message.</span></span>

<span data-ttu-id="0c659-149">Erweiterte Schlüssel für erweiterte 101-und 102-keytastaturen sind die Rechte ALT-Taste und die Rechte STRG-Taste im Hauptabschnitt der Tastatur. die Eingaben "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Tastatur und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur.</span><span class="sxs-lookup"><span data-stu-id="0c659-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="0c659-150">Einige andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="0c659-150">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c659-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c659-151">Requirements</span></span>



| <span data-ttu-id="0c659-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c659-152">Requirement</span></span> | <span data-ttu-id="0c659-153">Wert</span><span class="sxs-lookup"><span data-stu-id="0c659-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c659-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c659-154">Minimum supported client</span></span><br/> | <span data-ttu-id="0c659-155">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c659-155">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c659-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c659-156">Minimum supported server</span></span><br/> | <span data-ttu-id="0c659-157">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c659-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0c659-158">Header</span><span class="sxs-lookup"><span data-stu-id="0c659-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c659-159"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="0c659-159"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c659-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c659-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c659-161">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0c659-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0c659-162">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="0c659-162">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="0c659-163">**WM \_ -Zeichen**</span><span class="sxs-lookup"><span data-stu-id="0c659-163">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="0c659-164">**WM- \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="0c659-164">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

<span data-ttu-id="0c659-165">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0c659-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0c659-166">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="0c659-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

