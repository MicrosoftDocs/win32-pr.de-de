---
title: WM_KEYUP Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine nicht-System Taste losgelassen wird. Eine nicht-System Taste ist ein Schlüssel, der gedrückt wird, wenn die Alt-Taste nicht gedrückt wird, oder eine Tastatur Taste, die gedrückt wird, wenn ein Fenster den Tastaturfokus besitzt.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- Tastatur-und Maus Eingaben für WM_KEYUP Nachricht
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391792"
---
# <a name="wm_keyup-message"></a><span data-ttu-id="8f617-105">WM- \_ keyupmeldung</span><span class="sxs-lookup"><span data-stu-id="8f617-105">WM\_KEYUP message</span></span>

<span data-ttu-id="8f617-106">Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine nicht-System Taste losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="8f617-106">Posted to the window with the keyboard focus when a nonsystem key is released.</span></span> <span data-ttu-id="8f617-107">Eine nicht-System Taste ist ein Schlüssel, der gedrückt wird, wenn die Alt-Taste *nicht* gedrückt wird, oder eine Tastatur Taste, die gedrückt wird, wenn ein Fenster den Tastaturfokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="8f617-107">A nonsystem key is a key that is pressed when the ALT key is *not* pressed, or a keyboard key that is pressed when a window has the keyboard focus.</span></span>


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a><span data-ttu-id="8f617-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f617-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f617-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f617-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f617-110">Der Code des virtuellen Schlüssels des nicht System Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="8f617-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="8f617-111">Siehe [virtuelle Schlüssel Codes](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8f617-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f617-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f617-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f617-113">Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f617-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="8f617-114">Bits</span><span class="sxs-lookup"><span data-stu-id="8f617-114">Bits</span></span>  | <span data-ttu-id="8f617-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8f617-115">Meaning</span></span>                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f617-116">0-15</span><span class="sxs-lookup"><span data-stu-id="8f617-116">0-15</span></span>  | <span data-ttu-id="8f617-117">Die Wiederholungs Anzahl für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="8f617-117">The repeat count for the current message.</span></span> <span data-ttu-id="8f617-118">Der Wert gibt an, wie oft der Tastatur Schlag automatisch durchgeführt wird, wenn der Benutzer die Taste gedrückt hält.</span><span class="sxs-lookup"><span data-stu-id="8f617-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="8f617-119">Die Wiederholungs Anzahl ist für eine WM- **\_ KeyUp** -Meldung immer 1.</span><span class="sxs-lookup"><span data-stu-id="8f617-119">The repeat count is always 1 for a **WM\_KEYUP** message.</span></span> |
| <span data-ttu-id="8f617-120">16-23</span><span class="sxs-lookup"><span data-stu-id="8f617-120">16-23</span></span> | <span data-ttu-id="8f617-121">Der Überprüfungs Code.</span><span class="sxs-lookup"><span data-stu-id="8f617-121">The scan code.</span></span> <span data-ttu-id="8f617-122">Der Wert hängt vom OEM ab.</span><span class="sxs-lookup"><span data-stu-id="8f617-122">The value depends on the OEM.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="8f617-123">24</span><span class="sxs-lookup"><span data-stu-id="8f617-123">24</span></span>    | <span data-ttu-id="8f617-124">Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8f617-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="8f617-125">Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="8f617-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>         |
| <span data-ttu-id="8f617-126">25-28</span><span class="sxs-lookup"><span data-stu-id="8f617-126">25-28</span></span> | <span data-ttu-id="8f617-127">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="8f617-127">Reserved; do not use.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="8f617-128">29</span><span class="sxs-lookup"><span data-stu-id="8f617-128">29</span></span>    | <span data-ttu-id="8f617-129">Der Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="8f617-129">The context code.</span></span> <span data-ttu-id="8f617-130">Der Wert für eine **WM- \_ KeyUp** -Nachricht ist immer 0.</span><span class="sxs-lookup"><span data-stu-id="8f617-130">The value is always 0 for a **WM\_KEYUP** message.</span></span>                                                                                                                                             |
| <span data-ttu-id="8f617-131">30</span><span class="sxs-lookup"><span data-stu-id="8f617-131">30</span></span>    | <span data-ttu-id="8f617-132">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="8f617-132">The previous key state.</span></span> <span data-ttu-id="8f617-133">Der Wert ist für eine WM- **\_ KeyUp** -Meldung immer 1.</span><span class="sxs-lookup"><span data-stu-id="8f617-133">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                       |
| <span data-ttu-id="8f617-134">31</span><span class="sxs-lookup"><span data-stu-id="8f617-134">31</span></span>    | <span data-ttu-id="8f617-135">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="8f617-135">The transition state.</span></span> <span data-ttu-id="8f617-136">Der Wert ist für eine WM- **\_ KeyUp** -Meldung immer 1.</span><span class="sxs-lookup"><span data-stu-id="8f617-136">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                         |

<span data-ttu-id="8f617-137">Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="8f617-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f617-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f617-138">Return value</span></span>

<span data-ttu-id="8f617-139">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8f617-139">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f617-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f617-140">Remarks</span></span>

<span data-ttu-id="8f617-141">Die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion sendet eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster der obersten Ebene, wenn die F10-Taste oder die Alt-Taste losgelassen wurde.</span><span class="sxs-lookup"><span data-stu-id="8f617-141">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="8f617-142">Der *wParam* -Parameter der Nachricht ist auf SC \_ keymenu festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8f617-142">The *wParam* parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="8f617-143">Für erweiterte 101-und 102-Key-Tastaturen sind erweiterte Schlüssel die Rechte ALT-Taste und die STRG-Taste im Hauptabschnitt der Tastatur. die Tasten "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Keypad. und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur.</span><span class="sxs-lookup"><span data-stu-id="8f617-143">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="8f617-144">Andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="8f617-144">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="8f617-145">Anwendungen müssen *wParam* an [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) übergeben, ohne Sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8f617-145">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f617-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f617-146">Requirements</span></span>



| <span data-ttu-id="8f617-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f617-147">Requirement</span></span> | <span data-ttu-id="8f617-148">Wert</span><span class="sxs-lookup"><span data-stu-id="8f617-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f617-149">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f617-149">Minimum supported client</span></span><br/> | <span data-ttu-id="8f617-150">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f617-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8f617-151">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f617-151">Minimum supported server</span></span><br/> | <span data-ttu-id="8f617-152">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f617-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8f617-153">Header</span><span class="sxs-lookup"><span data-stu-id="8f617-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f617-154"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="8f617-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f617-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f617-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f617-156">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8f617-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8f617-157">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="8f617-157">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="8f617-158">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="8f617-158">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="8f617-159">**WM- \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="8f617-159">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="8f617-160">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="8f617-160">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="8f617-161">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8f617-161">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8f617-162">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="8f617-162">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

