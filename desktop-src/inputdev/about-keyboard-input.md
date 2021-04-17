---
title: Informationen über Tastatureingaben
description: In diesem Thema werden Tastatureingaben behandelt.
ms.assetid: de34727e-e8c7-481d-982d-0e42a02704db
keywords:
- Benutzereingabe, Tastatureingabe
- Erfassen von Benutzereingaben, Tastatureingaben
- Tastatureingabe
- Tastaturfokus
- Tastatureingaben
- Zeichen Nachrichten
- System Tastatureingaben
- nicht-System Tastatureingaben
- nicht-System-Zeichen Nachrichten
- unzustellbare Schlüssel
- Nachrichten mit unzustellbaren Zeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ad481bad6756bb374b98a5510bdc26f1cded6a
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104567262"
---
# <a name="about-keyboard-input"></a>Informationen über Tastatureingaben

Anwendungen sollten Benutzereingaben sowohl von der Tastatur als auch von der Maus akzeptieren. Eine Anwendung empfängt Tastatureingaben in Form von Nachrichten, die an Ihre Fenster gesendet werden.

Dieser Abschnitt enthält die folgenden Themen:

-   [Tastatureingabe Modell](#keyboard-input-model)
-   [Tastaturfokus und-Aktivierung](#keyboard-focus-and-activation)
-   [Tastatureingaben](#keystroke-messages)
    -   [Tastatureingaben für System und nicht System](#system-and-nonsystem-keystrokes)
    -   [Beschriebene Virtual Key-Codes](#virtual-key-codes-described)
    -   [Keystroke-Nachrichtenflags](#keystroke-message-flags)
-   [Zeichen Nachrichten](#character-messages)
    -   [Nicht-System-Zeichen Nachrichten](#nonsystem-character-messages)
    -   [Nachrichten mit unzustellbaren Zeichen](#dead-character-messages)
-   [Schlüssel Status](#key-status)
-   [Tastatureingaben und Zeichen Übersetzungen](#keystroke-and-character-translations)
-   [Unterstützung für heiße Schlüssel](#hot-key-support)
-   [Tastaturtasten für das Browsen und andere Funktionen](#keyboard-keys-for-browsing-and-other-functions)
-   [Simulieren von Eingaben](#simulating-input)
-   [Sprachen, Gebiets Schemas und Tastatur Layouts](#languages-locales-and-keyboard-layouts)

## <a name="keyboard-input-model"></a>Tastatureingabe Modell

Das System stellt geräteunabhängige Tastatur Unterstützung für Anwendungen bereit, indem ein Tastatur Gerätetreiber installiert wird, der für die aktuelle Tastatur geeignet ist. Das System stellt sprachunabhängige Tastatur Unterstützung bereit, indem das sprachspezifische Tastaturlayout verwendet wird, das zurzeit vom Benutzer oder der Anwendung ausgewählt wird. Der Tastatur Gerätetreiber empfängt Scan Codes von der Tastatur, die an das Tastaturlayout gesendet werden, wo Sie in Nachrichten übersetzt und an die entsprechenden Fenster in der Anwendung gesendet werden.

Jedem Schlüssel auf einer Tastatur zugewiesen ist, ist ein eindeutiger Wert, der als *Scan Code* bezeichnet wird, ein Geräte abhängiger Bezeichner für den Schlüssel auf der Tastatur. Eine Tastatur generiert zwei Überprüfungs Codes, wenn der Benutzer einen Schlüssel eingibt – einen, wenn der Benutzer die Taste drückt, und ein anderer, wenn der Benutzer die Taste loslässt.

Der Tastatur Gerätetreiber interpretiert einen Überprüfungs Code und übersetzt ihn in einen *virtuellen Schlüsselcode*, einen geräteunabhängigen Wert, der durch das System definiert ist, das den Zweck eines Schlüssels identifiziert. Nachdem Sie einen Überprüfungs Code übersetzt haben, erstellt das Tastaturlayout eine Meldung, die den Überprüfungs Code, den Code für den virtuellen Schlüssel und andere Informationen über die Tastatureingabe enthält. Anschließend wird die Nachricht in der System Meldungs Warteschlange abgelegt. Das System entfernt die Nachricht aus der Systemnachrichten Warteschlange und sendet Sie in der Nachrichten Warteschlange des entsprechenden Threads. Schließlich wird die Nachricht durch die Meldungs Schleife des Threads entfernt und zur Verarbeitung an die entsprechende Fenster Prozedur weitergeleitet. In der folgenden Abbildung wird das Tastatureingabe Modell veranschaulicht.

![Tastatureingabe-Verarbeitungsmodell](images/csinp-01.png)

## <a name="keyboard-focus-and-activation"></a>Tastaturfokus und-Aktivierung

Das System sendet Tastatur Meldungen an die Meldungs Warteschlange des Vordergrund Threads, der das Fenster mit dem Tastaturfokus erstellt hat. Der *Tastaturfokus* ist eine temporäre Eigenschaft eines Fensters. Das System teilt die Tastatur zwischen allen Fenstern auf der Anzeige, indem der Tastaturfokus in der Benutzer Richtung von einem Fenster zu einem anderen verschoben wird. Das Fenster, das den Tastaturfokus besitzt (aus der Meldungs Warteschlange des Threads, der es erstellt hat) alle Tastatur Meldungen, bis der Fokus in ein anderes Fenster geändert wird.

Ein Thread kann die [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) -Funktion aufrufen, um zu bestimmen, welches seiner Fenster (sofern vorhanden) aktuell den Tastaturfokus besitzt. Ein Thread kann den Tastaturfokus auf eines seiner Fenster festlegen, indem er die [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) -Funktion aufruft. Wenn sich der Tastaturfokus von einem Fenster in ein anderes ändert, sendet das System eine [**WM- \_ killfocus**](wm-killfocus.md) -Meldung an das Fenster, das den Fokus verloren hat, und sendet dann eine [**WM- \_ SetFocus**](wm-setfocus.md) -Meldung an das Fenster, das den Fokus erhalten hat.

Das Konzept des Tastaturfokus bezieht sich auf die des aktiven Fensters. Das *aktive Fenster* ist das Fenster auf oberster Ebene, mit dem der Benutzer gerade arbeitet. Das Fenster mit dem Tastaturfokus ist entweder das aktive Fenster oder ein untergeordnetes Fenster des aktiven Fensters. Um dem Benutzer zu helfen, das aktive Fenster zu identifizieren, platziert das System ihn am Anfang der Z-Reihenfolge und hebt seine Titelleiste (sofern eine) und einen Rahmen hervor.

Der Benutzer kann ein Fenster der obersten Ebene aktivieren, indem er darauf klickt, es mithilfe der Tastenkombination Alt + Tab oder ALT + ESC auswählen oder es aus der Aufgabenliste auswählen. Ein Thread kann ein Fenster der obersten Ebene mithilfe der [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) -Funktion aktivieren. Mithilfe der [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) -Funktion kann ermittelt werden, ob ein von ihm erstelltes Fenster der obersten Ebene aktiviert ist.

Wenn ein Fenster deaktiviert und ein anderes aktiviert wird, sendet das System die [**WM- \_ Aktivierungs**](wm-activate.md) Nachricht. Das nieder wertige Wort des *wParam* -Parameters ist 0 (null), wenn das Fenster deaktiviert wird, und ungleich 0 (null), wenn es aktiviert wird. Wenn die Standardfenster Prozedur die **WM- \_ Aktivierungs** Nachricht empfängt, wird der Tastaturfokus auf das aktive Fenster festgelegt.

Um zu verhindern, dass Ereignisse der Tastatur-und Maus Eingaben erreicht werden, verwenden Sie [**BlockInput**](/windows/win32/api/winuser/nf-winuser-blockinput). Beachten Sie, dass die **BlockInput** -Funktion nicht mit der asynchronen Tastatureingabe Zustands Tabelle in Konflikt steht. Dies bedeutet, dass der Aufruf der [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) -Funktion während der Eingabe blockiert wird, die asynchrone Tastatureingabe Zustands Tabelle ändert.

## <a name="keystroke-messages"></a>Tastatureingaben

Wenn eine Taste gedrückt wird, wird eine [**WM- \_ KeyDown**](wm-keydown.md) -oder eine [**WM- \_ syskeydown**](wm-syskeydown.md) -Meldung in die Thread Nachrichten Warteschlange eingefügt, die an das Fenster mit dem Tastaturfokus angeschlossen ist. Das Freigeben eines Schlüssels bewirkt, dass eine [**WM- \_ KeyUp**](wm-keyup.md) -oder eine [**WM- \_ syskeyup**](wm-syskeyup.md) -Meldung in die Warteschlange gestellt wird.

Key-up-und Key-Down-Meldungen treten in der Regel paarweise auf. wenn der Benutzer jedoch einen Schlüssel enthält, der lange genug ist, um die automatische Wiederholungsfunktion der Tastatur zu starten, generiert das System eine Reihe von [**WM- \_ KeyDown**](wm-keydown.md) -oder [**WM- \_ syskeydown**](wm-syskeydown.md) -Meldungen in einer Zeile. Anschließend wird eine einzelne [**WM- \_ KeyUp**](wm-keyup.md) -oder [**WM- \_ syskeyup**](wm-syskeyup.md) -Meldung generiert, wenn der Benutzer den Schlüssel freigibt.

Dieser Abschnitt enthält die folgenden Themen:

-   [Tastatureingaben für System und nicht System](#system-and-nonsystem-keystrokes)
-   [Beschriebene Virtual Key-Codes](#virtual-key-codes-described)
-   [Keystroke-Nachrichtenflags](#keystroke-message-flags)

### <a name="system-and-nonsystem-keystrokes"></a>Tastatureingaben für System und nicht System

Das System unterscheidet zwischen System Tastatureingaben und nicht-System Tastatureingaben. System Tastatureingaben verursachen System Tastatureingaben, [**WM \_ syskeydown**](wm-syskeydown.md) und [**WM \_ syskeyup**](wm-syskeyup.md). Nicht-System Tastatureingaben verursachen nicht-System Tastatureingaben, [**WM \_ KeyDown**](wm-keydown.md) und [**WM- \_ KeyUp**](wm-keyup.md).

Wenn die Fenster Prozedur eine systemkeystroke-Nachricht verarbeiten muss, stellen Sie sicher, dass die Prozedur nach der Verarbeitung der Nachricht an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion übergibt. Andernfalls werden alle System Vorgänge, die die Alt-Taste betreffen, immer dann deaktiviert, wenn das Fenster den Tastaturfokus besitzt. Das heißt, der Benutzer kann nicht auf die Menüs oder das System Menü des Fensters zugreifen oder die Tastenkombination ALT + ESC oder ALT + TAB verwenden, um ein anderes Fenster zu aktivieren.

System Tastatureingaben sind hauptsächlich für die Verwendung durch das System und nicht für eine Anwendung vorgesehen. Das System verwendet diese, um die integrierte Tastaturschnittstelle für Menüs bereitzustellen und dem Benutzer zu ermöglichen, das aktive Fenster zu steuern. System Tastatureingaben werden generiert, wenn der Benutzer einen Schlüssel in Kombination mit der Alt-Taste eingibt, oder wenn der Benutzer die Eingabe und kein Fenster den Tastaturfokus besitzt (z. b. wenn die aktive Anwendung minimiert wird). In diesem Fall werden die Nachrichten in der Nachrichten Warteschlange gepostet, die an das aktive Fenster angefügt ist.

Nicht-System Tastatureingaben sind für die Verwendung durch Anwendungsfenster vorgesehen. die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion führt keine Aktionen aus. Eine Fenster Prozedur kann alle nicht systemeigenen Tastatureingabe Nachrichten verwerfen, die nicht benötigt werden.

### <a name="virtual-key-codes-described"></a>Beschriebene Virtual-Key Codes

Der **wParam** -Parameter einer Tastatureingabe-Nachricht enthält den Code für den virtuellen Schlüssel des Schlüssels, der gedrückt oder freigegeben wurde. Eine Fenster Prozedur verarbeitet oder ignoriert eine Tastatureingabe-Nachricht, abhängig vom Wert des Codes des virtuellen Schlüssels.

Eine typische Fenster Prozedur verarbeitet nur eine kleine Teilmenge der Tastatureingabe Meldungen, die Sie empfängt, und ignoriert den Rest. Beispielsweise kann eine Fenster Prozedur nur die Nachrichten von [**WM \_ KeyDown**](wm-keydown.md) -Tastatureingaben verarbeiten, und nur diejenigen, die virtuelle Schlüsselcodes für die Cursor Verschiebungs Tasten, Umschalt Tasten (auch als Steuerelement Schlüssel bezeichnet) und Funktionstasten enthalten. Eine typische Fenster Prozedur verarbeitet keine Tastatureingaben von Zeichen Schlüsseln. Stattdessen wird die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion verwendet, um die Nachricht in Zeichen Nachrichten zu konvertieren. Weitere Informationen zu **translatemteage** und Zeichen Nachrichten finden Sie unter [Zeichen Nachrichten](#character-messages).

### <a name="keystroke-message-flags"></a>Keystroke-Nachrichtenflags

Der **LPARAM** -Parameter einer Tastatureingabe-Nachricht enthält zusätzliche Informationen über den Tastatur Strich, der die Meldung generiert hat. Diese Informationen umfassen die Wiederholungs Anzahl, den Überprüfungs Code, das erweiterte schlüsselflag, den Kontext Code, das vorherige schlüsselstatusflag und das Flag für den Übergangszustand. Die folgende Abbildung zeigt die Speicherorte dieser Flags und Werte im **LPARAM** -Parameter.

![die Speicherorte der Flags und Werte im lParam-Parameter einer Tastatureingabe-Nachricht.](images/csinp-02.png)

Eine Anwendung kann die folgenden Werte verwenden, um die Tastatureingabe-Flags zu bearbeiten.



| Wert            | BESCHREIBUNG                                                                       |
|------------------|-----------------------------------------------------------------------------------|
| **KF- \_ altdown**  | Bearbeitet das alt-schlüsselflag, das angibt, ob die Alt-Taste gedrückt wird.     |
| **KF \_ dlgmode**  | Bearbeitet das dialogmodusflag, das angibt, ob ein Dialogfeld aktiv ist. |
| **KF \_ erweitert** | Bearbeitet das erweiterte schlüsselflag.                                                |
| **KF- \_ menumode** | Bearbeitet das menümodusflag, das angibt, ob ein Menü aktiv ist.         |
| **KF \_ Wiederholung**   | Bearbeitet das vorherige schlüsselstatusflag.                                          |
| **KF- \_ up**       | Bearbeitet das Übergangs Zustands Kennzeichen.                                            |



 

### <a name="repeat-count"></a>Zahl der Wiederholungen

Sie können die Wiederholungs Anzahl überprüfen, um zu bestimmen, ob eine Tastatureingabe-Nachricht mehr als eine Tastatureingabe darstellt. Das System erhöht die Anzahl, wenn die Tastatur [**WM- \_ KeyDown**](wm-keydown.md) -oder [**WM- \_ syskeydown**](wm-syskeydown.md) -Meldungen schneller generiert, als Sie von einer Anwendung verarbeitet werden können. Dies tritt häufig auf, wenn der Benutzer einen Schlüssel enthält, der zum Starten der automatischen Wiederholungsfunktion der Tastatur ausreicht. Anstatt die System Meldungs Warteschlange mit den resultierenden KeyDown-Nachrichten zu füllen, kombiniert das System die Nachrichten in einer einzelnen Nachricht und erhöht die Wiederholungs Anzahl. Wenn Sie einen Schlüssel freigeben, kann die Funktion für die automatische Wiederholung nicht gestartet werden. Daher wird die Wiederholungs Anzahl für die [**WM- \_ KeyUp**](wm-keyup.md) -und [**WM- \_ syskeyup**](wm-syskeyup.md) -Meldungen immer auf 1

### <a name="scan-code"></a>Überprüfungs Code

Der Scan Code ist der Wert, der von der Tastatur Hardware generiert wird, wenn der Benutzer eine Taste drückt. Es handelt sich um einen geräteabhängigen Wert, der den gedrückten Schlüssel identifiziert, im Gegensatz zu dem durch den Schlüssel dargestellten Zeichen. Eine Anwendung ignoriert in der Regel Scan Codes. Stattdessen verwendet Sie die geräteunabhängigen virtuellen Schlüsselcodes, um Tastatureingaben zu interpretieren.

### <a name="extended-key-flag"></a>Extended-Key-Flag

Das Flag für erweiterte Schlüssel gibt an, ob die Tastatureingabe-Nachricht von einem der zusätzlichen Schlüssel auf der erweiterten Tastatur stammt. Die erweiterten Schlüssel bestehen aus der Alt-Taste und der STRG-Taste auf der rechten Seite der Tastatur. die Tasten "ins", "Entf", "Start", "Ende", "Bild-ab" und "Pfeil" in den Clustern auf der linken Seite der numerischen Keypad. die Num-Sperrtaste; die Pause-Taste (Strg + Pause); die Druck-Scrn-Taste; und die Unterteilung (/) und EINGABETASTE in der numerischen Tastatur. Das Flag für erweiterte Schlüssel wird festgelegt, wenn es sich bei dem Schlüssel um einen erweiterten Schlüssel handelt.

### <a name="context-code"></a>Kontext Code

Der Kontext Code gibt an, ob die Alt-Taste gedrückt wurde, als die Tastatureingabe-Nachricht generiert wurde. Der Code ist 1, wenn die Alt-Taste gedrückt war, und 0, wenn Sie aktiv war.

### <a name="previous-key-state-flag"></a>Vorheriges Key-State Flag

Das vorherige schlüsselstatusflag gibt an, ob der Schlüssel, der die Tastatureingabe-Nachricht generiert hat, zuvor auf dem neuesten Stand ist. Der Schlüssel ist 1, wenn der Schlüssel zuvor nicht aktiv war, und 0, wenn der Schlüssel zuvor war. Sie können dieses Flag verwenden, um Tastatureingabe-Nachrichten zu identifizieren, die vom automatischen Wiederholungs Feature der Tastatur generiert werden. Dieses Flag ist für [**WM \_ KeyDown**](wm-keydown.md) -und WM- [**\_ syskeydown**](wm-syskeydown.md) -Tastatureingabe-Meldungen, die von der automatischen Wiederholungsfunktion generiert wurden, auf 1 festgelegt. Für [**WM \_ KeyUp**](wm-keyup.md) -und [**WM- \_ syskeyup**](wm-syskeyup.md) -Nachrichten ist Sie immer auf 1 festgelegt.

### <a name="transition-state-flag"></a>Transition-State-Flag

Das Flag für den Übergangszustand gibt an, ob beim Drücken einer Taste oder beim Freigeben eines Schlüssels die Tastatureingabe-Nachricht generiert wurde. Dieses Flag ist für [**WM \_ KeyDown**](wm-keydown.md) -und [**WM- \_ syskeydown**](wm-syskeydown.md) -Meldungen immer auf 0 festgelegt. es ist für [**WM \_ KeyUp**](wm-keyup.md) -und [**WM \_ syskeyup**](wm-syskeyup.md) -Meldungen immer auf 1 festgelegt.

## <a name="character-messages"></a>Zeichen Nachrichten

Keystroke-Nachrichten stellen viele Informationen über Tastatureingaben bereit, stellen jedoch keine Zeichen Codes für Zeichen Tastatureingaben bereit. Um Zeichen Codes abzurufen, muss eine Anwendung die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion in der Thread Nachrichten Schleife enthalten. **Translatemess** übergibt eine [**WM- \_ KeyDown**](wm-keydown.md) -oder [**WM- \_ syskeydown**](wm-syskeydown.md) -Meldung an das Tastaturlayout. Das Layout überprüft den Code des virtuellen Schlüssels der Nachricht und stellt, wenn er einem Zeichen Schlüssel entspricht, den Zeichencode Äquivalent bereit (berücksichtigt den Zustand der UMSCHALT-und der FESTSTELL Sperrtaste). Anschließend wird eine Zeichen Nachricht generiert, die den Zeichencode enthält, und die Nachricht wird am Anfang der Nachrichten Warteschlange platziert. Die nächste Iterations Schleife der Nachrichten Schleife entfernt die Zeichen Nachricht aus der Warteschlange und sendet die Nachricht an die entsprechende Fenster Prozedur.

Dieser Abschnitt enthält die folgenden Themen:

-   [Nicht-System-Zeichen Nachrichten](#nonsystem-character-messages)
-   [Nachrichten mit unzustellbaren Zeichen](#dead-character-messages)

### <a name="nonsystem-character-messages"></a>Nicht-System-Zeichen Nachrichten

Eine Fenster Prozedur kann die folgenden Zeichen Nachrichten empfangen: [**WM \_ char**](wm-char.md), [**WM \_ deadchar**](wm-deadchar.md), [**WM \_ Sychar**](/windows/desktop/menurc/wm-syschar), [**WM \_ sysdeadchar**](wm-sysdeadchar.md)und [**WM \_ UNICHAR**](wm-unichar.md). Die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion generiert eine **WM \_ char** -oder **WM \_ deadchar** -Nachricht, wenn Sie eine [**WM- \_ KeyDown**](wm-keydown.md) -Nachricht verarbeitet. Auf ähnliche Weise wird eine **WM- \_ Sychar** -oder **WM- \_ sysdeadchar** -Nachricht generiert, wenn Sie eine [**WM- \_ syskeydown**](wm-syskeydown.md) -Nachricht verarbeitet.

Eine Anwendung, die Tastatureingaben verarbeitet, ignoriert in der Regel alle außer den [**WM \_**](wm-char.md) -und [**WM- \_ UNICHAR**](wm-unichar.md) -Nachrichten und übergibt alle anderen Nachrichten an die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion. Beachten Sie, dass **WM \_ char** das 16-Bit-Unicode-Transformations Format (UTF) verwendet, während **WM \_ UNICHAR** UTF-32 verwendet. Das System verwendet die WM-Meldungen " [**\_ Sychar**](/windows/desktop/menurc/wm-syschar) " und " [**WM \_ sysdeadchar**](wm-sysdeadchar.md) ", um die Menü-mnetmonics zu implementieren

Der **wParam** -Parameter aller Zeichen Nachrichten enthält den Zeichencode der Zeichen Taste, die gedrückt wurde. Der Wert des Zeichen Codes hängt von der Fenster Klasse des Fensters ab, das die Nachricht empfängt. Wenn die Unicode-Version der [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) -Funktion verwendet wurde, um die Fenster Klasse zu registrieren, stellt das System allen Fenstern dieser Klasse Unicode-Zeichen zur Verfügung. Andernfalls stellt das System ASCII-Zeichen Codes bereit. Weitere Informationen finden Sie unter [Unicode und Zeichensätze](/windows/desktop/Intl/unicode-and-character-sets).

Der Inhalt des **LPARAM** -Parameters einer Zeichen Nachricht ist mit dem Inhalt des **LPARAM** -Parameters der KeyDown-Nachricht identisch, die zum Ausgeben der Zeichen Nachricht übersetzt wurde. Weitere Informationen finden Sie unter [KeyStroke-Nachrichtenflags](#keystroke-message-flags).

### <a name="dead-character-messages"></a>Dead-Character Meldungen

Einige nicht englische Tastaturen enthalten Zeichen Schlüssel, für die nicht erwartet wird, dass Sie Zeichen selbst enthalten. Stattdessen werden Sie verwendet, um dem von der nachfolgenden Tastenkombination erzeugten Zeichen einen diakritischen Zeichensatz hinzuzufügen. Diese Schlüssel werden als unzustellbare *Schlüssel* bezeichnet. Der Schlüssel "circumflexkey" auf einer deutschen Tastatur ist ein Beispiel für eine unzustellbare Taste. Um das Zeichen, das aus einem "o" besteht, mit einem umgeht, würde ein deutscher Benutzer den Umgehungs Schlüssel eingeben, gefolgt von der Taste "o". Das Fenster mit dem Tastaturfokus erhält die folgende Sequenz von Meldungen:

1.  [**WM- \_ KeyDown**](wm-keydown.md)
2.  [**WM \_ deadchar**](wm-deadchar.md)
3.  [**WM- \_ KeyUp**](wm-keyup.md)
4.  [**WM- \_ KeyDown**](wm-keydown.md)
5.  [**WM \_ -Zeichen**](wm-char.md)
6.  [**WM- \_ KeyUp**](wm-keyup.md)

[**Translatemessen**](/windows/desktop/api/winuser/nf-winuser-translatemessage) generiert die [**WM \_ deadchar**](wm-deadchar.md) -Nachricht, wenn Sie die [**WM- \_ KeyDown**](wm-keydown.md) -Nachricht von einer unzustellbaren Taste verarbeitet. Obwohl der *wParam* -Parameter der **WM- \_ deadchar** -Nachricht den Zeichencode der diakritischen Zeichenfolge für den unzustellbaren Schlüssel enthält, wird die Nachricht von einer Anwendung normalerweise ignoriert. Stattdessen wird die vom nachfolgenden Tastatur Strich generierte [**WM \_ char**](wm-char.md) -Nachricht verarbeitet. Der *wParam* -Parameter der **WM- \_ char** -Nachricht enthält den Zeichencode des Buchstabens mit dem diakritischen Zeichen. Wenn der nachfolgende Tastatur Strich ein Zeichen generiert, das nicht mit einem diakritischen Zeichen kombiniert werden kann, generiert das System zwei **WM \_ char** -Nachrichten. Der *wParam* -Parameter des ersten-Parameters enthält den Zeichencode der diakritischen Zeichenfolge. der *wParam* -Parameter des zweiten-Parameters enthält den Zeichencode des nachfolgenden Zeichen Schlüssels.

Die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion generiert die [**WM- \_ sysdeadchar**](wm-sysdeadchar.md) -Nachricht, wenn Sie die [**WM- \_ syskeydown**](wm-syskeydown.md) -Nachricht von einer System-unzustellungstaste verarbeitet (eine unzustellbare Taste, die in Verbindung mit der Alt-Taste gedrückt wird). Eine Anwendung ignoriert in der Regel die **WM- \_ sysdeadchar** -Nachricht.

## <a name="key-status"></a>Schlüssel Status

Bei der Verarbeitung einer Tastatur Nachricht muss eine Anwendung möglicherweise den Status eines anderen Schlüssels außer dem, der die aktuelle Nachricht generiert hat, bestimmen. Beispielsweise muss eine Textverarbeitungsanwendung, die dem Benutzer das Drücken von Umschalt + Ende ermöglicht, um einen Textblock auszuwählen, den Status der Umschalttaste überprüfen, wenn eine Tastatureingabe Nachricht von der endtaste empfangen wird. Die Anwendung kann die [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) -Funktion verwenden, um den Status eines virtuellen Schlüssels zu dem Zeitpunkt zu ermitteln, zu dem die aktuelle Nachricht generiert wurde. Sie kann die [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) -Funktion verwenden, um den aktuellen Status eines virtuellen Schlüssels abzurufen.

Das Tastaturlayout verwaltet eine Liste von Namen. Der Name eines Schlüssels, der ein einzelnes Zeichen erzeugt, ist identisch mit dem Zeichen, das vom Schlüssel erzeugt wird. Der Name eines nicht-Zeichen Schlüssels, z. b. Tab und Enter, wird als Zeichenfolge gespeichert. Eine Anwendung kann den Namen eines beliebigen Schlüssels vom Gerätetreiber abrufen, indem Sie die [**getkeynametext**](/windows/win32/api/winuser/nf-winuser-getkeynametexta) -Funktion aufrufen.

## <a name="keystroke-and-character-translations"></a>Tastatureingaben und Zeichen Übersetzungen

Das System enthält mehrere spezielle Zweck Funktionen, die Scan Codes, Zeichen Codes und virtuelle Schlüsselcodes übersetzen, die von verschiedenen Tastatur Schlag Nachrichten bereitgestellt werden. Zu diesen Funktionen gehören [**mapvirtualkey**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya), [**toascii**](/windows/win32/api/winuser/nf-winuser-toascii), [**toUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)und [**vkkeyscan**](/windows/win32/api/winuser/nf-winuser-vkkeyscana).

Darüber hinaus unterstützt Microsoft Rich Edit 3,0 das [hexadeunicode-IME](/windows/desktop/Intl/hextounicode-ime), das es einem Benutzer ermöglicht, mithilfe von Tastenkombinationen zwischen hexadezimalen und Unicode-Zeichen zu konvertieren. Dies bedeutet, dass die Anwendung, wenn Microsoft Rich Edit 3,0 in eine Anwendung integriert ist, die Features des hexin-Unicode-IME erbt.

## <a name="hot-key-support"></a>Hot-Key Unterstützung

Ein *Hot Key* ist eine Tastenkombination, die eine [**WM- \_ Hotkey**](wm-hotkey.md) -Nachricht generiert, eine Meldung, die das System am Anfang der Nachrichten Warteschlange eines Threads platziert und alle vorhandenen Nachrichten in der Warteschlange umgeht. Anwendungen verwenden die Tastenkombinationen, um Tastatureingaben mit hoher Priorität vom Benutzer zu erhalten. Beispielsweise kann eine Anwendung durch Definieren eines aus der Tastenkombination STRG + C bestehenden Abkürzungs Schlüssels eine lange Operation Abbrechen.

Um einen Hotkey zu definieren, ruft eine Anwendung die [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) -Funktion auf und gibt die Kombination der Schlüssel an, die die [**WM- \_ Hotkey**](wm-hotkey.md) -Nachricht generiert, das Handle des Fensters zum Empfangen der Nachricht und den Bezeichner der Abkürzungs Taste. Wenn der Benutzer die Taste "Hot" drückt, wird eine **WM- \_ Hotkey** -Nachricht in der Nachrichten Warteschlange des Threads abgelegt, der das Fenster erstellt hat. Der *wParam* -Parameter der Nachricht enthält den Bezeichner der Abkürzungs Taste. Die Anwendung kann mehrere heiße Schlüssel für einen Thread definieren, aber jeder heiße Schlüssel im Thread muss über einen eindeutigen Bezeichner verfügen. Bevor die Anwendung beendet wird, sollte Sie die [**unregisterhotkey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) -Funktion verwenden, um die Hot-Taste zu zerstören.

Anwendungen können ein Hot Key-Steuerelement verwenden, um es den Benutzern zu erleichtern, eine Abkürzungs Taste auszuwählen. Hot Key-Steuerelemente werden in der Regel zum Definieren einer Taste verwendet, mit der ein Fenster aktiviert wird. Sie verwenden nicht die Funktionen [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) und [**unregisterhotkey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) . Stattdessen sendet eine Anwendung, die ein Hot Key-Steuerelement verwendet, in der Regel die " [**WM \_ SetHotKey**](wm-sethotkey.md) "-Nachricht, um den Hot Key festzulegen Immer wenn der Benutzer die Taste "heiß" drückt, sendet das System eine [**WM- \_ syscommand**](/windows/desktop/menurc/wm-syscommand) -Nachricht, die den SC- \_ Hotkey angibt Weitere Informationen zu Hot Key-Steuerelementen finden Sie unter "Verwenden von Hot Key-Steuerelementen" in [Hot Key](../controls/hot-key-controls.md)-Steuerelementen.

## <a name="keyboard-keys-for-browsing-and-other-functions"></a>Tastaturtasten für das Browsen und andere Funktionen

Windows bietet Unterstützung für Tastaturen mit speziellen Schlüsseln für Browserfunktionen, Medienfunktionen, Anwendungs Starts und die Energie Verwaltung. Der [**WM- \_ Befehl "appcommand**](wm-appcommand.md) " unterstützt die zusätzlichen Tastaturtasten. Außerdem wird die [**shellproc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) -Funktion so geändert, dass die zusätzlichen Tastaturtasten unterstützt werden.

Es ist unwahrscheinlich, dass ein untergeordnetes Fenster in einer Komponenten Anwendung Befehle für diese zusätzlichen Tastaturtasten direkt implementieren kann. Wenn einer dieser Schlüssel gedrückt wird, sendet [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) eine [**WM- \_ appcommand**](wm-appcommand.md) -Meldung an ein Fenster. **Defwindowproc** blinbt auch die **WM \_ appcommand** -Nachricht an das übergeordnete Fenster. Dies ähnelt der Art und Weise, wie Kontextmenüs mit der rechten Maustaste aufgerufen werden, d. h., dass **defwindowproc** eine [**WM- \_ ContextMenu**](/windows/desktop/menurc/wm-contextmenu) -Meldung mit einem Rechtsklick auf die Schaltfläche sendet und Sie an das übergeordnete Element weiterleitet. Wenn **defwindowproc** außerdem eine WM- **\_ appcommand** -Nachricht für ein Fenster der obersten Ebene empfängt, wird ein ShellHook mit dem Code **hshell \_ appcommand** aufgerufen.

Windows unterstützt auch den Microsoft Intellimaus-Explorer, bei dem es sich um eine Maus mit fünf Schaltflächen handelt. Die zwei zusätzlichen Schaltflächen unterstützen vorwärts-und rückwärts Browser Navigation. Weitere Informationen finden Sie unter [xbuttons](about-mouse-input.md).

## <a name="simulating-input"></a>Simulieren von Eingaben

Verwenden Sie die [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) -Funktion, um eine ununterbrochene Reihe von Benutzereingabe Ereignissen zu simulieren. Die-Funktion akzeptiert drei Parameter. Der erste Parameter, *cInputs*, gibt die Anzahl der Eingabeereignisse an, die simuliert werden. Der zweite Parameter *rginputs* ist ein Array von [**Eingabe**](/windows/win32/api/winuser/ns-winuser-input) Strukturen, die jeweils einen Typ von Eingabe Ereignis und zusätzliche Informationen zu diesem Ereignis beschreiben. Der letzte Parameter, *CBSIZE*, akzeptiert die Größe der **Eingabe** Struktur in Bytes.

Die [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) -Funktion wird verwendet, indem eine Reihe von simulierten Eingabe Ereignissen in den Eingabestream eines Geräts eingefügt werden. Der Effekt ähnelt dem wiederholten Aufrufen der [**Keybd- \_ Ereignis**](/windows/win32/api/winuser/nf-winuser-keybd_event) -oder [**Maus \_ Ereignis**](/windows/win32/api/winuser/nf-winuser-mouse_event) Funktion, mit dem Unterschied, dass das System sicherstellt, dass keine anderen Eingabeereignisse mit den simulierten Ereignissen zusammenhängen. Wenn der-Befehl abgeschlossen ist, gibt der Rückgabewert die Anzahl der erfolgreich wiedergegebenen Eingabeereignisse an. Wenn dieser Wert 0 (null) ist, wurde die Eingabe blockiert.

Die [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) -Funktion setzt den aktuellen Zustand der Tastatur nicht zurück. Wenn für den Benutzer beim Abrufen dieser Funktion Tasten gedrückt werden, können diese daher mit den Ereignissen, die von dieser Funktion generiert werden, beeinträchtigt werden. Wenn Sie sich Gedanken über mögliche Störungen machen, überprüfen Sie den Zustand der Tastatur mit der [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) -Funktion, und korrigieren Sie Sie bei Bedarf.

## <a name="languages-locales-and-keyboard-layouts"></a>Sprachen, Gebiets Schemas und Tastatur Layouts

Eine *Sprache* ist eine natürliche Sprache, wie z. b. Englisch, Französisch und Japanisch. Eine *unter Sprache* ist eine Variante einer natürlichen Sprache, die in einer bestimmten geografischen Region gesprochen wird, wie z. b. die englischen unter Sprachen, die im Vereinigten Königreich und der USA gesprochen werden. Anwendungen verwenden Werte, die als [sprach](/windows/desktop/Intl/language-identifiers)Bezeichner bezeichnet werden, um Sprachen und unter Sprachen eindeutig zu identifizieren.

Anwendungen verwenden normalerweise Gebiets Schemas, um die Sprache fest *zulegen, in* der Eingaben und Ausgaben verarbeitet werden. Wenn Sie z. b. das Gebiets Schema für die Tastatur festlegen, wirkt sich dies auf die von der Tastatur generierten Zeichen Werte aus. Das Festlegen des Gebiets Schemas für die Anzeige oder den Drucker wirkt sich auf die angezeigten oder gedruckten Symbole aus. Anwendungen legen das Gebiets Schema für eine Tastatur fest, indem Sie Tastaturlayouts laden und verwenden. Sie legen das Gebiets Schema für eine Anzeige oder einen Drucker fest, indem Sie eine Schriftart auswählen, die das angegebene Gebiets Schema unterstützt.

Mit einem Tastaturlayout wird nicht nur die physische Position der Tasten auf der Tastatur angegeben, sondern auch die Zeichen Werte bestimmt, die durch Drücken der Tasten generiert werden. Jedes Layout identifiziert die aktuelle Eingabe Sprache und bestimmt, welche Zeichen Werte durch welche Schlüssel und Tastenkombinationen generiert werden.

Jedes Tastaturlayout verfügt über ein entsprechendes handle, das das Layout und die Sprache identifiziert. Das niedrige Wort des Handles ist ein sprach Bezeichner. Das hohe Wort ist ein Geräte handle, das das physische Layout angibt, oder 0 (null), das ein Standardmäßiges Physisches Layout angibt. Der Benutzer kann eine beliebige Eingabe Sprache einem physischen Layout zuordnen. Beispielsweise kann ein englischsprachiger Benutzer, der sehr gelegentlich in Französisch arbeitet, die Eingabe Sprache der Tastatur auf Französisch festlegen, ohne das physische Layout der Tastatur zu ändern. Dies bedeutet, dass der Benutzer mit dem vertrauten englischen Layout Text in Französisch eingeben kann.

Anwendungen werden im Allgemeinen nicht erwartet, dass Eingabe Sprachen direkt bearbeitet werden. Stattdessen richtet der Benutzer sprach-und Layoutkombinationen ein und wechselt dann zwischen diesen. Wenn der Benutzer in Text klickt, der mit einer anderen Sprache gekennzeichnet ist, ruft die Anwendung die [**activatekeyboardlayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) -Funktion auf, um das Standardlayout des Benutzers für diese Sprache zu aktivieren. Wenn der Benutzer Text in einer Sprache bearbeitet, die nicht in der aktiven Liste enthalten ist, kann die Anwendung die [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) -Funktion mit der Sprache aufzurufen, um ein Layout auf der Grundlage dieser Sprache zu erhalten.

Die [**activatekeyboardlayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) -Funktion legt die Eingabe Sprache für den aktuellen Task fest. Der *HKL* -Parameter kann entweder das Handle für das Tastaturlayout oder eine Sprache mit 0 (null) sein. Tastaturlayout-Handles können von der [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) -Funktion oder der [**GetKeyboardLayoutList**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist) -Funktion abgerufen werden. Die **\_ Prev** -Werte für " **\_ Next** " und "HKL" können auch verwendet werden, um die nächste oder vorherige Tastatur auszuwählen.

Die [**getkeyboardlayoutname**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea) -Funktion Ruft den Namen des aktiven Tastaturlayouts für den aufrufenden Thread ab. Wenn eine Anwendung das aktive Layout mithilfe der [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) -Funktion erstellt, ruft **getkeyboardlayoutname** die gleiche Zeichenfolge ab, die zum Erstellen des Layouts verwendet wurde. Andernfalls ist die Zeichenfolge der primäre Sprach Bezeichner, der dem Gebiets Schema des aktiven Layouts entspricht. Dies bedeutet, dass die Funktion nicht notwendigerweise zwischen verschiedenen Layouts mit derselben Primärsprache unterscheiden kann, sodass keine spezifischen Informationen über die Eingabe Sprache zurückgeben kann. Die Funktion " [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) " kann jedoch verwendet werden, um die Eingabe Sprache zu bestimmen.

Die [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) -Funktion lädt ein Tastaturlayout und macht das Layout für den Benutzer verfügbar. Anwendungen können das Layout für den aktuellen Thread mithilfe des **KLF- \_ Aktivierungs** Werts sofort aktiv machen. Eine Anwendung kann den Wert der **KLF- \_ Neuanordnung** verwenden, um die Layouts neu anzuordnen, ohne auch den **KLF- \_ Aktivierungs** Wert anzugeben. Anwendungen sollten beim Laden von Tastaturlayouts immer den Wert des **KLF- \_ Ersatz Werts \_ OK** verwenden, um sicherzustellen, dass die Benutzereinstellung, falls vorhanden, ausgewählt ist.

Für mehrsprachige Unterstützung stellt die [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) -Funktion die **KLF- \_ replacelang** -und **KLF- \_ notellshell** -Flags bereit. Das **KLF \_ replacelang** -Flag leitet die Funktion um, um ein vorhandenes Tastaturlayout zu ersetzen, ohne die Sprache zu ändern. Der Versuch, ein vorhandenes Layout mit dem gleichen sprach Bezeichner zu ersetzen, aber ohne Angabe von **KLF \_ replacelang** ist ein Fehler. Das **KLF-Flag \_ notellshell** verhindert, dass die Funktion die Shell benachrichtigt, wenn ein Tastaturlayout hinzugefügt oder ersetzt wird. Dies ist nützlich für Anwendungen, die mehrere Layouts in einer aufeinander folgenden Reihe von Aufrufen hinzufügen. Dieses Flag sollte in allen bis auf den letzten-Befehl verwendet werden.

Die [**unloadkeyboardlayout**](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout) -Funktion ist darauf beschränkt, dass Sie die Standardeingabe Sprache des Systems nicht entladen kann. Dadurch wird sichergestellt, dass für den Benutzer immer ein Layout verfügbar ist, das den gleichen Zeichensatz wie die Shell und das Dateisystem verwendet.

 

 
