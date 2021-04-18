---
title: WM_SYSKEYDOWN Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn der Benutzer die Taste F10 drückt (wodurch die Menüleiste aktiviert wird) oder die Alt-Taste gedrückt hält und dann eine andere Taste drückt.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- Tastatur-und Maus Eingaben für WM_SYSKEYDOWN Nachricht
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341389"
---
# <a name="wm_syskeydown-message"></a><span data-ttu-id="9c52f-104">WM- \_ syskeydown-Meldung</span><span class="sxs-lookup"><span data-stu-id="9c52f-104">WM\_SYSKEYDOWN message</span></span>

<span data-ttu-id="9c52f-105">Wird an das Fenster mit dem Tastaturfokus gesendet, wenn der Benutzer die Taste F10 drückt (wodurch die Menüleiste aktiviert wird) oder die Alt-Taste gedrückt hält und dann eine andere Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="9c52f-105">Posted to the window with the keyboard focus when the user presses the F10 key (which activates the menu bar) or holds down the ALT key and then presses another key.</span></span> <span data-ttu-id="9c52f-106">Es tritt auch auf, wenn derzeit kein Fenster den Tastaturfokus besitzt. in diesem Fall wird die **WM- \_ syskeydown** -Nachricht an das aktive Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="9c52f-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYDOWN** message is sent to the active window.</span></span> <span data-ttu-id="9c52f-107">Das Fenster, in dem die Meldung empfangen wird, kann durch Überprüfen des Kontext Codes im *LPARAM* -Parameter zwischen diesen beiden Kontexten unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="9c52f-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a><span data-ttu-id="9c52f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c52f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c52f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c52f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c52f-110">Der Code für den virtuellen Schlüssel der Taste, die gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="9c52f-110">The virtual-key code of the key being pressed.</span></span> <span data-ttu-id="9c52f-111">Siehe [**virtuelle Schlüssel Codes**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9c52f-111">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c52f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c52f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c52f-113">Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c52f-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="9c52f-114">Bits</span><span class="sxs-lookup"><span data-stu-id="9c52f-114">Bits</span></span>  | <span data-ttu-id="9c52f-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9c52f-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c52f-116">0-15</span><span class="sxs-lookup"><span data-stu-id="9c52f-116">0-15</span></span>  | <span data-ttu-id="9c52f-117">Die Wiederholungs Anzahl für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="9c52f-117">The repeat count for the current message.</span></span> <span data-ttu-id="9c52f-118">Der Wert gibt an, wie oft der Tastatur Schlag automatisch durchgeführt wird, wenn der Benutzer die Taste gedrückt hält.</span><span class="sxs-lookup"><span data-stu-id="9c52f-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="9c52f-119">Wenn die Tastatureingabe lang genug gehalten wird, werden mehrere Nachrichten gesendet.</span><span class="sxs-lookup"><span data-stu-id="9c52f-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="9c52f-120">Die Wiederholungs Anzahl ist jedoch nicht kumulativ.</span><span class="sxs-lookup"><span data-stu-id="9c52f-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="9c52f-121">16-23</span><span class="sxs-lookup"><span data-stu-id="9c52f-121">16-23</span></span> | <span data-ttu-id="9c52f-122">Der Überprüfungs Code.</span><span class="sxs-lookup"><span data-stu-id="9c52f-122">The scan code.</span></span> <span data-ttu-id="9c52f-123">Der Wert hängt vom OEM ab.</span><span class="sxs-lookup"><span data-stu-id="9c52f-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="9c52f-124">24</span><span class="sxs-lookup"><span data-stu-id="9c52f-124">24</span></span>    | <span data-ttu-id="9c52f-125">Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9c52f-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="9c52f-126">Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="9c52f-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="9c52f-127">25-28</span><span class="sxs-lookup"><span data-stu-id="9c52f-127">25-28</span></span> | <span data-ttu-id="9c52f-128">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="9c52f-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9c52f-129">29</span><span class="sxs-lookup"><span data-stu-id="9c52f-129">29</span></span>    | <span data-ttu-id="9c52f-130">Der Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="9c52f-130">The context code.</span></span> <span data-ttu-id="9c52f-131">Der Wert ist 1, wenn die Alt-Taste gedrückt ist, während die Taste gedrückt wird. der Wert ist 0, wenn die **WM- \_ syskeydown** -Nachricht im aktiven Fenster gepostet wird, da kein Fenster den Tastaturfokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="9c52f-131">The value is 1 if the ALT key is down while the key is pressed; it is 0 if the **WM\_SYSKEYDOWN** message is posted to the active window because no window has the keyboard focus.</span></span>                                                                  |
| <span data-ttu-id="9c52f-132">30</span><span class="sxs-lookup"><span data-stu-id="9c52f-132">30</span></span>    | <span data-ttu-id="9c52f-133">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="9c52f-133">The previous key state.</span></span> <span data-ttu-id="9c52f-134">Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird, oder wenn der Schlüssel auf "0" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9c52f-134">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="9c52f-135">31</span><span class="sxs-lookup"><span data-stu-id="9c52f-135">31</span></span>    | <span data-ttu-id="9c52f-136">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="9c52f-136">The transition state.</span></span> <span data-ttu-id="9c52f-137">Der Wert für eine **WM- \_ syskeydown** -Nachricht ist immer 0.</span><span class="sxs-lookup"><span data-stu-id="9c52f-137">The value is always 0 for a **WM\_SYSKEYDOWN** message.</span></span>                                                                                                                                                                                         |

<span data-ttu-id="9c52f-138">Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="9c52f-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c52f-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c52f-139">Return value</span></span>

<span data-ttu-id="9c52f-140">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="9c52f-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c52f-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c52f-141">Remarks</span></span>

<span data-ttu-id="9c52f-142">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion untersucht den angegebenen Schlüssel und generiert eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Nachricht, wenn der Schlüssel entweder Tab oder eingegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9c52f-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function examines the specified key and generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message if the key is either TAB or ENTER.</span></span>

<span data-ttu-id="9c52f-143">Wenn der Kontext Code NULL ist, kann die Nachricht an die [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) -Funktion übermittelt werden, die Sie behandelt, als ob es sich um eine normale Schlüssel Nachricht anstatt um eine Zeichen Schlüssel Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="9c52f-143">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="9c52f-144">Dies ermöglicht das Verwenden von Zugriffstasten für das aktive Fenster, auch wenn das aktive Fenster nicht über den Tastaturfokus verfügt.</span><span class="sxs-lookup"><span data-stu-id="9c52f-144">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="9c52f-145">Aufgrund der automatischen Wiederholung können mehr als eine **WM- \_ syskeydown** -Meldung auftreten, bevor eine [**WM- \_ syskeyup**](wm-syskeyup.md) -Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c52f-145">Because of automatic repeat, more than one **WM\_SYSKEYDOWN** message may occur before a [**WM\_SYSKEYUP**](wm-syskeyup.md) message is sent.</span></span> <span data-ttu-id="9c52f-146">Der vorherige Schlüssel Zustand (Bit 30) kann verwendet werden, um zu bestimmen, ob die **WM- \_ syskeydown** -Meldung den ersten nach-unten-Übergang oder einen wiederholten Down-Übergang angibt.</span><span class="sxs-lookup"><span data-stu-id="9c52f-146">The previous key state (bit 30) can be used to determine whether the **WM\_SYSKEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="9c52f-147">Für erweiterte 101-und 102-Schlüssel-Tastaturen sind erweiterte Schlüssel die Rechte ALT-Taste und die STRG-Taste im Hauptabschnitt der Tastatur. die Tasten "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Keypad. und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur.</span><span class="sxs-lookup"><span data-stu-id="9c52f-147">For enhanced 101- and 102-key keyboards, enhanced keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="9c52f-148">Andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="9c52f-148">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="9c52f-149">Diese Meldung wird auch immer dann gesendet, wenn der Benutzer die Taste F10 ohne die Alt-Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="9c52f-149">This message is also sent whenever the user presses the F10 key without the ALT key.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c52f-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c52f-150">Requirements</span></span>



| <span data-ttu-id="9c52f-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c52f-151">Requirement</span></span> | <span data-ttu-id="9c52f-152">Wert</span><span class="sxs-lookup"><span data-stu-id="9c52f-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c52f-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9c52f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="9c52f-154">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c52f-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9c52f-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9c52f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="9c52f-156">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9c52f-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9c52f-157">Header</span><span class="sxs-lookup"><span data-stu-id="9c52f-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c52f-158"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="9c52f-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c52f-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c52f-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="9c52f-160">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="9c52f-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9c52f-161">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="9c52f-161">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9c52f-162">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="9c52f-162">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="9c52f-163">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="9c52f-163">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="9c52f-164">**WM- \_ syskeyup**</span><span class="sxs-lookup"><span data-stu-id="9c52f-164">**WM\_SYSKEYUP**</span></span>](wm-syskeyup.md)
</dt> <dt>

<span data-ttu-id="9c52f-165">**Licher**</span><span class="sxs-lookup"><span data-stu-id="9c52f-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9c52f-166">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="9c52f-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

