---
title: Fenster Meldungen (beginnen Sie mit Win32 und C++)
description: .
ms.assetid: 90c20456-44ed-4f0f-a6d3-b6c5660f0bc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7ea533a89cb0ccf7053945cd693cc6e1ef5c28
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "106353240"
---
# <a name="window-messages-get-started-with-win32-and-c"></a>Fenster Meldungen (beginnen Sie mit Win32 und C++)

Eine GUI-Anwendung muss auf Ereignisse vom Benutzer und vom Betriebssystem Antworten.

- **Ereignisse des Benutzers** umfassen alle Möglichkeiten, mit denen jemand mit Ihrem Programm interagieren kann: Mausklicks, Tastatureingaben, Mausklicks und so weiter.
- Zu den **Ereignissen des Betriebssystems** gehören alle Elemente, die sich auf das Verhalten des Programms auswirken können. Der Benutzer kann z. b. ein neues Hardware Gerät einbinden, oder Windows könnte einen niedrigeren Energiezustand (Standbymodus oder Ruhezustand) eingeben.

Diese Ereignisse können jederzeit während der Ausführung des Programms in nahezu beliebiger Reihenfolge auftreten. Wie Strukturieren Sie ein Programm, dessen Ausführungs Verlauf nicht im Voraus vorhergesagt werden kann?

Um dieses Problem zu beheben, verwendet Windows ein Nachrichten Übergabe Modell. Das Betriebssystem kommuniziert mit Ihrem Anwendungsfenster, indem Nachrichten an das Betriebssystem übergeben werden. Eine Nachricht ist einfach ein numerischer Code, der ein bestimmtes Ereignis festlegt. Wenn der Benutzer z. b. die linke Maustaste drückt, empfängt das Fenster eine Meldung mit dem folgenden Meldungs Code.

```C++
#define WM_LBUTTONDOWN    0x0201
```

Einigen Nachrichten sind Daten zugeordnet. Die [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Nachricht enthält z. b. die x-Koordinate und die y-Koordinate des Mauszeigers.

Um eine Nachricht an ein Fenster zu übergeben, ruft das Betriebssystem die für dieses Fenster Registrierte Fenster Prozedur auf. (Und nun wissen Sie, wofür die Fenster Prozedur vorgesehen ist.)

## <a name="the-message-loop"></a>Nachrichtenschleife

Eine Anwendung empfängt während der Ausführung Tausende von Nachrichten. (Beachten Sie, dass alle Tastatureingaben und Mausklicks eine Meldung generieren.) Außerdem kann eine Anwendung über mehrere Fenster verfügen, von denen jede über eine eigene Fenster Prozedur verfügt. Wie empfängt das Programm alle diese Nachrichten und übermitteln diese an die richtige Fenster Prozedur? Die Anwendung benötigt eine-Schleife, um die Nachrichten abzurufen und Sie an die richtigen Fenster zu verteilen.

Für jeden Thread, der ein Fenster erstellt, erstellt das Betriebssystem eine Warteschlange für Fenster Meldungen. Diese Warteschlange enthält Nachrichten für alle Fenster, die auf diesem Thread erstellt werden. Die Warteschlange selbst ist im Programm ausgeblendet. Die Warteschlange kann nicht direkt bearbeitet werden. Sie können jedoch eine Nachricht aus der Warteschlange abrufen, indem Sie die [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) -Funktion aufrufen.

```C++
MSG msg;
GetMessage(&msg, NULL, 0, 0);
```

Diese Funktion entfernt die erste Meldung von der Spitze der Warteschlange. Wenn die Warteschlange leer ist, wird die Funktion blockiert, bis eine andere Nachricht in die Warteschlange gestellt wird. Die Tatsache, dass [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) -Blöcke das Programm nicht reaktionsfähig machen. Wenn keine Nachrichten vorhanden sind, muss das Programm nichts tun. Wenn Sie die Hintergrundverarbeitung durchführen müssen, können Sie zusätzliche Threads erstellen, die weiterhin ausgeführt werden, während **GetMessage** auf eine andere Nachricht wartet. (Weitere Informationen finden [Sie unter Vermeiden von Engpässen in der Fenster Prozedur](writing-the-window-procedure.md).)

Der erste Parameter von [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ist die Adresse einer [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur. Wenn die Funktion erfolgreich ausgeführt wird, füllt Sie die **msg** -Struktur mit Informationen über die Meldung aus. Dies schließt das Zielfenster und den Nachrichten Code ein. Mit den anderen drei Parametern können Sie filtern, welche Nachrichten Sie aus der Warteschlange erhalten. In fast allen Fällen legen Sie diese Parameter auf 0 (null) fest.

Obwohl die [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Strukturinformationen über die Nachricht enthält, wird diese Struktur fast niemals direkt untersucht. Stattdessen übergeben Sie Sie direkt an zwei andere Funktionen.

```C++
TranslateMessage(&msg); 
DispatchMessage(&msg);
```

Die [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) -Funktion bezieht sich auf Tastatureingaben. Tastatureingaben (Key Down, Key up) werden in Zeichen übersetzt. Sie müssen nicht unbedingt wissen, wie diese Funktion funktioniert. Denken Sie nur daran, Sie vor [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)aufzurufen. Über den Link zur MSDN-Dokumentation erhalten Sie weitere Informationen, wenn Sie neugierig sind.

Die [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) -Funktion weist das Betriebssystem an, die Fenster Prozedur des Fensters aufzurufen, das das Ziel der Nachricht ist. Anders ausgedrückt: das Betriebssystem sucht das Fenster Handle in seiner Fenster Tabelle, sucht den dem Fenster zugeordneten Funktionszeiger und ruft die-Funktion auf.

Nehmen wir beispielsweise an, dass der Benutzer die linke Maustaste drückt. Dies verursacht eine Ereigniskette:

1. Das Betriebssystem stellt eine [**WM- \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Meldung in der Nachrichten Warteschlange.
2. Das Programm ruft die [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) -Funktion auf.
3. [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) Ruft die [**WM- \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Nachricht aus der Warteschlange ab und füllt die [**msg**](/windows/win32/api/winuser/ns-winuser-msg) -Struktur aus.
4. Das Programm ruft die Funktionen [**translatemess**](/windows/desktop/api/winuser/nf-winuser-translatemessage) und [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) auf.
5. Innerhalb von [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)Ruft das Betriebssystem die Fenster Prozedur auf.
6. Die Fenster Prozedur kann entweder auf die Nachricht reagieren oder Sie ignorieren.

Wenn die Fenster Prozedur zurückgegeben wird, kehrt sie zurück zu [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). Dadurch wird die Nachrichten Schleife für die nächste Nachricht zurückgegeben. Solange das Programm ausgeführt wird, werden Nachrichten weiterhin in der Warteschlange eintreffen. Daher müssen Sie über eine-Schleife verfügen, die kontinuierlich Nachrichten aus der Warteschlange abruft und diese sendet. Sie können sich die Schleife wie folgt vorstellen:

```C++
// WARNING: Don't actually write your loop this way.

while (1)      
{
    GetMessage(&msg, NULL, 0,  0);
    TranslateMessage(&msg); 
    DispatchMessage(&msg);
}
```

Wie bereits geschrieben, würde diese Schleife natürlich nie enden. An dieser Stelle kommt der Rückgabewert für die [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) -Funktion ins Spiel. In der Regel gibt **GetMessage** einen Wert ungleich 0 (null) zurück. Wenn Sie die Anwendung beenden und die Nachrichten Schleife abbrechen möchten, können Sie die [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) -Funktion aufzurufen.

```C++
        PostQuitMessage(0);
```

Die [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) -Funktion fügt eine WM-Beendungs Meldung in die Nachrichten Warteschlange ein. [**\_**](/windows/desktop/winmsg/wm-quit) **WM \_ "Quit** " ist eine spezielle Meldung: " [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) " gibt NULL zurück und signalisiert das Ende der Nachrichten Schleife. Hier ist die überarbeitete Nachrichten Schleife.

```C++
// Correct.

MSG msg = { };
while (GetMessage(&msg, NULL, 0, 0) > 0)
{
    TranslateMessage(&msg);
    DispatchMessage(&msg);
}
```

Solange [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) einen Wert ungleich 0 (null) zurückgibt, wird der Ausdruck in der **while** -Schleife als true ausgewertet. Nachdem Sie [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)aufgerufen haben, wird der Ausdruck "false", und das Programm bricht die Schleife aus. (Ein interessantes Ergebnis dieses Verhaltens besteht darin, dass Ihre Fenster Prozedur nie eine [**WM \_**](/windows/desktop/winmsg/wm-quit) -Beendungs Meldung empfängt. Daher müssen Sie in der Fenster Prozedur keine Case-Anweisung für diese Nachricht enthalten.)

Die nächste offensichtliche Frage ist, wann [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)aufgerufen werden soll. Wir kehren zu dieser Frage im Thema [Schließen des Fensters](closing-the-window.md)zurück, aber zunächst müssen wir unsere Fenster Prozedur schreiben.

## <a name="posted-messages-versus-sent-messages"></a>Im Vergleich zu gesendeten Nachrichten

Im vorherigen Abschnitt wurden Nachrichten in einer Warteschlange gesprochen. Manchmal Ruft das Betriebssystem eine Fenster Prozedur direkt auf, wobei die Warteschlange umgangen wird.

Die Terminologie für diesen Unterschied kann verwirrend sein:

-   Das *veröffentlichen* einer Nachricht bedeutet, dass die Nachricht in die Meldungs Warteschlange übergeht und über die Nachrichten Schleife ([**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) und [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)) weitergeleitet wird.
-   Das *senden* einer Nachricht bedeutet, dass die Nachricht die Warteschlange überspringt und das Betriebssystem die Fenster Prozedur direkt aufruft.

Der Unterschied ist vorerst nicht besonders wichtig. Die Fenster Prozedur verarbeitet alle Nachrichten. Einige Nachrichten umgehen jedoch die Warteschlange und wechseln direkt zu ihrer Fenster Prozedur. Es kann jedoch einen Unterschied machen, wenn Ihre Anwendung zwischen Fenstern kommuniziert. Eine ausführlichere Erörterung dieses Problems finden Sie im Thema [zu Nachrichten und Nachrichten Warteschlangen](/windows/desktop/winmsg/about-messages-and-message-queues).

## <a name="next"></a>Nächste

[Schreiben der Fenster Prozedur](writing-the-window-procedure.md)
