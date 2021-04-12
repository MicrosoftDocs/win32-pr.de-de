---
title: WM_SYSCHAR Meldung (Winuser. h)
description: Wird im Fenster mit dem Tastaturfokus gepostet, wenn eine WM- \_ syskeydown-Meldung von der translatemess-Funktion übersetzt wird.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR von Meldungs Menüs und anderen Ressourcen
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519196"
---
# <a name="wm_syschar-message"></a><span data-ttu-id="f8fba-104">WM- \_ syschar-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f8fba-104">WM\_SYSCHAR message</span></span>

<span data-ttu-id="f8fba-105">Wird im Fenster mit dem Tastaturfokus gepostet, wenn eine [**WM- \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown) -Meldung von der [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f8fba-105">Posted to the window with the keyboard focus when a [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="f8fba-106">Er gibt den Zeichencode eines System Zeichen Schlüssels an, bei dem es sich um einen Zeichen Schlüssel handelt, der gedrückt wird, während die Alt-Taste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="f8fba-106">It specifies the character code of a system character key   that is, a character key that is pressed while the ALT key is down.</span></span>


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a><span data-ttu-id="f8fba-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8fba-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8fba-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f8fba-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8fba-109">Der Zeichencode der Fenstermenü Taste.</span><span class="sxs-lookup"><span data-stu-id="f8fba-109">The character code of the window menu key.</span></span>

</dd> <dt>

<span data-ttu-id="f8fba-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8fba-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8fba-111">Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f8fba-111">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="f8fba-112">Bits</span><span class="sxs-lookup"><span data-stu-id="f8fba-112">Bits</span></span>                                                                             | <span data-ttu-id="f8fba-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f8fba-113">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8fba-114"><dt>0 15</dt></span><span class="sxs-lookup"><span data-stu-id="f8fba-114"><dt>0 15</dt></span></span> </dl>  | <span data-ttu-id="f8fba-115">Die Wiederholungs Anzahl für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="f8fba-115">The repeat count for the current message.</span></span> <span data-ttu-id="f8fba-116">Der Wert gibt an, wie oft der Tastatur Schlag automatisch wiederholt wird, weil der Benutzer die Taste gedrückt hält.</span><span class="sxs-lookup"><span data-stu-id="f8fba-116">The value is the number of times the keystroke was auto-repeated as a result of the user holding down the key.</span></span> <span data-ttu-id="f8fba-117">Wenn die Tastatureingabe lang genug gehalten wird, werden mehrere Nachrichten gesendet.</span><span class="sxs-lookup"><span data-stu-id="f8fba-117">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="f8fba-118">Die Wiederholungs Anzahl ist jedoch nicht kumulativ.</span><span class="sxs-lookup"><span data-stu-id="f8fba-118">However, the repeat count is not cumulative.</span></span><br/> |
| <dl> <span data-ttu-id="f8fba-119"><dt>16 23</dt></span><span class="sxs-lookup"><span data-stu-id="f8fba-119"><dt>16 23</dt></span></span> </dl> | <span data-ttu-id="f8fba-120">Der Überprüfungs Code.</span><span class="sxs-lookup"><span data-stu-id="f8fba-120">The scan code.</span></span> <span data-ttu-id="f8fba-121">Der Wert hängt vom Originalgerätehersteller (OEM) ab.</span><span class="sxs-lookup"><span data-stu-id="f8fba-121">The value depends on the original equipment manufacturer (OEM).</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="f8fba-122"><dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="f8fba-122"><dt>24</dt></span></span> </dl>    | <span data-ttu-id="f8fba-123">Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f8fba-123">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="f8fba-124">Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="f8fba-124">The value is 1 if it is an extended key; otherwise, it is 0.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="f8fba-125"><dt>25 28</dt></span><span class="sxs-lookup"><span data-stu-id="f8fba-125"><dt>25 28</dt></span></span> </dl> | <span data-ttu-id="f8fba-126">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="f8fba-126">Reserved; do not use.</span></span><br/>                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="f8fba-127"><dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="f8fba-127"><dt>29</dt></span></span> </dl>    | <span data-ttu-id="f8fba-128">Der Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="f8fba-128">The context code.</span></span> <span data-ttu-id="f8fba-129">Der Wert ist 1, wenn die Alt-Taste gedrückt gehalten wird, während die Taste gedrückt wird. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="f8fba-129">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="f8fba-130"><dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="f8fba-130"><dt>30</dt></span></span> </dl>    | <span data-ttu-id="f8fba-131">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="f8fba-131">The previous key state.</span></span> <span data-ttu-id="f8fba-132">Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird, oder wenn der Schlüssel auf "0" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f8fba-132">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span><br/>                                                                                                                                                      |
| <dl> <span data-ttu-id="f8fba-133"><dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="f8fba-133"><dt>31</dt></span></span> </dl>    | <span data-ttu-id="f8fba-134">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="f8fba-134">The transition state.</span></span> <span data-ttu-id="f8fba-135">Der Wert ist 1, wenn der Schlüssel freigegeben wird, oder der Wert ist 0, wenn die Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="f8fba-135">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span><br/>                                                                                                                                                              |

<span data-ttu-id="f8fba-136">Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="f8fba-136">For more detail, see [Keystroke Message Flags](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8fba-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f8fba-137">Return value</span></span>

<span data-ttu-id="f8fba-138">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f8fba-138">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8fba-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8fba-139">Remarks</span></span>

<span data-ttu-id="f8fba-140">Wenn der Kontext Code 0 (null) ist, kann die Nachricht an die [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) -Funktion übermittelt werden, die Sie behandelt, als ob es sich um eine Standard Schlüsselnachricht anstelle einer System-Zeichen Schlüssel Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="f8fba-140">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a standard key message instead of a system character-key message.</span></span> <span data-ttu-id="f8fba-141">Dies ermöglicht das Verwenden von Zugriffstasten für das aktive Fenster, auch wenn das aktive Fenster nicht über den Tastaturfokus verfügt.</span><span class="sxs-lookup"><span data-stu-id="f8fba-141">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="f8fba-142">Für erweiterte 101-und 102-Key-Tastaturen sind erweiterte Schlüssel die Rechte ALT-Taste und die STRG-Taste im Hauptabschnitt der Tastatur. die Eingaben "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Tastatur die Druck-Scrn-Taste; die Pause-Taste. der NumLock-Schlüssel; und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur.</span><span class="sxs-lookup"><span data-stu-id="f8fba-142">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; the PRINT SCRN key; the BREAK key; the NUMLOCK key; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="f8fba-143">Andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im-Parameter.</span><span class="sxs-lookup"><span data-stu-id="f8fba-143">Other keyboards may support the extended-key bit in the parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8fba-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f8fba-144">Requirements</span></span>



| <span data-ttu-id="f8fba-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f8fba-145">Requirement</span></span> | <span data-ttu-id="f8fba-146">Wert</span><span class="sxs-lookup"><span data-stu-id="f8fba-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8fba-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f8fba-147">Minimum supported client</span></span><br/> | <span data-ttu-id="f8fba-148">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8fba-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f8fba-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f8fba-149">Minimum supported server</span></span><br/> | <span data-ttu-id="f8fba-150">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f8fba-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f8fba-151">Header</span><span class="sxs-lookup"><span data-stu-id="f8fba-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8fba-152"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f8fba-152"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8fba-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8fba-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="f8fba-154">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="f8fba-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8fba-155">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="f8fba-155">**TranslateAccelerator**</span></span>](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="f8fba-156">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="f8fba-156">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="f8fba-157">**WM \_ syskeydown**</span><span class="sxs-lookup"><span data-stu-id="f8fba-157">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

<span data-ttu-id="f8fba-158">**Licher**</span><span class="sxs-lookup"><span data-stu-id="f8fba-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f8fba-159">Tastaturkürzel</span><span class="sxs-lookup"><span data-stu-id="f8fba-159">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

