---
title: Was ist ein Fenster?
description: .
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fcbba817e3e4c9059340d0a67c7170f4583270c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390206"
---
# <a name="what-is-a-window"></a>Was ist ein Fenster?

## <a name="what-is-a-window"></a>Was ist ein Fenster?

Natürlich sind Windows für Windows von zentraler Bedeutung. Sie sind so wichtig, dass Sie das Betriebssystem nach der Bezeichnung benannt haben. Was ist ein Fenster? Wenn Sie sich ein Fenster vorstellen, stellen Sie sich wahrscheinlich etwa Folgendes vor:

![Screenshot eines Anwendungsfensters](images/window01.png)

Dieser Fenstertyp wird als *Anwendungsfenster* oder *Hauptfenster* bezeichnet. Sie verfügt in der Regel über einen Frame mit einer Titelleiste, **minimieren** und **Maxi** mieren von Schaltflächen und anderen Standardbenutzer Oberflächenelementen. Der Frame wird als *nicht-Client Bereich* des Fensters bezeichnet und wird daher aufgerufen, da das Betriebssystem diesen Teil des Fensters verwaltet. Der Bereich innerhalb des Frames ist der *Client Bereich*. Dies ist der Teil des Fensters, den das Programm verwaltet.

Im folgenden finden Sie eine weitere Art von Fenster:

![Screenshot eines Steuerelement Fensters](images/window02.png)

Wenn Sie mit der Windows-Programmierung noch nicht vertraut sind, können Sie überraschen, dass UI-Steuerelemente wie Schaltflächen und Bearbeitungsfelder selbst Fenster sind. Der Hauptunterschied zwischen einem UI-Steuerelement und einem Anwendungsfenster besteht darin, dass ein Steuerelement nicht allein vorhanden ist. Stattdessen wird das-Steuerelement relativ zum Anwendungsfenster positioniert. Wenn Sie das Anwendungsfenster ziehen, wird das Steuerelement wie erwartet mit dem Steuerelement bewegt. Außerdem können das Steuerelement und das Anwendungsfenster miteinander kommunizieren. (Beispielsweise empfängt das Anwendungsfenster Click-Benachrichtigungen von einer Schaltfläche.)

Wenn Sie das *Fenster* betrachten, sollten Sie sich daher nicht einfach über das *Anwendungsfenster* in Gedanken machen. Betrachten Sie stattdessen ein Fenster als Programmierkonstrukt, das Folgendes:

-   Belegt einen bestimmten Teil des Bildschirms.
-   Kann zu einem bestimmten Zeitpunkt sichtbar sein oder nicht.
-   Weiß, wie sich selbst gezeichnet werden kann.
-   Reagiert auf Ereignisse vom Benutzer oder vom Betriebssystem.

## <a name="parent-windows-and-owner-windows"></a>Übergeordnete Fenster und Besitzer Fenster

Im Fall eines UI-Steuer Elements wird das Steuerelement Fenster als untergeordnetes Element *des Anwendungs* Fensters bezeichnet. Das Anwendungsfenster ist das über *geordnete* Element des Steuerelement Fensters. Das übergeordnete Fenster stellt das Koordinatensystem bereit, das zum Positionieren eines untergeordneten Fensters verwendet wird. Ein übergeordnetes Fenster wirkt sich auf Aspekte der Darstellung eines Fensters aus. Beispielsweise wird ein untergeordnetes Fenster abgeschnitten, sodass kein Teil des untergeordneten Fensters außerhalb der Grenzen des übergeordneten Fensters angezeigt werden kann.

Eine andere Beziehung ist die Beziehung zwischen einem Anwendungsfenster und einem modalen Dialogfeld Fenster. Wenn eine Anwendung ein modales Dialogfeld anzeigt, ist das Anwendungsfenster das *Besitzer* Fenster, und das Dialogfeld ist ein *eigenes* Fenster. Ein eigenes Fenster wird immer vor dem Besitzer Fenster angezeigt. Er ist ausgeblendet, wenn der Besitzer minimiert wird, und wird zur gleichen Zeit wie der Besitzer zerstört.

Die folgende Abbildung zeigt eine Anwendung, die ein Dialogfeld mit zwei Schaltflächen anzeigt:

![Screenshot einer Anwendung mit einem Dialogfeld](images/window03.png)

Das Fenster Anwendung ist im Besitz des Dialog Felds, und das Dialogfeld Fenster ist das übergeordnete Fenster der beiden Schaltflächen Fenster. Im folgenden Diagramm werden die folgenden Beziehungen veranschaulicht:

![Abbildung der Beziehungen zwischen über-und untergeordneten Elementen und Besitzer/Besitz](images/window04.png)

## <a name="window-handles"></a>Fenster Handles

Windows sind Objekte – Sie haben sowohl Code als auch Daten – sind jedoch keine C++-Klassen. Stattdessen verweist ein Programm mit einem Wert, der als *handle* bezeichnet wird, auf ein Fenster. Ein Handle ist ein nicht transparenter Typ. Im Wesentlichen ist es nur eine Zahl, die das Betriebssystem zum Identifizieren eines Objekts verwendet. Sie können Windows sehen, dass eine große Tabelle mit allen erstellten Fenstern vorhanden ist. Diese Tabelle wird verwendet, um Fenster nach Ihren Handles zu suchen. (Unabhängig davon, ob dies intern funktioniert, ist es nicht wichtig.) Der Datentyp für Fenster Handles ist **HWND**, was normalerweise als "aitch-Wind" bezeichnet wird. Fenster Handles werden von den Funktionen zurückgegeben, mit denen Windows: Erstellungs [**Fenster**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) und " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" erstellt werden.

Um einen Vorgang für ein Fenster auszuführen, wird in der Regel eine Funktion aufgerufen, die einen **HWND** -Wert als Parameter annimmt. Um z. b. ein Fenster auf dem Bildschirm neu zu positionieren, müssen Sie die Funktion "Report [**Window**](/windows/desktop/api/winuser/nf-winuser-movewindow) " (


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



Der erste Parameter ist das Handle für das Fenster, das Sie verschieben möchten. Die anderen Parameter geben den neuen Speicherort des Fensters an und geben an, ob das Fenster neu gezeichnet werden soll.

Beachten Sie, dass Handles keine Zeiger sind. Wenn *HWND* eine Variable ist, die ein Handle enthält, ist der Versuch, das Handle durch Schreiben zu dereferenzieren, `*hwnd` ein Fehler.

## <a name="screen-and-window-coordinates"></a>Bildschirm-und Fenster Koordinaten

Koordinaten werden in geräteunabhängigen Pixeln gemessen. Bei der Erörterung von Grafiken werden wir mehr über den *geräteunabhängigen* Teil von *geräteunabhängigen Pixeln* erfahren.

Abhängig von ihrer Aufgabe können Sie Koordinaten relativ zum Bildschirm, relativ zu einem Fenster (einschließlich des Frames) oder relativ zum Client Bereich eines Fensters messen. Beispielsweise würden Sie ein Fenster auf dem Bildschirm mithilfe von Bildschirm Koordinaten positionieren, aber Sie würden in einem Fenster mithilfe von Client Koordinaten zeichnen. In jedem Fall ist der Ursprung (0,0) immer die linke obere Ecke des Bereichs.

![Darstellung der Bildschirm-, Fenster-und Client Koordinaten](images/coordinates01.png)

## <a name="next"></a>Nächste

[WinMain: der Einstiegspunkt der Anwendung](winmain--the-application-entry-point.md)

 

 