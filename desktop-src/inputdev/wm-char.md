---
title: WM_CHAR Meldung (Winuser. h)
description: Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine WM- \_ KeyDown-Meldung von der translatemess-Funktion übersetzt wird. Die Meldung "WM \_ char" enthält den Zeichencode der Taste, die gedrückt wurde.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- Tastatur-und Maus Eingaben für WM_CHAR Nachricht
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354182"
---
# <a name="wm_char-message"></a><span data-ttu-id="c17b2-105">WM- \_ char-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c17b2-105">WM\_CHAR message</span></span>

<span data-ttu-id="c17b2-106">Wird an das Fenster mit dem Tastaturfokus gesendet, wenn eine [**WM- \_ KeyDown**](wm-keydown.md) -Meldung von der [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion übersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c17b2-106">Posted to the window with the keyboard focus when a [**WM\_KEYDOWN**](wm-keydown.md) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="c17b2-107">Die Meldung " **WM \_ char** " enthält den Zeichencode der Taste, die gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="c17b2-107">The **WM\_CHAR** message contains the character code of the key that was pressed.</span></span>


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a><span data-ttu-id="c17b2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c17b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c17b2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c17b2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c17b2-110">Der Zeichencode des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="c17b2-110">The character code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="c17b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c17b2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c17b2-112">Die Wiederholungs Anzahl, der Überprüfungs Code, das erweiterte schlüsselflag, der Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c17b2-112">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="c17b2-113">Bits</span><span class="sxs-lookup"><span data-stu-id="c17b2-113">Bits</span></span>  | <span data-ttu-id="c17b2-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c17b2-114">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c17b2-115">0-15</span><span class="sxs-lookup"><span data-stu-id="c17b2-115">0-15</span></span>  | <span data-ttu-id="c17b2-116">Die Wiederholungs Anzahl für die aktuelle Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c17b2-116">The repeat count for the current message.</span></span> <span data-ttu-id="c17b2-117">Der Wert gibt an, wie oft der Tastatur Schlag automatisch durchgeführt wird, wenn der Benutzer die Taste gedrückt hält.</span><span class="sxs-lookup"><span data-stu-id="c17b2-117">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="c17b2-118">Wenn die Tastatureingabe lang genug gehalten wird, werden mehrere Nachrichten gesendet.</span><span class="sxs-lookup"><span data-stu-id="c17b2-118">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="c17b2-119">Die Wiederholungs Anzahl ist jedoch nicht kumulativ.</span><span class="sxs-lookup"><span data-stu-id="c17b2-119">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="c17b2-120">16-23</span><span class="sxs-lookup"><span data-stu-id="c17b2-120">16-23</span></span> | <span data-ttu-id="c17b2-121">Der Überprüfungs Code.</span><span class="sxs-lookup"><span data-stu-id="c17b2-121">The scan code.</span></span> <span data-ttu-id="c17b2-122">Der Wert hängt vom OEM ab.</span><span class="sxs-lookup"><span data-stu-id="c17b2-122">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="c17b2-123">24</span><span class="sxs-lookup"><span data-stu-id="c17b2-123">24</span></span>    | <span data-ttu-id="c17b2-124">Gibt an, ob der Schlüssel ein erweiterter Schlüssel ist, z. b. die Rechte ALT-Taste und die STRG-Taste, die auf einer erweiterten 101-oder 102-Tastatur-Tastatur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c17b2-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="c17b2-125">Der Wert ist 1, wenn es sich um einen erweiterten Schlüssel handelt. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="c17b2-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="c17b2-126">25-28</span><span class="sxs-lookup"><span data-stu-id="c17b2-126">25-28</span></span> | <span data-ttu-id="c17b2-127">Bleiben Verwenden Sie nicht.</span><span class="sxs-lookup"><span data-stu-id="c17b2-127">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c17b2-128">29</span><span class="sxs-lookup"><span data-stu-id="c17b2-128">29</span></span>    | <span data-ttu-id="c17b2-129">Der Kontext Code.</span><span class="sxs-lookup"><span data-stu-id="c17b2-129">The context code.</span></span> <span data-ttu-id="c17b2-130">Der Wert ist 1, wenn die Alt-Taste gedrückt gehalten wird, während die Taste gedrückt wird. Andernfalls ist der Wert 0.</span><span class="sxs-lookup"><span data-stu-id="c17b2-130">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="c17b2-131">30</span><span class="sxs-lookup"><span data-stu-id="c17b2-131">30</span></span>    | <span data-ttu-id="c17b2-132">Der vorherige Schlüssel Zustand.</span><span class="sxs-lookup"><span data-stu-id="c17b2-132">The previous key state.</span></span> <span data-ttu-id="c17b2-133">Der Wert ist 1, wenn der Schlüssel vor dem Senden der Nachricht nicht angezeigt wird, oder wenn der Schlüssel auf "0" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c17b2-133">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="c17b2-134">31</span><span class="sxs-lookup"><span data-stu-id="c17b2-134">31</span></span>    | <span data-ttu-id="c17b2-135">Der Übergangszustand.</span><span class="sxs-lookup"><span data-stu-id="c17b2-135">The transition state.</span></span> <span data-ttu-id="c17b2-136">Der Wert ist 1, wenn der Schlüssel freigegeben wird, oder der Wert ist 0, wenn die Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="c17b2-136">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="c17b2-137">Weitere Details finden Sie unter [KeyStroke-Nachrichtenflags](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="c17b2-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c17b2-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c17b2-138">Return value</span></span>

<span data-ttu-id="c17b2-139">Eine Anwendung sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c17b2-139">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="c17b2-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c17b2-140">Example</span></span>

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
<span data-ttu-id="c17b2-141">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="c17b2-141">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="c17b2-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c17b2-142">Remarks</span></span>

<span data-ttu-id="c17b2-143">Die Meldung " **WM \_ char** " verwendet UTF (Unicode Transformation Format)-16.</span><span class="sxs-lookup"><span data-stu-id="c17b2-143">The **WM\_CHAR** message uses Unicode Transformation Format (UTF)-16.</span></span>

<span data-ttu-id="c17b2-144">Es gibt nicht notwendigerweise eine eins-zu-eins-Entsprechung zwischen den gedrückten Schlüsseln und den generierten Zeichen Meldungen. Daher sind die Informationen im höherwertigen Wort des *LPARAM* -Parameters für Anwendungen in der Regel nicht nützlich.</span><span class="sxs-lookup"><span data-stu-id="c17b2-144">There is not necessarily a one-to-one correspondence between keys pressed and character messages generated, and so the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="c17b2-145">Die Informationen im höherwertigen Wort gelten nur für die letzte [**WM- \_ KeyDown**](wm-keydown.md) -Nachricht, die vor der Bereitstellung der **WM- \_ char** -Nachricht steht.</span><span class="sxs-lookup"><span data-stu-id="c17b2-145">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_CHAR** message.</span></span>

<span data-ttu-id="c17b2-146">Erweiterte Schlüssel für erweiterte 101-und 102-keytastaturen sind die Rechte ALT-Taste und die Rechte STRG-Taste im Hauptabschnitt der Tastatur. die Eingaben "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Tastatur und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur.</span><span class="sxs-lookup"><span data-stu-id="c17b2-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="c17b2-147">Einige andere Tastaturen unterstützen möglicherweise das Extended-Key-Bit im *LPARAM* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="c17b2-147">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="c17b2-148">Die [**WM \_ UNICHAR**](wm-unichar.md) -Nachricht ist mit **WM \_ char** identisch, mit der Ausnahme, dass Sie UTF-32 verwendet.</span><span class="sxs-lookup"><span data-stu-id="c17b2-148">The [**WM\_UNICHAR**](wm-unichar.md) message is the same as **WM\_CHAR**, except it uses UTF-32.</span></span> <span data-ttu-id="c17b2-149">Er ist darauf ausgelegt, Unicode-Zeichen an ANSI-Fenster zu senden oder bereitzustellen, und er kann Unicode-Zeichen der ergänzenden Ebene verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c17b2-149">It is designed to send or post Unicode characters to ANSI windows, and it can handle Unicode Supplementary Plane characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c17b2-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c17b2-150">Requirements</span></span>



| <span data-ttu-id="c17b2-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c17b2-151">Requirement</span></span> | <span data-ttu-id="c17b2-152">Wert</span><span class="sxs-lookup"><span data-stu-id="c17b2-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c17b2-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c17b2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c17b2-154">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c17b2-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c17b2-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c17b2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c17b2-156">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c17b2-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c17b2-157">Header</span><span class="sxs-lookup"><span data-stu-id="c17b2-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="c17b2-158"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="c17b2-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c17b2-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c17b2-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="c17b2-160">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="c17b2-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c17b2-161">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="c17b2-161">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="c17b2-162">**WM- \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="c17b2-162">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="c17b2-163">**WM \_ UNICHAR**</span><span class="sxs-lookup"><span data-stu-id="c17b2-163">**WM\_UNICHAR**</span></span>](wm-unichar.md)
</dt> <dt>

<span data-ttu-id="c17b2-164">**Licher**</span><span class="sxs-lookup"><span data-stu-id="c17b2-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c17b2-165">Tastatureingabe</span><span class="sxs-lookup"><span data-stu-id="c17b2-165">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

