---
title: WM_KEYDOWN Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine nicht-System Taste gedrückt wird. Eine nicht-System Taste ist ein Schlüssel, der gedrückt wird, wenn die Alt-Taste nicht gedrückt wird.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- Tastatur-und Maus Eingaben für WM_KEYDOWN Nachricht
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359791"
---
# <a name="wm_keydown-message"></a><span data-ttu-id="7358c-105">WM- \_ KeyDown-Meldung</span><span class="sxs-lookup"><span data-stu-id="7358c-105">WM\_KEYDOWN message</span></span>

<span data-ttu-id="7358c-106">Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine nicht-System Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="7358c-106">Posted to the window with the keyboard focus when a nonsystem key is pressed.</span></span> <span data-ttu-id="7358c-107">Eine nicht-System Taste ist ein Schlüssel, der gedrückt wird, wenn die Alt-Taste nicht gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="7358c-107">A nonsystem key is a key that is pressed when the ALT key is not pressed.</span></span>


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a><span data-ttu-id="7358c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7358c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7358c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7358c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7358c-110">Der Code des virtuellen Schlüssels des nicht System Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="7358c-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="7358c-111">Siehe [virtuelle Schlüssel Codes](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7358c-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="7358c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7358c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7358c-113">Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie im folgenden gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7358c-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown following.</span></span>



| <span data-ttu-id="7358c-114">Bits</span><span class="sxs-lookup"><span data-stu-id="7358c-114">Bits</span></span>  | <span data-ttu-id="7358c-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7358c-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7358c-116">0-15</span><span class="sxs-lookup"><span data-stu-id="7358c-116">0-15</span></span>  | <span data-ttu-id="7358c-117">Die Wiederholungs Anzahl für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7358c-117">The repeat count for the current message.</span></span> <span data-ttu-id="7358c-118">Der Wert gibt an, wie oft der Tastatur Schlag automatisch durchgeführt wird, wenn der Benutzer die Taste gedrückt hält.</span><span class="sxs-lookup"><span data-stu-id="7358c-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="7358c-119">Wenn die Tastatureingabe lang genug gehalten wird, werden mehrere Nachrichten gesendet.</span><span class="sxs-lookup"><span data-stu-id="7358c-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="7358c-120">Die Wiederholungs Anzahl ist jedoch nicht kumulativ.</span><span class="sxs-lookup"><span data-stu-id="7358c-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="7358c-121">16-23</span><span class="sxs-lookup"><span data-stu-id="7358c-121">16-23</span></span> | <span data-ttu-id="7358c-122">Der Überprüfungs Code.</span><span class="sxs-lookup"><span data-stu-id="7358c-122">The scan code.</span></span> <span data-ttu-id="7358c-123">Der Wert hängt vom OEM ab.</span><span class="sxs-lookup"><span data-stu-id="7358c-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="7358c-124">24</span><span class="sxs-lookup"><span data-stu-id="7358c-124">24</span></span>    | <span data-ttu-id="7358c-125">Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7358c-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="7358c-126">Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="7358c-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="7358c-127">25-28</span><span class="sxs-lookup"><span data-stu-id="7358c-127">25-28</span></span> | <span data-ttu-id="7358c-128">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="7358c-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7358c-129">29</span><span class="sxs-lookup"><span data-stu-id="7358c-129">29</span></span>    | <span data-ttu-id="7358c-130">Der Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="7358c-130">The context code.</span></span> <span data-ttu-id="7358c-131">Der Wert für eine **WM- \_ KeyDown** -Nachricht ist immer 0.</span><span class="sxs-lookup"><span data-stu-id="7358c-131">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="7358c-132">30</span><span class="sxs-lookup"><span data-stu-id="7358c-132">30</span></span>    | <span data-ttu-id="7358c-133">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="7358c-133">The previous key state.</span></span> <span data-ttu-id="7358c-134">Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird, oder 0 (null), wenn der Schlüssel auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="7358c-134">The value is 1 if the key is down before the message is sent, or it is zero if the key is up.</span></span>                                                                                                                                                 |
| <span data-ttu-id="7358c-135">31</span><span class="sxs-lookup"><span data-stu-id="7358c-135">31</span></span>    | <span data-ttu-id="7358c-136">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="7358c-136">The transition state.</span></span> <span data-ttu-id="7358c-137">Der Wert für eine **WM- \_ KeyDown** -Nachricht ist immer 0.</span><span class="sxs-lookup"><span data-stu-id="7358c-137">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                            |

<span data-ttu-id="7358c-138">Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="7358c-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7358c-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7358c-139">Return value</span></span>

<span data-ttu-id="7358c-140">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="7358c-140">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="7358c-141">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7358c-141">Example</span></span>

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

<span data-ttu-id="7358c-142">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="7358c-142">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="7358c-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7358c-143">Remarks</span></span>

<span data-ttu-id="7358c-144">Wenn die F10-Taste gedrückt wird, legt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion ein internes Flag fest.</span><span class="sxs-lookup"><span data-stu-id="7358c-144">If the F10 key is pressed, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets an internal flag.</span></span> <span data-ttu-id="7358c-145">Wenn **defwindowproc** die [**WM- \_ KeyUp**](wm-keyup.md) -Nachricht empfängt, überprüft die Funktion, ob das interne Flag festgelegt ist, und sendet, wenn dies der Fall ist, eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Meldung an das Fenster der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="7358c-145">When **DefWindowProc** receives the [**WM\_KEYUP**](wm-keyup.md) message, the function checks whether the internal flag is set and, if so, sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window.</span></span> <span data-ttu-id="7358c-146">Der **WM \_ syscommand** -Parameter der Nachricht ist auf SC \_ keymenu festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7358c-146">The **WM\_SYSCOMMAND** parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="7358c-147">Aufgrund der autoretorf-Funktion werden möglicherweise mehr als eine **WM- \_ KeyDown** -Nachricht gesendet, bevor eine [**WM- \_ KeyUp**](wm-keyup.md) -Nachricht gepostet wird.</span><span class="sxs-lookup"><span data-stu-id="7358c-147">Because of the autorepeat feature, more than one **WM\_KEYDOWN** message may be posted before a [**WM\_KEYUP**](wm-keyup.md) message is posted.</span></span> <span data-ttu-id="7358c-148">Der vorherige Schlüssel Zustand (Bit 30) kann verwendet werden, um zu bestimmen, ob die **WM- \_ KeyDown** -Meldung den ersten nach-unten-Übergang oder einen wiederholten Down-Übergang angibt.</span><span class="sxs-lookup"><span data-stu-id="7358c-148">The previous key state (bit 30) can be used to determine whether the **WM\_KEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="7358c-149">Für erweiterte 101-und 102-Key-Tastaturen sind erweiterte Schlüssel die Rechte ALT-Taste und die STRG-Taste im Hauptabschnitt der Tastatur. die Tasten "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Keypad. und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur.</span><span class="sxs-lookup"><span data-stu-id="7358c-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="7358c-150">Andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="7358c-150">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="7358c-151">Anwendungen müssen *wParam* an [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) übergeben, ohne Sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7358c-151">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="7358c-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7358c-152">Requirements</span></span>



| <span data-ttu-id="7358c-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7358c-153">Requirement</span></span> | <span data-ttu-id="7358c-154">Wert</span><span class="sxs-lookup"><span data-stu-id="7358c-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7358c-155">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7358c-155">Minimum supported client</span></span><br/> | <span data-ttu-id="7358c-156">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7358c-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7358c-157">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7358c-157">Minimum supported server</span></span><br/> | <span data-ttu-id="7358c-158">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7358c-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7358c-159">Header</span><span class="sxs-lookup"><span data-stu-id="7358c-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="7358c-160"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="7358c-160"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7358c-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7358c-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="7358c-162">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="7358c-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7358c-163">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="7358c-163">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="7358c-164">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="7358c-164">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="7358c-165">**WM \_ -Zeichen**</span><span class="sxs-lookup"><span data-stu-id="7358c-165">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="7358c-166">**WM- \_ KeyUp**</span><span class="sxs-lookup"><span data-stu-id="7358c-166">**WM\_KEYUP**</span></span>](wm-keyup.md)
</dt> <dt>

[<span data-ttu-id="7358c-167">**WM ( \_ syscommand)**</span><span class="sxs-lookup"><span data-stu-id="7358c-167">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="7358c-168">**Licher**</span><span class="sxs-lookup"><span data-stu-id="7358c-168">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7358c-169">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="7358c-169">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

