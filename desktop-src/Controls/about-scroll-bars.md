---
title: Informationen zu Scrollleisten
description: In einem Fenster kann ein Datenobjekt angezeigt werden, z. B. ein Dokument oder eine Bitmap, das größer als der Clientbereich des Fensters ist.
ms.assetid: 9cb3afad-79ef-4817-950a-c8c1de39401b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93b3088df389753123e2a267ef3bc15eccb1b54626085ee90af7a20978107dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922370"
---
# <a name="about-scroll-bars"></a>Informationen zu Scrollleisten

In einem Fenster kann ein Datenobjekt angezeigt werden, z. B. ein Dokument oder eine Bitmap, das größer als der Clientbereich des Fensters ist. Wenn eine Bildlaufleiste bereitgestellt wird, kann der Benutzer einen Bildlauf für ein Datenobjekt im Clientbereich durchführen, um die Teile des Objekts anzuzeigen, die über die Rahmen des Fensters hinausgehen.

Scrollleisten sollten in jedem Fenster enthalten sein, für das der Inhalt des Clientbereichs über die Rahmen des Fensters hinaus reicht. Die Ausrichtung einer Scrollleiste bestimmt die Richtung, in der der Bildlauf erfolgt, wenn der Benutzer die Scrollleiste verwendet. Eine horizontale Scrollleiste ermöglicht es dem Benutzer, den Inhalt eines Fensters nach links oder rechts zu scrollen. Eine vertikale Scrollleiste ermöglicht es dem Benutzer, den Inhalt nach oben oder unten zu scrollen.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Teile einer Bildlaufleiste](#parts-of-a-scroll-bar)
-   [Standard-Bildlaufleisten und Bildlaufleisten-Steuerelemente](#standard-scroll-bars-and-scroll-bar-controls)
-   [Scrollfeldposition und Bildlaufbereich](#scroll-box-position-and-scrolling-range)
-   [Sichtbarkeit der Scrollleiste](#scroll-bar-visibility)
-   [Scrollleistenanforderungen](#scroll-bar-requests)
-   [Tastaturschnittstelle für eine Bildlaufleiste](#keyboard-interface-for-a-scroll-bar)
-   [Scrollen im Clientbereich](#scrolling-the-client-area)
-   [Scrollleistenfarben und -metriken](#scroll-bar-colors-and-metrics)

## <a name="parts-of-a-scroll-bar"></a>Teile einer Bildlaufleiste

Eine Scrollleiste besteht aus einem schattierten Strich  mit einer Pfeilschaltfläche an jedem Ende und einem Bildlauffeld (manchmal als Strich bezeichnet) zwischen den Pfeilschaltflächen. Eine Scrollleiste stellt die Gesamtlänge oder Breite eines Datenobjekts im Clientbereich eines Fensters dar. Das Bildlauffeld stellt den Teil des -Objekts dar, der im Clientbereich sichtbar ist. Die Position des Bildlauffelds ändert sich, wenn der Benutzer ein Datenobjekt scrollt, um einen anderen Teil davon anzuzeigen. Das System passt auch die Größe des Bildlauffelds einer Scrollleiste so an, dass es angibt, welcher Teil des gesamten Datenobjekts derzeit im Fenster sichtbar ist. Wenn der größte Teil des Objekts sichtbar ist, nimmt das Bildlauffeld den großteil der Bildlaufleisten-Leiste ein. Wenn nur ein kleiner Teil des Objekts sichtbar ist, nimmt das Bildlauffeld einen kleinen Teil der Bildlaufleisten-Leiste ein.

Der Benutzer führt einen Bildlauf im Inhalt eines Fensters durch, indem er auf eine der Pfeilschaltflächen klickt, indem er auf den Bereich in der schattierten Scrollleiste klickt oder indem er das Bildlauffeld zieht. Wenn der Benutzer auf eine Pfeilschaltfläche klickt, scrollt die Anwendung den Inhalt um eine Einheit (in der Regel eine einzelne Zeile oder Spalte). Wenn der Benutzer auf die schattierten Bereiche klickt, scrollt die Anwendung den Inhalt um ein Fenster. Der Umfang des Bildlaufs, der auftritt, wenn der Benutzer das Bildlauffeld zieht, hängt davon ab, wie weit der Benutzer das Bildlauffeld zieht, und vom Bildlaufbereich der Scrollleiste. Weitere Informationen zum Bildlaufbereich finden Sie unter [Scrollfeldposition und Bildlaufbereich](#scroll-box-position-and-scrolling-range).

Der folgende Screenshot zeigt ein umfangreiches Bearbeitungssteuerfeld mit vertikalen und horizontalen Bildlaufleisten, wie sie in Windows Vista angezeigt werden können. Die vertikale Scrollleiste ist derzeit "heiß", da der Mauszeiger darauf zeigt, als der Screenshot aufgenommen wurde.

![Screenshot eines Rich-Edit-Steuerelements mit Scrollleisten](images/sbvista.png)

## <a name="standard-scroll-bars-and-scroll-bar-controls"></a>Standard-Bildlaufleisten und Bildlaufleisten-Steuerelemente

Eine Scrollleiste ist in einem Fenster entweder als Standard-Scrollleiste oder als Bildlaufleisten-Steuerelement enthalten. Eine Standard-Scrollleiste befindet sich im Nicht-Clientbereich eines Fensters. Sie wird mit dem Fenster erstellt und angezeigt, wenn das Fenster angezeigt wird. Der einzige Zweck einer Standard-Scrollleiste besteht in der Möglichkeit, dem Benutzer das Generieren von Scrollanforderungen zum Anzeigen des gesamten Inhalts des Clientbereichs zu ermöglichen. Sie können eine Standardscrollleiste in ein Fenster mit [**WS \_ HSCROLL,**](/windows/desktop/winmsg/window-styles) [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)oder beiden Stilen angeben, wenn Sie das Fenster erstellen. Der **WS \_ HSCROLL-Stil** erstellt eine horizontale Scrollleiste, die am unteren Rand des Clientbereichs positioniert ist. Der **WS \_ VSCROLL-Stil** erstellt eine vertikale Scrollleiste, die rechts vom Clientbereich positioniert ist. Die \_ Systemmetrikwerte SM CXHSCROLL und SM CYHSCROLL definieren die Breite und Höhe einer standardmäßigen \_ horizontalen Scrollleiste. Die Werte SM \_ CXVSCROLL und SM CYVSCROLL definieren die Breite und Höhe einer \_ standardmäßigen vertikalen Scrollleiste. Eine Standard-Scrollleiste ist Teil des zugehörigen Fensters und verfügt daher nicht über ein eigenes Fensterhand handle.

Ein Bildlaufleisten-Steuerelement ist ein Steuerelementfenster, das zur SCROLLBAR-Fensterklasse gehört. Ein Bildlaufleisten-Steuerelement wird angezeigt und funktioniert wie eine Standard-Scrollleiste, aber es ist ein separates Fenster. Als separates Fenster übernimmt ein Bildlaufleisten-Steuerelement den direkten Eingabefokus. Im Gegensatz zu einer Standard-Scrollleiste verfügt ein Bildlaufleisten-Steuerelement auch über eine integrierte Tastaturschnittstelle.

Sie können so viele Bildlaufleisten-Steuerelemente wie erforderlich in einem einzelnen Fenster verwenden. Wenn Sie ein Bildlaufleisten-Steuerelement erstellen, müssen Sie die Größe und Position der Scrollleiste angeben. Wenn jedoch die Größe des Fensters eines Bildlaufleisten-Steuerelements geändert werden kann, müssen Anpassungen an der Größe der Bildlaufleiste vorgenommen werden, wenn sich die Größe des Fensters ändert.

Der Vorteil der Verwendung einer Standard-Scrollleiste ist, dass das System die Scrollleiste erstellt und automatisch ihre Größe und Position fest legt. Standard-Scrollleisten sind jedoch manchmal zu restriktiv. Angenommen, Sie möchten einen Clientbereich in Quadranten unterteilen und einen separaten Satz von Scrollleisten verwenden, um den Inhalt der einzelnen Quadranten zu steuern. Sie können keine Standard-Scrollleisten verwenden, da Sie nur einen Satz von Scrollleisten für ein bestimmtes Fenster erstellen können. Verwenden Sie stattdessen Bildlaufleisten-Steuerelemente, da Sie einem Fenster so viele hinzufügen können, wie Sie möchten.

Anwendungen können Bildlaufleisten-Steuerelemente für andere Zwecke als das Scrollen im Inhalt eines Fensters bereitstellen. Eine Bildschirmschoneranwendung kann z. B. eine Bildlaufleiste bereitstellen, um die Geschwindigkeit zu festlegen, mit der Grafiken auf dem Bildschirm verschoben werden.

Ein Bildlaufleisten-Steuerelement kann über eine Reihe von Stilen verfügen, die zum Steuern der Ausrichtung und Position der Scrollleiste dienen. Sie geben die Stile an, die Sie beim Aufrufen der [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) zum Erstellen eines Bildlaufleisten-Steuerelements verwenden möchten. Einige der Stile erstellen ein Bildlaufleisten-Steuerelement, das eine Standardbreite oder -höhe verwendet. Sie müssen jedoch immer die x- und y-Koordinaten und die anderen Dimensionen der Bildlaufleiste angeben.

Eine Tabelle mit Bildlaufleisten-Steuerelementstilen finden Sie unter [Bildlaufleisten-Steuerelementstile.](scroll-bar-control-styles.md)

> [!Note]  
> Um visuelle Stile mit Bildlaufleisten zu verwenden, muss eine Anwendung ein Manifest enthalten und [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) am Anfang des Programms aufrufen. Informationen zu visuellen Stilen finden Sie unter [Visuelle Stile.](themes-overview.md) Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

 

## <a name="scroll-box-position-and-scrolling-range"></a>Scrollfeldposition und Bildlaufbereich

Die Position des Bildlauffelds wird als ganze Zahl dargestellt. Sie ist relativ zum linken oder oberen Ende der Scrollleiste, je nachdem, ob die Scrollleiste horizontal oder vertikal ist. Die Position muss innerhalb der minimalen und maximalen Werte des Bildlaufbereichs liegen. Beispielsweise befindet sich in einer Scrollleiste mit einem Bereich von 0 bis 100 die Position 50 in der Mitte, und die verbleibenden Positionen werden gleichmäßig entlang der Scrollleiste verteilt. Der anfängliche Bereich hängt von der Scrollleiste ab. Standard-Scrollleisten haben einen anfänglichen Bereich von 0 bis 100; Bildlaufleisten-Steuerelemente verfügen über einen leeren Bereich (mindeste und maximale Werte sind null), es sei denn, Sie geben beim Erstellen des Steuerelements einen expliziten Bereich an. Sie können den Bereich jederzeit ändern. Sie können die [**Funktion SetScrollInfo verwenden,**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) um die Bereichswerte und die [**GetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) zum Abrufen der aktuellen Bereichswerte zu verwenden.

Eine Anwendung passt den Bildlaufbereich in der Regel an praktische ganze Zahlen an, wodurch es einfach ist, die Position des Bildlauffelds in einen Wert zu übersetzen, der dem zu scrollierenden Datenobjekt entspricht. Wenn eine Anwendung beispielsweise 260 Zeilen einer Textdatei in einem Fenster anzeigen muss, in dem nur 16 Zeilen gleichzeitig angezeigt werden können, kann der vertikale Scrollleistenbereich auf 1 bis 244 festgelegt werden. Wenn sich das Bildlauffeld an Position 1 befindet, befindet sich die erste Zeile oben im Fenster. Wenn sich das Bildlauffeld an Position 244 befindet, befindet sich die letzte Zeile (Zeile 260) am unteren Rand des Fensters. Wenn eine Anwendung versucht, einen Positionswert anzugeben, der kleiner als das Minimum oder größer als das Maximum ist, wird stattdessen der minimale oder maximale Bildlaufbereichswert verwendet.

Sie können eine Seitengröße für eine Scrollleiste festlegen. Die *Seitengröße stellt* die Anzahl der Dateneinheiten dar, die in den Clientbereich des Besitzerfensters passen können, wenn die aktuelle Größe angegeben wird. Wenn der Clientbereich beispielsweise 16 Textzeilen enthalten kann, würde eine Anwendung die Seitengröße auf 16 festlegen. Das System verwendet die Seitengröße zusammen mit dem Bildlaufbereich und der Länge der Bildlaufleiste, um die Größe des Bildlauffelds fest zu legen. Wenn die Größe eines Fensters geändert wird, das eine Bildlaufleiste enthält, sollte eine Anwendung die [**Funktion SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) aufrufen, um die Seitengröße fest zu legen. Eine Anwendung kann die aktuelle Seitengröße abrufen, indem sie die [**sendende GetScrollInfo-Funktion**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) aufruft.

Um eine nützliche Beziehung zwischen dem Scrollleistenbereich und dem Datenobjekt zu erstellen, muss eine Anwendung den Bereich jedes Mal anpassen, wenn sich die Größe des Datenobjekts ändert.

Wenn der Benutzer das Bildlauffeld in einer Bildlaufleiste verschiebt, meldet die Scrollleiste die Position des Bildlauffelds als ganze Zahl im Bildlaufbereich. Wenn die Position der Mindestwert ist, befindet sich das Bildlauffeld am oberen Ende einer vertikalen Scrollleiste oder am linken Ende einer horizontalen Scrollleiste. Wenn die Position der Maximalwert ist, befindet sich das Bildlauffeld am unteren Rand einer vertikalen Scrollleiste oder am rechten Ende einer horizontalen Scrollleiste.

Der Maximalwert, den eine Bildlaufleiste melden kann (d. h. die maximale Scrollposition), hängt von der Seitengröße ab. Wenn die Bildlaufleiste eine Seitengröße größer als 1 hat, ist die maximale Bildlaufposition kleiner als der maximale Bereichswert. Sie können die folgende Formel verwenden, um die maximale Scrollposition zu berechnen:


```
MaxScrollPos = MaxRangeValue - (PageSize - 1) 
```



Eine Anwendung muss das Bildlauffeld in einer Scrollleiste verschieben. Obwohl der Benutzer eine Anforderung zum Scrollen in einer Scrollleiste stellt, aktualisiert die Scrollleiste nicht automatisch die Position des Bildlauffelds. Stattdessen wird die Anforderung an das übergeordnete Fenster übergibt, das einen Bildlauf für die Daten durchführen und die Position des Bildlauffelds aktualisieren muss. Eine Anwendung verwendet die [**SetScrollInfo-Funktion,**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) um die Position des Bildlauffelds zu aktualisieren. Andernfalls wird die [**SetScrollPos-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) verwendet. Da sie die Bildlauffeldbewegung steuert, kann die Anwendung das Bildlauffeld in Schritten verschieben, die für die daten, die gescrollt werden, am besten funktionieren.

## <a name="scroll-bar-visibility"></a>Sichtbarkeit der Scrollleiste

Das System blendet eine Standardscrollleiste aus und deaktiviert sie, wenn die gleichen Minimal- und Höchstwerte angegeben sind. Das System blendet auch eine Standard-Scrollleiste aus und deaktiviert sie, wenn Sie eine Seitengröße angeben, die den gesamten Bildlaufbereich der Scrollleiste enthält. Dies ist die Möglichkeit, eine Bildlaufleiste vorübergehend auszublenden, wenn sie für den Inhalt des Clientbereichs nicht benötigt wird. Scrollanforderungen müssen nicht durch die Scrollleiste gestellt werden, wenn sie ausgeblendet ist. Das System aktiviert die Bildlaufleiste und zeigt sie erneut an, wenn Sie die minimalen und maximalen Werte auf ungleiche Werte festlegen und wenn die Seitengröße nicht den gesamten Bildlaufbereich enthält. Die [**ShowScrollBar-Funktion**](/windows/desktop/api/Winuser/nf-winuser-showscrollbar) kann auch verwendet werden, um eine Bildlaufleiste auszublenden oder anzuzeigen. Sie wirkt sich nicht auf den Bereich, die Seitengröße oder die Bildlauffeldposition der Bildlaufleiste aus.

Die [**EnableScrollBar-Funktion**](/windows/desktop/api/Winuser/nf-winuser-enablescrollbar) kann verwendet werden, um einen oder beide Pfeile einer Bildlaufleiste zu deaktivieren. Eine Anwendung zeigt deaktivierte Pfeile grau an und reagiert nicht auf Benutzereingaben.

## <a name="scroll-bar-requests"></a>Scrollleistenanforderungen

Der Benutzer stellt Scrollanforderungen, indem er auf verschiedene Teile einer Scrollleiste klickt. Das System sendet die Anforderung in Form einer [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) an das angegebene Fenster. Eine horizontale Scrollleiste sendet die **WM \_ HSCROLL-Nachricht.** Eine vertikale Scrollleiste sendet die **\_ WM-VSCROLL-Nachricht.** Jede Nachricht enthält einen Anforderungscode, der der Aktion des Benutzers, dem Handle der Scrollleiste (nur Bildlaufleistensteuerelementen) und in einigen Fällen der Position des Bildlauffelds entspricht.

Das folgende Diagramm zeigt den Anforderungscode, den der Benutzer generiert, wenn er auf verschiedene Teile einer Bildlaufleiste klickt.

![Diagramm mit den Anforderungscodes, die den einzelnen Regionen auf zwei Bildlaufleisten zugeordnet sind](images/csscr-02.png)

Die \_ SB-Werte geben die Aktion an, die der Benutzer vornimmt. Eine Anwendung untersucht die Codes, die die [**WM \_ HSCROLL-**](wm-hscroll.md) und [**WM \_ VSCROLL-Nachrichten**](wm-vscroll.md) begleitet, und führt dann den entsprechenden Scrollvorgang aus. In der folgenden Tabelle wird die Aktion des Benutzers für jeden Wert angegeben, gefolgt von der Antwort der Anwendung. In jedem Fall wird eine Einheit von der Anwendung entsprechend den Daten definiert. Die typische Einheit für das vertikale Scrollen von Text ist beispielsweise eine Textzeile.



| Anforderung           | Aktion                                                                               | Antwort                                                                                                                                                                                                                                                                                                                         |
|-------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SB \_ LINEUP        | Der Benutzer klickt auf den oberen Bildlaufpfeil.                                                | Dekrement wird die Position des Bildlauffelds. scrollt um eine Einheit nach oben in den Daten.                                                                                                                                                                                                                                              |
| SB \_ LINEDOWN      | Der Benutzer klickt auf den unteren Bildlaufpfeil.                                             | Erhöht die Position des Bildlauffelds. scrollt um eine Einheit nach unten in den Daten.                                                                                                                                                                                                                                           |
| SB \_ LINELEFT      | Der Benutzer klickt auf den linken Bildlaufpfeil.                                               | Dekrement wird die Position des Bildlauffelds. scrollt um eine Einheit zum linken Ende der Daten.                                                                                                                                                                                                                                         |
| SB \_ LINERIGHT     | Der Benutzer klickt auf den Pfeil nach rechts.                                              | Erhöht die Position des Bildlauffelds. scrollt um eine Einheit zum rechten Ende der Daten.                                                                                                                                                                                                                                        |
| SB \_ PAGEUP        | Der Benutzer klickt auf die Bildlaufleiste oberhalb des Bildlauffelds.                           | Dekrementiert die Bildlauffeldposition um die Anzahl der Dateneinheiten im Fenster. scrollt um die gleiche Anzahl von Einheiten nach oben in den Daten.                                                                                                                                                                                    |
| SB \_ PAGEDOWN      | Der Benutzer klickt auf die Bildlaufleiste unterhalb des Bildlauffelds.                           | Erhöht die Position des Bildlauffelds um die Anzahl der Dateneinheiten im Fenster. führt einen Bildlauf zum unteren Rand der Daten um die gleiche Anzahl von Einheiten durch.                                                                                                                                                                                 |
| SB \_ PAGELEFT      | Der Benutzer klickt links neben dem Bildlauffeld auf die Bildlaufleiste.                  | Dekrementiert die Bildlauffeldposition um die Anzahl der Dateneinheiten im Fenster. führt einen Bildlauf zum linken Ende der Daten um die gleiche Anzahl von Einheiten durch.                                                                                                                                                                               |
| SB \_ PAGERIGHT     | Der Benutzer klickt rechts neben dem Bildlauffeld auf die Bildlaufleiste.                 | Erhöht die Position des Bildlauffelds um die Anzahl der Dateneinheiten im Fenster. führt einen Bildlauf zum rechten Ende der Daten um die gleiche Anzahl von Einheiten durch.                                                                                                                                                                              |
| SB \_ THUMBPOSITION | Der Benutzer gibt das Bildlauffeld nach dem Ziehen frei.                                  | Legt das Bildlauffeld auf die in der Meldung angegebene Position fest. führt einen Bildlauf der Daten um die gleiche Anzahl von Einheiten durch, die das Bildlauffeld verschoben hat.                                                                                                                                                                                             |
| SB \_ THUMBTRACK    | Der Benutzer zieht das Bildlauffeld.                                                       | Legt das Bildlauffeld auf die in der Meldung angegebene Position fest und führt einen Bildlauf der Daten um die gleiche Anzahl von Einheiten durch, die das Bildlauffeld für Anwendungen verschoben hat, die Daten schnell zeichnen. Anwendungen, die daten nicht schnell zeichnen können, müssen auf den SB \_ THUMBPOSITION-Anforderungscode warten, bevor das Bildlauffeld verschoben und die Daten gescrollt werden. |
| SB \_ ENDSCROLL     | Der Benutzer gibt die Maus los, nachdem er ihn auf einem Pfeil oder in der Bildlaufleiste gedrückt gehalten hat. | Es ist keine Antwort erforderlich.                                                                                                                                                                                                                                                                                                           |



 

Eine Scrollleiste generiert SB \_ THUMBPOSITION- und SB \_ THUMBTRACK-Anforderungscode, wenn der Benutzer auf das Scrollfeld klickt und es zieht. Eine Anwendung sollte so programmiert werden, dass sie entweder den SB \_ THUMBTRACK- oder SB \_ THUMBPOSITION-Anforderungscode verarbeitet.

Der SB \_ THUMBPOSITION-Anforderungscode tritt auf, wenn der Benutzer die Maustaste nach dem Klicken auf das Bildlauffeld freigibt. Eine Anwendung, die diese Nachricht verarbeitet, führt den Bildlaufvorgang aus, nachdem der Benutzer das Bildlauffeld an die gewünschte Position gezogen und die Maustaste losgelassen hat.

Der SB \_ THUMBTRACK-Anforderungscode tritt auf, wenn der Benutzer das Scrollfeld zieht. Wenn eine Anwendung SB \_ THUMBTRACK-Anforderungscodes verarbeitet, kann sie den Inhalt eines Fensters scrollen, während der Benutzer das Scrollfeld zieht. Eine Scrollleiste kann jedoch in kurzer Zeit viele SB \_ THUMBTRACK-Anforderungscode generieren, sodass eine Anwendung diese Anforderungscodes nur verarbeiten sollte, wenn der Inhalt des Fensters schnell neu maliert werden kann.

## <a name="keyboard-interface-for-a-scroll-bar"></a>Tastaturschnittstelle für eine Bildlaufleiste

Ein Bildlaufleisten-Steuerelement stellt eine integrierte Tastaturoberfläche bereit, die es dem Benutzer ermöglicht, Scrollanforderungen mithilfe der Tastatur auszugeben. eine Standardbildlaufleiste nicht. Wenn ein Bildlaufleisten-Steuerelement über den Tastaturfokus verfügt, sendet es [**WM \_ HSCROLL-**](wm-hscroll.md) und [**WM \_ VSCROLL-Meldungen**](wm-vscroll.md) an das übergeordnete Fenster, wenn der Benutzer die Pfeiltasten drückt. Der Anforderungscode wird mit jeder Nachricht gesendet, die der Pfeiltaste entspricht, die der Benutzer gedrückt hat. Im Folgenden werden die Pfeiltasten und die entsprechenden Anforderungscodes angezeigt.



| Pfeiltaste | Anforderungscode                  |
|-----------|-------------------------------|
| DOWN      | SB \_ LINEDOWN oder SB \_ LINERIGHT |
| ENDE       | SB \_ BOTTOM                    |
| POS1      | SB \_ TOP                       |
| LEFT      | SB \_ LINEUP oder SB \_ LINELEFT    |
| PGDN      | SB \_ PAGEDOWN oder SB \_ PAGERIGHT |
| PGUP      | SB \_ PAGEUP oder SB \_ PAGELEFT    |
| RIGHT     | SB \_ LINEDOWN oder SB \_ LINERIGHT |
| UP        | SB \_ LINEUP oder SB \_ LINELEFT    |



 

 

> [!Note]  
> Die Tastaturschnittstelle eines Scrollleisten-Steuerelements sendet die \_ SB TOP- und SB \_ BOTTOM-Anforderungscodes. Der SB \_ TOP-Anforderungscode gibt an, dass der Benutzer den oberen Wert des Scrollbereichs erreicht hat. Eine Anwendung führt einen Bildlauf des Fensterinhalts nach unten durch, sodass der obere Rand des Datenobjekts sichtbar ist. Der SB \_ BOTTOM-Anforderungscode gibt an, dass der Benutzer den unteren Wert des Scrollbereichs erreicht hat. Wenn eine Anwendung den SB \_ BOTTOM-Anforderungscode verarbeitet, scrollt sie den Fensterinhalt nach oben, sodass der untere Rand des Datenobjekts sichtbar ist.

 

Wenn Sie eine Tastaturschnittstelle für eine Standard-Scrollleiste wünschen, können Sie eine selbst erstellen, indem Sie die [**WM \_ KEYDOWN-Nachricht**](/windows/desktop/inputdev/wm-keydown) in Ihrer Fensterprozedur verarbeiten und dann die entsprechende Scrollaktion basierend auf dem code mit virtuellen Schlüsseln ausführen, der die Nachricht begleitet. Informationen zum Erstellen einer Tastaturschnittstelle für eine Scrollleiste finden Sie unter [Creating a Keyboard Interface for a Standard Scroll Bar](using-scroll-bars.md).

## <a name="scrolling-the-client-area"></a>Scrollen im Clientbereich

Die einfachste Möglichkeit zum Scrollen des Inhalts eines Clientbereichs besteht darin, ihn zu löschen und dann neu zu zeichnen. Dies ist die Methode, die eine Anwendung wahrscheinlich mit SB \_ PAGEUP-, SB \_ PAGEDOWN- und SB \_ TOP-Anforderungscodes verwendet, die in der Regel völlig neue Inhalte erfordern.

Bei einigen Anforderungscodes wie SB \_ LINEUP und SB \_ LINEDOWN muss nicht der gesamte Inhalt gelöscht werden, da einige nach dem Scrollen sichtbar bleiben. Die [**ScrollWindowEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) behält einen Teil des Inhalts des Clientbereichs bei, verschiebt den beibehaltenen Teil um einen angegebenen Betrag und bereitet dann den Rest des Clientbereichs für das Zeichnen neuer Informationen vor. **ScrollWindowEx** verwendet die [**BitBlt-Funktion,**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) um einen bestimmten Teil des Datenobjekts an einen neuen Speicherort im Clientbereich zu verschieben. Alle ungedeckten Teile des Clientbereichs (alles, was nicht beibehalten wird) werden ungültig, gelöscht und gezeichnet, wenn die nächste [**WM \_ PAINT-Meldung**](/windows/desktop/gdi/wm-paint) auftritt.

Die [**ScrollWindowEx-Funktion**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) kann verwendet werden, um einen Teil des Clientbereichs vom Scrollvorgang auszuschließen. Dadurch wird verhindert, dass Elemente mit festen Positionen, z. B. untergeordnete Fenster, innerhalb des Clientbereichs verschoben werden. Der Teil des Clientbereichs, der die neuen Informationen empfangen soll, wird automatisch für ungültig erklärt, sodass die Anwendung keine eigenen Clippingbereiche berechnen muss. Weitere Informationen zum Clipping finden Sie unter [Clipping](/windows/desktop/gdi/clipping).

In der Regel führt eine Anwendung einen Bildlauf des Inhalts eines Fensters in die richtungsentgegengesetzte Richtung durch, die durch die Bildlaufleiste angegeben wird. Wenn der Benutzer beispielsweise im Bereich unterhalb des Bildlauffelds auf die Bildlaufleiste klickt, führt eine Anwendung einen Bildlauf des Objekts im Fenster nach oben durch, um einen Teil des Objekts anzuzeigen, der sich unterhalb des sichtbaren Teils befindet.

Sie können auch einen rechteckigen Bereich mithilfe der [**ScrollDC-Funktion**](/windows/desktop/api/Winuser/nf-winuser-scrolldc) scrollen.

## <a name="scroll-bar-colors-and-metrics"></a>Bildlaufleistenfarben und Metriken

Der systemdefinierte Farbwert COLOR \_ SCROLLBAR steuert die Farbe innerhalb einer Bildlaufleiste. Verwenden Sie die [**GetSysColor-Funktion,**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) um die Farbe der Bildlaufleistenunterstützung zu bestimmen, und die [**SetSysColors-Funktion,**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) um die Farbe der Scrollleistenverläufe festzulegen. Beachten Sie jedoch, dass sich diese Farbänderung auf alle Bildlaufleisten im System auswirkt.

Sie können die Abmessungen der Bitmaps abrufen, die das System in Standardschiebeleisten verwendet, indem Sie die [**GetSystemMetrics-Funktion**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) aufrufen. Im Folgenden sind die Systemmetrikwerte angegeben, die Bildlaufleisten zugeordnet sind.



| Systemmetrik | BESCHREIBUNG                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| SM \_ CXHSCROLL | Breite der Pfeilbitmap auf der horizontalen Bildlaufleiste                                                                             |
| SM \_ CXHTHUMB  | Breite des Bildlauffelds auf der horizontalen Bildlaufleiste. Dieser Wert ruft die Breite einer Bildlaufleiste ab, die eine Seitengröße von 0 (null) aufweist.    |
| SM \_ CXVSCROLL | Breite der Pfeilbitmap auf der vertikalen Bildlaufleiste                                                                               |
| SM \_ CYHSCROLL | Höhe der Pfeilbitmap auf der horizontalen Bildlaufleiste                                                                            |
| SM \_ CYVSCROLL | Höhe der Pfeilbitmap auf der vertikalen Bildlaufleiste                                                                              |
| SM \_ CYVTHUMB  | Höhe des Bildlauffelds auf der vertikalen Bildlaufleiste. Dieser Wert ruft die Höhe einer Bildlaufleiste ab, die eine Seitengröße von 0 (null) auf hat. |



 

 

 
