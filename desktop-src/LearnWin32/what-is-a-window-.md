---
title: Was ist ein Fenster?
description: Was ist ein Fenster?
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8494738e3985f78930549f313cb2868b79b34f3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103848"
---
# <a name="what-is-a-window"></a>Was ist ein Fenster?

## <a name="what-is-a-window"></a>Was ist ein Fenster?

Fenster sind für Windows natürlich von zentraler Bedeutung. Sie sind so wichtig, dass sie das Betriebssystem nach ihnen benannt haben. Aber was ist ein Fenster? Wenn Sie an ein Fenster denken, stellen Sie sich wahrscheinlich etwas wie das hier dargestellte vor:

![Screenshot eines Anwendungsfensters](images/window01.png)

Dieser Fenstertyp wird als *Anwendungsfenster oder* *Hauptfenster bezeichnet.* Sie verfügt in der Regel über einen Rahmen mit einer Titelleiste, Schaltflächen **zum** Minimieren und **Maximieren** und anderen Standardelementen der Benutzeroberfläche. Der Frame wird als *Nicht-Clientbereich* des Fensters bezeichnet, der so genannt wird, da das Betriebssystem diesen Teil des Fensters verwaltet. Der Bereich innerhalb des Frames ist der *Clientbereich*. Dies ist der Teil des Fensters, der von Ihrem Programm verwaltet wird.

Hier ist ein weiterer Fenstertyp:

![Screenshot eines Steuerelementfensters](images/window02.png)

Wenn Sie noch nicht mit der Windows-Programmierung arbeiten, ist es vielleicht überraschend, dass Benutzeroberflächensteuerelemente wie Schaltflächen und Bearbeitungsfelder selbst Fenster sind. Der Hauptunterschied zwischen einem Ui-Steuerelement und einem Anwendungsfenster ist, dass ein Steuerelement allein nicht vorhanden ist. Stattdessen wird das Steuerelement relativ zum Anwendungsfenster positioniert. Wenn Sie das Anwendungsfenster ziehen, wird das Steuerelement wie erwartet damit bewegt. Außerdem können das Steuerelement und das Anwendungsfenster miteinander kommunizieren. (Das Anwendungsfenster empfängt beispielsweise Klickbenachrichtigungen von einer Schaltfläche.)

Wenn Sie also *an fenster* denken, denken Sie nicht einfach an das *Anwendungsfenster*. Stellen Sie sich stattdessen ein Fenster als Programmierkonstrukt vor, das:

-   Belegt einen bestimmten Teil des Bildschirms.
-   Kann zu einem bestimmten Zeitpunkt sichtbar sein oder nicht.
-   Weiß, wie man sich selbst zeichnet.
-   Reagiert auf Ereignisse des Benutzers oder des Betriebssystems.

## <a name="parent-windows-and-owner-windows"></a>Übergeordnete Fenster und Besitzerfenster

Im Fall eines Ui-Steuerelements wird das Steuerelementfenster als *untergeordnetes* Element des Anwendungsfensters bezeichnet. Das Anwendungsfenster ist das *übergeordnete* Element des Steuerelementfensters. Das übergeordnete Fenster stellt das Koordinatensystem bereit, das zum Positionieren eines untergeordneten Fensters verwendet wird. Ein übergeordnetes Fenster wirkt sich auf Aspekte der Darstellung eines Fensters aus. Beispielsweise wird ein untergeordnetes Fenster abgeschnitten, sodass kein Teil des untergeordneten Fensters außerhalb der Rahmen des übergeordneten Fensters angezeigt werden kann.

Eine weitere Beziehung ist die Beziehung zwischen einem Anwendungsfenster und einem modalen Dialogfenster. Wenn eine Anwendung ein modales Dialogfeld anzeigt, ist das Anwendungsfenster das *Besitzerfenster,* und das Dialogfeld ist ein *eigenes* Fenster. Ein eigenes Fenster wird immer vor dem Besitzerfenster angezeigt. Sie wird ausgeblendet, wenn der Besitzer minimiert und gleichzeitig mit dem Besitzer zerstört wird.

Die folgende Abbildung zeigt eine Anwendung, die ein Dialogfeld mit zwei Schaltflächen anzeigt:

![Screenshot einer Anwendung mit einem Dialogfeld](images/window03.png)

Das Anwendungsfenster besitzt das Dialogfeldfenster, und das Dialogfeldfenster ist das übergeordnete Fenster beider Schaltflächenfenster. Das folgende Diagramm zeigt diese Beziehungen:

![Abbildung mit über- und untergeordneten Beziehungen und Besitzer-/Besitzerbeziehungen](images/window04.png)

## <a name="window-handles"></a>Fensterhandles

Windows sind Objekte – sie verfügen sowohl über Code als auch über Daten – aber sie sind keine C++-Klassen. Stattdessen verweist ein Programm mithilfe eines Werts, der als Handle bezeichnet wird, auf ein *Fenster.* Ein Handle ist ein nicht transparenter Typ. Im Wesentlichen ist es nur eine Zahl, die das Betriebssystem verwendet, um ein Objekt zu identifizieren. Sie können sich windows als große Tabelle aller erstellten Fenster einbilden. Sie verwendet diese Tabelle, um Fenster nach ihren Handles zu suchen. (Ob dies intern genau so funktioniert, ist nicht wichtig.) Der Datentyp für Fensterhandles ist **HWND,** was in der Regel als "aitch-wind" ausgesprochen wird. Fensterhandles werden von den Funktionen zurückgegeben, die Fenster erstellen: [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) und [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

Um einen Vorgang für ein Fenster durchzuführen, rufen Sie in der Regel eine Funktion auf, die einen **HWND-Wert** als Parameter akzeptiert. Um beispielsweise ein Fenster auf dem Bildschirm neu zu positionieren, rufen Sie die [**MoveWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-movewindow) auf:


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



Der erste Parameter ist das Handle für das Fenster, das Sie verschieben möchten. Die anderen Parameter geben die neue Position des Fensters an und geben an, ob das Fenster neu gezeichnet werden soll.

Beachten Sie, dass Handles keine Zeiger sind. Wenn *hwnd eine* Variable ist, die ein Handle enthält, ist der Versuch, das Handle durch Schreiben zu dereferenzieren, `*hwnd` ein Fehler.

## <a name="screen-and-window-coordinates"></a>Bildschirm- und Fensterkoordinaten

Koordinaten werden in geräteunabhängigen Pixeln gemessen. Wir werden mehr über den  geräteunabhängigen Teil der geräteunabhängigen Pixel sagen, *wenn* wir grafiken besprechen.

Je nach Aufgabe können Sie Koordinaten relativ zum Bildschirm, relativ zu einem Fenster (einschließlich des Rahmens) oder relativ zum Clientbereich eines Fensters messen. Beispielsweise würden Sie ein Fenster mit Bildschirmkoordinaten auf dem Bildschirm positionieren, aber Sie würden in einem Fenster mit Clientkoordinaten zeichnen. In jedem Fall ist der Ursprung (0, 0) immer die linke obere Ecke des Bereichs.

![Abbildung mit Bildschirm-, Fenster- und Clientkoordinaten](images/coordinates01.png)

## <a name="next"></a>Nächste

[WinMain: Der Einstiegspunkt für die Anwendung](winmain--the-application-entry-point.md)

 

 
