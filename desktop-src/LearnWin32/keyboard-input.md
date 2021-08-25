---
title: Tastatureingabe (Erste Schritte mit Win32 und C++)
description: Tastatureingaben
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3ed8ac1e8d7cd8e6ea35c9e9f58c10fd516cca010b5e5dce667817b32028c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822350"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a>Tastatureingabe (Erste Schritte mit Win32 und C++)

Die Tastatur wird für verschiedene Eingabetypen verwendet, einschließlich:

-   Zeicheneingabe. Text, den der Benutzer in ein Dokument oder ein Bearbeitungsfeld eingibt.
-   Tastenkombinationen. Tastenstriche, die Anwendungsfunktionen aufrufen; Drücken Sie z. B. STRG+O, um eine Datei zu öffnen.
-   Systembefehle. Tastenstriche, die Systemfunktionen aufrufen; z. B. ALT + TAB, um Fenster zu wechseln.

Bei der Tastatureingabe ist es wichtig zu beachten, dass ein Tastenstrich nicht mit einem Zeichen identisch ist. Wenn Sie z. B. die A-Taste drücken, kann dies zu einem der folgenden Zeichen führen.

-   a
-   Ein
-   á (wenn die Tastatur die Kombination diakritischer Zeichen unterstützt)

Wenn die ALT-TASTE gedrückt gehalten wird, erzeugt das Drücken der A-Taste AUßERDEM ALT+A, was das System überhaupt nicht als Zeichen behandelt, sondern als Systembefehl.

## <a name="key-codes"></a>Schlüsselcodes

Wenn Sie eine Taste drücken, generiert die Hardware einen *Scancode.* Scancodes variieren von Tastatur zu Tastatur, und es gibt separate Scancodes für Key-Up- und Key-Down-Ereignisse. Scancodes sind ihnen fast nie wichtig. Der Tastaturtreiber übersetzt Scancodes in Codes mit *virtuellen Schlüsseln.* Codes für virtuelle Schlüssel sind geräteunabhängig. Durch Drücken der A-Taste auf einer Tastatur wird der gleiche Code mit virtuellen Tasten generiert.

Im Allgemeinen entsprechen Codes für virtuelle Schlüssel weder ASCII-Codes noch einem anderen Zeichencodierungsstandard. Dies ist offensichtlich, wenn Sie darüber nachdenken, da der gleiche Schlüssel verschiedene Zeichen (a, A, á) generieren kann und einige Schlüssel, z. B. Funktionstasten, keinem Zeichen entsprechen.

Die folgenden Codes für virtuelle Schlüssel werden jedoch ASCII-Entsprechungen zugeordnet:

-   0 bis 9 Schlüssel = ASCII '0' – '9' (0x30 – 0x39)
-   A- bis Z-Schlüssel = ASCII "A" – "Z" (0x41 – 0x5A)

In einigen Punkten ist diese Zuordnung leider, da Sie sich aus den beschriebenen Gründen niemals Codes für virtuelle Schlüssel als Zeichen vorstellen sollten.

Die Headerdatei WinUser.h definiert Konstanten für die meisten Codes für virtuelle Schlüssel. Der Virtuelle Schlüsselcode für die NACH-LINKS-TASTE lautet beispielsweise **VK \_ LEFT** (0x25). Die vollständige Liste der Codes für virtuelle Schlüssel finden Sie unter Codes für [**virtuelle Schlüssel.**](/windows/desktop/inputdev/virtual-key-codes) Für die Codes mit virtuellen Schlüsseln, die ASCII-Werten entsprechen, werden keine Konstanten definiert. Beispielsweise ist der Code des virtuellen Schlüssels für den A-Schlüssel 0x41, aber es gibt keine Konstante mit dem Namen **VK \_ A.** Verwenden Sie stattdessen einfach den numerischen Wert.

## <a name="key-down-and-key-up-messages"></a>Key-Down und Key-Up Nachrichten

Wenn Sie eine Taste drücken, empfängt das Fenster mit Tastaturfokus eine der folgenden Meldungen.

-   [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)
-   [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)

Die [**WM \_ SYSKEYDOWN-Meldung**](/windows/desktop/inputdev/wm-syskeydown) gibt einen *Systemschlüssel* an, bei dem es sich um einen Schlüsselstrich handelt, der einen Systembefehl aufruft. Es gibt zwei Arten von Systemschlüsseln:

-   ALT + beliebiger Schlüssel
-   F10

Die Taste F10 aktiviert die Menüleiste eines Fensters. Verschiedene ALT-Tastenkombinationen rufen Systembefehle auf. Beispielsweise wechselt ALT + TAB zu einem neuen Fenster. Wenn ein Fenster über ein Menü verfügt, kann außerdem die ALT-TASTE verwendet werden, um Menüelemente zu aktivieren. Einige ALT-Tastenkombinationen haben keinerlei Möglichkeiten.

Alle anderen Tastenstriche werden als Nichtsystemschlüssel betrachtet und erzeugen die [**WM \_ KEYDOWN-Nachricht.**](/windows/desktop/inputdev/wm-keydown) Dies schließt die anderen Funktionsschlüssel als F10 ein.

Wenn Sie einen Schlüssel freigeben, sendet das System eine entsprechende Key-Up-Nachricht:

-   [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)
-   [**WM \_ SYSKEYUP**](/windows/desktop/inputdev/wm-syskeyup)

Wenn Sie eine Taste gedrückt halten, die lang genug ist, um die Wiederholungsfunktion der Tastatur zu starten, sendet das System mehrere Tastenabdehnungsmeldungen, gefolgt von einer einzelnen Taste-nach-oben-Nachricht.

In allen vier tastaturbasierten Meldungen, die bisher erläutert wurden, enthält der *wParam-Parameter* den Virtuellen Schlüsselcode des Schlüssels. Der *lParam-Parameter* enthält verschiedene Informationen, die in 32 Bits gepackt sind. In der Regel benötigen Sie die Informationen in *lParam* nicht. Ein flag, das nützlich sein kann, ist Bit 30, das Flag "Vorheriger Schlüsselzustand", das für wiederholte Key-Down-Nachrichten auf 1 festgelegt ist.

Wie der Name schon sagt, sind Systemschlüsselstriche in erster Linie für die Verwendung durch das Betriebssystem vorgesehen. Wenn Sie die [**\_ WM-SYSKEYDOWN-Nachricht**](/windows/desktop/inputdev/wm-syskeydown) abfangen, rufen Sie [**defWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) anschließend auf. Andernfalls blockieren Sie die Verarbeitung des Befehls durch das Betriebssystem.

## <a name="character-messages"></a>Zeichenmeldungen

Schlüsselstriche werden von der [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) in Zeichen konvertiert, die wir zum ersten Mal in [Modul 1](your-first-windows-program.md)gesehen haben. Diese Funktion untersucht Key-Down-Nachrichten und übersetzt sie in Zeichen. Für jedes erzeugte Zeichen fügt die **TranslateMessage-Funktion** eine [**WM \_ CHAR-**](/windows/desktop/inputdev/wm-char) oder [**WM \_ SYSCHAR-Nachricht**](/windows/desktop/menurc/wm-syschar) in die Nachrichtenwarteschlange des Fensters ein. Der *wParam-Parameter* der Nachricht enthält das UTF-16-Zeichen.

Wie Sie vielleicht vermuten, werden [**WM \_ CHAR-Nachrichten**](/windows/desktop/inputdev/wm-char) aus [**WM \_ KEYDOWN-Nachrichten**](/windows/desktop/inputdev/wm-keydown) generiert, während [**WM \_ SYSCHAR-Nachrichten**](/windows/desktop/menurc/wm-syschar) aus [**WM \_ SYSKEYDOWN-Nachrichten**](/windows/desktop/inputdev/wm-syskeydown) generiert werden. Angenommen, der Benutzer drückt die UMSCHALTTASTE gefolgt von der TASTE A. Wenn Sie ein Standardtastaturlayout verwenden, erhalten Sie die folgende Sequenz von Meldungen:

**WM \_ KEYDOWN:** UMSCHALT  
**WM \_ KEYDOWN:** A  
**WM \_ CHAR**: 'A'  


Andererseits würde die Kombination ALT +P Folgendes generieren:

 **WM \_ SYSKEYDOWN:** \_ VK-MENÜ  
**WM \_ SYSKEYDOWN:** 0x50  
**WM \_ SYSCHAR:**'p'  
**WM \_ SYSKEYUP:** 0x50  
**WM \_ KEYUP:** \_ VK-MENÜ  


(Der Code des virtuellen Schlüssels für den ALT-Schlüssel heißt VK. \_ MENU aus historischen Gründen.)

Die [**WM \_ SYSCHAR-Meldung**](/windows/desktop/menurc/wm-syschar) gibt ein Systemzeichen an. Wie bei [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)sollten Sie diese Meldung in der Regel direkt an [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben. Andernfalls können Standardsystembefehle beeinträchtigt werden. Behandeln Sie WM **\_ SYSCHAR** insbesondere nicht als Text, den der Benutzer eingegeben hat.

Die [**WM \_ CHAR-Nachricht**](/windows/desktop/inputdev/wm-char) ist das, was Sie normalerweise als Zeicheneingabe betrachten. Der Datentyp für das Zeichen ist **wchar \_ t**, der ein UTF-16 Unicode-Zeichen darstellt. Die Zeicheneingabe kann Zeichen außerhalb des ASCII-Bereichs enthalten, insbesondere bei Tastaturlayouts, die häufig außerhalb der USA verwendet werden. Sie können verschiedene Tastaturlayouts ausprobieren, indem Sie eine regionale Tastatur installieren und dann das Feature Bildschirmtastatur verwenden.

Benutzer können auch einen Eingabemethoden-Editor (Input Method Editor, IME) installieren, um komplexe Skripts wie japanische Zeichen mit einer Standardtastatur einzugeben. Wenn Sie beispielsweise eine japanische IME verwenden, um das Katakana-Zeichen (ka) einzugeben, erhalten Sie möglicherweise die folgenden Meldungen:

**WM \_ KEYDOWN:** VK \_ PROCESSKEY (der IME PROCESS-Schlüssel)  
**WM \_ KEYUP:** 0x4B  
**WM \_ KEYDOWN:** VK \_ PROCESSKEY  
**WM \_ KEYUP:** 0x41  
**WM \_ KEYDOWN:** VK \_ PROCESSKEY  
**WM \_ CHAR:**  
**WM \_ KEYUP:** VK \_ RETURN  


Einige Tastenkombinationen mit STRG werden in ASCII-Steuerzeichen übersetzt. Beispielsweise wird STRG+A in das ASCII-ZEICHEN STRG+A (SOH) (ASCII-Wert 0x01) übersetzt. Bei der Texteingabe sollten Sie in der Regel die Steuerzeichen herausfiltern. Vermeiden Sie außerdem die Verwendung von [**WM \_ CHAR,**](/windows/desktop/inputdev/wm-char) um Tastenkombinationen zu implementieren. Verwenden Sie stattdessen [**WM \_ KEYDOWN-Nachrichten,**](/windows/desktop/inputdev/wm-keydown) oder besser noch, eine Zugriffstastentabelle. Zugriffstastentabellen werden im nächsten Thema, [Accelerator Tables , beschrieben.](accelerator-tables.md)

Der folgende Code zeigt die Haupttastaturmeldungen im Debugger an. Versuchen Sie, mit verschiedenen Tastenkombinationen zu spielen und zu sehen, welche Meldungen generiert werden.


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



## <a name="miscellaneous-keyboard-messages"></a>Sonstige Tastaturmeldungen

Einige andere Tastaturmeldungen können von den meisten Anwendungen ignoriert werden.

-   Die [**WM \_ DEADCHAR-Nachricht**](/windows/desktop/inputdev/wm-deadchar) wird für einen Kombinationsschlüssel gesendet, z. B. für einen diakritischen Schlüssel. Wenn Sie beispielsweise auf einer Tastatur in spanischer Sprache Akzent (') gefolgt von E eingeben, wird das Zeichen "e" erzeugt. WM **\_ DEADCHAR wird** für das Akzentzeichen gesendet.
-   Die [**WM \_ UNICHAR-Nachricht**](/windows/desktop/inputdev/wm-unichar) ist veraltet. Dadurch können ANSI-Programme Unicode-Zeicheneingaben empfangen.
-   Das [**WM \_ IME \_ CHAR-Zeichen**](/windows/desktop/Intl/wm-ime-char) wird gesendet, wenn ein IME eine Tastatureingabesequenz in Zeichen übersetzt. Er wird zusätzlich zur üblichen [**WM \_ CHAR-Nachricht**](/windows/desktop/inputdev/wm-char) gesendet.

## <a name="keyboard-state"></a>Tastaturstatus

Die Tastaturmeldungen sind ereignisgesteuert. Das heißt, Sie erhalten eine Meldung, wenn etwas Interessantes passiert, z. B. ein Drücken der Taste, und die Meldung informiert Sie darüber, was gerade passiert ist. Sie können den Zustand eines Schlüssels aber auch jederzeit testen, indem Sie die [**GetKeyState-Funktion**](/windows/desktop/api/winuser/nf-winuser-getkeystate) aufrufen.

Überlegen Sie beispielsweise, wie Sie die Kombination aus linker Maustaste und ALT-TASTE erkennen würden. Sie können den Zustand der ALT-TASTE nachverfolgen, indem Sie auf Tastenstrichmeldungen lauschen und ein Flag speichern. [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) erspart Ihnen jedoch die Probleme. Wenn Sie die [**\_ WM-LBUTTONDOWN-Nachricht**](/windows/desktop/inputdev/wm-lbuttondown) erhalten, rufen Sie **getKeyState einfach** wie folgt auf:


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



Die [**GetKeyState-Nachricht**](/windows/desktop/api/winuser/nf-winuser-getkeystate) verwendet einen virtuellen Schlüsselcode als Eingabe und gibt einen Satz von Bitflags zurück (eigentlich nur zwei Flags). Der Wert 0x8000 das Bitflag enthält, das testet, ob die Taste gerade gedrückt wird.

Die meisten Tastaturen verfügen über zwei ALT-Tasten: links und rechts. Im vorherigen Beispiel wird überprüft, ob eines der Beiden gedrückt ist. Sie können auch [**GetKeyState verwenden,**](/windows/desktop/api/winuser/nf-winuser-getkeystate) um zwischen den linken und rechten Instanzen der ALT-, UMSCHALT- oder STRG-Tasten zu unterscheiden. Der folgende Code testet beispielsweise, ob die rechte ALT-TASTE gedrückt wird.


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



Die [**GetKeyState-Funktion**](/windows/desktop/api/winuser/nf-winuser-getkeystate) ist interessant, da sie einen *virtuellen Tastaturzustand* meldet. Dieser virtuelle Status basiert auf dem Inhalt Ihrer Nachrichtenwarteschlange und wird aktualisiert, wenn Sie Nachrichten aus der Warteschlange entfernen. Während das Programm Fenstermeldungen verarbeitet, erhalten Sie mit **GetKeyState** eine Momentaufnahme der Tastatur zu dem Zeitpunkt, zu dem jede Nachricht in die Warteschlange gestellt wurde. Wenn beispielsweise die letzte Nachricht in der Warteschlange [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)war, meldet **GetKeyState** den Tastaturzustand zu dem Zeitpunkt, zu dem der Benutzer auf die Maustaste geklickt hat.

Da [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) auf Ihrer Nachrichtenwarteschlange basiert, ignoriert es auch Tastatureingaben, die an ein anderes Programm gesendet wurden. Wenn der Benutzer zu einem anderen Programm wechselt, werden alle Tastendrucke, die an dieses Programm gesendet werden, von **GetKeyState ignoriert.** Wenn Sie wirklich den unmittelbaren physischen Zustand der Tastatur kennen möchten, gibt es dafür eine Funktion: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate). Für die meisten Ui-Code ist die richtige Funktion **jedoch GetKeyState.**

## <a name="next"></a>Nächste

[Zugriffstastentabellen](accelerator-tables.md)

 

 
