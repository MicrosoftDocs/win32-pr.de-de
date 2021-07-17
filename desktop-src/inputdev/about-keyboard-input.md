---
title: Informationen zur Tastatureingabe
description: In diesem Thema wird die Tastatureingabe erläutert.
ms.assetid: de34727e-e8c7-481d-982d-0e42a02704db
keywords:
- Benutzereingabe,Tastatureingabe
- Erfassen von Benutzereingaben, Tastatureingabe
- Tastatureingabe
- Tastaturfokus
- Tastatureingabemeldungen
- Zeichenmeldungen
- Systemtastenanschläge
- Nichtsystemtastenanschläge
- Nichtsystemzeichenmeldungen
- In dead keys
- Nachrichten mit in dead-Zeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de85794901be3fef37156bde29520039f85702b
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373195"
---
# <a name="about-keyboard-input"></a>Informationen zur Tastatureingabe

Anwendungen sollten Benutzereingaben über die Tastatur und über die Maus akzeptieren. Eine Anwendung empfängt Tastatureingaben in Form von Nachrichten, die an ihre Fenster gesendet werden.

Dieser Abschnitt enthält die folgenden Themen:

-   [Tastatureingabemodell](#keyboard-input-model)
-   [Tastaturfokus und -aktivierung](#keyboard-focus-and-activation)
-   [Tastatureingabemeldungen](#keystroke-messages)
    -   [System- und Nichtsystem-Tastatureingaben](#system-and-nonsystem-keystrokes)
    -   [Beschriebene Codes für virtuelle Schlüssel](#virtual-key-codes-described)
    -   [Meldungsflags für Tastatureingaben](#keystroke-message-flags)
-   [Zeichenmeldungen](#character-messages)
    -   [Nichtsystemzeichenmeldungen](#nonsystem-character-messages)
    -   [Nachrichten mit ungefingenen Zeichen](#dead-character-messages)
-   [Schlüsselstatus](#key-status)
-   [Tastaturanschläge und Zeichenübersetzungen](#keystroke-and-character-translations)
-   [Hot-Key-Unterstützung](#hot-key-support)
-   [Tastaturtasten für Das Durchsuchen und andere Funktionen](#keyboard-keys-for-browsing-and-other-functions)
-   [Simulieren von Eingaben](#simulating-input)
-   [Sprachen, Locales und Tastaturlayouts](#languages-locales-and-keyboard-layouts)

## <a name="keyboard-input-model"></a>Tastatureingabemodell

Das System bietet geräteunabhängige Tastaturunterstützung für Anwendungen, indem ein Tastaturgerätetreiber installiert wird, der für die aktuelle Tastatur geeignet ist. Das System bietet sprachunabhängige Tastaturunterstützung mithilfe des sprachspezifischen Tastaturlayouts, das derzeit vom Benutzer oder der Anwendung ausgewählt wird. Der Tastaturgerätetreiber empfängt Scancodes von der Tastatur, die an das Tastaturlayout gesendet werden, wo sie in Nachrichten übersetzt und an die entsprechenden Fenster in Ihrer Anwendung gesendet werden.

Jeder Taste auf einer Tastatur ist ein eindeutiger Wert zugewiesen, der als Scancode bezeichnet *wird.* Dabei handelt es sich um einen geräteabhängigen Bezeichner für die Taste auf der Tastatur. Eine Tastatur generiert zwei Scancodes, wenn der Benutzer eine Taste ein gibt– einen, wenn der Benutzer die Taste drückt, und einen anderen, wenn der Benutzer die Taste frei gibt.

Der Tastaturgerätetreiber interpretiert einen Scancode und übersetzt ihn in einen virtuellen Schlüsselcode *,einen* geräteunabhängigen Wert, der vom System definiert wird und den Zweck einer Taste identifiziert. Nach der Übersetzung eines Scancodes erstellt das Tastaturlayout eine Meldung, die den Scancode, den Code der virtuellen Taste und andere Informationen über die Tastatureingabe enthält, und platziert die Nachricht dann in der Systemnachrichtenwarteschlange. Das System entfernt die Nachricht aus der Systemnachrichtenwarteschlange und übermittelt sie an die Nachrichtenwarteschlange des entsprechenden Threads. Schließlich entfernt die Meldungsschleife des Threads die Nachricht und übergibt sie zur Verarbeitung an die entsprechende Fensterprozedur. Die folgende Abbildung veranschaulicht das Tastatureingabemodell.

![Tastatureingabeverarbeitungsmodell](images/csinp-01.png)

## <a name="keyboard-focus-and-activation"></a>Tastaturfokus und -aktivierung

Das System übermittelt Tastaturmeldungen an die Nachrichtenwarteschlange des Vordergrundthreads, der das Fenster mit dem Tastaturfokus erstellt hat. Der *Tastaturfokus* ist eine temporäre Eigenschaft eines Fensters. Das System teilt die Tastatur für alle Fenster auf der Anzeige, indem es den Tastaturfokus in Der Richtung des Benutzers von einem Fenster in ein anderes verschiebt. Das Fenster mit dem Tastaturfokus empfängt (aus der Nachrichtenwarteschlange des Threads, der ihn erstellt hat) alle Tastaturmeldungen, bis sich der Fokus in ein anderes Fenster ändert.

Ein Thread kann die [**GetFocus-Funktion**](/windows/win32/api/winuser/nf-winuser-getfocus) aufrufen, um zu bestimmen, welches seiner Fenster (sofern verfügbar) derzeit den Tastaturfokus besitzt. Ein Thread kann den Tastaturfokus auf eines seiner Fenster legen, indem er die [**SetFocus-Funktion**](/windows/win32/api/winuser/nf-winuser-setfocus) aufruft. Wenn sich der Tastaturfokus von einem Fenster in ein anderes ändert, sendet das System eine WM KILLFOCUS-Nachricht an das Fenster, das den Fokus verloren hat, und sendet dann eine [**WM \_ SETFOCUS-Nachricht**](wm-setfocus.md) an das Fenster, das den Fokus erhalten hat. [**\_**](wm-killfocus.md)

Das Konzept des Tastaturfokus bezieht sich auf das des aktiven Fensters. Das *aktive Fenster* ist das Fenster der obersten Ebene, mit dem der Benutzer gerade arbeitet. Das Fenster mit dem Tastaturfokus ist entweder das aktive Fenster oder ein untergeordnetes Fenster des aktiven Fensters. Damit der Benutzer das aktive Fenster identifizieren kann, platziert das System es oben in der Z-Reihenfolge und hebt seine Titelleiste (sofern es eines auf hat) und den Rahmen hervor.

Der Benutzer kann ein Fenster der obersten Ebene aktivieren, indem er darauf klickt, es mithilfe der Tastenkombination ALT+TAB oder ALT+ESC auswählt oder es aus der Aufgabenliste. Ein Thread kann ein Fenster der obersten Ebene mithilfe der [**SetActiveWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-setactivewindow) aktivieren. Mithilfe der [**GetActiveWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-getactivewindow) kann ermittelt werden, ob ein erstelltes Fenster der obersten Ebene aktiv ist.

Wenn ein Fenster deaktiviert und ein anderes aktiviert wird, sendet das System die [**WM \_ ACTIVATE-Nachricht.**](wm-activate.md) Das niedrige Wort des *wParam-Parameters* ist 0 (null), wenn das Fenster deaktiviert wird, und ungleich 0 (null), wenn es aktiviert wird. Wenn die Standardfensterprozedur die **WM \_ ACTIVATE-Meldung** empfängt, wird der Tastaturfokus auf das aktive Fenster festgelegt.

Um zu blockieren, dass Tastatur- und Mauseingabeereignisse Anwendungen erreichen, verwenden [**Sie BlockInput**](/windows/win32/api/winuser/nf-winuser-blockinput). Beachten Sie, dass **die BlockInput-Funktion** die asynchrone Eingabezustandstabelle der Tastatur nicht beeinträchtigt. Dies bedeutet, dass das Aufrufen der [**SendInput-Funktion,**](/windows/win32/api/winuser/nf-winuser-sendinput) während die Eingabe blockiert wird, die asynchrone Eingabezustandstabelle ändert.

## <a name="keystroke-messages"></a>Tastatureingabemeldungen

Durch Drücken einer Taste wird eine [**WM \_ KEYDOWN-**](wm-keydown.md) oder [**WM \_ SYSKEYDOWN-Nachricht**](wm-syskeydown.md) in die Threadnachrichtenwarteschlange platziert, die an das Fenster angefügt ist, das den Tastaturfokus besitzt. Das Freigeben eines Schlüssels bewirkt, dass eine [**WM \_ KEYUP-**](wm-keyup.md) oder [**WM \_ SYSKEYUP-Nachricht**](wm-syskeyup.md) in die Warteschlange gestellt wird.

Tastenauf- und Tastenkombinationsmeldungen treten in der Regel paarweise auf. Wenn der Benutzer jedoch eine Taste hält, die lang genug ist, um die automatische Wiederholungsfunktion der Tastatur zu starten, generiert das System eine Reihe von [**WM \_ KEYDOWN-**](wm-keydown.md) oder [**WM \_ SYSKEYDOWN-Meldungen**](wm-syskeydown.md) in einer Zeile. Anschließend wird eine einzelne [**WM \_ KEYUP-**](wm-keyup.md) oder [**WM \_ SYSKEYUP-Nachricht**](wm-syskeyup.md) generiert, wenn der Benutzer den Schlüssel frei gibt.

Dieser Abschnitt enthält die folgenden Themen:

-   [System- und Nichtsystem-Tastatureingaben](#system-and-nonsystem-keystrokes)
-   [Beschriebene Codes für virtuelle Schlüssel](#virtual-key-codes-described)
-   [Meldungsflags für Tastatureingaben](#keystroke-message-flags)

### <a name="system-and-nonsystem-keystrokes"></a>System- und Nichtsystem-Tastatureingaben

Das System unterscheidet zwischen Systemtastenanschlägen und Nichtsystemtastenanschlägen. Systemtasteneingaben erzeugen Systemtasteneingabemeldungen, [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) und [**WM \_ SYSKEYUP.**](wm-syskeyup.md) Nichtsystemtasteneingaben erzeugen Nichtsystem-Tastatureingabemeldungen, [**WM \_ KEYDOWN**](wm-keydown.md) und [**WM \_ KEYUP**](wm-keyup.md).

Wenn Ihre Fensterprozedur eine Systemtasteneingabenachricht verarbeiten muss, stellen Sie sicher, dass sie nach der Verarbeitung der Nachricht von der Prozedur an die [**DefWindowProc-Funktion übergeben**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) wird. Andernfalls werden alle Systemvorgänge mit der ALT-TASTE deaktiviert, wenn das Fenster den Tastaturfokus besitzt. Das heißt, der Benutzer kann nicht auf die Menüs oder das Systemmenü des Fensters zugreifen oder die Tastenkombination ALT+ESC oder ALT+TAB verwenden, um ein anderes Fenster zu aktivieren.

Systemtasteneingabemeldungen sind in erster Linie für die Verwendung durch das System und nicht durch eine Anwendung. Das System verwendet sie, um die integrierte Tastaturschnittstelle für Menüs zur Verfügung zu stellen und dem Benutzer zu ermöglichen, zu steuern, welches Fenster aktiv ist. Systemtasteneingabemeldungen werden generiert, wenn der Benutzer eine Taste in Kombination mit der ALT-Taste ein gibt oder wenn der Benutzer ein- und kein Fenster den Tastaturfokus besitzt (z. B. wenn die aktive Anwendung minimiert ist). In diesem Fall werden die Nachrichten an die Nachrichtenwarteschlange gesendet, die an das aktive Fenster angefügt ist.

Nichtsystemtasteneingabemeldungen sind für die Verwendung durch Anwendungsfenster verfügbar. Die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) führt nichts mit ihnen aus. Eine Fensterprozedur kann alle Nichtsystem-Tastatureingabemeldungen verwerfen, die sie nicht benötigt.

### <a name="virtual-key-codes-described"></a>Virtual-Key Codes

Der **wParam-Parameter** einer Tastatureingabenachricht enthält den virtuellen Schlüsselcode der Taste, die gedrückt oder freigegeben wurde. Eine Fensterprozedur verarbeitet oder ignoriert eine Tastatureingabemeldung, abhängig vom Wert des Codes für virtuelle Schlüssel.

Eine typische Fensterprozedur verarbeitet nur eine kleine Teilmenge der Tastaturanschläge, die sie empfängt, und ignoriert den Rest. Eine Fensterprozedur kann z. B. nur [**WM \_ KEYDOWN-Tastatureingabemeldungen**](wm-keydown.md) verarbeiten, und nur solche, die virtuelle Schlüsselcodes für die Cursorbewegungsschlüssel, Umschalttasten (auch als Steuerungsschlüssel bezeichnet) und Funktionstasten enthalten. Eine typische Fensterprozedur verarbeiten keine Tastatureingabemeldungen von Zeichentasten. Stattdessen wird die [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) verwendet, um die Nachricht in Zeichennachrichten zu konvertieren. Weitere Informationen zu **TranslateMessage und Zeichennachrichten** finden Sie unter [Zeichenmeldungen](#character-messages).

### <a name="keystroke-message-flags"></a>Meldungsflags für Tastatureingaben

Der **lParam-Parameter** einer Tastatureingabenachricht enthält zusätzliche Informationen über die Tastatureingabe, die die Nachricht generiert hat. Diese Informationen umfassen die Wiederholungsanzahl, den Überprüfungscode, das Flag für erweiterte Schlüssel, den Kontextcode, das vorherige Schlüsselzustandsflag und das Übergangszustandsflag. Die folgende Abbildung zeigt die Speicherorte dieser Flags und Werte im **lParam-Parameter.**

![die Positionen der Flags und Werte im lparam-Parameter einer Tastatureingabenachricht](images/csinp-02.png)

Eine Anwendung kann die folgenden Werte verwenden, um die Tastatureingabeflags zu bearbeiten.



| Wert            | BESCHREIBUNG                                                                       |
|------------------|-----------------------------------------------------------------------------------|
| **\_ALT-AB-ALT-TASTE**  | Bearbeitet das ALT-Tastenflag, das angibt, ob die ALT-TASTE gedrückt wird.     |
| **KF \_ DLGMODE**  | Bearbeitet das Dialogfeldmodusflag, das angibt, ob ein Dialogfeld aktiv ist. |
| **EXTENDED \_ (ERWEITERT)** | Bearbeitet das erweiterte Schlüsselflag.                                                |
| **MENUMODE \_ (MENÜMODUS)** | Bearbeitet das Menümodusflag, das angibt, ob ein Menü aktiv ist.         |
| **\_BESENSER WIEDERHOLUNG**   | Bearbeitet das vorherige Schlüsselzustandsflag.                                          |
| **\_NACH-OBEN**       | Bearbeitet das Übergangszustandsflag.                                            |

Beispielcode:

```cpp
case WM_KEYDOWN:
case WM_KEYUP:
case WM_SYSKEYDOWN:
case WM_SYSKEYUP:
{
    WORD vkCode = LOWORD(wParam);                                       // virtual-key code

    BYTE scanCode = LOBYTE(HIWORD(lParam));                             // scan code
    BOOL scanCodeE0 = (HIWORD(lParam) & KF_EXTENDED) == KF_EXTENDED;    // extended-key flag, 1 if scancode has 0xE0 prefix

    BOOL upFlag = (HIWORD(lParam) & KF_UP) == KF_UP;                    // transition-state flag, 1 on keyup
    BOOL repeatFlag = (HIWORD(lParam) & KF_REPEAT) == KF_REPEAT;        // previous key-state flag, 1 on autorepeat
    WORD repeatCount = LOWORD(lParam);                                  // repeat count, > 0 if several keydown messages was combined into one message

    BOOL altDownFlag = (HIWORD(lParam) & KF_ALTDOWN) == KF_ALTDOWN;     // ALT key was pressed

    BOOL dlgModeFlag = (HIWORD(lParam) & KF_DLGMODE) == KF_DLGMODE;     // dialog box is active
    BOOL menuModeFlag = (HIWORD(lParam) & KF_MENUMODE) == KF_MENUMODE;  // menu is active
    
    // ...
}
break;
```

### <a name="repeat-count"></a>Zahl der Wiederholungen

Sie können die Wiederholungsanzahl überprüfen, um zu bestimmen, ob eine Tastatureingabenachricht mehr als einen Tastaturanschlag darstellt. Das System erhöht die Anzahl, wenn die Tastatur [**WM \_ KEYDOWN-**](wm-keydown.md) oder [**WM \_ SYSKEYDOWN-Meldungen**](wm-syskeydown.md) schneller generiert, als eine Anwendung sie verarbeiten kann. Dies tritt häufig auf, wenn der Benutzer eine Taste lang genug hält, um das Feature für automatische Wiederholungen der Tastatur zu starten. Anstatt die Systemnachrichtenwarteschlange mit den resultierenden Key-Down-Nachrichten zu füllen, kombiniert das System die Nachrichten in einer einzelnen Key Down-Nachricht und erhöht die Wiederholungsanzahl. Das Freigeben eines Schlüssels kann das Feature für die automatische Wiederholung nicht starten, sodass die Wiederholungsanzahl für [**WM \_ KEYUP-**](wm-keyup.md) und [**WM \_ SYSKEYUP-Nachrichten**](wm-syskeyup.md) immer auf 1 festgelegt ist.

### <a name="scan-code"></a>Scan Code

Der Scancode ist der Wert, den die Tastaturhardware generiert, wenn der Benutzer eine Taste drückt. Es handelt sich um einen geräteabhängigen Wert, der den gedrückten Schlüssel identifiziert, im Gegensatz zum durch die Taste dargestellten Zeichen. Eine Anwendung ignoriert in der Regel Scancodes. Stattdessen werden geräteunabhängige Codes für virtuelle Schlüssel verwendet, um Tastatureingabemeldungen zu interpretieren.

### <a name="extended-key-flag"></a>Extended-Key Flag

Das Flag für erweiterte Tasten gibt an, ob die Tastatureingabenachricht von einer der zusätzlichen Tasten auf der erweiterten Tastatur stammt. Die erweiterten Tasten bestehen aus der ALT- und STRG-Taste auf der rechten Seite der Tastatur. DIE INS-, DEL-, HOME-, END-, PAGE UP-, PAGE DOWN- und Pfeiltasten in den Clustern links neben der numerischen Tastatur; DIE NUM-SPERRE; DIE STRG+PAUSE-TASTE; PRINT PRINTN-Taste; und die Division (/) und die EINGABETASTEn in der numerischen Tastatur. Das Flag für erweiterte Schlüssel wird festgelegt, wenn der Schlüssel ein erweiterter Schlüssel ist.

Wenn angegeben, wurde dem Scancode ein Präfix byte mit dem Wert 0xE0 (224) vorangestellt.

### <a name="context-code"></a>Kontextcode

Der Kontextcode gibt an, ob die ALT-TASTE beim Erstellen der Tastatureingabenachricht nicht mehr verwendet wurde. Der Code ist 1, wenn die ALT-TASTE gedrückt war, und 0, wenn sie hoch war.

### <a name="previous-key-state-flag"></a>Vorheriges Key-State Flag

Das vorherige Schlüsselzustandsflag gibt an, ob der Schlüssel, der die Tastatureingabenachricht generiert hat, zuvor nach oben oder unten war. Er ist 1, wenn der Schlüssel zuvor heruntergefahren war, und 0, wenn der Schlüssel zuvor hoch war. Sie können dieses Flag verwenden, um Tastatureingabemeldungen zu identifizieren, die von der Automatischen Wiederholungsfunktion der Tastatur generiert wurden. Dieses Flag ist auf 1 für [**WM \_ KEYDOWN-**](wm-keydown.md) und [**WM \_ SYSKEYDOWN-Tastatureingabemeldungen**](wm-syskeydown.md) festgelegt, die von der automatischen Wiederholungsfunktion generiert werden. Sie ist für WM [**\_ KEYUP-**](wm-keyup.md) und [**WM \_ SYSKEYUP-Meldungen immer auf**](wm-syskeyup.md) 1 festgelegt.

### <a name="transition-state-flag"></a>Transition-State Flag

Das Übergangszustandsflag gibt an, ob durch Drücken einer Taste oder Freigeben einer Taste die Tastatureingabemeldung generiert wurde. Dieses Flag ist für [**WM \_ KEYDOWN-**](wm-keydown.md) und [**WM \_ SYSKEYDOWN-Meldungen**](wm-syskeydown.md) immer auf 0 festgelegt. Für [**WM \_ KEYUP-**](wm-keyup.md) und [**WM \_ SYSKEYUP-Meldungen**](wm-syskeyup.md) ist es immer auf 1 festgelegt.

## <a name="character-messages"></a>Zeichenmeldungen

Tastatureingabemeldungen enthalten viele Informationen zu Tastaturanschlägen, stellen jedoch keine Zeichencodes für Zeichentasteneingaben zur Verfügung. Um Zeichencodes abzurufen, muss eine Anwendung die [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) in ihre Threadnachrichtenschleife ein schließen. **TranslateMessage** übergibt eine [**WM \_ KEYDOWN- oder**](wm-keydown.md) WM [**\_ SYSKEYDOWN-Nachricht**](wm-syskeydown.md) an das Tastaturlayout. Das Layout untersucht den virtuellen Schlüsselcode der Nachricht und stellt, wenn er einem Zeichenschlüssel entspricht, das Äquivalent des Zeichencodes (unter Berücksichtigung des Zustands der UMSCHALT- und CAPS LOCK-Schlüssel) zur Lage. Anschließend wird eine Zeichenmeldung generiert, die den Zeichencode enthält, und die Nachricht wird am Anfang der Nachrichtenwarteschlange platziert. Bei der nächsten Iteration der Nachrichtenschleife wird die Zeichennachricht aus der Warteschlange entfernt und an die entsprechende Fensterprozedur gesendet.

Dieser Abschnitt enthält die folgenden Themen:

-   [Nichtsystemzeichenmeldungen](#nonsystem-character-messages)
-   [Nachrichten mit ungefingenen Zeichen](#dead-character-messages)

### <a name="nonsystem-character-messages"></a>Nichtsystemzeichenmeldungen

Eine Fensterprozedur kann die folgenden Zeichenmeldungen empfangen: [**WM \_ CHAR**](wm-char.md), [**WM \_ DEADCHAR**](wm-deadchar.md), [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar), [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)und [**WM \_ UNICHAR**](wm-unichar.md). Die [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) generiert eine **WM \_ CHAR-** oder **WM \_ DEADCHAR-Nachricht,** wenn sie eine [**WM \_ KEYDOWN-Nachricht**](wm-keydown.md) verarbeitet. Auf ähnliche Weise wird eine **WM \_ SYSCHAR-** oder **WM \_ SYSDEADCHAR-Meldung** generiert, wenn eine [**WM \_ SYSKEYDOWN-Nachricht verarbeitet**](wm-syskeydown.md) wird.

Eine Anwendung, die Tastatureingaben verarbeitet, ignoriert in der Regel alle [**WM \_ CHAR-**](wm-char.md) und [**WM \_ UNICHAR-Meldungen**](wm-unichar.md) und über gibt alle anderen Nachrichten an die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) weiter. Beachten **Sie, dass WM \_ CHAR** das 16-Bit-Unicode-Transformationsformat (UTF) verwendet, während **WM \_ UNICHAR** UTF-32 verwendet. Das System verwendet die [**WM \_ SYSCHAR-**](/windows/desktop/menurc/wm-syschar) und [**WM \_ SYSDEADCHAR-Meldungen,**](wm-sysdeadchar.md) um Menü-Mnemonische Nachrichten zu implementieren.

Der **wParam-Parameter** aller Zeichenmeldungen enthält den Zeichencode der gedrückten Zeichentaste. Der Wert des Zeichencodes hängt von der Fensterklasse des Fensters ab, das die Nachricht empfängt. Wenn die Unicode-Version der [**RegisterClass-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerclassa) verwendet wurde, um die Fensterklasse zu registrieren, stellt das System Unicode-Zeichen für alle Fenster dieser Klasse zur Verfügung. Andernfalls stellt das System ASCII-Zeichencodes zur. Weitere Informationen finden Sie unter [Unicode und Zeichensätze.](/windows/desktop/Intl/unicode-and-character-sets)

Der Inhalt des **lParam-Parameters** einer Zeichenmeldung ist identisch mit dem Inhalt des **lParam-Parameters** der Key-Down-Nachricht, die übersetzt wurde, um die Zeichenmeldung zu erzeugen. Weitere Informationen finden Sie unter [Keystroke Message Flags](#keystroke-message-flags).

### <a name="dead-character-messages"></a>Dead-Character Nachrichten

Einige nicht englische Tastaturen enthalten Zeichentasten, von denen nicht erwartet wird, dass sie Zeichen selbst erzeugen. Stattdessen werden sie verwendet, um dem Zeichen, das von der nachfolgenden Tastatureingabe erzeugt wird, ein diakritisches Zeichen hinzuzufügen. Diese Schlüssel werden als in dead *keys bezeichnet.* Die Beugetaste auf einer deutschen Tastatur ist ein Beispiel für einen unwegsamen Schlüssel. Zum Eingeben des Zeichens, das aus einem "o" mit einem Beugeflex-Zeichen besteht, würde ein deutsches Benutzer den Beugflexschlüssel gefolgt von der Taste "o" eingeben. Das Fenster mit dem Tastaturfokus erhält die folgende Nachrichtensequenz:

1.  [**WM \_ KEYDOWN**](wm-keydown.md)
2.  [**WM \_ DEADCHAR**](wm-deadchar.md)
3.  [**WM \_ KEYUP**](wm-keyup.md)
4.  [**WM \_ KEYDOWN**](wm-keydown.md)
5.  [**WM \_ CHAR**](wm-char.md)
6.  [**WM \_ KEYUP**](wm-keyup.md)

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) generiert die [**WM \_ DEADCHAR-Nachricht,**](wm-deadchar.md) wenn die [**WM \_ KEYDOWN-Nachricht**](wm-keydown.md) aus einem in dead key verarbeitet wird. Obwohl der *wParam-Parameter* der **WM \_ DEADCHAR-Nachricht** den Zeichencode des diakritischen für den in dead-Schlüssel enthält, ignoriert eine Anwendung die Nachricht in der Regel. Stattdessen wird die [**WM \_ CHAR-Nachricht**](wm-char.md) verarbeitet, die von der nachfolgenden Tastatureingabe generiert wird. Der *wParam-Parameter* der **WM \_ CHAR-Nachricht** enthält den Zeichencode des Buchstabens mit dem diakritischen Zeichen. Wenn die nachfolgende Tastatureingabe ein Zeichen generiert, das nicht mit einem diakritischen Zeichen kombiniert werden kann, generiert das System zwei **WM \_ CHAR-Meldungen.** Der *wParam-Parameter* des ersten enthält den Zeichencode des diakritischen - Der *wParam-Parameter* des zweiten enthält den Zeichencode des nachfolgenden Zeichenschlüssels.

Die [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) generiert die [**WM \_ SYSDEADCHAR-Nachricht,**](wm-sysdeadchar.md) wenn sie die [**WM \_ SYSKEYDOWN-Nachricht**](wm-syskeydown.md) aus einem in dead-Systemschlüssel verarbeitet (eine in dead-Taste, die in Kombination mit der ALT-Taste gedrückt wird). Eine Anwendung ignoriert in der Regel die **WM \_ SYSDEADCHAR-Meldung.**

## <a name="key-status"></a>Schlüsselstatus

Während der Verarbeitung einer Tastaturmeldung muss eine Anwendung möglicherweise den Status einer anderen Taste als der, die die aktuelle Meldung generiert hat, bestimmen. Beispielsweise muss eine Textverarbeitungsanwendung, die es dem Benutzer ermöglicht, UMSCHALT+END zu drücken, um einen Textblock auszuwählen, den Status der UMSCHALTTASTE überprüfen, wenn er eine Tastatureingabenachricht von der END-Taste empfängt. Die Anwendung kann die [**GetKeyState-Funktion**](/windows/win32/api/winuser/nf-winuser-getkeystate) verwenden, um den Status eines virtuellen Schlüssels zu dem Zeitpunkt zu bestimmen, zu dem die aktuelle Nachricht generiert wurde. Sie kann die [**GetAsyncKeyState-Funktion verwenden,**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) um den aktuellen Status eines virtuellen Schlüssels abzurufen.

Das Tastaturlayout verwaltet eine Liste von Namen. Der Name eines Schlüssels, der ein einzelnes Zeichen erzeugt, ist mit dem vom Schlüssel erzeugten Zeichen identisch. Der Name eines Nichtzeichenschlüssels wie TAB und ENTER wird als Zeichenfolge gespeichert. Eine Anwendung kann den Namen eines beliebigen Schlüssels aus dem Gerätetreiber abrufen, indem sie die [**GetKeyNameText-Funktion**](/windows/win32/api/winuser/nf-winuser-getkeynametexta) aufruft.

## <a name="keystroke-and-character-translations"></a>Tastaturanschläge und Zeichenübersetzungen

Das System umfasst mehrere spezielle Funktionen, die Scancodes, Zeichencodes und Codes für virtuelle Schlüssel übersetzen, die von verschiedenen Tastatureingabenachrichten bereitgestellt werden. Zu diesen Funktionen [**gehören MapVirtualKey,**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya) [**ToAscii,**](/windows/win32/api/winuser/nf-winuser-toascii) [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)und [**VkKeyScan.**](/windows/win32/api/winuser/nf-winuser-vkkeyscana)

Darüber hinaus unterstützt Microsoft Rich Edit 3.0 [den HexToUnicode-IME,](/windows/desktop/Intl/hextounicode-ime)der es einem Benutzer ermöglicht, mithilfe von Hot-Schlüsseln zwischen Hexadezimal- und Unicode-Zeichen zu konvertieren. Dies bedeutet, dass die Anwendung die Features des HexToUnicode-IME erbt, wenn Microsoft Rich Edit 3.0 in eine Anwendung integriert wird.

## <a name="hot-key-support"></a>Hot-Key Support

Ein *heißer* Schlüssel ist eine Schlüsselkombination, die eine [**WM \_ HOTKEY-Nachricht**](wm-hotkey.md) generiert. Dabei handelt es sich um eine Nachricht, die das System am Anfang der Nachrichtenwarteschlange eines Threads platziert und alle vorhandenen Nachrichten in der Warteschlange umgeht. Anwendungen verwenden Hot-Tasten, um Tastatureingaben mit hoher Priorität vom Benutzer zu erhalten. Wenn Sie beispielsweise eine hot-Taste definieren, die aus der Tastenkombination STRG+C besteht, kann eine Anwendung dem Benutzer ermöglichen, einen längeren Vorgang abzubricht.

Um einen hot-Schlüssel zu definieren, ruft eine Anwendung die [**RegisterHotKey-Funktion**](/windows/win32/api/winuser/nf-winuser-registerhotkey) auf und gibt die Kombination der Schlüssel, die die [**WM \_ HOTKEY-Nachricht**](wm-hotkey.md) generiert, das Handle für das Fenster zum Empfangen der Nachricht und den Bezeichner des heißen Schlüssels an. Wenn der Benutzer die heiße Taste drückt, wird eine **WM \_ HOTKEY-Nachricht** in der Nachrichtenwarteschlange des Threads platziert, der das Fenster erstellt hat. Der *wParam-Parameter* der Nachricht enthält den Bezeichner des heißen Schlüssels. Die Anwendung kann mehrere hot-Schlüssel für einen Thread definieren, aber jeder hot-Schlüssel im Thread muss einen eindeutigen Bezeichner haben. Bevor die Anwendung beendet wird, sollte sie die [**UnregisterHotKey-Funktion**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) verwenden, um den heißen Schlüssel zu zerstören.

Anwendungen können ein Hot Key-Steuerelement verwenden, um dem Benutzer die Auswahl eines hot-Schlüssels zu ermöglichen. Hot Key-Steuerelemente werden in der Regel verwendet, um einen hot-Schlüssel zu definieren, der ein Fenster aktiviert. Sie verwenden nicht die [**Funktionen RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) [**und UnregisterHotKey.**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) Stattdessen sendet eine Anwendung, die ein Hot Key-Steuerelement verwendet, in der Regel die [**WM \_ SETHOTKEY-Nachricht,**](wm-sethotkey.md) um den heißen Schlüssel fest zu legen. Wenn der Benutzer die hot-Taste drückt, sendet das System eine [**WM \_ SYSCOMMAND-Nachricht,**](/windows/desktop/menurc/wm-syscommand) in der SC \_ HOTKEY angegeben wird. Weitere Informationen zu Hot Key-Steuerelementen finden Sie unter "Verwenden von Hot Key-Steuerelementen" unter [Hot Key-Steuerelemente](../controls/hot-key-controls.md).

## <a name="keyboard-keys-for-browsing-and-other-functions"></a>Tastaturtasten für Das Durchsuchen und andere Funktionen

Windows bietet Unterstützung für Tastaturen mit speziellen Tasten für Browserfunktionen, Medienfunktionen, Anwendungsstart und Energieverwaltung. WM [**\_ APPCOMMAND unterstützt**](wm-appcommand.md) die zusätzlichen Tastaturtasten. Darüber hinaus wird die [**ShellProc-Funktion**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) geändert, um die zusätzlichen Tastaturtasten zu unterstützen.

Es ist unwahrscheinlich, dass ein untergeordnetes Fenster in einer Komponentenanwendung Befehle für diese zusätzlichen Tastaturtasten direkt implementieren kann. Wenn also eine dieser Tasten gedrückt wird, sendet [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) eine [**WM \_ APPCOMMAND-Nachricht**](wm-appcommand.md) an ein Fenster. **DefWindowProc überlädt** auch die **WM \_ APPCOMMAND-Nachricht** im übergeordneten Fenster. Dies ähnelt der Art und Weise, wie Kontextmenüs mit der rechten Maustaste aufgerufen werden. **DefWindowProc** sendet eine [**WM \_ CONTEXTMENU-Nachricht**](/windows/desktop/menurc/wm-contextmenu) bei einem Rechtsklick und überlädt sie dem übergeordneten Element. Wenn **DefWindowProc** außerdem eine **WM \_ APPCOMMAND-Nachricht** für ein Fenster der obersten Ebene empfängt, wird ein Shellhook mit dem Code **HSHELL \_ APPCOMMAND aufrufen.**

Windows unterstützt auch den Microsoft IntelliMouse-Explorer, bei dem es sich um eine Maus mit fünf Schaltflächen handelt. Die beiden zusätzlichen Schaltflächen unterstützen die Navigation im Vorwärts- und Rückwärtsbrowser. Weitere Informationen finden Sie unter [XBUTTONs](about-mouse-input.md).

## <a name="simulating-input"></a>Simulieren von Eingaben

Verwenden Sie die SendInput-Funktion, um eine ununterbrochene Reihe von [**Benutzereingabeereignissen zu**](/windows/win32/api/winuser/nf-winuser-sendinput) simulieren. Die Funktion akzeptiert drei Parameter. Der erste Parameter, *cInputs,* gibt die Anzahl der Eingabeereignisse an, die simuliert werden. Der zweite Parameter, *rgInputs,* ist ein Array von [**INPUT-Strukturen,**](/windows/win32/api/winuser/ns-winuser-input) die jeweils einen Typ von Eingabeereignis und zusätzliche Informationen zu diesem Ereignis beschreiben. Der letzte Parameter *cbSize* akzeptiert die Größe der **INPUT-Struktur** in Bytes.

Die [**SendInput-Funktion**](/windows/win32/api/winuser/nf-winuser-sendinput) fügt eine Reihe simulierter Eingabeereignisse in den Eingabestream eines Geräts ein. Der Effekt ähnelt dem wiederholten Aufrufen [**\_**](/windows/win32/api/winuser/nf-winuser-mouse_event) des [**keybd-Ereignisses \_**](/windows/win32/api/winuser/nf-winuser-keybd_event) oder der Mausereignisfunktion, außer dass das System sicherstellt, dass sich keine anderen Eingabeereignisse mit den simulierten Ereignissen ineinander vermischen. Nach Abschluss des Aufrufs gibt der Rückgabewert die Anzahl der erfolgreich abgespielten Eingabeereignisse an. Wenn dieser Wert 0 (null) ist, wurde die Eingabe blockiert.

Die [**SendInput-Funktion**](/windows/win32/api/winuser/nf-winuser-sendinput) setzt den aktuellen Zustand der Tastatur nicht zurück. Wenn der Benutzer beim Aufrufen dieser Funktion tastend gedrückt wird, kann er daher die Von dieser Funktion generierten Ereignisse beeinträchtigen. Wenn Sie Bedenken über mögliche Störungen haben, überprüfen Sie den Zustand der Tastatur mit der [**GetAsyncKeyState-Funktion,**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) und korrigieren Sie sie nach Bedarf.

## <a name="languages-locales-and-keyboard-layouts"></a>Sprachen, Locales und Tastaturlayouts

Eine *Sprache* ist eine natürliche Sprache, z. B. Englisch, Französisch und Japanisch. Eine *Untersprache* ist eine Variante einer natürlichen Sprache, die in einer bestimmten geografischen Region gesprochen wird, z. B. den englischen Untersprachen, die im Vereinigten Königreich gesprochen werden, und USA. Anwendungen verwenden Werte, die als [Sprachbezeichner bezeichnet werden,](/windows/desktop/Intl/language-identifiers)um Sprachen und Untersprachen eindeutig zu identifizieren.

Anwendungen verwenden in der *Regel Locales* zum Festlegen der Sprache, in der Eingabe und Ausgabe verarbeitet werden. Das Festlegen des Locale für die Tastatur wirkt sich z. B. auf die Zeichenwerte aus, die von der Tastatur generiert werden. Das Festlegen des Locale für die Anzeige oder den Drucker wirkt sich auf die angezeigten oder gedruckten Glyphen aus. Anwendungen legen das Locale für eine Tastatur fest, indem sie Tastaturlayouts laden und verwenden. Sie legen das Locale für eine Anzeige oder einen Drucker fest, indem sie eine Schriftart auswählen, die das angegebene Locale unterstützt.

Ein Tastaturlayout gibt nicht nur die physische Position der Tasten auf der Tastatur an, sondern bestimmt auch die Zeichenwerte, die durch Drücken dieser Tasten generiert werden. Jedes Layout identifiziert die aktuelle Eingabesprache und bestimmt, welche Zeichenwerte von welchen Schlüsseln und Tastenkombinationen generiert werden.

Jedes Tastaturlayout verfügt über ein entsprechendes Handle, das das Layout und die Sprache identifiziert. Das niedrige Wort des Handles ist ein Sprachbezeichner. Das hohe Wort ist ein Gerätehand handle, das das physische Layout angibt, oder ist 0 (null), was ein physisches Standardlayout angibt. Der Benutzer kann jede Eingabesprache einem physischen Layout zuordnen. Beispielsweise kann ein englischsprachiger Benutzer, der gelegentlich in Französisch arbeitet, die Eingabesprache der Tastatur auf Französisch festlegen, ohne das physische Layout der Tastatur zu ändern. Dies bedeutet, dass der Benutzer Text in Französisch mithilfe des vertrauten englischen Layouts eingeben kann.

Es wird in der Regel nicht erwartet, dass Anwendungen Eingabesprachen direkt bearbeiten. Stattdessen richtet der Benutzer Sprach- und Layoutkombinationen ein und wechselt dann zwischen diesen. Wenn der Benutzer auf Text klickt, der mit einer anderen Sprache markiert ist, ruft die Anwendung die [**ActivateKeyboardLayout-Funktion**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) auf, um das Standardlayout des Benutzers für diese Sprache zu aktivieren. Wenn der Benutzer Text in einer Sprache bearbeitet, die nicht in der aktiven Liste enthalten ist, kann die Anwendung die [**LoadKeyboardLayout-Funktion**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) mit der Sprache aufrufen, um ein Layout basierend auf dieser Sprache zu erhalten.

Die [**ActivateKeyboardLayout-Funktion**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) legt die Eingabesprache für die aktuelle Aufgabe fest. Der *hkl-Parameter* kann entweder das Handle für das Tastaturlayout oder ein bezeichner mit einer erweiterten Sprache (0) sein. Tastaturlayouthandles können über die [**Funktion LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) oder [**GetKeyboardLayoutList ermittelt**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist) werden. Die **Werte HKL \_ NEXT** und **HKL \_ PREV** können auch verwendet werden, um die nächste oder vorherige Tastatur auszuwählen.

Die [**GetKeyboardLayoutName-Funktion**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea) ruft den Namen des aktiven Tastaturlayouts für den aufrufenden Thread ab. Wenn eine Anwendung das aktive Layout mithilfe der [**LoadKeyboardLayout-Funktion**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) erstellt, ruft **GetKeyboardLayoutName** dieselbe Zeichenfolge ab, die zum Erstellen des Layouts verwendet wurde. Andernfalls ist die Zeichenfolge der Bezeichner der primären Sprache, der dem Locale des aktiven Layouts entspricht. Dies bedeutet, dass die Funktion möglicherweise nicht notwendigerweise zwischen verschiedenen Layouts mit der gleichen primären Sprache unterscheidet und daher keine spezifischen Informationen zur Eingabesprache zurückgeben kann. Die [**GetKeyboardLayout-Funktion**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) kann jedoch verwendet werden, um die Eingabesprache zu bestimmen.

Die [**LoadKeyboardLayout-Funktion**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) lädt ein Tastaturlayout und macht das Layout für den Benutzer verfügbar. Anwendungen können das Layout für den aktuellen Thread sofort aktiv machen, indem sie den **KLF \_ ACTIVATE-Wert** verwenden. Eine Anwendung kann den **KLF \_ REORDER-Wert** verwenden, um die Layouts neu zu anordnen, ohne auch den **KLF \_ ACTIVATE-Wert anzugeben.** Anwendungen sollten beim Laden von Tastaturlayouts immer den **KLF \_ SUBSTITUTE \_ OK-Wert** verwenden, um sicherzustellen, dass die Einstellung des Benutzers ausgewählt ist( falls dies der Fall ist).

Zur Unterstützung mehrsprachiger Inhalte stellt [**die LoadKeyboardLayout-Funktion**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) die **FLAGs KLF \_ REPLACELANG** und **KLF \_ NOTELLSHELL** zur Verwendung. Das **KLF \_ REPLACELANG-Flag** leitet die Funktion an, ein vorhandenes Tastaturlayout zu ersetzen, ohne die Sprache zu ändern. Der Versuch, ein vorhandenes Layout mit demselben Sprachbezeichner zu ersetzen, aber ohne **KLF \_ REPLACELANG** anzugeben, ist ein Fehler. Das **KLF \_ NOTELLSHELL-Flag** verhindert, dass die Funktion die Shell benachrichtigt, wenn ein Tastaturlayout hinzugefügt oder ersetzt wird. Dies ist nützlich für Anwendungen, die mehrere Layouts in einer aufeinanderfolgenden Reihe von Aufrufen hinzufügen. Dieses Flag sollte bis auf den letzten Aufruf verwendet werden.

Die [**UnloadKeyboardLayout-Funktion**](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout) ist darauf beschränkt, dass sie die Standardeingabesprache des Systems nicht entladen kann. Dadurch wird sichergestellt, dass dem Benutzer immer ein Layout für die Eingabe von Text mit demselben Zeichensatz zur Verfügung steht, der von der Shell und dem Dateisystem verwendet wird.

 

 
