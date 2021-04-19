---
title: Tastatureingabe (Get Started with Win32 and C++)
description: Tastatureingabe
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "106357137"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a><span data-ttu-id="b23e4-103">Tastatureingabe (Get Started with Win32 and C++)</span><span class="sxs-lookup"><span data-stu-id="b23e4-103">Keyboard Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="b23e4-104">Die Tastatur wird für verschiedene Typen von Eingaben verwendet, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="b23e4-104">The keyboard is used for several distinct types of input, including:</span></span>

-   <span data-ttu-id="b23e4-105">Zeicheneingabe.</span><span class="sxs-lookup"><span data-stu-id="b23e4-105">Character input.</span></span> <span data-ttu-id="b23e4-106">Text, der vom Benutzer in ein Dokument oder ein Bearbeitungsfeld eingetippt wird.</span><span class="sxs-lookup"><span data-stu-id="b23e4-106">Text that the user types into a document or edit box.</span></span>
-   <span data-ttu-id="b23e4-107">Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-107">Keyboard shortcuts.</span></span> <span data-ttu-id="b23e4-108">Tastenkombinationen, die Anwendungsfunktionen aufrufen. beispielsweise STRG + O zum Öffnen einer Datei.</span><span class="sxs-lookup"><span data-stu-id="b23e4-108">Key strokes that invoke application functions; for example, CTRL + O to open a file.</span></span>
-   <span data-ttu-id="b23e4-109">System Befehle.</span><span class="sxs-lookup"><span data-stu-id="b23e4-109">System commands.</span></span> <span data-ttu-id="b23e4-110">Tastenkombinationen, die Systemfunktionen aufrufen. Beispiel: Alt + Tab zum Wechseln von Fenstern.</span><span class="sxs-lookup"><span data-stu-id="b23e4-110">Key strokes that invoke system functions; for example, ALT + TAB to switch windows.</span></span>

<span data-ttu-id="b23e4-111">Bei der Betrachtung von Tastatureingaben ist es wichtig, sich daran zu erinnern, dass ein Schlüssel Strich nicht mit einem Zeichen identisch ist.</span><span class="sxs-lookup"><span data-stu-id="b23e4-111">When thinking about keyboard input, it is important to remember that a key stroke is not the same as a character.</span></span> <span data-ttu-id="b23e4-112">Wenn Sie z. b. die Taste drücken, kann dies zu einem der folgenden Zeichen führen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-112">For example, pressing the A key could result in any of the following characters.</span></span>

-   <span data-ttu-id="b23e4-113">a</span><span class="sxs-lookup"><span data-stu-id="b23e4-113">a</span></span>
-   <span data-ttu-id="b23e4-114">Ein</span><span class="sxs-lookup"><span data-stu-id="b23e4-114">A</span></span>
-   <span data-ttu-id="b23e4-115">á (wenn die Tastatur das Kombinieren von Diakritik unterstützt)</span><span class="sxs-lookup"><span data-stu-id="b23e4-115">á (if the keyboard supports combining diacritics)</span></span>

<span data-ttu-id="b23e4-116">Wenn die Alt-Taste gedrückt gehalten wird, wird durch Drücken der Taste Alt + A erzeugt, die das System nicht als Zeichen behandelt, sondern als Systembefehl.</span><span class="sxs-lookup"><span data-stu-id="b23e4-116">Further, if the ALT key is held down, pressing the A key produces ALT+A, which the system does not treat as a character at all, but rather as a system command.</span></span>

## <a name="key-codes"></a><span data-ttu-id="b23e4-117">Schlüssel Codes</span><span class="sxs-lookup"><span data-stu-id="b23e4-117">Key Codes</span></span>

<span data-ttu-id="b23e4-118">Wenn Sie eine Taste drücken, generiert die Hardware einen Überprüfungs *Code*.</span><span class="sxs-lookup"><span data-stu-id="b23e4-118">When you press a key, the hardware generates a *scan code*.</span></span> <span data-ttu-id="b23e4-119">Überprüfungs Codes variieren von einer Tastatur zur nächsten, und es gibt separate Überprüfungs Codes für Key-up-und Key-down-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b23e4-119">Scan codes vary from one keyboard to the next, and there are separate scan codes for key-up and key-down events.</span></span> <span data-ttu-id="b23e4-120">Sie werden die Scan Codes fast nie interessieren.</span><span class="sxs-lookup"><span data-stu-id="b23e4-120">You will almost never care about scan codes.</span></span> <span data-ttu-id="b23e4-121">Der Tastaturtreiber übersetzt Scan Codes in *virtuelle Schlüsselcodes*.</span><span class="sxs-lookup"><span data-stu-id="b23e4-121">The keyboard driver translates scan codes into *virtual-key codes*.</span></span> <span data-ttu-id="b23e4-122">Virtuelle Schlüsselcodes sind Geräte unabhängig.</span><span class="sxs-lookup"><span data-stu-id="b23e4-122">Virtual-key codes are device-independent.</span></span> <span data-ttu-id="b23e4-123">Wenn Sie auf eine beliebige Tastatur eine Taste drücken, wird derselbe Code für den virtuellen Schlüssel generiert.</span><span class="sxs-lookup"><span data-stu-id="b23e4-123">Pressing the A key on any keyboard generates the same virtual-key code.</span></span>

<span data-ttu-id="b23e4-124">Im allgemeinen entsprechen die Codes von virtuellen Schlüsseln nicht ASCII-Codes oder einem anderen Zeichen Codierungsstandard.</span><span class="sxs-lookup"><span data-stu-id="b23e4-124">In general, virtual-key codes do not correspond to ASCII codes or any other character-encoding standard.</span></span> <span data-ttu-id="b23e4-125">Dies ist offensichtlich, wenn Sie sich Gedanken darüber machen, da derselbe Schlüssel andere Zeichen generieren kann (a, a, á), und einige Schlüssel, wie z. b. Funktionstasten, entsprechen keinem Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-125">This is obvious if you think about it, because the same key can generate different characters (a, A, á), and some keys, such as function keys, do not correspond to any character.</span></span>

<span data-ttu-id="b23e4-126">Dies bedeutet, dass die folgenden virtuellen Schlüsselcodes ASCII-Entsprechungen zugeordnet werden:</span><span class="sxs-lookup"><span data-stu-id="b23e4-126">That said, the following virtual-key codes do map to ASCII equivalents:</span></span>

-   <span data-ttu-id="b23e4-127">0 bis 9 Schlüssel = ASCII ' 0 ' – ' 9 ' (0x30 – 0x39)</span><span class="sxs-lookup"><span data-stu-id="b23e4-127">0 through 9 keys = ASCII '0' – '9' (0x30 – 0x39)</span></span>
-   <span data-ttu-id="b23e4-128">A bis Z Keys = ASCII ' A ' – ' Z ' (0x41 – 0x5A)</span><span class="sxs-lookup"><span data-stu-id="b23e4-128">A through Z keys = ASCII 'A' – 'Z' (0x41 – 0x5A)</span></span>

<span data-ttu-id="b23e4-129">In gewisser Hinsicht ist diese Zuordnung unglücklich, denn Sie sollten sich aus den beschriebenen Gründen nie mit virtuellen Schlüsselcodes als Zeichen vorstellen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-129">In some respects this mapping is unfortunate, because you should never think of virtual-key codes as characters, for the reasons discussed.</span></span>

<span data-ttu-id="b23e4-130">Die Header Datei WinUser. h definiert Konstanten für den größten Teil der Codes von virtuellen Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="b23e4-130">The header file WinUser.h defines constants for most of the virtual-key codes.</span></span> <span data-ttu-id="b23e4-131">Beispielsweise ist der Code des virtuellen Schlüssels für die nach-links-Taste **VK \_ left** (0x25).</span><span class="sxs-lookup"><span data-stu-id="b23e4-131">For example, the virtual-key code for the LEFT ARROW key is **VK\_LEFT** (0x25).</span></span> <span data-ttu-id="b23e4-132">Eine umfassende Liste der Codes für virtuelle Schlüssel finden Sie unter [**Code für virtuelle**](/windows/desktop/inputdev/virtual-key-codes)Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b23e4-132">For the complete list of virtual-key codes, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="b23e4-133">Für die virtuellen Schlüsselcodes, die ASCII-Werten entsprechen, sind keine Konstanten definiert.</span><span class="sxs-lookup"><span data-stu-id="b23e4-133">No constants are defined for the virtual-key codes that match ASCII values.</span></span> <span data-ttu-id="b23e4-134">Beispielsweise ist der Code des virtuellen Schlüssels für die A-Taste 0x41, aber es ist keine Konstante mit dem Namen " **VK \_ A**" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="b23e4-134">For example, the virtual-key code for the A key is 0x41, but there is no constant named **VK\_A**.</span></span> <span data-ttu-id="b23e4-135">Verwenden Sie stattdessen einfach den numerischen Wert.</span><span class="sxs-lookup"><span data-stu-id="b23e4-135">Instead, just use the numeric value.</span></span>

## <a name="key-down-and-key-up-messages"></a><span data-ttu-id="b23e4-136">Key-Down und Key-Up Meldungen</span><span class="sxs-lookup"><span data-stu-id="b23e4-136">Key-Down and Key-Up Messages</span></span>

<span data-ttu-id="b23e4-137">Wenn Sie eine Taste drücken, empfängt das Fenster, das den Tastaturfokus besitzt, eine der folgenden Meldungen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-137">When you press a key, the window that has keyboard focus receives one of the following messages.</span></span>

-   [<span data-ttu-id="b23e4-138">**WM \_ syskeydown**</span><span class="sxs-lookup"><span data-stu-id="b23e4-138">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
-   [<span data-ttu-id="b23e4-139">**WM- \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="b23e4-139">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)

<span data-ttu-id="b23e4-140">Die [**WM- \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown) -Meldung gibt eine *System Taste* an, bei der es sich um einen Schlüssel Strich handelt, der einen Systembefehl aufruft.</span><span class="sxs-lookup"><span data-stu-id="b23e4-140">The [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message indicates a *system key*, which is a key stroke that invokes a system command.</span></span> <span data-ttu-id="b23e4-141">Es gibt zwei Typen von System Schlüsseln:</span><span class="sxs-lookup"><span data-stu-id="b23e4-141">There are two types of system key:</span></span>

-   <span data-ttu-id="b23e4-142">ALT + beliebige Taste</span><span class="sxs-lookup"><span data-stu-id="b23e4-142">ALT + any key</span></span>
-   <span data-ttu-id="b23e4-143">F10</span><span class="sxs-lookup"><span data-stu-id="b23e4-143">F10</span></span>

<span data-ttu-id="b23e4-144">Die Taste F10 aktiviert die Menüleiste eines Fensters.</span><span class="sxs-lookup"><span data-stu-id="b23e4-144">The F10 key activates the menu bar of a window.</span></span> <span data-ttu-id="b23e4-145">Verschiedene Kombinationen aus Alt-Taste rufen Systembefehle auf.</span><span class="sxs-lookup"><span data-stu-id="b23e4-145">Various ALT-key combinations invoke system commands.</span></span> <span data-ttu-id="b23e4-146">Beispielsweise wechselt Alt + Tab zu einem neuen Fenster.</span><span class="sxs-lookup"><span data-stu-id="b23e4-146">For example, ALT + TAB switches to a new window.</span></span> <span data-ttu-id="b23e4-147">Wenn ein Fenster außerdem über ein Menü verfügt, kann die Alt-Taste zum Aktivieren von Menü Elementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b23e4-147">In addition, if a window has a menu, the ALT key can be used to activate menu items.</span></span> <span data-ttu-id="b23e4-148">Einige ALT-Tastenkombinationen machen nichts.</span><span class="sxs-lookup"><span data-stu-id="b23e4-148">Some ALT key combinations do not do anything.</span></span>

<span data-ttu-id="b23e4-149">Alle anderen Schlüssel Striche werden als nicht-Systemschlüssel betrachtet und die [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht erzeugt.</span><span class="sxs-lookup"><span data-stu-id="b23e4-149">All other key strokes are considered nonsystem keys and produce the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span> <span data-ttu-id="b23e4-150">Dies schließt die anderen Funktionstasten als F10 ein.</span><span class="sxs-lookup"><span data-stu-id="b23e4-150">This includes the function keys other than F10.</span></span>

<span data-ttu-id="b23e4-151">Wenn Sie einen Schlüssel freigeben, sendet das System eine entsprechende Schlüssel Nachricht:</span><span class="sxs-lookup"><span data-stu-id="b23e4-151">When you release a key, the system sends a corresponding key-up message:</span></span>

-   [<span data-ttu-id="b23e4-152">**WM- \_ KeyUp**</span><span class="sxs-lookup"><span data-stu-id="b23e4-152">**WM\_KEYUP**</span></span>](/windows/desktop/inputdev/wm-keyup)
-   [<span data-ttu-id="b23e4-153">**WM- \_ syskeyup**</span><span class="sxs-lookup"><span data-stu-id="b23e4-153">**WM\_SYSKEYUP**</span></span>](/windows/desktop/inputdev/wm-syskeyup)

<span data-ttu-id="b23e4-154">Wenn Sie einen Schlüssel gedrückt halten, um die Wiederholungsfunktion der Tastatur zu starten, sendet das System mehrere Schlüssel Meldungen, gefolgt von einer einzelnen Schlüssel Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b23e4-154">If you hold down a key long enough to start the keyboard's repeat feature, the system sends multiple key-down messages, followed by a single key-up message.</span></span>

<span data-ttu-id="b23e4-155">In allen vier der bisher behandelten Tastatur Meldungen enthält der *wParam* -Parameter den Code für den virtuellen Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="b23e4-155">In all four of the keyboard messages discussed so far, the *wParam* parameter contains the virtual-key code of the key.</span></span> <span data-ttu-id="b23e4-156">Der *LPARAM* -Parameter enthält verschiedene Informationen, die in 32 Bits verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="b23e4-156">The *lParam* parameter contains some miscellaneous information packed into 32 bits.</span></span> <span data-ttu-id="b23e4-157">In der Regel benötigen Sie die Informationen in *LPARAM* nicht.</span><span class="sxs-lookup"><span data-stu-id="b23e4-157">You typically do not need the information in *lParam*.</span></span> <span data-ttu-id="b23e4-158">Ein Flag, das nützlich sein kann, ist Bit 30, das "Previous Key State"-Flag, das für wiederholte Schlüssel Meldungen auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b23e4-158">One flag that might be useful is bit 30, the "previous key state" flag, which is set to 1 for repeated key-down messages.</span></span>

<span data-ttu-id="b23e4-159">Wie der Name schon sagt, sind Systemschlüssel Striche hauptsächlich für die Verwendung durch das Betriebssystem vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-159">As the name implies, system key strokes are primarily intended for use by the operating system.</span></span> <span data-ttu-id="b23e4-160">Wenn Sie die [**WM- \_ syskeydownnachricht abfangen**](/windows/desktop/inputdev/wm-syskeydown) , müssen Sie [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) nachher aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-160">If you intercept the [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message, call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) afterward.</span></span> <span data-ttu-id="b23e4-161">Andernfalls blockieren Sie die Verarbeitung des Befehls durch das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="b23e4-161">Otherwise, you will block the operating system from handling the command.</span></span>

## <a name="character-messages"></a><span data-ttu-id="b23e4-162">Zeichen Nachrichten</span><span class="sxs-lookup"><span data-stu-id="b23e4-162">Character Messages</span></span>

<span data-ttu-id="b23e4-163">Schlüssel Striche werden von der [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion in Zeichen konvertiert, die wir zuerst in [Modul 1](your-first-windows-program.md)gesehen haben.</span><span class="sxs-lookup"><span data-stu-id="b23e4-163">Key strokes are converted into characters by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function, which we first saw in [Module 1](your-first-windows-program.md).</span></span> <span data-ttu-id="b23e4-164">Diese Funktion untersucht KeyDown-Meldungen und übersetzt Sie in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-164">This function examines key-down messages and translates them into characters.</span></span> <span data-ttu-id="b23e4-165">Für jedes Zeichen, das erzeugt wird, fügt die Funktion **translatemess** eine "WM char"-oder "WM"- [**\_ Sychar**](/windows/desktop/inputdev/wm-char) -Nachricht in die Nachrichten Warteschlange des Fensters ein. [**\_**](/windows/desktop/menurc/wm-syschar)</span><span class="sxs-lookup"><span data-stu-id="b23e4-165">For each character that is produced, the **TranslateMessage** function puts a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) or [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message on the message queue of the window.</span></span> <span data-ttu-id="b23e4-166">Der *wParam* -Parameter der Nachricht enthält das UTF-16-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-166">The *wParam* parameter of the message contains the UTF-16 character.</span></span>

<span data-ttu-id="b23e4-167">Möglicherweise werden WM- [**\_ char**](/windows/desktop/inputdev/wm-char) -Nachrichten aus [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Meldungen generiert, während [**WM- \_ Sychar**](/windows/desktop/menurc/wm-syschar) -Nachrichten aus [**WM- \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown) -Nachrichten generiert werden.</span><span class="sxs-lookup"><span data-stu-id="b23e4-167">As you might guess, [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages are generated from [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, while [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) messages are generated from [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) messages.</span></span> <span data-ttu-id="b23e4-168">Nehmen wir beispielsweise an, dass der Benutzer die UMSCHALTTASTE drückt, gefolgt von der A-Taste.</span><span class="sxs-lookup"><span data-stu-id="b23e4-168">For example, suppose the user presses the SHIFT key followed by the A key.</span></span> <span data-ttu-id="b23e4-169">Wenn Sie ein Standardmäßiges Tastaturlayout annehmen, erhalten Sie die folgende Sequenz von Nachrichten:</span><span class="sxs-lookup"><span data-stu-id="b23e4-169">Assuming a standard keyboard layout, you would get the following sequence of messages:</span></span>

<span data-ttu-id="b23e4-170">**WM \_ KeyDown**: Shift</span><span class="sxs-lookup"><span data-stu-id="b23e4-170">**WM\_KEYDOWN**: SHIFT</span></span>  
<span data-ttu-id="b23e4-171">**WM \_ KeyDown**: A</span><span class="sxs-lookup"><span data-stu-id="b23e4-171">**WM\_KEYDOWN**: A</span></span>  
<span data-ttu-id="b23e4-172">**WM \_ CHAR**: ' A '</span><span class="sxs-lookup"><span data-stu-id="b23e4-172">**WM\_CHAR**: 'A'</span></span>  


<span data-ttu-id="b23e4-173">Auf der anderen Seite generiert die Kombination ALT + P Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b23e4-173">On the other hand, the combination ALT + P would generate:</span></span>

 <span data-ttu-id="b23e4-174">**WM \_ syskeydown**: VK- \_ Menü</span><span class="sxs-lookup"><span data-stu-id="b23e4-174">**WM\_SYSKEYDOWN**: VK\_MENU</span></span>  
<span data-ttu-id="b23e4-175">**WM \_ Syskeydown**: 0x50</span><span class="sxs-lookup"><span data-stu-id="b23e4-175">**WM\_SYSKEYDOWN**: 0x50</span></span>  
<span data-ttu-id="b23e4-176">**WM \_ Syschar**: ' p '</span><span class="sxs-lookup"><span data-stu-id="b23e4-176">**WM\_SYSCHAR**: 'p'</span></span>  
<span data-ttu-id="b23e4-177">**WM \_ Syskeyup**: 0x50</span><span class="sxs-lookup"><span data-stu-id="b23e4-177">**WM\_SYSKEYUP**: 0x50</span></span>  
<span data-ttu-id="b23e4-178">**WM \_ KeyUp**: VK- \_ Menü</span><span class="sxs-lookup"><span data-stu-id="b23e4-178">**WM\_KEYUP**: VK\_MENU</span></span>  


<span data-ttu-id="b23e4-179">(Der Code des virtuellen Schlüssels für die Alt-Taste wird als "VK \_ " bezeichnet. Menü aus historischen Gründen.)</span><span class="sxs-lookup"><span data-stu-id="b23e4-179">(The virtual-key code for the ALT key is named VK\_MENU for historical reasons.)</span></span>

<span data-ttu-id="b23e4-180">Die [**WM- \_ syschar**](/windows/desktop/menurc/wm-syschar) -Meldung gibt ein System Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="b23e4-180">The [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message indicates a system character.</span></span> <span data-ttu-id="b23e4-181">Wie bei [**WM- \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown)sollten Sie diese Nachricht in der Regel direkt an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben.</span><span class="sxs-lookup"><span data-stu-id="b23e4-181">As with [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), you should generally pass this message directly to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="b23e4-182">Andernfalls können Sie die Standardsystem Befehle stören.</span><span class="sxs-lookup"><span data-stu-id="b23e4-182">Otherwise, you may interfere with standard system commands.</span></span> <span data-ttu-id="b23e4-183">Behandeln Sie vor allem die " **WM \_ syschar** " nicht als Text, den der Benutzer eingegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b23e4-183">In particular, do not treat **WM\_SYSCHAR** as text that the user has typed.</span></span>

<span data-ttu-id="b23e4-184">Die Meldung " [**WM \_ char**](/windows/desktop/inputdev/wm-char) " ist das, was Sie normalerweise als Zeicheneingabe betrachten.</span><span class="sxs-lookup"><span data-stu-id="b23e4-184">The [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message is what you normally think of as character input.</span></span> <span data-ttu-id="b23e4-185">Der Datentyp für das Zeichen ist **WCHAR \_ t**, das ein UTF-16-Unicode-Zeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="b23e4-185">The data type for the character is **wchar\_t**, representing a UTF-16 Unicode character.</span></span> <span data-ttu-id="b23e4-186">Zeichen Eingaben können Zeichen außerhalb des ASCII-Bereichs enthalten, insbesondere bei Tastaturlayouts, die häufig außerhalb der USA verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b23e4-186">Character input can include characters outside the ASCII range, especially with keyboard layouts that are commonly used outside of the United States.</span></span> <span data-ttu-id="b23e4-187">Sie können verschiedene Tastaturlayouts ausprobieren, indem Sie eine regionale Tastatur installieren und anschließend die Tastatur Funktion auf dem Bildschirm verwenden.</span><span class="sxs-lookup"><span data-stu-id="b23e4-187">You can try different keyboard layouts by installing a regional keyboard and then using the On-Screen Keyboard feature.</span></span>

<span data-ttu-id="b23e4-188">Benutzer können auch einen Eingabemethoden-Editor (Input Method Editor, IME) installieren, um komplexe Skripts, z. b. japanische Zeichen, mit einer Standardtastatur einzugeben.</span><span class="sxs-lookup"><span data-stu-id="b23e4-188">Users can also install an Input Method Editor (IME) to enter complex scripts, such as Japanese characters, with a standard keyboard.</span></span> <span data-ttu-id="b23e4-189">Wenn Sie z. b. eine japanische IME-Taste verwenden, um das Katakana Character カ (KA) einzugeben, erhalten Sie möglicherweise die folgenden Meldungen:</span><span class="sxs-lookup"><span data-stu-id="b23e4-189">For example, using a Japanese IME to enter the katakana character カ (ka), you might get the following messages:</span></span>

<span data-ttu-id="b23e4-190">**WM \_ KeyDown**: VK \_ ProcessKey (die Taste für den IME-Prozess)</span><span class="sxs-lookup"><span data-stu-id="b23e4-190">**WM\_KEYDOWN**: VK\_PROCESSKEY (the IME PROCESS key)</span></span>  
<span data-ttu-id="b23e4-191">**WM \_ KeyUp**: 0x4B</span><span class="sxs-lookup"><span data-stu-id="b23e4-191">**WM\_KEYUP**: 0x4B</span></span>  
<span data-ttu-id="b23e4-192">**WM \_ KeyDown**: VK \_ ProcessKey</span><span class="sxs-lookup"><span data-stu-id="b23e4-192">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="b23e4-193">**WM \_ KeyUp**: 0x41</span><span class="sxs-lookup"><span data-stu-id="b23e4-193">**WM\_KEYUP**: 0x41</span></span>  
<span data-ttu-id="b23e4-194">**WM \_ KeyDown**: VK \_ ProcessKey</span><span class="sxs-lookup"><span data-stu-id="b23e4-194">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="b23e4-195">**WM \_ CHAR**: カ</span><span class="sxs-lookup"><span data-stu-id="b23e4-195">**WM\_CHAR**: カ</span></span>  
<span data-ttu-id="b23e4-196">**WM \_ KeyUp**: VK \_ Return</span><span class="sxs-lookup"><span data-stu-id="b23e4-196">**WM\_KEYUP**: VK\_RETURN</span></span>  


<span data-ttu-id="b23e4-197">Einige Tastenkombinationen für STRG werden in ASCII-Steuerzeichen übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b23e4-197">Some CTRL key combinations are translated into ASCII control characters.</span></span> <span data-ttu-id="b23e4-198">Beispielsweise wird STRG + A in das ASCII-Zeichen STRG-A (SoH) übersetzt (ASCII-Wert 0x01).</span><span class="sxs-lookup"><span data-stu-id="b23e4-198">For example, CTRL+A is translated to the ASCII ctrl-A (SOH) character (ASCII value 0x01).</span></span> <span data-ttu-id="b23e4-199">Bei Texteingaben sollten Sie die Steuerzeichen in der Regel herausfiltern.</span><span class="sxs-lookup"><span data-stu-id="b23e4-199">For text input, you should generally filter out the control characters.</span></span> <span data-ttu-id="b23e4-200">Vermeiden Sie außerdem die Verwendung von [**WM \_ char**](/windows/desktop/inputdev/wm-char) zum Implementieren von Tastenkombinationen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-200">Also, avoid using [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) to implement keyboard shortcuts.</span></span> <span data-ttu-id="b23e4-201">Verwenden Sie stattdessen die [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Meldungen, oder verwenden Sie eine Zugriffstasten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b23e4-201">Instead, use [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages; or even better, use an accelerator table.</span></span> <span data-ttu-id="b23e4-202">Zugriffstasten Tabellen werden im nächsten Thema, Zugriffstasten [Tabellen](accelerator-tables.md), beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b23e4-202">Accelerator tables are described in the next topic, [Accelerator Tables](accelerator-tables.md).</span></span>

<span data-ttu-id="b23e4-203">Der folgende Code zeigt die Haupt Tastatur Meldungen im Debugger an.</span><span class="sxs-lookup"><span data-stu-id="b23e4-203">The following code displays the main keyboard messages in the debugger.</span></span> <span data-ttu-id="b23e4-204">Experimentieren Sie mit verschiedenen Tastenkombinationen, und sehen Sie sich an, welche Meldungen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="b23e4-204">Try playing with different keystroke combinations and see what messages are generated.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a><span data-ttu-id="b23e4-205">Verschiedene Tastatur Meldungen</span><span class="sxs-lookup"><span data-stu-id="b23e4-205">Miscellaneous Keyboard Messages</span></span>

<span data-ttu-id="b23e4-206">Einige andere Tastatur Meldungen können von den meisten Anwendungen sicher ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="b23e4-206">Some other keyboard messages can safely be ignored by most applications.</span></span>

-   <span data-ttu-id="b23e4-207">Die [**WM \_ deadchar**](/windows/desktop/inputdev/wm-deadchar) -Nachricht wird für einen kombinierten Schlüssel, z. b. eine diakritische, gesendet.</span><span class="sxs-lookup"><span data-stu-id="b23e4-207">The [**WM\_DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) message is sent for a combining key, such as a diacritic.</span></span> <span data-ttu-id="b23e4-208">Beispielsweise wird auf der Tastatur der Sprache "Akzent" (") gefolgt von E" das Zeichen "é" erzeugt.</span><span class="sxs-lookup"><span data-stu-id="b23e4-208">For example, on a Spanish language keyboard, typing accent (') followed by E produces the character é.</span></span> <span data-ttu-id="b23e4-209">Der **WM- \_ deadchar** -Wert wird für das Akzentzeichen gesendet.</span><span class="sxs-lookup"><span data-stu-id="b23e4-209">The **WM\_DEADCHAR** is sent for the accent character.</span></span>
-   <span data-ttu-id="b23e4-210">Die [**WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) -Nachricht ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="b23e4-210">The [**WM\_UNICHAR**](/windows/desktop/inputdev/wm-unichar) message is obsolete.</span></span> <span data-ttu-id="b23e4-211">Sie ermöglicht ANSI-Programmen den Empfang von Unicode-Zeichen Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b23e4-211">It enables ANSI programs to receive Unicode character input.</span></span>
-   <span data-ttu-id="b23e4-212">Das Zeichen " [**WM \_ IME \_ char**](/windows/desktop/Intl/wm-ime-char) " wird gesendet, wenn ein IME eine Tastatureingabe-Sequenz in Zeichen übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b23e4-212">The [**WM\_IME\_CHAR**](/windows/desktop/Intl/wm-ime-char) character is sent when an IME translates a keystroke sequence into characters.</span></span> <span data-ttu-id="b23e4-213">Es wird zusätzlich zur üblichen [**WM \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="b23e4-213">It is sent in addition to the usual [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>

## <a name="keyboard-state"></a><span data-ttu-id="b23e4-214">Tastatur Zustand</span><span class="sxs-lookup"><span data-stu-id="b23e4-214">Keyboard State</span></span>

<span data-ttu-id="b23e4-215">Die Tastatur Meldungen sind ereignisgesteuert.</span><span class="sxs-lookup"><span data-stu-id="b23e4-215">The keyboard messages are event-driven.</span></span> <span data-ttu-id="b23e4-216">Das heißt, Sie erhalten eine Nachricht, wenn etwas Interessantes passiert, z. b. einen Tastendruck, und die Meldung gibt Aufschluss darüber, was gerade passiert ist.</span><span class="sxs-lookup"><span data-stu-id="b23e4-216">That is, you get a message when something interesting happens, such as a key press, and the message tells you what just happened.</span></span> <span data-ttu-id="b23e4-217">Sie können den Status eines Schlüssels jedoch auch jederzeit testen, indem Sie die [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-217">But you can also test the state of a key at any time, by calling the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function.</span></span>

<span data-ttu-id="b23e4-218">Nehmen Sie beispielsweise an, wie Sie die Tastenkombination mit der linken Maustaste und Alt-Taste erkennen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-218">For example, consider how would you detect the combination of left mouse click + ALT key.</span></span> <span data-ttu-id="b23e4-219">Sie können den Zustand der Alt-Taste nachverfolgen, indem Sie auf Tastatur Schlag Nachrichten lauschen und ein Flag speichern, aber [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) spart Ihnen die Probleme.</span><span class="sxs-lookup"><span data-stu-id="b23e4-219">You could track the state of the ALT key by listening for key-stroke messages and storing a flag, but [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) saves you the trouble.</span></span> <span data-ttu-id="b23e4-220">Wenn Sie die [**WM- \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Meldung erhalten, können Sie einfach **GetKeyState** wie folgt aufrufen:</span><span class="sxs-lookup"><span data-stu-id="b23e4-220">When you receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, just call **GetKeyState** as follows:</span></span>


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



<span data-ttu-id="b23e4-221">Die [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) -Nachricht nimmt einen Code für virtuelle Schlüssel als Eingabe an und gibt einen Satz von Bitflags zurück (tatsächlich nur zwei Flags).</span><span class="sxs-lookup"><span data-stu-id="b23e4-221">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) message takes a virtual-key code as input and returns a set of bit flags (actually just two flags).</span></span> <span data-ttu-id="b23e4-222">Der Wert 0X8000 enthält das Bitflag, das testet, ob der Schlüssel aktuell gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="b23e4-222">The value 0x8000 contains the bit flag that tests whether the key is currently pressed.</span></span>

<span data-ttu-id="b23e4-223">Die meisten Tastaturen haben zwei Alt-Taste, Links und rechts.</span><span class="sxs-lookup"><span data-stu-id="b23e4-223">Most keyboards have two ALT keys, left and right.</span></span> <span data-ttu-id="b23e4-224">Im vorherigen Beispiel wird getestet, ob eine von Ihnen gedrückt wurde.</span><span class="sxs-lookup"><span data-stu-id="b23e4-224">The previous example tests whether either of them of pressed.</span></span> <span data-ttu-id="b23e4-225">Sie können [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) auch verwenden, um zwischen den linken und rechten Instanzen der Alt-Taste, der UMSCHALTTASTE oder der STRG-Taste zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="b23e4-225">You can also use [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) to distinguish between the left and right instances of the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="b23e4-226">Der folgende Code testet z. b., ob die Rechte ALT-Taste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="b23e4-226">For example, the following code tests if the right ALT key is pressed.</span></span>


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



<span data-ttu-id="b23e4-227">Die [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) -Funktion ist interessant, da Sie einen *virtuellen* Tastatur Zustand meldet.</span><span class="sxs-lookup"><span data-stu-id="b23e4-227">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function is interesting because it reports a *virtual* keyboard state.</span></span> <span data-ttu-id="b23e4-228">Dieser virtuelle Status basiert auf dem Inhalt der Nachrichten Warteschlange und wird aktualisiert, wenn Sie Nachrichten aus der Warteschlange entfernen.</span><span class="sxs-lookup"><span data-stu-id="b23e4-228">This virtual state is based on the contents of your message queue, and gets updated as you remove messages from the queue.</span></span> <span data-ttu-id="b23e4-229">Wenn das Programmfenster Meldungen verarbeitet, gibt **GetKeyState** Ihnen eine Momentaufnahme der Tastatur zu dem Zeitpunkt, zu dem die einzelnen Nachrichten in die Warteschlange eingereiht wurden.</span><span class="sxs-lookup"><span data-stu-id="b23e4-229">As your program processes window messages, **GetKeyState** gives you a snapshot of the keyboard at the time that each message was queued.</span></span> <span data-ttu-id="b23e4-230">Wenn die letzte Nachricht in der Warteschlange z. b. [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)war, meldet **GetKeyState** den Tastatur Zustand zu dem Zeitpunkt, an dem der Benutzer auf die Maustaste geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="b23e4-230">For example, if the last message on the queue was [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** reports the keyboard state at the moment when the user clicked the mouse button.</span></span>

<span data-ttu-id="b23e4-231">Da [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) auf der Meldungs Warteschlange basiert, werden auch Tastatureingaben ignoriert, die an ein anderes Programm gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="b23e4-231">Because [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) is based on your message queue, it also ignores keyboard input that was sent to another program.</span></span> <span data-ttu-id="b23e4-232">Wenn der Benutzer zu einem anderen Programm wechselt, werden alle Tastenkombinationen, die an das Programm gesendet werden, von **GetKeyState** ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b23e4-232">If the user switches to another program, any key presses that are sent to that program are ignored by **GetKeyState**.</span></span> <span data-ttu-id="b23e4-233">Wenn Sie den unmittelbaren physischen Zustand der Tastatur wirklich kennen möchten, gibt es hierfür eine Funktion: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="b23e4-233">If you really want to know the immediate physical state of the keyboard, there is a function for that: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span> <span data-ttu-id="b23e4-234">Bei den meisten UI-Code ist die korrekte Funktion jedoch **GetKeyState**.</span><span class="sxs-lookup"><span data-stu-id="b23e4-234">For most UI code, however, the correct function is **GetKeyState**.</span></span>

## <a name="next"></a><span data-ttu-id="b23e4-235">Nächste</span><span class="sxs-lookup"><span data-stu-id="b23e4-235">Next</span></span>

[<span data-ttu-id="b23e4-236">Zugriffstasten Tabellen</span><span class="sxs-lookup"><span data-stu-id="b23e4-236">Accelerator Tables</span></span>](accelerator-tables.md)

 

 
