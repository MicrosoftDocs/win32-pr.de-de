---
title: Was ist ein Fenster?
description: Was ist ein Fenster?
ms.assetid: eef5e139-91f9-4d8b-9153-e178d7416d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0af5d845d1a7eac6474dec9da08dcfde8df9f9fd67bf16d6f59cad94c5af0fe2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631440"
---
# <a name="what-is-a-window"></a>Was ist ein Fenster?

## <a name="what-is-a-window"></a>Was ist ein Fenster?

Offensichtlich sind Fenster für die Windows. Sie sind so wichtig, dass sie das Betriebssystem nach ihnen benannt haben. Aber was ist ein Fenster? Wenn Sie an ein Fenster denken, stellen Sie sich wahrscheinlich etwas wie das hier dargestellte vor:

![Screenshot eines Anwendungsfensters](images/window01.png)

Dieser Fenstertyp wird als *Anwendungsfenster oder* *Hauptfenster bezeichnet.* Sie verfügt in der Regel über einen Frame mit einer Titelleiste, Schaltflächen **zum** Minimieren und **Maximieren** und anderen Standardelementen der Benutzeroberfläche. Der Frame wird als *Nicht-Clientbereich* des Fensters bezeichnet, der so genannt wird, da das Betriebssystem diesen Teil des Fensters verwaltet. Der Bereich innerhalb des Frames ist der *Clientbereich*. Dies ist der Teil des Fensters, der von Ihrem Programm verwaltet wird.

Hier ist ein weiterer Fenstertyp:

![Screenshot eines Steuerelementfensters](images/window02.png)

Wenn Sie noch nicht mit Windows arbeiten, ist es vielleicht überraschend, dass Benutzeroberflächensteuerelemente wie Schaltflächen und Bearbeitungsfelder selbst Fenster sind. Der Hauptunterschied zwischen einem Ui-Steuerelement und einem Anwendungsfenster ist, dass ein Steuerelement allein nicht vorhanden ist. Stattdessen wird das Steuerelement relativ zum Anwendungsfenster positioniert. Wenn Sie das Anwendungsfenster ziehen, wird das Steuerelement wie erwartet damit bewegt. Außerdem können das Steuerelement und das Anwendungsfenster miteinander kommunizieren. (Beispielsweise empfängt das Anwendungsfenster Klickbenachrichtigungen von einer Schaltfläche.)

Denken Sie daher im Fenster *nicht* einfach an das *Anwendungsfenster*. Stellen Sie sich stattdessen ein Fenster als Programmierkonstrukt vor, das:

-   Nimmt einen bestimmten Teil des Bildschirms ein.
-   Kann zu einem bestimmten Zeitpunkt sichtbar sein oder nicht.
-   Weiß, wie man sich selbst zeichnen kann.
-   Reagiert auf Ereignisse des Benutzers oder des Betriebssystems.

## <a name="parent-windows-and-owner-windows"></a>Übergeordnete Windows und Besitzer Windows

Im Fall eines Ui-Steuerelements wird das Steuerelementfenster als *untergeordnetes* Steuerelement des Anwendungsfensters bezeichnet. Das Anwendungsfenster ist das *übergeordnete Element* des Steuerelementfensters. Im übergeordneten Fenster wird das Koordinatensystem für die Positionierung eines untergeordneten Fensters angezeigt. Ein übergeordnetes Fenster wirkt sich auf Aspekte der Darstellung eines Fensters aus. Beispielsweise wird ein untergeordnetes Fenster abgeschnitten, sodass kein Teil des untergeordneten Fensters außerhalb der Rahmen des übergeordneten Fensters angezeigt werden kann.

Eine weitere Beziehung ist die Beziehung zwischen einem Anwendungsfenster und einem modalen Dialogfenster. Wenn eine Anwendung ein modales Dialogfeld anzeigt, ist das Anwendungsfenster *das* Besitzerfenster, und das Dialogfeld ist ein Fenster *im Besitz.* Ein Fenster im Besitz wird immer vor dem Besitzerfenster angezeigt. Sie wird ausgeblendet, wenn der Besitzer minimiert und gleichzeitig als Besitzer zerstört wird.

Die folgende Abbildung zeigt eine Anwendung, die ein Dialogfeld mit zwei Schaltflächen anzeigt:

![Screenshot einer Anwendung mit einem Dialogfeld](images/window03.png)

Das Anwendungsfenster besitzt das Dialogfeld, und das Dialogfeld ist das übergeordnete Element beider Schaltflächenfenster. Das folgende Diagramm zeigt diese Beziehungen:

![Abbildung mit Über-/Unter- und Besitzer-/Besitzerbeziehungen](images/window04.png)

## <a name="window-handles"></a>Fensterhandles

Windows sind Objekte – sie verfügen sowohl über Code als auch über Daten –, aber sie sind keine C++-Klassen. Stattdessen verweist ein Programm mithilfe eines Werts, der als Handle bezeichnet wird, auf ein *Fenster.* Ein Handle ist ein nicht transparenter Typ. Im Wesentlichen ist es nur eine Zahl, die das Betriebssystem verwendet, um ein Objekt zu identifizieren. Sie können sich Windows, dass sie eine große Tabelle aller erstellten Fenster haben. Sie verwendet diese Tabelle, um Fenster nach ihren Handles zu suchen. (Ob dies intern genau so funktioniert, ist nicht wichtig.) Der Datentyp für Fensterhandles ist **HWND,** was in der Regel als "aitch-wind" ausgesprochen wird. Fensterhandles werden von den Funktionen zurückgegeben, die Fenster erstellen: [**CreateWindow**](/windows/desktop/DirectShow/cbasewindow-docreatewindow) und [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)

Um einen Vorgang für ein Fenster durchzuführen, rufen Sie in der Regel eine Funktion auf, die einen **HWND-Wert** als Parameter akzeptiert. Um beispielsweise ein Fenster auf dem Bildschirm neu zu positionieren, rufen Sie die [**MoveWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-movewindow) auf:


```C++
BOOL MoveWindow(HWND hWnd, int X, int Y, int nWidth, int nHeight, BOOL bRepaint);
```



Der erste Parameter ist das Handle für das Fenster, das Sie verschieben möchten. Die anderen Parameter geben die neue Position des Fensters an und geben an, ob das Fenster neu gezeichnet werden soll.

Beachten Sie, dass Handles keine Zeiger sind. Wenn *hwnd eine* Variable ist, die ein Handle enthält, ist der Versuch, das Handle durch Schreiben zu dereferenzieren, `*hwnd` ein Fehler.

## <a name="screen-and-window-coordinates"></a>Bildschirm- und Fensterkoordinaten

Koordinaten werden in geräteunabhängigen Pixeln gemessen. Wir werden mehr über den  geräteunabhängigen Teil der geräteunabhängigen Pixel sagen, *wenn* wir grafiken besprechen.

Je nach Aufgabe können Sie Koordinaten relativ zum Bildschirm, relativ zu einem Fenster (einschließlich des Rahmens) oder relativ zum Clientbereich eines Fensters messen. Beispielsweise würden Sie ein Fenster auf dem Bildschirm mit Bildschirmkoordinaten positionieren, aber Sie würden in einem Fenster mithilfe von Clientkoordinaten zeichnen. In jedem Fall ist der Ursprung (0, 0) immer die linke obere Ecke der Region.

![Abbildung mit Bildschirm-, Fenster- und Clientkoordinaten](images/coordinates01.png)

## <a name="next"></a>Nächste

[WinMain: Der Anwendungseinstiegspunkt](winmain--the-application-entry-point.md)

 

 
