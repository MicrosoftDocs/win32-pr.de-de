---
title: Fenstermeldungen (Los geht's mit Win32 und C++)
description: Fenstermeldungen (Los geht's mit Win32 und C++)
ms.assetid: 90c20456-44ed-4f0f-a6d3-b6c5660f0bc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00da564396e0f95947e33fb7d8db8b217ac5cdf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103838"
---
# <a name="window-messages-get-started-with-win32-and-c"></a>Fenstermeldungen (Los geht's mit Win32 und C++)

Eine GUI-Anwendung muss auf Ereignisse des Benutzers und des Betriebssystems reagieren.

- **Zu den Ereignissen des Benutzers** gehören alle Möglichkeiten, wie jemand mit Ihrem Programm interagieren kann: Mausklicks, Tastenstriche, Gesten auf dem Touchscreen usw.
- **Ereignisse aus dem Betriebssystem** enthalten etwas "außerhalb" des Programms, das sich auf das Verhalten des Programms auswirken kann. Beispielsweise kann der Benutzer ein neues Hardwaregerät anschließen oder Windows in einen Energiesparmodus (Energiesparmodus oder Ruhezustand) versetzt werden.

Diese Ereignisse können jederzeit während der Ausführung des Programms in nahezu beliebiger Reihenfolge auftreten. Wie strukturieren Sie ein Programm, dessen Ausführungsablauf nicht im Voraus vorhergesagt werden kann?

Windows verwendet ein Nachrichtenübergabemodell, um dieses Problem zu lösen. Das Betriebssystem kommuniziert mit Ihrem Anwendungsfenster, indem es Nachrichten an das Fenster übergibt. Eine Nachricht ist einfach ein numerischer Code, der ein bestimmtes Ereignis kennzeichnet. Wenn der Benutzer beispielsweise die linke Maustaste drückt, empfängt das Fenster eine Meldung mit dem folgenden Meldungscode.

```C++
#define WM_LBUTTONDOWN    0x0201
```

Einigen Nachrichten sind Daten zugeordnet. Beispielsweise enthält die [**\_ WM-LBUTTONDOWN-Nachricht**](/windows/desktop/inputdev/wm-lbuttondown) die x-Koordinate und die y-Koordinate des Mauscursors.

Um eine Meldung an ein Fenster zu übergeben, ruft das Betriebssystem die für dieses Fenster registrierte Fensterprozedur auf. (Und jetzt wissen Sie, wofür die Fensterprozedur vorgesehen ist.)

## <a name="the-message-loop"></a>Nachrichtenschleife

Eine Anwendung empfängt Tausende von Nachrichten, während sie ausgeführt wird. (Beachten Sie, dass bei jeder Tastatureingabe und jedem Mausklick eine Meldung generiert wird.) Darüber hinaus kann eine Anwendung über mehrere Fenster verfügen, die jeweils über eine eigene Fensterprozedur verfügen. Wie empfängt das Programm alle diese Nachrichten und übermittelt sie an die richtige Fensterprozedur? Die Anwendung benötigt eine Schleife, um die Nachrichten abzurufen und an die richtigen Fenster zu senden.

Für jeden Thread, der ein Fenster erstellt, erstellt das Betriebssystem eine Warteschlange für Fenstermeldungen. Diese Warteschlange enthält Nachrichten für alle Fenster, die in diesem Thread erstellt werden. Die Warteschlange selbst wird im Programm ausgeblendet. Sie können die Warteschlange nicht direkt bearbeiten. Sie können jedoch eine Nachricht aus der Warteschlange pullen, indem Sie die [**GetMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-getmessage) aufrufen.

```C++
MSG msg;
GetMessage(&msg, NULL, 0, 0);
```

Diese Funktion entfernt die erste Nachricht vom Anfang der Warteschlange. Wenn die Warteschlange leer ist, blockiert die Funktion, bis eine andere Nachricht in die Warteschlange gestellt wird. Die Tatsache, dass [**GetMessage-Blöcke**](/windows/desktop/api/winuser/nf-winuser-getmessage) ihr Programm nicht reagieren lassen. Wenn keine Nachrichten enthalten sind, muss das Programm nichts tun. Wenn Sie eine Hintergrundverarbeitung durchführen müssen, können Sie zusätzliche Threads erstellen, die weiterhin ausgeführt werden, während **GetMessage** auf eine andere Nachricht wartet. (Weitere Informationen [finden Sie unter Vermeiden von Engpässen in der Fensterprozedur.)](writing-the-window-procedure.md)

Der erste Parameter von [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) ist die Adresse einer [**MSG-Struktur.**](/windows/win32/api/winuser/ns-winuser-msg) Wenn die Funktion erfolgreich ist, füllt sie die **MSG-Struktur** mit Informationen zur Nachricht auf. Dies schließt das Zielfenster und den Meldungscode ein. Mit den anderen drei Parametern können Sie filtern, welche Nachrichten Sie aus der Warteschlange erhalten. In fast allen Fällen legen Sie diese Parameter auf 0 (null) fest.

Obwohl die [**MSG-Struktur**](/windows/win32/api/winuser/ns-winuser-msg) Informationen über die Nachricht enthält, werden Sie diese Struktur fast nie direkt untersuchen. Stattdessen übergeben Sie es direkt an zwei andere Funktionen.

```C++
TranslateMessage(&msg); 
DispatchMessage(&msg);
```

Die [**TranslateMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-translatemessage) bezieht sich auf Tastatureingaben. Tastatureingaben (Nach unten, Schlüssel nach oben) werden in Zeichen übersetzt. Sie müssen nicht wirklich wissen, wie diese Funktion funktioniert. Denken Sie daran, sie vor [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)aufzurufen. Der Link zur MSDN-Dokumentation enthält weitere Informationen, wenn Sie interessiert sind.

Die [**DispatchMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) weist das Betriebssystem an, die Fensterprozedur des Fensters aufzurufen, das das Ziel der Nachricht ist. Anders ausgedrückt: Das Betriebssystem sucht das Fensterhandle in seiner Fenstertabelle, sucht den Funktionszeiger, der dem Fenster zugeordnet ist, und ruft die Funktion auf.

Angenommen, der Benutzer drückt die linke Maustaste. Dies führt zu einer Kette von Ereignissen:

1. Das Betriebssystem fügt eine [**\_ WM-LBUTTONDOWN-Nachricht**](/windows/desktop/inputdev/wm-lbuttondown) in die Nachrichtenwarteschlange ein.
2. Ihr Programm ruft die [**GetMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-getmessage) auf.
3. [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) pullt die [**\_ WM-LBUTTONDOWN-Nachricht**](/windows/desktop/inputdev/wm-lbuttondown) aus der Warteschlange und füllt die [**MSG-Struktur**](/windows/win32/api/winuser/ns-winuser-msg) aus.
4. Ihr Programm ruft die Funktionen [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) und [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) auf.
5. In [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)ruft das Betriebssystem Die Fensterprozedur auf.
6. Ihre Fensterprozedur kann entweder auf die Nachricht reagieren oder sie ignorieren.

Wenn die Fensterprozedur zurückgegeben wird, kehrt sie zurück zu [**DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) Dadurch wird die Meldungsschleife für die nächste Nachricht zurückgegeben. Solange Ihr Programm ausgeführt wird, werden nachrichten weiterhin in der Warteschlange eintreffen. Daher benötigen Sie eine Schleife, die kontinuierlich Nachrichten aus der Warteschlange abruft und verteilt. Sie können sich die Schleife wie folgt vorstellen:

```C++
// WARNING: Don't actually write your loop this way.

while (1)      
{
    GetMessage(&msg, NULL, 0,  0);
    TranslateMessage(&msg); 
    DispatchMessage(&msg);
}
```

Wie geschrieben, würde diese Schleife natürlich nie enden. Hier kommt der Rückgabewert für die [**GetMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-getmessage) ein. Normalerweise gibt **GetMessage** einen Wert ungleich 0 (null) zurück. Wenn Sie die Anwendung beenden und die Nachrichtenschleife verlassen möchten, rufen Sie die [**PostQuitMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) auf.

```C++
        PostQuitMessage(0);
```

Die [**PostQuitMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) setzt eine [**WM \_ QUIT-Nachricht**](/windows/desktop/winmsg/wm-quit) in die Nachrichtenwarteschlange. **WM \_ QUIT** ist eine spezielle Nachricht: Dies bewirkt, dass [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 0 (null) zurück gibt und das Ende der Nachrichtenschleife signalisiert. Hier ist die überarbeitete Meldungsschleife.

```C++
// Correct.

MSG msg = { };
while (GetMessage(&msg, NULL, 0, 0) > 0)
{
    TranslateMessage(&msg);
    DispatchMessage(&msg);
}
```

Solange [**GetMessage einen**](/windows/desktop/api/winuser/nf-winuser-getmessage) Wert ungleich 0 (null) zurückgibt, wird der Ausdruck in der **while-Schleife** als true ausgewertet. Nachdem Sie [**PostQuitMessage aufrufen,**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)wird der Ausdruck false, und das Programm bricht aus der Schleife aus. (Ein interessantes Ergebnis dieses Verhaltens ist, dass Ihre Fensterprozedur nie eine [**WM \_ QUIT-Nachricht**](/windows/desktop/winmsg/wm-quit) empfängt. Daher benötigen Sie keine Case-Anweisung für diese Meldung in Ihrer Fensterprozedur.)

Die nächste offensichtliche Frage ist, wann [**PostQuitMessage aufruft werden soll.**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) Wir kehren zu dieser Frage im Thema [Schließen](closing-the-window.md)des Fensters zurück, aber zuerst müssen wir unsere Fensterprozedur schreiben.

## <a name="posted-messages-versus-sent-messages"></a>Gesendete Nachrichten im Vergleich zu gesendeten Nachrichten

Im vorherigen Abschnitt wurde erläutert, wie Nachrichten in eine Warteschlange gestellt werden. Manchmal wird vom Betriebssystem eine Fensterprozedur direkt aufrufen, um die Warteschlange zu umgehen.

Die Terminologie für diese Unterscheidung kann verwirrend sein:

-   *Das* Posten einer Nachricht bedeutet, dass die Nachricht in die Nachrichtenwarteschlange über die Nachrichtenschleife [**(GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) und [**DispatchMessage) gesendet wird.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)
-   *Das* Senden einer Nachricht bedeutet, dass die Nachricht die Warteschlange überspringt und das Betriebssystem die Fensterprozedur direkt aufruft.

Im Moment ist der Unterschied nicht sehr wichtig. Die Fensterprozedur verarbeitet alle Meldungen. Einige Nachrichten umgehen jedoch die Warteschlange und wechseln direkt zu Ihrer Fensterprozedur. Es kann jedoch einen Unterschied machen, wenn Ihre Anwendung zwischen Fenstern kommuniziert. Eine ausführlichere Erläuterung dieses Problems finden Sie im Thema [Informationen zu Nachrichten und Nachrichtenwarteschlangen.](/windows/desktop/winmsg/about-messages-and-message-queues)

## <a name="next"></a>Nächste

[Schreiben der Fensterprozedur](writing-the-window-procedure.md)
