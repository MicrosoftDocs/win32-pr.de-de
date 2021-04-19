---
title: Verwenden von Tastatureingaben
description: In diesem Abschnitt werden Aufgaben behandelt, die mit Tastatureingaben verknüpft sind.
ms.assetid: d08e7f12-6595-4234-bfc4-08daad93e4c4
keywords:
- Benutzereingabe, Tastatureingabe
- Erfassen von Benutzereingaben, Tastatureingaben
- Tastatureingabe
- Tastatureingaben
- Zeichen Nachrichten
- Caretzeichen, Tastatureingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d76b3f90a626506430b91e7539069c6ecdf634c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341933"
---
# <a name="using-keyboard-input"></a><span data-ttu-id="d5413-109">Verwenden von Tastatureingaben</span><span class="sxs-lookup"><span data-stu-id="d5413-109">Using Keyboard Input</span></span>

<span data-ttu-id="d5413-110">Ein Fenster empfängt Tastatureingaben in Form von Tastatureingaben und Zeichen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d5413-110">A window receives keyboard input in the form of keystroke messages and character messages.</span></span> <span data-ttu-id="d5413-111">Die an das Fenster angefügte Nachrichten Schleife muss Code enthalten, um Tastatureingabe-Nachrichten in die entsprechenden Zeichen Nachrichten zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="d5413-111">The message loop attached to the window must include code to translate keystroke messages into the corresponding character messages.</span></span> <span data-ttu-id="d5413-112">Wenn im Fenster der Client Bereich Tastatureingaben angezeigt werden, sollte ein Caretzeichen erstellt und angezeigt werden, um die Position anzugeben, an der das nächste Zeichen eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d5413-112">If the window displays keyboard input in its client area, it should create and display a caret to indicate the position where the next character will be entered.</span></span> <span data-ttu-id="d5413-113">In den folgenden Abschnitten wird der Code beschrieben, der beim empfangen, verarbeiten und Anzeigen von Tastatureingaben beteiligt ist:</span><span class="sxs-lookup"><span data-stu-id="d5413-113">The following sections describe the code involved in receiving, processing, and displaying keyboard input:</span></span>

-   [<span data-ttu-id="d5413-114">Verarbeiten von Tastatureingaben</span><span class="sxs-lookup"><span data-stu-id="d5413-114">Processing Keystroke Messages</span></span>](#processing-keystroke-messages)
-   [<span data-ttu-id="d5413-115">Übersetzen von Zeichen Meldungen</span><span class="sxs-lookup"><span data-stu-id="d5413-115">Translating Character Messages</span></span>](#translating-character-messages)
-   [<span data-ttu-id="d5413-116">Verarbeiten von Zeichen Meldungen</span><span class="sxs-lookup"><span data-stu-id="d5413-116">Processing Character Messages</span></span>](#processing-character-messages)
-   [<span data-ttu-id="d5413-117">Verwenden der Einfügemarke</span><span class="sxs-lookup"><span data-stu-id="d5413-117">Using the Caret</span></span>](#using-the-caret)
-   [<span data-ttu-id="d5413-118">Anzeigen von Tastatureingaben</span><span class="sxs-lookup"><span data-stu-id="d5413-118">Displaying Keyboard Input</span></span>](#displaying-keyboard-input)

## <a name="processing-keystroke-messages"></a><span data-ttu-id="d5413-119">Verarbeiten von Tastatureingaben</span><span class="sxs-lookup"><span data-stu-id="d5413-119">Processing Keystroke Messages</span></span>

<span data-ttu-id="d5413-120">Die Fenster Prozedur des Fensters, das über den Tastaturfokus verfügt, empfängt Tastatureingaben, wenn der Benutzer die Tastatur eingibt.</span><span class="sxs-lookup"><span data-stu-id="d5413-120">The window procedure of the window that has the keyboard focus receives keystroke messages when the user types at the keyboard.</span></span> <span data-ttu-id="d5413-121">Die Tastatureingabe Nachrichten sind [**WM \_ KeyDown**](wm-keydown.md), [**WM \_ KeyUp**](wm-keyup.md), [**WM \_ syskeydown**](wm-syskeydown.md)und [**WM \_ syskeyup**](wm-syskeyup.md).</span><span class="sxs-lookup"><span data-stu-id="d5413-121">The keystroke messages are [**WM\_KEYDOWN**](wm-keydown.md), [**WM\_KEYUP**](wm-keyup.md), [**WM\_SYSKEYDOWN**](wm-syskeydown.md), and [**WM\_SYSKEYUP**](wm-syskeyup.md).</span></span> <span data-ttu-id="d5413-122">Eine typische Fenster Prozedur ignoriert alle Tastatureingabe-Meldungen außer **WM \_ KeyDown**.</span><span class="sxs-lookup"><span data-stu-id="d5413-122">A typical window procedure ignores all keystroke messages except **WM\_KEYDOWN**.</span></span> <span data-ttu-id="d5413-123">Das System sendet die **WM- \_ KeyDown** -Nachricht, wenn der Benutzer eine Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="d5413-123">The system posts the **WM\_KEYDOWN** message when the user presses a key.</span></span>

<span data-ttu-id="d5413-124">Wenn die Fenster Prozedur die [**WM- \_ KeyDown**](wm-keydown.md) -Nachricht empfängt, sollte Sie den Code der virtuellen Taste untersuchen, der die Nachricht begleitet, um zu bestimmen, wie die Tastatureingabe verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="d5413-124">When the window procedure receives the [**WM\_KEYDOWN**](wm-keydown.md) message, it should examine the virtual-key code that accompanies the message to determine how to process the keystroke.</span></span> <span data-ttu-id="d5413-125">Der Code des virtuellen Schlüssels befindet sich im *wParam* -Parameter der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d5413-125">The virtual-key code is in the message's *wParam* parameter.</span></span> <span data-ttu-id="d5413-126">In der Regel verarbeitet eine Anwendung nur Tastatureingaben, die von nicht-Zeichen Schlüsseln generiert werden, z. b. die Funktionstasten, die Cursor Verschiebungs Tasten und die speziellen Schlüssel, wie z. b. ins, del, Home und End.</span><span class="sxs-lookup"><span data-stu-id="d5413-126">Typically, an application processes only keystrokes generated by noncharacter keys, including the function keys, the cursor movement keys, and the special purpose keys such as INS, DEL, HOME, and END.</span></span>

<span data-ttu-id="d5413-127">Das folgende Beispiel zeigt das Fenster Prozedur Framework, das eine typische Anwendung verwendet, um Tastatureingaben zu empfangen und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d5413-127">The following example shows the window procedure framework that a typical application uses to receive and process keystroke messages.</span></span>


```
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT: 
                    
                    // Process the LEFT ARROW key. 
                     
                    break; 
 
                case VK_RIGHT: 
                    
                    // Process the RIGHT ARROW key. 
                     
                    break; 
 
                case VK_UP: 
                    
                    // Process the UP ARROW key. 
                     
                    break; 
 
                case VK_DOWN: 
                    
                    // Process the DOWN ARROW key. 
                     
                    break; 
 
                case VK_HOME: 
                    
                    // Process the HOME key. 
                     
                    break; 
 
                case VK_END: 
                    
                    // Process the END key. 
                     
                    break; 
 
                case VK_INSERT: 
                    
                    // Process the INS key. 
                     
                    break; 
 
                case VK_DELETE: 
                    
                    // Process the DEL key. 
                     
                    break; 
 
                case VK_F2: 
                    
                    // Process the F2 key. 
                    
                    break; 
 
                
                // Process other non-character keystrokes. 
                 
                default: 
                    break; 
            } 
```



## <a name="translating-character-messages"></a><span data-ttu-id="d5413-128">Übersetzen von Zeichen Meldungen</span><span class="sxs-lookup"><span data-stu-id="d5413-128">Translating Character Messages</span></span>

<span data-ttu-id="d5413-129">Jeder Thread, der Zeichen Eingaben vom Benutzer empfängt, muss die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion in der Nachrichten Schleife enthalten.</span><span class="sxs-lookup"><span data-stu-id="d5413-129">Any thread that receives character input from the user must include the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function in its message loop.</span></span> <span data-ttu-id="d5413-130">Diese Funktion untersucht den Code für den virtuellen Schlüssel einer Tastatureingabe-Nachricht und stellt eine Zeichen Nachricht in die Meldungs Warteschlange, wenn der Code einem Zeichen entspricht.</span><span class="sxs-lookup"><span data-stu-id="d5413-130">This function examines the virtual-key code of a keystroke message and, if the code corresponds to a character, places a character message into the message queue.</span></span> <span data-ttu-id="d5413-131">Die Zeichen Nachricht wird entfernt und bei der nächsten Iterationen der Nachrichten Schleife gesendet. der *wParam* -Parameter der Nachricht enthält den Zeichencode.</span><span class="sxs-lookup"><span data-stu-id="d5413-131">The character message is removed and dispatched on the next iteration of the message loop; the *wParam* parameter of the message contains the character code.</span></span>

<span data-ttu-id="d5413-132">Im Allgemeinen sollte die Nachrichten Schleife eines Threads die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion verwenden, um jede Nachricht und nicht nur die Nachrichten mit einem virtuellen Schlüssel zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="d5413-132">In general, a thread's message loop should use the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function to translate every message, not just virtual-key messages.</span></span> <span data-ttu-id="d5413-133">Obwohl **translatemess** keine Auswirkung auf andere Nachrichten Typen hat, wird sichergestellt, dass Tastatureingaben ordnungsgemäß übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="d5413-133">Although **TranslateMessage** has no effect on other types of messages, it guarantees that keyboard input is translated correctly.</span></span> <span data-ttu-id="d5413-134">Im folgenden Beispiel wird gezeigt, wie die **translatemess** -Funktion in eine typische Thread Nachrichten Schleife eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="d5413-134">The following example shows how to include the **TranslateMessage** function in a typical thread message loop.</span></span>


```
MSG msg;
BOOL bRet;

while (( bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0) 
{
    if (bRet == -1);
    {
        // handle the error and possibly exit
    }
    else
    { 
        if (TranslateAccelerator(hwndMain, haccl, &msg) == 0) 
        { 
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



## <a name="processing-character-messages"></a><span data-ttu-id="d5413-135">Verarbeiten von Zeichen Meldungen</span><span class="sxs-lookup"><span data-stu-id="d5413-135">Processing Character Messages</span></span>

<span data-ttu-id="d5413-136">Eine Fenster Prozedur empfängt eine Zeichen Nachricht, wenn die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion einen virtuellen Schlüsselcode übersetzt, der einem Zeichen Schlüssel entspricht.</span><span class="sxs-lookup"><span data-stu-id="d5413-136">A window procedure receives a character message when the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function translates a virtual-key code corresponding to a character key.</span></span> <span data-ttu-id="d5413-137">Die Zeichen Nachrichten lauten [**WM \_ char**](wm-char.md), [**WM \_ deadchar**](wm-deadchar.md), [**WM \_ Sychar**](/windows/desktop/menurc/wm-syschar)und [**WM \_ sysdeadchar**](wm-sysdeadchar.md).</span><span class="sxs-lookup"><span data-stu-id="d5413-137">The character messages are [**WM\_CHAR**](wm-char.md), [**WM\_DEADCHAR**](wm-deadchar.md), [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar), and [**WM\_SYSDEADCHAR**](wm-sysdeadchar.md).</span></span> <span data-ttu-id="d5413-138">Eine typische Fenster Prozedur ignoriert alle Zeichen Meldungen außer **WM \_ char**.</span><span class="sxs-lookup"><span data-stu-id="d5413-138">A typical window procedure ignores all character messages except **WM\_CHAR**.</span></span> <span data-ttu-id="d5413-139">Die **translatemess** -Funktion generiert eine **WM- \_ char** -Nachricht, wenn der Benutzer einen der folgenden Schlüssel drückt:</span><span class="sxs-lookup"><span data-stu-id="d5413-139">The **TranslateMessage** function generates a **WM\_CHAR** message when the user presses any of the following keys:</span></span>

-   <span data-ttu-id="d5413-140">Beliebige Zeichen Taste</span><span class="sxs-lookup"><span data-stu-id="d5413-140">Any character key</span></span>
-   <span data-ttu-id="d5413-141">RÜCKTASTE</span><span class="sxs-lookup"><span data-stu-id="d5413-141">BACKSPACE</span></span>
-   <span data-ttu-id="d5413-142">EINGABETASTE (Wagen Rücklauf)</span><span class="sxs-lookup"><span data-stu-id="d5413-142">ENTER (carriage return)</span></span>
-   <span data-ttu-id="d5413-143">ESC</span><span class="sxs-lookup"><span data-stu-id="d5413-143">ESC</span></span>
-   <span data-ttu-id="d5413-144">UMSCHALT + Eingabe (Zeilenvorschub)</span><span class="sxs-lookup"><span data-stu-id="d5413-144">SHIFT+ENTER (linefeed)</span></span>
-   <span data-ttu-id="d5413-145">TAB</span><span class="sxs-lookup"><span data-stu-id="d5413-145">TAB</span></span>

<span data-ttu-id="d5413-146">Wenn eine Fenster Prozedur die Meldung " [**WM \_ char**](wm-char.md) " empfängt, sollte Sie den Zeichencode untersuchen, der die Nachricht begleitet, um zu bestimmen, wie das Zeichen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5413-146">When a window procedure receives the [**WM\_CHAR**](wm-char.md) message, it should examine the character code that accompanies the message to determine how to process the character.</span></span> <span data-ttu-id="d5413-147">Der Zeichencode befindet sich im *wParam* -Parameter der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d5413-147">The character code is in the message's *wParam* parameter.</span></span>

<span data-ttu-id="d5413-148">Das folgende Beispiel zeigt das Fenster Prozedur Framework, das eine typische Anwendung verwendet, um Zeichen Nachrichten zu empfangen und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d5413-148">The following example shows the window procedure framework that a typical application uses to receive and process character messages.</span></span>


```
        case WM_CHAR: 
            switch (wParam) 
            { 
                case 0x08: 
                    
                    // Process a backspace. 
                     
                    break; 
 
                case 0x0A: 
                    
                    // Process a linefeed. 
                     
                    break; 
 
                case 0x1B: 
                    
                    // Process an escape. 
                    
                    break; 
 
                case 0x09: 
                    
                    // Process a tab. 
                     
                    break; 
 
                case 0x0D: 
                    
                    // Process a carriage return. 
                     
                    break; 
 
                default: 
                    
                    // Process displayable characters. 
                     
                    break; 
            } 
```



## <a name="using-the-caret"></a><span data-ttu-id="d5413-149">Verwenden der Einfügemarke</span><span class="sxs-lookup"><span data-stu-id="d5413-149">Using the Caret</span></span>

<span data-ttu-id="d5413-150">Ein Fenster, das Tastatureingaben empfängt, zeigt in der Regel die Zeichen an, die der Benutzer im Client Bereich des Fensters eingibt.</span><span class="sxs-lookup"><span data-stu-id="d5413-150">A window that receives keyboard input typically displays the characters the user types in the window's client area.</span></span> <span data-ttu-id="d5413-151">Ein Fenster sollte eine Einfügemarke verwenden, um die Position im Client Bereich anzugeben, an der das nächste Zeichen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d5413-151">A window should use a caret to indicate the position in the client area where the next character will appear.</span></span> <span data-ttu-id="d5413-152">Das Fenster sollte auch die Einfügemarke beim Empfang des Tastaturfokus erstellen und anzeigen und die Einfügemarke ausblenden und zerstören, wenn Sie den Fokus verliert.</span><span class="sxs-lookup"><span data-stu-id="d5413-152">The window should also create and display the caret when it receives the keyboard focus, and hide and destroy the caret when it loses the focus.</span></span> <span data-ttu-id="d5413-153">Diese Vorgänge können von einem Fenster bei der Verarbeitung der Nachrichten " [**WM \_ SetFocus**](wm-setfocus.md) " und " [**WM \_ killfocus**](wm-killfocus.md) " durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d5413-153">A window can perform these operations in the processing of the [**WM\_SETFOCUS**](wm-setfocus.md) and [**WM\_KILLFOCUS**](wm-killfocus.md) messages.</span></span> <span data-ttu-id="d5413-154">Weitere Informationen zu Carets finden Sie unter [Caretzeichen](/windows/desktop/menurc/carets).</span><span class="sxs-lookup"><span data-stu-id="d5413-154">For more information about carets, see [Carets](/windows/desktop/menurc/carets).</span></span>

## <a name="displaying-keyboard-input"></a><span data-ttu-id="d5413-155">Anzeigen von Tastatureingaben</span><span class="sxs-lookup"><span data-stu-id="d5413-155">Displaying Keyboard Input</span></span>

<span data-ttu-id="d5413-156">Das Beispiel in diesem Abschnitt zeigt, wie eine Anwendung Zeichen von der Tastatur empfangen, Sie im Client Bereich eines Fensters anzeigen und die Position der Einfügemarke mit jedem typisierten Zeichen aktualisieren kann.</span><span class="sxs-lookup"><span data-stu-id="d5413-156">The example in this section shows how an application can receive characters from the keyboard, display them in the client area of a window, and update the position of the caret with each character typed.</span></span> <span data-ttu-id="d5413-157">Außerdem wird veranschaulicht, wie die Einfügemarke in Reaktion auf den nach-links-Pfeil, den Pfeil nach rechts, den Pfeil nach rechts und den Ende Tastatureingaben verschoben wird, und zeigt, wie ausgewählter Text als Reaktion auf die Tastenkombination UMSCHALT + nach-rechts hervorgehoben wird</span><span class="sxs-lookup"><span data-stu-id="d5413-157">It also demonstrates how to move the caret in response to the LEFT ARROW, RIGHT ARROW, HOME, and END keystrokes, and shows how to highlight selected text in response to the SHIFT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="d5413-158">Während der Verarbeitung der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Meldung wird durch die im Beispiel gezeigte Fenster Prozedur ein 64K-Puffer zum Speichern von Tastatureingaben zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d5413-158">During processing of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message, the window procedure shown in the example allocates a 64K buffer for storing keyboard input.</span></span> <span data-ttu-id="d5413-159">Außerdem werden die Metriken der aktuell geladenen Schriftart abgerufen, und die Höhe und die durchschnittliche Breite der Zeichen in der Schriftart werden gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d5413-159">It also retrieves the metrics of the currently loaded font, saving the height and average width of characters in the font.</span></span> <span data-ttu-id="d5413-160">Die Höhe und Breite werden bei der Verarbeitung der [**WM- \_ Größen**](/windows/desktop/winmsg/wm-size) Nachricht verwendet, um die Zeilenlänge und die maximale Zeilen Anzahl basierend auf der Größe des Client Bereichs zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="d5413-160">The height and width are used in processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to calculate the line length and maximum number of lines, based on the size of the client area.</span></span>

<span data-ttu-id="d5413-161">Die Fenster Prozedur erstellt die Einfügemarke und zeigt diese an, wenn die [**WM \_ SetFocus**](wm-setfocus.md) -Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="d5413-161">The window procedure creates and displays the caret when processing the [**WM\_SETFOCUS**](wm-setfocus.md) message.</span></span> <span data-ttu-id="d5413-162">Beim Verarbeiten der [**WM- \_ killfocus**](wm-killfocus.md) -Nachricht wird die Einfügemarke ausgeblendet und gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d5413-162">It hides and deletes the caret when processing the [**WM\_KILLFOCUS**](wm-killfocus.md) message.</span></span>

<span data-ttu-id="d5413-163">Bei der Verarbeitung der " [**WM \_ char**](wm-char.md) "-Nachricht zeigt die Fenster Prozedur Zeichen an, speichert Sie im Eingabepuffer und aktualisiert die Position der Einfügemarke.</span><span class="sxs-lookup"><span data-stu-id="d5413-163">When processing the [**WM\_CHAR**](wm-char.md) message, the window procedure displays characters, stores them in the input buffer, and updates the caret position.</span></span> <span data-ttu-id="d5413-164">Die Fenster Prozedur konvertiert auch Tabstopp Zeichen in vier aufeinander folgende Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="d5413-164">The window procedure also converts tab characters to four consecutive space characters.</span></span> <span data-ttu-id="d5413-165">Rücktaste, linefeed und Escapezeichen generieren ein Signal, werden jedoch nicht anderweitig verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d5413-165">Backspace, linefeed, and escape characters generate a beep, but are not otherwise processed.</span></span>

<span data-ttu-id="d5413-166">Die Fenster Prozedur führt bei der Verarbeitung der [**WM- \_ keydownnachricht**](wm-keydown.md) die Bewegungen Links, rechts, Ende und Home Caretzeichen aus.</span><span class="sxs-lookup"><span data-stu-id="d5413-166">The window procedure performs the left, right, end, and home caret movements when processing the [**WM\_KEYDOWN**](wm-keydown.md) message.</span></span> <span data-ttu-id="d5413-167">Bei der Verarbeitung der Aktion der nach-rechts-Taste wird der Zustand der Umschalttaste von der Fenster Prozedur überprüft. wenn der Wert nicht ist, wird das Zeichen rechts neben der Einfügemarke ausgewählt, wenn die Einfügemarke verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="d5413-167">While processing the action of the RIGHT ARROW key, the window procedure checks the state of the SHIFT key and, if it is down, selects the character to the right of the caret as the caret is moved.</span></span>

<span data-ttu-id="d5413-168">Beachten Sie, dass der folgende Code so geschrieben ist, dass er entweder als Unicode oder als ANSI kompiliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d5413-168">Note that the following code is written so that it can be compiled either as Unicode or as ANSI.</span></span> <span data-ttu-id="d5413-169">Wenn der Quellcode Unicode definiert, werden Zeichen folgen als Unicode-Zeichen behandelt. Andernfalls werden Sie als ANSI-Zeichen behandelt.</span><span class="sxs-lookup"><span data-stu-id="d5413-169">If the source code defines UNICODE, strings are handled as Unicode characters; otherwise, they are handled as ANSI characters.</span></span>


```
#define BUFSIZE 65535 
#define SHIFTED 0x8000 
 
LONG APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    HDC hdc;                   // handle to device context 
    TEXTMETRIC tm;             // structure for text metrics 
    static DWORD dwCharX;      // average width of characters 
    static DWORD dwCharY;      // height of characters 
    static DWORD dwClientX;    // width of client area 
    static DWORD dwClientY;    // height of client area 
    static DWORD dwLineLen;    // line length 
    static DWORD dwLines;      // text lines in client area 
    static int nCaretPosX = 0; // horizontal position of caret 
    static int nCaretPosY = 0; // vertical position of caret 
    static int nCharWidth = 0; // width of a character 
    static int cch = 0;        // characters in buffer 
    static int nCurChar = 0;   // index of current character 
    static PTCHAR pchInputBuf; // input buffer 
    int i, j;                  // loop counters 
    int cCR = 0;               // count of carriage returns 
    int nCRIndex = 0;          // index of last carriage return 
    int nVirtKey;              // virtual-key code 
    TCHAR szBuf[128];          // temporary buffer 
    TCHAR ch;                  // current character 
    PAINTSTRUCT ps;            // required by BeginPaint 
    RECT rc;                   // output rectangle for DrawText 
    SIZE sz;                   // string dimensions 
    COLORREF crPrevText;       // previous text color 
    COLORREF crPrevBk;         // previous background color
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Get the metrics of the current font. 
 
            hdc = GetDC(hwndMain); 
            GetTextMetrics(hdc, &tm); 
            ReleaseDC(hwndMain, hdc); 
 
            // Save the average character width and height. 
 
            dwCharX = tm.tmAveCharWidth; 
            dwCharY = tm.tmHeight; 
 
            // Allocate a buffer to store keyboard input. 
 
            pchInputBuf = (LPTSTR) GlobalAlloc(GPTR, 
                BUFSIZE * sizeof(TCHAR)); 
            return 0; 
 
        case WM_SIZE: 
 
            // Save the new width and height of the client area. 
 
            dwClientX = LOWORD(lParam); 
            dwClientY = HIWORD(lParam); 
 
            // Calculate the maximum width of a line and the 
            // maximum number of lines in the client area. 
            
            dwLineLen = dwClientX - dwCharX; 
            dwLines = dwClientY / dwCharY; 
            break; 
 
 
        case WM_SETFOCUS: 
 
            // Create, position, and display the caret when the 
            // window receives the keyboard focus. 
 
            CreateCaret(hwndMain, (HBITMAP) 1, 0, dwCharY); 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            ShowCaret(hwndMain); 
            break; 
 
        case WM_KILLFOCUS: 
 
            // Hide and destroy the caret when the window loses the 
            // keyboard focus. 
 
            HideCaret(hwndMain); 
            DestroyCaret(); 
            break; 
 
        case WM_CHAR:
        // check if current location is close enough to the
        // end of the buffer that a buffer overflow may
        // occur. If so, add null and display contents. 
    if (cch > BUFSIZE-5)
    {
        pchInputBuf[cch] = 0x00;
        SendMessage(hwndMain, WM_PAINT, 0, 0);
    } 
            switch (wParam) 
            { 
                case 0x08:  // backspace 
                case 0x0A:  // linefeed 
                case 0x1B:  // escape 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case 0x09:  // tab 
 
                    // Convert tabs to four consecutive spaces. 
 
                    for (i = 0; i < 4; i++) 
                        SendMessage(hwndMain, WM_CHAR, 0x20, 0); 
                    return 0; 
 
                case 0x0D:  // carriage return 
 
                    // Record the carriage return and position the 
                    // caret at the beginning of the new line.

                    pchInputBuf[cch++] = 0x0D; 
                    nCaretPosX = 0; 
                    nCaretPosY += 1; 
                    break; 
 
                default:    // displayable character 
 
                    ch = (TCHAR) wParam; 
                    HideCaret(hwndMain); 
 
                    // Retrieve the character's width and output 
                    // the character. 
 
                    hdc = GetDC(hwndMain); 
                    GetCharWidth32(hdc, (UINT) wParam, (UINT) wParam, 
                        &nCharWidth); 
                    TextOut(hdc, nCaretPosX, nCaretPosY * dwCharY, 
                        &ch, 1); 
                    ReleaseDC(hwndMain, hdc); 
 
                    // Store the character in the buffer.
 
                    pchInputBuf[cch++] = ch; 
 
                    // Calculate the new horizontal position of the 
                    // caret. If the position exceeds the maximum, 
                    // insert a carriage return and move the caret 
                    // to the beginning of the next line. 
 
                    nCaretPosX += nCharWidth; 
                    if ((DWORD) nCaretPosX > dwLineLen) 
                    { 
                        nCaretPosX = 0;
                        pchInputBuf[cch++] = 0x0D; 
                        ++nCaretPosY; 
                    } 
                    nCurChar = cch; 
                    ShowCaret(hwndMain); 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_LEFT:   // LEFT ARROW 
 
                    // The caret can move only to the beginning of 
                    // the current line. 
 
                    if (nCaretPosX > 0) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the left of 
                        // the caret, calculate the character's 
                        // width, then subtract the width from the 
                        // current horizontal position of the caret 
                        // to obtain the new position. 
 
                        ch = pchInputBuf[--nCurChar]; 
                        hdc = GetDC(hwndMain); 
                        GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                        ReleaseDC(hwndMain, hdc); 
                        nCaretPosX = max(nCaretPosX - nCharWidth, 
                            0); 
                        ShowCaret(hwndMain); 
                    } 
                    break; 
 
                case VK_RIGHT:  // RIGHT ARROW 
 
                    // Caret moves to the right or, when a carriage 
                    // return is encountered, to the beginning of 
                    // the next line. 
 
                    if (nCurChar < cch) 
                    { 
                        HideCaret(hwndMain); 
 
                        // Retrieve the character to the right of 
                        // the caret. If it's a carriage return, 
                        // position the caret at the beginning of 
                        // the next line. 
 
                        ch = pchInputBuf[nCurChar]; 
                        if (ch == 0x0D) 
                        { 
                            nCaretPosX = 0; 
                            nCaretPosY++; 
                        } 
 
                        // If the character isn't a carriage 
                        // return, check to see whether the SHIFT 
                        // key is down. If it is, invert the text 
                        // colors and output the character. 
 
                        else 
                        { 
                            hdc = GetDC(hwndMain); 
                            nVirtKey = GetKeyState(VK_SHIFT); 
                            if (nVirtKey & SHIFTED) 
                            { 
                                crPrevText = SetTextColor(hdc, 
                                    RGB(255, 255, 255)); 
                                crPrevBk = SetBkColor(hdc, 
                                    RGB(0,0,0)); 
                                TextOut(hdc, nCaretPosX, 
                                    nCaretPosY * dwCharY, 
                                    &ch, 1); 
                                SetTextColor(hdc, crPrevText); 
                                SetBkColor(hdc, crPrevBk); 
                            } 
 
                            // Get the width of the character and 
                            // calculate the new horizontal 
                            // position of the caret. 
 
                            GetCharWidth32(hdc, ch, ch, &nCharWidth); 
                            ReleaseDC(hwndMain, hdc); 
                            nCaretPosX = nCaretPosX + nCharWidth; 
                        } 
                        nCurChar++; 
                        ShowCaret(hwndMain); 
                        break; 
                    } 
                    break; 
 
                case VK_UP:     // UP ARROW 
                case VK_DOWN:   // DOWN ARROW 
                    MessageBeep((UINT) -1); 
                    return 0; 
 
                case VK_HOME:   // HOME 
 
                    // Set the caret's position to the upper left 
                    // corner of the client area. 
 
                    nCaretPosX = nCaretPosY = 0; 
                    nCurChar = 0; 
                    break; 
 
                case VK_END:    // END  
 
                    // Move the caret to the end of the text. 
 
                    for (i=0; i < cch; i++) 
                    { 
                        // Count the carriage returns and save the 
                        // index of the last one. 
 
                        if (pchInputBuf[i] == 0x0D) 
                        { 
                            cCR++; 
                            nCRIndex = i + 1; 
                        } 
                    } 
                    nCaretPosY = cCR; 
 
                    // Copy all text between the last carriage 
                    // return and the end of the keyboard input 
                    // buffer to a temporary buffer. 
 
                    for (i = nCRIndex, j = 0; i < cch; i++, j++) 
                        szBuf[j] = pchInputBuf[i]; 
                    szBuf[j] = TEXT('\0'); 
 
                    // Retrieve the text extent and use it 
                    // to set the horizontal position of the 
                    // caret. 
 
                    hdc = GetDC(hwndMain);
                    hResult = StringCchLength(szBuf, 128, pcch);
                    if (FAILED(hResult))
                    {
                    // TODO: write error handler
                    } 
                    GetTextExtentPoint32(hdc, szBuf, *pcch, 
                        &sz); 
                    nCaretPosX = sz.cx; 
                    ReleaseDC(hwndMain, hdc); 
                    nCurChar = cch; 
                    break; 
 
                default: 
                    break; 
            } 
            SetCaretPos(nCaretPosX, nCaretPosY * dwCharY); 
            break; 
 
        case WM_PAINT: 
            if (cch == 0)       // nothing in input buffer 
                break; 
 
            hdc = BeginPaint(hwndMain, &ps); 
            HideCaret(hwndMain); 
 
            // Set the clipping rectangle, and then draw the text 
            // into it. 
 
            SetRect(&rc, 0, 0, dwLineLen, dwClientY); 
            DrawText(hdc, pchInputBuf, -1, &rc, DT_LEFT); 
 
            ShowCaret(hwndMain); 
            EndPaint(hwndMain, &ps); 
            break; 
        
        // Process other messages. 
        
        case WM_DESTROY: 
            PostQuitMessage(0); 
 
            // Free the input buffer. 
 
            GlobalFree((HGLOBAL) pchInputBuf); 
            UnregisterHotKey(hwndMain, 0xAAAA); 
            break; 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
} 
```



 

 