---
description: In diesem Thema wird erläutert, wie Hooks verwendet werden sollen.
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: Übersicht über Hooks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10754f7275ce06c17b668e04c7792e6296a854fbe14a6ebc9544fbb70c73e9cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201225"
---
# <a name="hooks-overview"></a>Übersicht über Hooks

Ein *Hook* ist ein Mechanismus, mit dem eine Anwendung Ereignisse wie Nachrichten, Mausaktionen und Tastatureingaben abfangen kann. Eine Funktion, die einen bestimmten Ereignistyp abfingt, wird als *Hookprozedur bezeichnet.* Eine Hookprozedur kann für jedes empfangene Ereignis agieren und dann das Ereignis ändern oder verwerfen.

Im folgenden Beispiel wird für Hooks verwendet:

-   Überwachen von Meldungen zu Debugzwecken
-   Bereitstellen von Unterstützung für die Aufzeichnung und Wiedergabe von Makros
-   Bereitstellen von Unterstützung für einen Hilfeschlüssel (F1)
-   Simulieren von Maus- und Tastatureingaben
-   Implementieren einer CBT-Anwendung (Computer-Based Training)

> [!Note]  
> Hooks verlangsamen das System in der Regel, da sie die Verarbeitungsmenge erhöhen, die das System für jede Nachricht ausführen muss. Installieren Sie einen Hook nur bei Bedarf, und entfernen Sie ihn so bald wie möglich.

 

In diesem Abschnitt wird Folgendes erläutert:

-   [Hookketten](#hook-chains)
-   [Hook-Prozeduren](#hook-procedures)
-   [Hooktypen](#hook-types)
    -   [WH \_ CALLWNDPROC und WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
    -   [WH \_ CBT](#wh_cbt)
    -   [WH \_ DEBUG](#wh_debug)
    -   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
    -   [WH \_ GETMESSAGE](#wh_getmessage)
    -   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
    -   [WH \_ JOURNALRECORD](#wh_journalrecord)
    -   [WH \_ KEYBOARD \_ LL](#wh_keyboard_ll)
    -   [\_WH-TASTATUR](#wh_keyboard)
    -   [WH \_ MOUSE \_ LL](#wh_mouse_ll)
    -   [\_WH-MAUS](#wh_mouse)
    -   [WH \_ MSGFILTER und WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [\_WH-SHELL](#wh_shell)

## <a name="hook-chains"></a>Hookketten

Das System unterstützt viele verschiedene Arten von Hooks. jeder Typ bietet Zugriff auf einen anderen Aspekt des Nachrichtenbehandlungsmechanismus. Beispielsweise kann eine Anwendung den [WH \_ MOUSE-Hook](#wh_mouse) verwenden, um den Nachrichtendatenverkehr für Mausnachrichten zu überwachen.

Das System verwaltet eine separate Hookkette für jeden Hooktyp. Eine *Hookkette ist* eine Liste von Zeigern auf spezielle, anwendungsdefinierte Rückruffunktionen, die als *Hook-Prozeduren bezeichnet werden.* Wenn eine Nachricht auftritt, die einem bestimmten Hooktyp zugeordnet ist, übergibt das System die Nachricht an jede Hookprozedur, auf die in der Hookkette nacheinander verwiesen wird. Die Aktion, die eine Hookprozedur ergreifen kann, hängt vom Typ des beteiligten Hooks ab. Die Hookverfahren für einige Arten von Hooks können nur Nachrichten überwachen. Andere können Nachrichten ändern oder ihren Fortschritt durch die Kette beenden, um zu verhindern, dass sie die nächste Hookprozedur oder das Zielfenster erreichen.

## <a name="hook-procedures"></a>Hook-Prozeduren

Um einen bestimmten Hooktyp zu nutzen, stellt der Entwickler eine Hookprozedur zur Verfügung und verwendet die [**SetWindowsHookEx-Funktion,**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) um sie in der Kette zu installieren, die dem Hook zugeordnet ist. Eine Hookprozedur muss die folgende Syntax haben:

``` syntax
LRESULT CALLBACK HookProc(
  int nCode, 
  WPARAM wParam, 
  LPARAM lParam
)
{
   // process event
   ...

   return CallNextHookEx(NULL, nCode, wParam, lParam);
}
```

*HookProc ist* ein Platzhalter für einen anwendungsdefinierten Namen.

Der *nCode-Parameter* ist ein Hookcode, mit dem die Hookprozedur die durchzuführende Aktion bestimmt. Der Wert des Hookcodes hängt vom Typ des Hooks ab. Jeder Typ verfügt über einen eigenen Merkmalssatz von Hookcodes. Die Werte der *Parameter wParam* und *lParam* hängen vom Hookcode ab, enthalten jedoch in der Regel Informationen zu einer gesendeten oder gesendeten Nachricht.

Die [**SetWindowsHookEx-Funktion**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) installiert immer eine Hookprozedur am Anfang einer Hookkette. Wenn ein Ereignis auftritt, das von einem bestimmten Hooktyp überwacht wird, ruft das System die Prozedur am Anfang der Hookkette auf, die dem Hook zugeordnet ist. Jede Hookprozedur in der Kette bestimmt, ob das Ereignis an die nächste Prozedur übergeben werden soll. Eine Hookprozedur übergibt ein Ereignis durch Aufrufen der [**CallNextHookEx-Funktion**](/windows/win32/api/winuser/nf-winuser-callnexthookex) an die nächste Prozedur.

Beachten Sie, dass die Hookverfahren für einige Arten von Hooks nur Nachrichten überwachen können. das System übergibt Nachrichten an jede Hookprozedur, unabhängig davon, ob eine bestimmte Prozedur [**CallNextHookEx aufruft.**](/windows/win32/api/winuser/nf-winuser-callnexthookex)

Ein *globaler Hook* überwacht Nachrichten für alle Threads auf demselben Desktop wie der aufrufende Thread. Ein *threadspezifischer Hook überwacht* Nachrichten nur für einen einzelnen Thread. Eine globale Hookprozedur kann im Kontext einer beliebigen Anwendung auf demselben Desktop wie der aufrufende Thread aufgerufen werden, sodass sich die Prozedur in einem separaten DLL-Modul befindet. Eine threadspezifische Hookprozedur wird nur im Kontext des zugeordneten Threads aufgerufen. Wenn eine Anwendung eine Hookprozedur für einen ihrer eigenen Threads installiert, kann sich die Hookprozedur entweder im selben Modul wie der Rest des Anwendungscodes oder in einer DLL befindet. Wenn die Anwendung eine Hookprozedur für einen Thread einer anderen Anwendung installiert, muss die Prozedur in einer DLL enthalten sein. Weitere Informationen finden Sie unter [Dynamic Link Libraries](../dlls/dynamic-link-libraries.md).

> [!Note]  
> Sie sollten globale Hooks nur zu Debugzwecken verwenden. Andernfalls sollten Sie sie vermeiden. Globale Hooks beeinträchtigen die Systemleistung und verursachen Konflikte mit anderen Anwendungen, die die gleiche Art von globalem Hook implementieren.

 

## <a name="hook-types"></a>Hooktypen

Mit jedem Hooktyp kann eine Anwendung einen anderen Aspekt des Nachrichtenbehandlungsmechanismus des Systems überwachen. In den folgenden Abschnitten werden die verfügbaren Hooks beschrieben.

-   [WH \_ CALLWNDPROC und WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
-   [WH \_ CBT](#wh_cbt)
-   [WH \_ DEBUG](#wh_debug)
-   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
-   [WH \_ GETMESSAGE](#wh_getmessage)
-   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
-   [WH \_ JOURNALRECORD](#wh_journalrecord)
-   [WH \_ KEYBOARD \_ LL](#wh_keyboard_ll)
-   [\_WH-TASTATUR](#wh_keyboard)
-   [WH \_ MOUSE \_ LL](#wh_mouse_ll)
-   [\_WH-MAUS](#wh_mouse)
-   [WH \_ MSGFILTER und WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
-   [\_WH-SHELL](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a>WH \_ CALLWNDPROC und WH \_ CALLWNDPROCRET

Mit **den Hooks WH \_ CALLWNDPROC** und **WH \_ CALLWNDPROCRET** können Sie Nachrichten überwachen, die an Fensterprozeduren gesendet werden. Das System ruft eine **WH \_ CALLWNDPROC-Hookprozedur** auf, bevor die Nachricht an die Prozedur für das empfangende Fenster übergeben wird, und ruft die **WH \_ CALLWNDPROCRET-Hookprozedur** auf, nachdem die Fensterprozedur die Nachricht verarbeitet hat.

Der **WH \_ CALLWNDPROCRET-Hook** übergibt einen Zeiger auf eine [**CWPRETSTRUCT-Struktur**](/windows/win32/api/winuser/ns-winuser-cwpretstruct) an die Hookprozedur. Die -Struktur enthält den Rückgabewert der Fensterprozedur, die die Nachricht verarbeitet hat, sowie die der Nachricht zugeordneten Meldungsparameter. Das Unterklassen des Fensters funktioniert nicht für Nachrichten, die zwischen Prozessen festgelegt wurden.

Weitere Informationen finden Sie in den [*Rückruffunktionen CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) und [*CallWndRetProc.*](/windows/win32/api/winuser/nc-winuser-hookproc)

### <a name="wh_cbt"></a>WH \_ CBT

Das System ruft eine **\_ WH-CBT-Hookprozedur** vor dem Aktivieren, Erstellen, Zerstören, Minimieren, Maximieren, Verschieben oder Anpassen eines Fensters auf, bevor ein Systembefehl abgeschlossen wird; vor dem Entfernen eines Maus- oder Tastaturereignisses aus der Systemnachrichtenwarteschlange, vor dem Festlegen des Eingabefokus oder vor dem Synchronisieren mit der Systemnachrichtenwarteschlange. Der Wert, den die Hookprozedur zurückgibt, bestimmt, ob das System einen dieser Vorgänge zulässt oder verhindert. Der **WH \_ CBT-Hook** ist in erster Linie für computerbasierte Trainingsanwendungen (CBT) vorgesehen.

Weitere Informationen finden Sie unter [*der CBTProc-Rückruffunktion.*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85))

Weitere Informationen finden Sie unter [WinEvents](/windows/desktop/WinAuto/winevents-infrastructure).

### <a name="wh_debug"></a>WH \_ DEBUG

Das System ruft vor dem Aufrufen von Hookprozeduren, die einem anderen Hook im System zugeordnet sind, eine **WH-DEBUG-Hookprozedur \_** auf. Sie können diesen Hook verwenden, um zu bestimmen, ob das System hook-Prozeduren aufrufen darf, die anderen Hooktypen zugeordnet sind.

Weitere Informationen finden Sie unter [*der DebugProc-Rückruffunktion.*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85))

### <a name="wh_foregroundidle"></a>WH \_ FOREGROUNDIDLE

Mit **dem WH \_ FOREGROUNDIDLE-Hook** können Sie Aufgaben mit niedriger Priorität in Zeiten ausführen, in denen sich der Vordergrundthread im Leerlauf befindet. Das System ruft eine **WH \_ FOREGROUNDIDLE-Hookprozedur** auf, wenn sich der Vordergrundthread der Anwendung im Leerlauf befindet.

Weitere Informationen finden Sie unter [*der ForegroundIdleProc-Rückruffunktion.*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85))

### <a name="wh_getmessage"></a>WH \_ GETMESSAGE

Der **WH \_ GETMESSAGE-Hook** ermöglicht es einer Anwendung, Nachrichten zu überwachen, die von der [**GetMessage-**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**PeekMessage-Funktion zurückgegeben werden**](/windows/win32/api/winuser/nf-winuser-peekmessagea) sollen. Sie können den **WH \_ GETMESSAGE-Hook** verwenden, um Maus- und Tastatureingaben sowie andere Nachrichten zu überwachen, die an die Nachrichtenwarteschlange gesendet werden.

Weitere Informationen finden Sie unter [*der GetMsgProc-Rückruffunktion.*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))

### <a name="wh_journalplayback"></a>WH \_ JOURNALPLAYBACK

Mit **dem Hook WH \_ JOURNALPLAYBACK** kann eine Anwendung Nachrichten in die Systemnachrichtenwarteschlange einfügen. Sie können diesen Hook verwenden, um eine Reihe von Maus- und Tastaturereignissen wieder zu spielen, die zuvor mithilfe von [WH \_ JOURNALRECORD aufgezeichnet wurden.](#wh_journalrecord) Reguläre Maus- und Tastatureingaben werden deaktiviert, solange ein **WH \_ JOURNALPLAYBACK-Hook** installiert ist. Ein **WH \_ JOURNALPLAYBACK-Hook** ist ein globaler Hook– er kann nicht als threadspezifischer Hook verwendet werden.

Der **WH \_ JOURNALPLAYBACK-Hook** gibt einen Time out-Wert zurück. Dieser Wert gibt dem System an, wie viele Millisekunden gewartet werden soll, bevor die aktuelle Nachricht vom Wiedergabehook verarbeitet wird. Dies ermöglicht es dem Hook, die Zeitliche Steuerung der Ereignisse zu steuern, die er wieder gibt.

Weitere Informationen finden Sie unter der [*Rückruffunktion JournalPlaybackProc.*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))

### <a name="wh_journalrecord"></a>WH \_ JOURNALRECORD

Mit **dem Hook WH \_ JOURNALRECORD** können Sie Eingabeereignisse überwachen und aufzeichnen. In der Regel verwenden Sie diesen Hook, um eine Sequenz von Maus- und Tastaturereignissen zu erfassen, die später mithilfe von [WH \_ JOURNALPLAYBACK wiedergegeben werden.](#wh_journalplayback) Der **WH \_ JOURNALRECORD-Hook** ist ein globaler Hook– er kann nicht als threadspezifischer Hook verwendet werden.

Weitere Informationen finden Sie unter der [*Rückruffunktion JournalRecordProc.*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))

### <a name="wh_keyboard_ll"></a>WH \_ KEYBOARD \_ LL

Mit **dem WH \_ KEYBOARD \_ LL-Hook** können Sie Tastatureingabeereignisse überwachen, die in einer Threadeingabewarteschlange veröffentlicht werden.

Weitere Informationen finden Sie unter [*der Rückruffunktion LowLevelKeyboardProc.*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85))

### <a name="wh_keyboard"></a>\_WH-TASTATUR

Mit **dem WH \_ KEYBOARD-Hook** kann eine Anwendung den Nachrichtendatenverkehr für [**WM \_ KEYDOWN-**](/windows/desktop/inputdev/wm-keydown) und [**WM \_ KEYUP-Nachrichten**](/windows/desktop/inputdev/wm-keyup) überwachen, die von der [**GetMessage-**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**PeekMessage-Funktion zurückgegeben werden**](/windows/win32/api/winuser/nf-winuser-peekmessagea) sollen. Sie können den **WH \_ KEYBOARD-Hook verwenden,** um Tastatureingaben zu überwachen, die an eine Nachrichtenwarteschlange gesendet werden.

Weitere Informationen finden Sie unter [*der KeyboardProc-Rückruffunktion.*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85))

### <a name="wh_mouse_ll"></a>WH \_ MOUSE \_ LL

Mit **dem WH \_ MOUSE \_ LL-Hook** können Sie Mauseingabeereignisse überwachen, die in einer Threadeingabewarteschlange veröffentlicht werden.

Weitere Informationen finden Sie unter [*der LowLevelMouseProc-Rückruffunktion.*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85))

### <a name="wh_mouse"></a>\_WH-MAUS

Mit **dem WH \_ MOUSE-Hook** können Sie Mausnachrichten überwachen, die von der GetMessage- oder [**PeekMessage-Funktion zurückgegeben werden**](/windows/win32/api/winuser/nf-winuser-peekmessagea) sollen. [](/windows/win32/api/winuser/nf-winuser-getmessage) Sie können den **WH \_ MOUSE-Hook** verwenden, um Mauseingaben zu überwachen, die in eine Nachrichtenwarteschlange gesendet werden.

Weitere Informationen finden Sie unter [*der MouseProc-Rückruffunktion.*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85))

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a>WH \_ MSGFILTER und WH \_ SYSMSGFILTER

Mit den **HOOKs \_ WH MSGFILTER** und **WH \_ SYSMSGFILTER** können Sie Nachrichten überwachen, die über ein Menü, eine Scrollleiste, ein Meldungsfeld oder ein Dialogfeld verarbeitet werden sollen, und erkennen, wann ein anderes Fenster aktiviert werden soll, wenn der Benutzer die Tastenkombination ALT+TAB oder ALT+ESC drückt. Der **WH \_ MSGFILTER-Hook** kann nur Nachrichten überwachen, die an ein Menü, eine Scrollleiste, ein Meldungsfeld oder ein Dialogfeld übergeben werden, das von der Anwendung erstellt wurde, die die Hookprozedur installiert hat. Der **WH \_ SYSMSGFILTER-Hook** überwacht solche Nachrichten für alle Anwendungen.

Die **\_ WH-Hooks MSGFILTER** und **WH \_ SYSMSGFILTER** ermöglichen Ihnen das Filtern von Nachrichten während modaler Schleifen, die der Filterung in der Hauptnachrichtenschleife entsprechen. Beispielsweise untersucht eine Anwendung häufig eine neue Nachricht in der Hauptschleife zwischen dem Zeitpunkt, zu dem sie die Nachricht aus der Warteschlange abruft, und dem Zeitpunkt, zu dem sie die Nachricht versendet, und führt bei Bedarf eine spezielle Verarbeitung durch. Während einer modalen Schleife ruft das System jedoch Nachrichten ab und gibt sie weiter, ohne dass eine Anwendung die Möglichkeit hat, die Nachrichten in der Hauptnachrichtenschleife zu filtern. Wenn eine Anwendung eine **\_ WH-MSGFILTER-** oder **\_ WH-SYSMSGFILTER-Hookprozedur** installiert, ruft das System die Prozedur während der modalen Schleife auf.

Eine Anwendung kann den **WH \_ MSGFILTER-Hook** direkt aufrufen, indem sie die [**CallMsgFilter-Funktion**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) aufruft. Mit dieser Funktion kann die Anwendung denselben Code verwenden, um Nachrichten während modaler Schleifen zu filtern, wie sie in der Hauptnachrichtenschleife verwendet. Kapseln Sie dazu die Filtervorgänge in einer **WH MSGFILTER-Hookprozedur, \_** und rufen Sie **CallMsgFilter zwischen** den Aufrufen der [**GetMessage-**](/windows/win32/api/winuser/nf-winuser-getmessage) und [**DispatchMessage-Funktionen**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) auf.

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

Das letzte Argument von [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) wird einfach an die Hookprozedur übergeben. Sie können einen beliebigen Wert eingeben. Die Hookprozedur kann durch Definieren einer Konstante wie **MSGF \_ MAINLOOP** diesen Wert verwenden, um zu bestimmen, von wo die Prozedur aufgerufen wurde.

Weitere Informationen finden Sie unter den [*Rückruffunktionen MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) und [*SysMsgProc.*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85))

### <a name="wh_shell"></a>\_WH-SHELL

Eine Shellanwendung kann den **WH \_ SHELL-Hook** verwenden, um wichtige Benachrichtigungen zu erhalten. Das System ruft eine **WH \_ SHELL-Hookprozedur** auf, wenn die Shellanwendung aktiviert wird und wenn ein Fenster der obersten Ebene erstellt oder zerstört wird.

Beachten Sie, dass benutzerdefinierte Shellanwendungen keine **WH \_ SHELL-Nachrichten** empfangen. Daher muss jede Anwendung, die sich selbst als Standardshell registriert, die [**SystemParametersInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) aufrufen, bevor sie (oder eine andere Anwendung) **WH SHELL-Nachrichten \_ empfangen** kann. Diese Funktion muss mit **SPI \_ SETMINIMIZEDMETRICS und** einer [**MINIMIZEDMETRICS-Struktur aufgerufen**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) werden. Legen Sie **den iArrange-Member** dieser -Struktur auf **ARW \_ HIDE fest.**

Weitere Informationen finden Sie unter [*der ShellProc-Rückruffunktion.*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))

 

 
