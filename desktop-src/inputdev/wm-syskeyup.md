---
title: WM_SYSKEYUP Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn der Benutzer eine Taste loslässt, die gedrückt wurde, während die Alt-Taste gedrückt gehalten wurde.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- Tastatur-und Maus Eingaben für WM_SYSKEYUP Nachricht
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352058"
---
# <a name="wm_syskeyup-message"></a><span data-ttu-id="ce9b4-104">WM- \_ syskeyup-Meldung</span><span class="sxs-lookup"><span data-stu-id="ce9b4-104">WM\_SYSKEYUP message</span></span>

<span data-ttu-id="ce9b4-105">Wird an das Fenster mit dem Tastaturfokus gesendet, wenn der Benutzer eine Taste loslässt, die gedrückt wurde, während die Alt-Taste gedrückt gehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-105">Posted to the window with the keyboard focus when the user releases a key that was pressed while the ALT key was held down.</span></span> <span data-ttu-id="ce9b4-106">Es tritt auch auf, wenn derzeit kein Fenster den Tastaturfokus besitzt. in diesem Fall wird die **WM- \_ syskeyup** -Nachricht an das aktive Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYUP** message is sent to the active window.</span></span> <span data-ttu-id="ce9b4-107">Das Fenster, in dem die Meldung empfangen wird, kann durch Überprüfen des Kontext Codes im *LPARAM* -Parameter zwischen diesen beiden Kontexten unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>

<span data-ttu-id="ce9b4-108">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a><span data-ttu-id="ce9b4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce9b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce9b4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce9b4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce9b4-111">Der Code für den virtuellen Schlüssel des Schlüssels, der freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-111">The virtual-key code of the key being released.</span></span> <span data-ttu-id="ce9b4-112">Siehe [**virtuelle Schlüssel Codes**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ce9b4-112">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="ce9b4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce9b4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce9b4-114">Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-114">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="ce9b4-115">Bits</span><span class="sxs-lookup"><span data-stu-id="ce9b4-115">Bits</span></span>  | <span data-ttu-id="ce9b4-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ce9b4-116">Meaning</span></span>                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce9b4-117">0-15</span><span class="sxs-lookup"><span data-stu-id="ce9b4-117">0-15</span></span>  | <span data-ttu-id="ce9b4-118">Die Wiederholungs Anzahl für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-118">The repeat count for the current message.</span></span> <span data-ttu-id="ce9b4-119">Der Wert gibt an, wie oft der Tastatur Schlag automatisch durchgeführt wird, wenn der Benutzer die Taste gedrückt hält.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-119">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="ce9b4-120">Die Wiederholungs Anzahl ist immer eine für eine **WM- \_ syskeyup** -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-120">The repeat count is always one for a **WM\_SYSKEYUP** message.</span></span>         |
| <span data-ttu-id="ce9b4-121">16-23</span><span class="sxs-lookup"><span data-stu-id="ce9b4-121">16-23</span></span> | <span data-ttu-id="ce9b4-122">Der Überprüfungs Code.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-122">The scan code.</span></span> <span data-ttu-id="ce9b4-123">Der Wert hängt vom OEM ab.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-123">The value depends on the OEM.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="ce9b4-124">24</span><span class="sxs-lookup"><span data-stu-id="ce9b4-124">24</span></span>    | <span data-ttu-id="ce9b4-125">Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="ce9b4-126">Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ce9b4-126">The value is 1 if it is an extended key; otherwise, it is zero.</span></span>                   |
| <span data-ttu-id="ce9b4-127">25-28</span><span class="sxs-lookup"><span data-stu-id="ce9b4-127">25-28</span></span> | <span data-ttu-id="ce9b4-128">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-128">Reserved; do not use.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="ce9b4-129">29</span><span class="sxs-lookup"><span data-stu-id="ce9b4-129">29</span></span>    | <span data-ttu-id="ce9b4-130">Der Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-130">The context code.</span></span> <span data-ttu-id="ce9b4-131">Der Wert ist 1, wenn die Alt-Taste gedrückt ist, während die Taste losgelassen wird. der Wert ist 0 (null), wenn die **WM- \_ syskeyup** -Nachricht im aktiven Fenster gepostet wird, da kein Fenster den Tastaturfokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-131">The value is 1 if the ALT key is down while the key is released; it is zero if the **WM\_SYSKEYUP** message is posted to the active window because no window has the keyboard focus.</span></span> |
| <span data-ttu-id="ce9b4-132">30</span><span class="sxs-lookup"><span data-stu-id="ce9b4-132">30</span></span>    | <span data-ttu-id="ce9b4-133">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-133">The previous key state.</span></span> <span data-ttu-id="ce9b4-134">Der Wert für eine **WM- \_ syskeyup** -Nachricht lautet immer 1.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-134">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                 |
| <span data-ttu-id="ce9b4-135">31</span><span class="sxs-lookup"><span data-stu-id="ce9b4-135">31</span></span>    | <span data-ttu-id="ce9b4-136">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-136">The transition state.</span></span> <span data-ttu-id="ce9b4-137">Der Wert für eine **WM- \_ syskeyup** -Nachricht lautet immer 1.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-137">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                   |

<span data-ttu-id="ce9b4-138">Weitere Informationen finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="ce9b4-138">For more details, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce9b4-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce9b4-139">Return value</span></span>

<span data-ttu-id="ce9b4-140">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce9b4-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce9b4-141">Remarks</span></span>

<span data-ttu-id="ce9b4-142">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion sendet eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster der obersten Ebene, wenn die F10-Taste oder die Alt-Taste losgelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="ce9b4-143">Der *wParam* -Parameter der Nachricht ist auf **SC \_ keymenu** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-143">The *wParam* parameter of the message is set to **SC\_KEYMENU**.</span></span>

<span data-ttu-id="ce9b4-144">Wenn der Kontext Code NULL ist, kann die Nachricht an die [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) -Funktion übermittelt werden, die Sie behandelt, als ob es sich um eine normale Schlüssel Nachricht anstatt um eine Zeichen Schlüssel Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-144">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="ce9b4-145">Dies ermöglicht das Verwenden von Zugriffstasten für das aktive Fenster, auch wenn das aktive Fenster nicht über den Tastaturfokus verfügt.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-145">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="ce9b4-146">Für erweiterte 101-und 102-Key-Tastaturen sind erweiterte Schlüssel die Rechte ALT-Taste und die STRG-Taste im Hauptabschnitt der Tastatur. die Tasten "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Keypad. und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="ce9b4-147">Andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-147">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="ce9b4-148">Für nicht-U. S. Erweiterte Tastatur Tastatur mit 102-Taste, die Rechte ALT-Taste wird als STRG + ALT-Taste behandelt.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-148">For non-U.S. enhanced 102-key keyboards, the right ALT key is handled as a CTRL+ALT key.</span></span> <span data-ttu-id="ce9b4-149">In der folgenden Tabelle wird die Reihenfolge der Nachrichten angezeigt, die sich ergeben, wenn der Benutzer diesen Schlüssel drückt und freigibt.</span><span class="sxs-lookup"><span data-stu-id="ce9b4-149">The following table shows the sequence of messages that result when the user presses and releases this key.</span></span>



| <span data-ttu-id="ce9b4-150">`Message`</span><span class="sxs-lookup"><span data-stu-id="ce9b4-150">Message</span></span>                           | <span data-ttu-id="ce9b4-151">Code des virtuellen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="ce9b4-151">Virtual-key code</span></span> |
|-----------------------------------|------------------|
| [<span data-ttu-id="ce9b4-152">**WM- \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-152">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="ce9b4-153">**VK- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-153">**VK\_CONTROL**</span></span>  |
| [<span data-ttu-id="ce9b4-154">**WM- \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-154">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="ce9b4-155">**VK- \_ Menü**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-155">**VK\_MENU**</span></span>     |
| [<span data-ttu-id="ce9b4-156">**WM- \_ KeyUp**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-156">**WM\_KEYUP**</span></span>](wm-keyup.md)     | <span data-ttu-id="ce9b4-157">**VK- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-157">**VK\_CONTROL**</span></span>  |
| <span data-ttu-id="ce9b4-158">**WM- \_ syskeyup**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-158">**WM\_SYSKEYUP**</span></span>                  | <span data-ttu-id="ce9b4-159">**VK- \_ Menü**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-159">**VK\_MENU**</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="ce9b4-160">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce9b4-160">Requirements</span></span>



| <span data-ttu-id="ce9b4-161">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce9b4-161">Requirement</span></span> | <span data-ttu-id="ce9b4-162">Wert</span><span class="sxs-lookup"><span data-stu-id="ce9b4-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce9b4-163">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce9b4-163">Minimum supported client</span></span><br/> | <span data-ttu-id="ce9b4-164">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce9b4-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ce9b4-165">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce9b4-165">Minimum supported server</span></span><br/> | <span data-ttu-id="ce9b4-166">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce9b4-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ce9b4-167">Header</span><span class="sxs-lookup"><span data-stu-id="ce9b4-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce9b4-168"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="ce9b4-168"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce9b4-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce9b4-169">See also</span></span>

<dl> <dt>

<span data-ttu-id="ce9b4-170">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ce9b4-171">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-171">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="ce9b4-172">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-172">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="ce9b4-173">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-173">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="ce9b4-174">**WM \_ syskeydown**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-174">**WM\_SYSKEYDOWN**</span></span>](wm-syskeydown.md)
</dt> <dt>

<span data-ttu-id="ce9b4-175">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ce9b4-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ce9b4-176">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="ce9b4-176">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

