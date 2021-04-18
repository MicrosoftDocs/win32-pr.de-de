---
description: In diesem Thema wird erläutert, wie Hooks verwendet werden sollten.
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: Übersicht über Hooks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c5d89f111604418d1dc3ea9a4ebce6fe0a8124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352231"
---
# <a name="hooks-overview"></a>Übersicht über Hooks

Ein *Hook* ist ein Mechanismus, mit dem eine Anwendung Ereignisse abfangen kann, z. b. Nachrichten, Mausaktionen und Tastatureingaben. Eine Funktion, die einen bestimmten Ereignistyp abfängt, wird als *Hook-Prozedur* bezeichnet. Eine Hook-Prozedur kann auf jedes empfangene Ereignis reagieren und dann das Ereignis ändern oder verwerfen.

Im folgenden Beispiel wird für Hooks verwendet:

-   Überwachen von Meldungen zu Debugzwecken
-   Unterstützung für die Aufzeichnung und Wiedergabe von Makros bereitstellen
-   Unterstützung für eine Hilfe Taste (F1)
-   Maus-und Tastatureingabe simulieren
-   Implementieren einer computerbasierten Schulungs Anwendung (CBT)

> [!Note]  
> Hooks neigen dazu, das System zu verlangsamen, da Sie die Verarbeitungs Menge erhöhen, die das System für jede Nachricht ausführen muss. Sie sollten einen Hook nur dann installieren, wenn dies erforderlich ist, und ihn so bald wie möglich entfernen.

 

In diesem Abschnitt wird Folgendes erläutert:

-   [Hook-Ketten](#hook-chains)
-   [Hook-Verfahren](#hook-procedures)
-   [Hook-Typen](#hook-types)
    -   [WH \_ callwndproc und WH \_ callwndprokret](#wh_callwndproc-and-wh_callwndprocret)
    -   [WH \_ CBT](#wh_cbt)
    -   [WH- \_ Debug](#wh_debug)
    -   [WH \_ foregroundidle](#wh_foregroundidle)
    -   [WH \_ GetMessage](#wh_getmessage)
    -   [WH \_ journalplayback](#wh_journalplayback)
    -   [WH \_ Journaldatensatz](#wh_journalrecord)
    -   [WH \_ Tastatur \_](#wh_keyboard_ll)
    -   [WH- \_ Tastatur](#wh_keyboard)
    -   [WH- \_ Maustaste \_](#wh_mouse_ll)
    -   [WH- \_ Maus](#wh_mouse)
    -   [WH \_ msgfilter und WH \_ sysmsgfilter](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [WH- \_ Shell](#wh_shell)

## <a name="hook-chains"></a>Hook-Ketten

Das System unterstützt viele verschiedene Arten von Hooks. Jeder Typ bietet Zugriff auf einen anderen Aspekt seines Nachrichten Behandlungs Mechanismus. Eine Anwendung kann z. b. den Datenverkehr mit dem Datenverkehr "Wh" für Maus Nachrichten überwachen. [ \_ ](#wh_mouse)

Das System verwaltet für jeden Typ von Hook eine separate Hook-Kette. Eine *Hookkette* ist eine Liste von Zeigern zu speziellen, Anwendungs definierten Rückruf Funktionen, die als *Hook-Prozeduren* bezeichnet werden. Wenn eine Nachricht auftritt, die einem bestimmten Hook-Typ zugeordnet ist, übergibt das System die Nachricht an jede Hook-Prozedur, auf die in der Hook-Kette verwiesen wird. Die Aktion, die eine Hook-Prozedur ausführen kann, hängt vom Typ des Beteiligten Hooks ab. Die Hook-Prozeduren für einige Arten von Hooks können nur Nachrichten überwachen. andere Benutzer können Nachrichten ändern oder den Fortschritt durch die Kette abbrechen, sodass Sie nicht mehr die nächste Hook-Prozedur oder das Zielfenster erreichen können.

## <a name="hook-procedures"></a>Hook-Verfahren

Um von einer bestimmten Art von Hook profitieren zu können, stellt der Entwickler eine Hook-Prozedur bereit und verwendet die [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) -Funktion, um Sie in der dem Hook zugeordneten Kette zu installieren. Eine Hook-Prozedur muss folgende Syntax aufweisen:

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

"Host *" ist ein* Platzhalter für einen Anwendungs definierten Namen.

Der *nCode* -Parameter ist ein Hook-Code, den die Hook-Prozedur verwendet, um die auszuführende Aktion zu bestimmen. Der Wert des Hook-Codes hängt vom Typ des Hooks ab. Jeder Typ verfügt über einen eigenen Merkmals Satz von Hook-Codes. Die Werte der *wParam* -und *LPARAM* -Parameter hängen von dem Hook-Code ab, Sie enthalten jedoch in der Regel Informationen zu einer Nachricht, die gesendet oder gepostet wurde.

Die Funktion " [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) " installiert immer eine Hook-Prozedur am Anfang einer Hook-Kette. Wenn ein Ereignis auftritt, das von einem bestimmten Hook-Typ überwacht wird, ruft das System die Prozedur am Anfang der dem Hook zugeordneten Hook-Kette auf. Jede Hook-Prozedur in der Kette bestimmt, ob das Ereignis an die nächste Prozedur übergeben wird. Eine Hook-Prozedur übergibt ein Ereignis an das nächste Verfahren, indem die [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex) -Funktion aufgerufen wird.

Beachten Sie, dass die Hook-Prozeduren für einige Arten von Hooks nur Nachrichten überwachen können. Das System übergibt Nachrichten an jede Hook-Prozedur, unabhängig davon, ob eine bestimmte Prozedur [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex)aufruft.

Ein *globaler Hook* überwacht Nachrichten für alle Threads im gleichen Desktop wie der aufrufende Thread. Ein *Thread spezifischer Hook* überwacht Nachrichten nur für einen einzelnen Thread. Eine globale Hook-Prozedur kann im Kontext einer beliebigen Anwendung im selben Desktop wie der aufrufende Thread aufgerufen werden, sodass sich die Prozedur in einem separaten dll-Modul befinden muss. Eine Thread spezifische Hook-Prozedur wird nur im Kontext des zugeordneten Threads aufgerufen. Wenn eine Anwendung eine Hook-Prozedur für einen ihrer eigenen Threads installiert, kann sich die Hook-Prozedur entweder im gleichen Modul wie der restliche Code der Anwendung oder in einer DLL befinden. Wenn die Anwendung eine Hook-Prozedur für einen Thread einer anderen Anwendung installiert, muss sich die Prozedur in einer DLL befinden. Weitere Informationen finden Sie unter [Dynamic Link Libraries (Dynamic Link Libraries](../dlls/dynamic-link-libraries.md)).

> [!Note]  
> Sie sollten globale Hooks nur zu Debuggingzwecken verwenden. Andernfalls sollten Sie diese vermeiden. Globale Hooks beeinträchtigen die Systemleistung und verursachen Konflikte mit anderen Anwendungen, die denselben Typ von globalem Hook implementieren.

 

## <a name="hook-types"></a>Hook-Typen

Mit jedem Hook-Typ kann eine Anwendung einen anderen Aspekt des Nachrichten Behandlungs Mechanismus des Systems überwachen. In den folgenden Abschnitten werden die verfügbaren Hooks beschrieben.

-   [WH \_ callwndproc und WH \_ callwndprokret](#wh_callwndproc-and-wh_callwndprocret)
-   [WH \_ CBT](#wh_cbt)
-   [WH- \_ Debug](#wh_debug)
-   [WH \_ foregroundidle](#wh_foregroundidle)
-   [WH \_ GetMessage](#wh_getmessage)
-   [WH \_ journalplayback](#wh_journalplayback)
-   [WH \_ Journaldatensatz](#wh_journalrecord)
-   [WH \_ Tastatur \_](#wh_keyboard_ll)
-   [WH- \_ Tastatur](#wh_keyboard)
-   [WH- \_ Maustaste \_](#wh_mouse_ll)
-   [WH- \_ Maus](#wh_mouse)
-   [WH \_ msgfilter und WH \_ sysmsgfilter](#wh_msgfilter-and-wh_sysmsgfilter)
-   [WH- \_ Shell](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a>WH \_ callwndproc und WH \_ callwndprokret

Mit den " **WH \_ callwndproc** " und " **WH \_ callwndprokret** " können Sie Nachrichten überwachen, die an Fenster Prozeduren gesendet werden Das System ruft eine " **WH \_ callwndproc** "-Hook-Prozedur auf, bevor die Nachricht an die Empfangs Fenster Prozedur übergeben wird, und ruft die " **WH \_ callwndprokret** "-Hook-Prozedur auf, nachdem die Fenster Prozedur die Nachricht verarbeitet hat

Der " **WH \_ callwndprokret** "-Hook übergibt einen Zeiger auf eine [**cwpretstruct**](/windows/win32/api/winuser/ns-winuser-cwpretstruct) -Struktur an die Hook-Prozedur. Die-Struktur enthält den Rückgabewert der Fenster Prozedur, von der die Nachricht verarbeitet wurde, sowie die Nachrichten Parameter, die der Meldung zugeordnet sind. Unterklassen das Fenster funktioniert nicht für Nachrichten, die zwischen Prozessen festgelegt sind.

Weitere Informationen finden Sie in den [*callwndproc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) -und [*callwndretproc*](/windows/win32/api/winuser/nc-winuser-hookproc) -Rückruf Funktionen.

### <a name="wh_cbt"></a>WH \_ CBT

Das System ruft eine **WH \_ CBT** -Hook-Prozedur vor dem aktivieren, erstellen, zerstören, minimieren, maximieren, verschieben oder Anpassen eines Fensters auf, vor dem Abschließen eines System Befehls, vor dem Entfernen eines Maus-oder Tastatur Ereignisses aus der System Meldungs Warteschlange, vor dem Festlegen des Eingabefokus oder vor der Synchronisierung mit der System Meldungs Warteschlange. Der Wert, den die Hook-Prozedur zurückgibt, bestimmt, ob das System einen dieser Vorgänge zulässt oder verhindert. Der **WH \_ CBT** -Hook ist hauptsächlich für computerbasierte Schulungs Anwendungen (CBT) vorgesehen.

Weitere Informationen finden Sie unter der [*cbtproc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85)) -Rückruffunktion.

Weitere Informationen finden Sie unter [WinEvents](/windows/desktop/WinAuto/winevents-infrastructure).

### <a name="wh_debug"></a>WH- \_ Debug

Das System ruft vor dem Aufrufen von Hook-Prozeduren, die einem anderen Hook im System zugeordnet sind, eine " **WH- \_ debughook** Sie können diesen Hook verwenden, um zu bestimmen, ob das System das aufzurufen von Hook-Prozeduren zulässt, die anderen Arten von Hooks zugeordnet sind.

Weitere Informationen finden Sie in der [*debugproc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85)) -Rückruffunktion.

### <a name="wh_foregroundidle"></a>WH \_ foregroundidle

Der **WH \_ foregroundidle** -Hook ermöglicht Ihnen das Ausführen von Aufgaben mit niedriger Priorität in Zeiten, in denen sich der Vordergrund Thread im Leerlauf befindet. Das System ruft eine **WH \_ foregroundidle** -Hook-Prozedur auf, wenn der Vordergrund Thread der Anwendung sich im Leerlauf befindet.

Weitere Informationen finden Sie in der [*foregroundidleproc*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85)) -Rückruffunktion.

### <a name="wh_getmessage"></a>WH \_ GetMessage

Der **WH \_ GetMessage** -Hook ermöglicht einer Anwendung das Überwachen von Nachrichten, die von der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion oder der [**Peer-Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Funktion zurückgegeben werden. Mit dem " **WH \_ GetMessage** "-Hook können Sie die Maus-und Tastatureingaben sowie andere in der Nachrichten Warteschlange gesendetes Meldungen überwachen.

Weitere Informationen finden Sie in der [*getmsgproc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) -Rückruffunktion.

### <a name="wh_journalplayback"></a>WH \_ journalplayback

Der **WH \_ journalplayback** -Hook ermöglicht einer Anwendung das Einfügen von Nachrichten in die System Meldungs Warteschlange. Mit diesem Hook können Sie eine Reihe von Maus-und Tastatur Ereignissen wiedergeben, die zuvor mithilfe von " [WH \_ journalrecord](#wh_journalrecord)" aufgezeichnet wurden. Normale Maus-und Tastatureingaben werden deaktiviert, solange ein " **WH \_ journalplayback** "-Hook installiert ist. Ein **WH \_ journalplayback** -Hook ist ein globaler Hook – er kann nicht als Thread spezifischer Hook verwendet werden.

Der **WH \_ journalplayback** -Hook gibt einen Timeout Wert zurück. Dieser Wert teilt dem System mit, wie viele Millisekunden gewartet werden muss, bevor die aktuelle Nachricht vom Wiedergabe Hook verarbeitet wird. Dies ermöglicht es dem Hook, die zeitliche Steuerung der wiedergegeben Ereignisse zu steuern.

Weitere Informationen finden Sie in der [*journalplaybackproc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) -Rückruffunktion.

### <a name="wh_journalrecord"></a>WH \_ Journaldatensatz

Mit dem " **WH \_ journalrecord** "-Hook können Sie Eingabeereignisse überwachen und aufzeichnen. In der Regel verwenden Sie diesen Hook zum Aufzeichnen einer Sequenz von Maus-und Tastatur Ereignissen, um Sie später mithilfe von " [WH \_ journalplayback](#wh_journalplayback)" wiederzugeben. Der " **WH \_ journalrecord** "-Hook ist ein globaler Hook – er kann nicht als Thread spezifischer Hook verwendet werden.

Weitere Informationen finden Sie in der [*journalrecordproc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) -Rückruffunktion.

### <a name="wh_keyboard_ll"></a>WH \_ Tastatur \_

Mit dem " **WH \_ Keyboard \_ ll** Hook" können Sie Tastatureingabe Ereignisse überwachen, die in einer Thread Eingabe Warteschlange gepostet werden.

Weitere Informationen finden Sie unter der [*LowLevelKeyboardProc*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85)) -Rückruffunktion.

### <a name="wh_keyboard"></a>WH- \_ Tastatur

Der **WH- \_ Tastatur** Hook ermöglicht einer Anwendung, den Nachrichtenverkehr für [**WM- \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) -und [**WM- \_ KeyUp**](/windows/desktop/inputdev/wm-keyup) -Meldungen zu überwachen, die von der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion oder der [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Funktion zurückgegeben werden Mithilfe des WH- **\_ Tastatur** Hooks können Sie Tastatureingaben überwachen, die in einer Nachrichten Warteschlange gepostet werden.

Weitere Informationen finden Sie in der [*keyboardproc*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85)) -Rückruffunktion.

### <a name="wh_mouse_ll"></a>WH- \_ Maustaste \_

Mit dem " **WH \_ Mouse \_ ll** Hook" können Sie Mauseingabe Ereignisse überwachen, die in einer Thread Eingabe Warteschlange gepostet werden.

Weitere Informationen finden Sie unter der [*lowlevelmousetproc*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85)) -Rückruffunktion.

### <a name="wh_mouse"></a>WH- \_ Maus

Mit dem "Wh"-mousehook können Sie Maus Meldungen überwachen, die von der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion oder der [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Funktion zurückgegeben werden. **\_** Mit dem "Wh"-mousehook können Sie Maus Eingaben überwachen, die in einer Nachrichten Warteschlange gepostet **\_**

Weitere Informationen finden Sie unter [*mousetproc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85)) -Rückruffunktion.

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a>WH \_ msgfilter und WH \_ sysmsgfilter

Mit den Gruppen " **WH \_ msgfilter** " und " **WH \_ sysmsgfilter** " können Sie Nachrichten überwachen, die über ein Menü, eine Bild Lauf Leiste, ein Meldungs Feld oder ein Dialogfeld verarbeitet werden sollen, und erkennen, wann ein anderes Fenster aktiviert werden soll, wenn der Benutzer die Tastenkombination Alt + Tab oder ALT + ESC drückt. Der " **WH \_ msgfilter** "-Hook kann nur Nachrichten überwachen, die an ein Menü, eine Bild Lauf Leiste, ein Meldungs Feld oder ein Dialogfeld übermittelt wurden Der " **WH \_ sysmsgfilter** "-Hook überwacht solche Nachrichten für alle Anwendungen.

Mit den " **WH \_ msgfilter** "-und " **WH \_ sysmsgfilter** "-Hooks können Sie bei modalen Schleifen eine Nachrichtenfilterung durchführen, die der in der Hauptnachrichten Schleife durchgeführten Filterung entspricht. Beispielsweise untersucht eine Anwendung häufig eine neue Nachricht in der Hauptschleife zwischen dem Zeitpunkt, zu dem Sie die Nachricht aus der Warteschlange abruft, und dem Zeitpunkt, an dem die Nachricht gesendet wird, und führt gegebenenfalls eine spezielle Verarbeitung durch. Während einer modalen Schleife ruft das System jedoch Nachrichten ab und sendet Sie, ohne dass eine Anwendung die Möglichkeit erhält, die Nachrichten in der Hauptnachrichten Schleife zu filtern. Wenn eine Anwendung eine " **WH \_ msgfilter** "-oder " **WH \_ sysmsgfilter** "-Hook-Prozedur installiert, ruft das System die Prozedur während der modalen Schleife auf.

Eine Anwendung kann den " **WH \_ msgfilter** "-Hook direkt aufrufen, indem Sie die [**callmsgfilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) -Funktion aufruft. Mit dieser Funktion kann die Anwendung denselben Code zum Filtern von Nachrichten in modalen Schleifen verwenden, wie Sie in der Hauptnachrichten Schleife verwendet wird. Kapseln Sie hierzu die Filter Vorgänge in einer **WH \_ msgfilter** -Hook-Prozedur, und rufen Sie **callmsgfilter** zwischen den Aufrufen der Funktionen [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) und [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) auf.

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

Das letzte Argument von [**callmsgfilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) wird einfach an die Hook-Prozedur übermittelt. Sie können einen beliebigen Wert eingeben. Die Hook-Prozedur kann durch Definieren einer Konstanten wie **MSGF \_ mainloop** diesen Wert verwenden, um zu bestimmen, wo die Prozedur von aufgerufen wurde.

Weitere Informationen finden Sie unter den " [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) "-und " [*sysmsgproc*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85)) "-Rückruf Funktionen.

### <a name="wh_shell"></a>WH- \_ Shell

Eine Shellanwendung kann mit dem **WH- \_ ShellHook** wichtige Benachrichtigungen erhalten. Das System ruft eine **WH- \_ ShellHook** -Prozedur auf, wenn die Shellanwendung aktiviert wird und wenn ein Fenster der obersten Ebene erstellt oder zerstört wird.

Beachten Sie, dass benutzerdefinierte Shellanwendungen keine **WH- \_ shellnachrichten** empfangen. Daher muss jede Anwendung, die sich selbst als Standardshell registriert, die [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion aufrufen, bevor Sie (oder eine andere Anwendung) **WH- \_ Shell** -Nachrichten empfangen kann. Diese Funktion muss mit **SPI \_ setminimizedmetrics** und einer [**minimizedmetrics**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) -Struktur aufgerufen werden. Legen Sie den **iarrange** -Member dieser Struktur auf **ARW \_ Hide** fest.

Weitere Informationen finden Sie unter [*shellproc*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) -Rückruffunktion.

 

 
