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
# <a name="keyboard-input-get-started-with-win32-and-c"></a>Tastatureingabe (Get Started with Win32 and C++)

Die Tastatur wird für verschiedene Typen von Eingaben verwendet, einschließlich:

-   Zeicheneingabe. Text, der vom Benutzer in ein Dokument oder ein Bearbeitungsfeld eingetippt wird.
-   Tastenkombinationen. Tastenkombinationen, die Anwendungsfunktionen aufrufen. beispielsweise STRG + O zum Öffnen einer Datei.
-   System Befehle. Tastenkombinationen, die Systemfunktionen aufrufen. Beispiel: Alt + Tab zum Wechseln von Fenstern.

Bei der Betrachtung von Tastatureingaben ist es wichtig, sich daran zu erinnern, dass ein Schlüssel Strich nicht mit einem Zeichen identisch ist. Wenn Sie z. b. die Taste drücken, kann dies zu einem der folgenden Zeichen führen.

-   a
-   Ein
-   á (wenn die Tastatur das Kombinieren von Diakritik unterstützt)

Wenn die Alt-Taste gedrückt gehalten wird, wird durch Drücken der Taste Alt + A erzeugt, die das System nicht als Zeichen behandelt, sondern als Systembefehl.

## <a name="key-codes"></a>Schlüssel Codes

Wenn Sie eine Taste drücken, generiert die Hardware einen Überprüfungs *Code*. Überprüfungs Codes variieren von einer Tastatur zur nächsten, und es gibt separate Überprüfungs Codes für Key-up-und Key-down-Ereignisse. Sie werden die Scan Codes fast nie interessieren. Der Tastaturtreiber übersetzt Scan Codes in *virtuelle Schlüsselcodes*. Virtuelle Schlüsselcodes sind Geräte unabhängig. Wenn Sie auf eine beliebige Tastatur eine Taste drücken, wird derselbe Code für den virtuellen Schlüssel generiert.

Im allgemeinen entsprechen die Codes von virtuellen Schlüsseln nicht ASCII-Codes oder einem anderen Zeichen Codierungsstandard. Dies ist offensichtlich, wenn Sie sich Gedanken darüber machen, da derselbe Schlüssel andere Zeichen generieren kann (a, a, á), und einige Schlüssel, wie z. b. Funktionstasten, entsprechen keinem Zeichen.

Dies bedeutet, dass die folgenden virtuellen Schlüsselcodes ASCII-Entsprechungen zugeordnet werden:

-   0 bis 9 Schlüssel = ASCII ' 0 ' – ' 9 ' (0x30 – 0x39)
-   A bis Z Keys = ASCII ' A ' – ' Z ' (0x41 – 0x5A)

In gewisser Hinsicht ist diese Zuordnung unglücklich, denn Sie sollten sich aus den beschriebenen Gründen nie mit virtuellen Schlüsselcodes als Zeichen vorstellen.

Die Header Datei WinUser. h definiert Konstanten für den größten Teil der Codes von virtuellen Schlüsseln. Beispielsweise ist der Code des virtuellen Schlüssels für die nach-links-Taste **VK \_ left** (0x25). Eine umfassende Liste der Codes für virtuelle Schlüssel finden Sie unter [**Code für virtuelle**](/windows/desktop/inputdev/virtual-key-codes)Schlüssel. Für die virtuellen Schlüsselcodes, die ASCII-Werten entsprechen, sind keine Konstanten definiert. Beispielsweise ist der Code des virtuellen Schlüssels für die A-Taste 0x41, aber es ist keine Konstante mit dem Namen " **VK \_ A**" vorhanden. Verwenden Sie stattdessen einfach den numerischen Wert.

## <a name="key-down-and-key-up-messages"></a>Key-Down und Key-Up Meldungen

Wenn Sie eine Taste drücken, empfängt das Fenster, das den Tastaturfokus besitzt, eine der folgenden Meldungen.

-   [**WM \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown)
-   [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown)

Die [**WM- \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown) -Meldung gibt eine *System Taste* an, bei der es sich um einen Schlüssel Strich handelt, der einen Systembefehl aufruft. Es gibt zwei Typen von System Schlüsseln:

-   ALT + beliebige Taste
-   F10

Die Taste F10 aktiviert die Menüleiste eines Fensters. Verschiedene Kombinationen aus Alt-Taste rufen Systembefehle auf. Beispielsweise wechselt Alt + Tab zu einem neuen Fenster. Wenn ein Fenster außerdem über ein Menü verfügt, kann die Alt-Taste zum Aktivieren von Menü Elementen verwendet werden. Einige ALT-Tastenkombinationen machen nichts.

Alle anderen Schlüssel Striche werden als nicht-Systemschlüssel betrachtet und die [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Nachricht erzeugt. Dies schließt die anderen Funktionstasten als F10 ein.

Wenn Sie einen Schlüssel freigeben, sendet das System eine entsprechende Schlüssel Nachricht:

-   [**WM- \_ KeyUp**](/windows/desktop/inputdev/wm-keyup)
-   [**WM- \_ syskeyup**](/windows/desktop/inputdev/wm-syskeyup)

Wenn Sie einen Schlüssel gedrückt halten, um die Wiederholungsfunktion der Tastatur zu starten, sendet das System mehrere Schlüssel Meldungen, gefolgt von einer einzelnen Schlüssel Nachricht.

In allen vier der bisher behandelten Tastatur Meldungen enthält der *wParam* -Parameter den Code für den virtuellen Schlüssel. Der *LPARAM* -Parameter enthält verschiedene Informationen, die in 32 Bits verpackt sind. In der Regel benötigen Sie die Informationen in *LPARAM* nicht. Ein Flag, das nützlich sein kann, ist Bit 30, das "Previous Key State"-Flag, das für wiederholte Schlüssel Meldungen auf 1 festgelegt ist.

Wie der Name schon sagt, sind Systemschlüssel Striche hauptsächlich für die Verwendung durch das Betriebssystem vorgesehen. Wenn Sie die [**WM- \_ syskeydownnachricht abfangen**](/windows/desktop/inputdev/wm-syskeydown) , müssen Sie [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) nachher aufzurufen. Andernfalls blockieren Sie die Verarbeitung des Befehls durch das Betriebssystem.

## <a name="character-messages"></a>Zeichen Nachrichten

Schlüssel Striche werden von der [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion in Zeichen konvertiert, die wir zuerst in [Modul 1](your-first-windows-program.md)gesehen haben. Diese Funktion untersucht KeyDown-Meldungen und übersetzt Sie in Zeichen. Für jedes Zeichen, das erzeugt wird, fügt die Funktion **translatemess** eine "WM char"-oder "WM"- [**\_ Sychar**](/windows/desktop/inputdev/wm-char) -Nachricht in die Nachrichten Warteschlange des Fensters ein. [**\_**](/windows/desktop/menurc/wm-syschar) Der *wParam* -Parameter der Nachricht enthält das UTF-16-Zeichen.

Möglicherweise werden WM- [**\_ char**](/windows/desktop/inputdev/wm-char) -Nachrichten aus [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Meldungen generiert, während [**WM- \_ Sychar**](/windows/desktop/menurc/wm-syschar) -Nachrichten aus [**WM- \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown) -Nachrichten generiert werden. Nehmen wir beispielsweise an, dass der Benutzer die UMSCHALTTASTE drückt, gefolgt von der A-Taste. Wenn Sie ein Standardmäßiges Tastaturlayout annehmen, erhalten Sie die folgende Sequenz von Nachrichten:

**WM \_ KeyDown**: Shift  
**WM \_ KeyDown**: A  
**WM \_ CHAR**: ' A '  


Auf der anderen Seite generiert die Kombination ALT + P Folgendes:

 **WM \_ syskeydown**: VK- \_ Menü  
**WM \_ Syskeydown**: 0x50  
**WM \_ Syschar**: ' p '  
**WM \_ Syskeyup**: 0x50  
**WM \_ KeyUp**: VK- \_ Menü  


(Der Code des virtuellen Schlüssels für die Alt-Taste wird als "VK \_ " bezeichnet. Menü aus historischen Gründen.)

Die [**WM- \_ syschar**](/windows/desktop/menurc/wm-syschar) -Meldung gibt ein System Zeichen an. Wie bei [**WM- \_ syskeydown**](/windows/desktop/inputdev/wm-syskeydown)sollten Sie diese Nachricht in der Regel direkt an [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)übergeben. Andernfalls können Sie die Standardsystem Befehle stören. Behandeln Sie vor allem die " **WM \_ syschar** " nicht als Text, den der Benutzer eingegeben hat.

Die Meldung " [**WM \_ char**](/windows/desktop/inputdev/wm-char) " ist das, was Sie normalerweise als Zeicheneingabe betrachten. Der Datentyp für das Zeichen ist **WCHAR \_ t**, das ein UTF-16-Unicode-Zeichen darstellt. Zeichen Eingaben können Zeichen außerhalb des ASCII-Bereichs enthalten, insbesondere bei Tastaturlayouts, die häufig außerhalb der USA verwendet werden. Sie können verschiedene Tastaturlayouts ausprobieren, indem Sie eine regionale Tastatur installieren und anschließend die Tastatur Funktion auf dem Bildschirm verwenden.

Benutzer können auch einen Eingabemethoden-Editor (Input Method Editor, IME) installieren, um komplexe Skripts, z. b. japanische Zeichen, mit einer Standardtastatur einzugeben. Wenn Sie z. b. eine japanische IME-Taste verwenden, um das Katakana Character カ (KA) einzugeben, erhalten Sie möglicherweise die folgenden Meldungen:

**WM \_ KeyDown**: VK \_ ProcessKey (die Taste für den IME-Prozess)  
**WM \_ KeyUp**: 0x4B  
**WM \_ KeyDown**: VK \_ ProcessKey  
**WM \_ KeyUp**: 0x41  
**WM \_ KeyDown**: VK \_ ProcessKey  
**WM \_ CHAR**: カ  
**WM \_ KeyUp**: VK \_ Return  


Einige Tastenkombinationen für STRG werden in ASCII-Steuerzeichen übersetzt. Beispielsweise wird STRG + A in das ASCII-Zeichen STRG-A (SoH) übersetzt (ASCII-Wert 0x01). Bei Texteingaben sollten Sie die Steuerzeichen in der Regel herausfiltern. Vermeiden Sie außerdem die Verwendung von [**WM \_ char**](/windows/desktop/inputdev/wm-char) zum Implementieren von Tastenkombinationen. Verwenden Sie stattdessen die [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -Meldungen, oder verwenden Sie eine Zugriffstasten Tabelle. Zugriffstasten Tabellen werden im nächsten Thema, Zugriffstasten [Tabellen](accelerator-tables.md), beschrieben.

Der folgende Code zeigt die Haupt Tastatur Meldungen im Debugger an. Experimentieren Sie mit verschiedenen Tastenkombinationen, und sehen Sie sich an, welche Meldungen generiert werden.


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



## <a name="miscellaneous-keyboard-messages"></a>Verschiedene Tastatur Meldungen

Einige andere Tastatur Meldungen können von den meisten Anwendungen sicher ignoriert werden.

-   Die [**WM \_ deadchar**](/windows/desktop/inputdev/wm-deadchar) -Nachricht wird für einen kombinierten Schlüssel, z. b. eine diakritische, gesendet. Beispielsweise wird auf der Tastatur der Sprache "Akzent" (") gefolgt von E" das Zeichen "é" erzeugt. Der **WM- \_ deadchar** -Wert wird für das Akzentzeichen gesendet.
-   Die [**WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) -Nachricht ist veraltet. Sie ermöglicht ANSI-Programmen den Empfang von Unicode-Zeichen Eingaben.
-   Das Zeichen " [**WM \_ IME \_ char**](/windows/desktop/Intl/wm-ime-char) " wird gesendet, wenn ein IME eine Tastatureingabe-Sequenz in Zeichen übersetzt. Es wird zusätzlich zur üblichen [**WM \_ char**](/windows/desktop/inputdev/wm-char) -Nachricht gesendet.

## <a name="keyboard-state"></a>Tastatur Zustand

Die Tastatur Meldungen sind ereignisgesteuert. Das heißt, Sie erhalten eine Nachricht, wenn etwas Interessantes passiert, z. b. einen Tastendruck, und die Meldung gibt Aufschluss darüber, was gerade passiert ist. Sie können den Status eines Schlüssels jedoch auch jederzeit testen, indem Sie die [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) -Funktion aufrufen.

Nehmen Sie beispielsweise an, wie Sie die Tastenkombination mit der linken Maustaste und Alt-Taste erkennen. Sie können den Zustand der Alt-Taste nachverfolgen, indem Sie auf Tastatur Schlag Nachrichten lauschen und ein Flag speichern, aber [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) spart Ihnen die Probleme. Wenn Sie die [**WM- \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Meldung erhalten, können Sie einfach **GetKeyState** wie folgt aufrufen:


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



Die [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) -Nachricht nimmt einen Code für virtuelle Schlüssel als Eingabe an und gibt einen Satz von Bitflags zurück (tatsächlich nur zwei Flags). Der Wert 0X8000 enthält das Bitflag, das testet, ob der Schlüssel aktuell gedrückt ist.

Die meisten Tastaturen haben zwei Alt-Taste, Links und rechts. Im vorherigen Beispiel wird getestet, ob eine von Ihnen gedrückt wurde. Sie können [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) auch verwenden, um zwischen den linken und rechten Instanzen der Alt-Taste, der UMSCHALTTASTE oder der STRG-Taste zu unterscheiden. Der folgende Code testet z. b., ob die Rechte ALT-Taste gedrückt ist.


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



Die [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) -Funktion ist interessant, da Sie einen *virtuellen* Tastatur Zustand meldet. Dieser virtuelle Status basiert auf dem Inhalt der Nachrichten Warteschlange und wird aktualisiert, wenn Sie Nachrichten aus der Warteschlange entfernen. Wenn das Programmfenster Meldungen verarbeitet, gibt **GetKeyState** Ihnen eine Momentaufnahme der Tastatur zu dem Zeitpunkt, zu dem die einzelnen Nachrichten in die Warteschlange eingereiht wurden. Wenn die letzte Nachricht in der Warteschlange z. b. [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown)war, meldet **GetKeyState** den Tastatur Zustand zu dem Zeitpunkt, an dem der Benutzer auf die Maustaste geklickt hat.

Da [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) auf der Meldungs Warteschlange basiert, werden auch Tastatureingaben ignoriert, die an ein anderes Programm gesendet wurden. Wenn der Benutzer zu einem anderen Programm wechselt, werden alle Tastenkombinationen, die an das Programm gesendet werden, von **GetKeyState** ignoriert. Wenn Sie den unmittelbaren physischen Zustand der Tastatur wirklich kennen möchten, gibt es hierfür eine Funktion: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate). Bei den meisten UI-Code ist die korrekte Funktion jedoch **GetKeyState**.

## <a name="next"></a>Nächste

[Zugriffstasten Tabellen](accelerator-tables.md)

 

 
