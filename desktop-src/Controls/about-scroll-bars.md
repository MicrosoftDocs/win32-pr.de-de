---
title: Informationen zu Scrollleisten
description: Ein Fenster kann ein Datenobjekt anzeigen, z. b. ein Dokument oder eine Bitmap, das größer ist als der Client Bereich des Fensters.
ms.assetid: 9cb3afad-79ef-4817-950a-c8c1de39401b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d410e98ea1fe722d6dc1c4869010df30f99bddb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039634"
---
# <a name="about-scroll-bars"></a>Informationen zu Scrollleisten

Ein Fenster kann ein Datenobjekt anzeigen, z. b. ein Dokument oder eine Bitmap, das größer ist als der Client Bereich des Fensters. Bei Bereitstellung mit einer Schiebe Leiste kann der Benutzer einen Bildlauf in einem Datenobjekt im Client Bereich durchführen, um die Teile des Objekts anzuzeigen, die über die Rahmen des Fensters hinausgehen.

Bild Lauf leisten sollten in jedem Fenster enthalten sein, für das der Inhalt des Client Bereichs über den Rahmen des Fensters hinausreicht. Die Ausrichtung einer Schiebe Leiste bestimmt die Richtung, in der ein Bildlauf durchgeführt wird, wenn der Benutzer die Bild Lauf Leiste betreibt. Eine horizontale Schiebe Leiste ermöglicht dem Benutzer einen Bildlauf nach links oder rechts durch den Inhalt eines Fensters. Eine vertikale Schiebe Leiste ermöglicht dem Benutzer den Bildlauf nach oben oder unten.

Die folgenden Themen werden in diesem Abschnitt erläutert.

-   [Teile einer Schiebe Leiste](#parts-of-a-scroll-bar)
-   [Standard-Bild Lauf leisten und ScrollBar-Steuerelemente](#standard-scroll-bars-and-scroll-bar-controls)
-   [Bild Lauf Feld Position und Bild Laufbereich](#scroll-box-position-and-scrolling-range)
-   [Sichtbarkeit der Scrollleiste](#scroll-bar-visibility)
-   [ScrollBar-Anforderungen](#scroll-bar-requests)
-   [Tastaturschnittstelle für eine Schiebe Leiste](#keyboard-interface-for-a-scroll-bar)
-   [Scrollen des Client Bereichs](#scrolling-the-client-area)
-   [Farben und Metriken der Bild Lauf Leiste](#scroll-bar-colors-and-metrics)

## <a name="parts-of-a-scroll-bar"></a>Teile einer Schiebe Leiste

Eine Schiebe Leiste besteht aus einer schattierten Welle mit einer Pfeil Schaltfläche an jedem Ende und einem Bild Lauf *Feld* (manchmal auch als Ziehpunkt bezeichnet) zwischen den Pfeil Schaltflächen. Eine Bild Lauf Leiste stellt die Gesamtlänge oder Breite eines Datenobjekts im Client Bereich eines Fensters dar. das Bild Lauf Feld stellt den Teil des-Objekts dar, der im Client Bereich angezeigt wird. Die Position des Bild Lauf Felds ändert sich, wenn der Benutzer einen Bildlauf in einem Datenobjekt durchführt, um einen anderen Teil davon anzuzeigen. Das System passt auch die Größe des Bild Lauf Felds einer Schiebe Leiste an, sodass es angibt, welcher Teil des gesamten Datenobjekts momentan im Fenster sichtbar ist. Wenn der größte Teil des Objekts sichtbar ist, belegt das Bild Lauf Feld den größten Teil der Schiebe leisten-Schiebe Leiste. Ebenso, wenn nur ein kleiner Teil des Objekts sichtbar ist, belegt das Bild Lauf Feld einen kleinen Teil der Schiebe leisten-Schiebe Leiste.

Der Benutzer scrollt den Inhalt eines Fensters durch Klicken auf eine der Pfeil Schaltflächen, indem er auf den Bereich in der schattierten Schiebe leisten-Säule klickt oder das Bild Lauf Feld zieht. Wenn der Benutzer auf eine Pfeil Schaltfläche klickt, führt die Anwendung im Inhalt einen Bildlauf um eine Einheit durch (in der Regel eine einzelne Zeile oder Spalte). Wenn der Benutzer auf die schattierten Bereiche klickt, führt die Anwendung im Inhalt einen Bildlauf um ein Fenster durch. Der Bildlauf, der auftritt, wenn der Benutzer das Bild Lauf Feld zieht, hängt von der Entfernung, auf die der Benutzer das Bild Lauf Feld zieht, und dem scrollbereich der Bild Lauf Leiste ab. Weitere Informationen zum scrollbereich finden Sie unter [Scrollbox-Position und](#scroll-box-position-and-scrolling-range)Bild Laufbereich.

Der folgende Screenshot zeigt ein umfassendes Bearbeitungs Steuerelement mit vertikalen und horizontalen Bild Lauf leisten, die in Windows Vista angezeigt werden können. Die vertikale Schiebe Leiste ist zurzeit "Hot", da der Mauszeiger darauf zeigt, als der Screenshot erstellt wurde.

![Screenshot eines Rich-Edit-Steuer Elements mit Scrollleisten](images/sbvista.png)

## <a name="standard-scroll-bars-and-scroll-bar-controls"></a>Standard-Bild Lauf leisten und ScrollBar-Steuerelemente

Eine Schiebe Leiste ist entweder als Standard Scrollleiste oder als Schiebe leisten-Steuerelement in einem Fenster enthalten. Eine Standard Scrollleiste befindet sich im nicht-Client Bereich eines Fensters. Sie wird mit dem Fenster erstellt und angezeigt, wenn das Fenster angezeigt wird. Der einzige Zweck einer Standard Scrollleiste besteht darin, dass der Benutzer das Generieren von scrollanforderungen zum Anzeigen des gesamten Inhalts des Client Bereichs ermöglicht. Sie können eine Standardbild Lauf Leiste in ein Fenster einschließen, indem Sie beim Erstellen des Fensters [**WS \_ HScroll**](/windows/desktop/winmsg/window-styles), [**WS \_ VScroll**](/windows/desktop/winmsg/window-styles)oder beide Stile angeben. Der **WS \_ HScroll** -Stil erstellt eine horizontale Schiebe Leiste, die sich am unteren Rand des Client Bereichs befindet. Der **WS- \_ VScroll** -Stil erstellt eine vertikale Schiebe Leiste, die sich auf der rechten Seite des Client Bereichs befindet. Die \_ Metrikwerte "SM cxhscroll" und "SM \_ cyhscroll" definieren die Breite und Höhe einer horizontalen Standard Scrollleiste. Die SM \_ cxvscroll-und SM \_ cyvscroll-Werte definieren die Breite und Höhe einer vertikalen Standard Scrollleiste. Eine Standard Scrollleiste ist Teil des zugehörigen Fensters und verfügt daher nicht über ein eigenes Fenster handle.

Ein Bild Lauf leisten-Steuerelement ist ein Steuerelement Fenster, das zur ScrollBar-Fenster Klasse gehört. Ein Bild Lauf leisten-Steuerelement wird angezeigt und funktioniert wie eine Standard Scrollleiste, aber es ist ein separates Fenster. Als separates Fenster übernimmt ein ScrollBar-Steuerelement den direkten Eingabefokus. Anders als bei einer Standard Scrollleiste verfügt ein ScrollBar-Steuerelement auch über eine integrierte Tastaturschnittstelle.

Sie können beliebig viele ScrollBar-Steuerelemente in einem einzelnen Fenster verwenden. Wenn Sie ein Bild Lauf leisten-Steuerelement erstellen, müssen Sie die Größe und Position der Scrollleiste angeben. Wenn die Größe des Fensters eines Schiebe leisten-Steuer Elements geändert werden kann, müssen jedoch Anpassungen an der Größe der Scrollleiste vorgenommen werden, wenn sich die Fenstergröße ändert.

Der Vorteil der Verwendung einer Standard Scrollleiste besteht darin, dass das System die Scrollleiste erstellt und automatisch seine Größe und Position festlegt. Standard Scrollleisten sind jedoch manchmal zu restriktiv. Angenommen, Sie möchten einen Client Bereich in Quadranten aufteilen und einen separaten Satz von Schiebe leisten verwenden, um den Inhalt der einzelnen Quadranten zu steuern. Standard Scrollleisten können nicht verwendet werden, da Sie nur einen Satz von Bild Lauf leisten für ein bestimmtes Fenster erstellen können. Verwenden Sie stattdessen ScrollBar-Steuerelemente, da Sie beliebig viele von Ihnen einem Fenster hinzufügen können.

Anwendungen können Schiebe leisten-Steuerelemente für andere Zwecke als den Bildlauf des Inhalts eines Fensters bereitstellen. Beispielsweise kann eine Bildschirmschoner-Anwendung eine Schiebe Leiste zum Festlegen der Geschwindigkeit bereitstellen, mit der Grafiken auf dem Bildschirm verschoben werden.

Ein Schiebe leisten-Steuerelement kann über eine Reihe von Stilen verfügen, mit denen die Ausrichtung und Position der Bild Lauf Leiste gesteuert werden kann. Sie geben die gewünschten Stile an, wenn Sie die Funktion " [**roatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) " zum Erstellen eines ScrollBar-Steuer Elements aufrufen. Einige der Stile erstellen ein ScrollBar-Steuerelement, das eine Standardbreite oder-Höhe verwendet. Allerdings müssen Sie immer die x-und y-Koordinaten und die anderen Dimensionen der Bild Lauf Leiste angeben.

Eine Tabelle mit ScrollBar-Steuerelement Stilen finden Sie unter [ScrollBar-Steuerelement Stile](scroll-bar-control-styles.md).

> [!Note]  
> Um visuelle Stile mit Bild Lauf leisten zu verwenden, muss eine Anwendung ein Manifest einschließen und muss am Anfang des Programms [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) aufgerufen werden. Weitere Informationen zu visuellen Stilen finden Sie unter [visuelle Stile](themes-overview.md). Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

 

## <a name="scroll-box-position-and-scrolling-range"></a>Bild Lauf Feld Position und Bild Laufbereich

Die Position des Bild Lauf Felds wird als ganze Zahl dargestellt. Er ist relativ zum linken oder oberen Ende der Schiebe Leiste, abhängig davon, ob die Bild Lauf Leiste horizontal oder vertikal ist. Die Position muss innerhalb der minimalen und maximalen Werte des scrollbereichs liegen. Beispielsweise befindet sich in einer Bild Lauf Leiste mit einem Bereich von 0 bis 100 die Position 50 in der Mitte, wobei die restlichen Positionen gleichmäßig entlang der Scrollleiste verteilt sind. Der anfängliche Bereich hängt von der Scrollleiste ab. Standard Scrollleisten haben einen Anfangsbereich von 0 bis 100. Bild Lauf leisten-Steuerelemente weisen einen leeren Bereich auf (die minimalen und maximalen Werte sind null), es sei denn, Sie geben einen expliziten Bereich an, wenn das Steuerelement erstellt wird Sie können den Bereich jederzeit ändern. Sie können die [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion verwenden, um die Bereichs Werte festzulegen, und die [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) -Funktion, um die aktuellen Bereichs Werte abzurufen.

In einer Anwendung wird der Bild Laufbereich in der Regel an bequeme ganze Zahlen angepasst, sodass die Position des Bild Lauf Felds in einen Wert übersetzt werden kann, der dem zu bildenden Datenobjekt entspricht. Wenn eine Anwendung z. b. 260 Zeilen einer Textdatei in einem Fenster anzeigen muss, in dem jeweils nur 16 Zeilen angezeigt werden können, kann der Bereich der vertikalen Schiebe Leiste auf 1 bis 244 festgelegt werden. Wenn sich das Bild Lauf Feld an der Position 1 befindet, wird die erste Zeile am oberen Rand des Fensters angezeigt. Wenn sich das Bild Lauf Feld an der Position 244 befindet, wird die letzte Zeile (Zeile 260) am unteren Rand des Fensters angezeigt. Wenn eine Anwendung versucht, einen Positionswert festzulegen, der kleiner ist als der Mindestwert oder größer als der Höchstwert, wird stattdessen der minimale oder maximale scrollbereichwert verwendet.

Sie können eine Seitengröße für eine Bild Lauf Leiste festlegen. Die *Seitengröße* stellt die Anzahl der Dateneinheiten dar, die in den Client Bereich des Besitzer Fensters unter Berücksichtigung der aktuellen Größe passen. Wenn der Client Bereich z. b. 16 Textzeilen enthalten kann, wird die Seitengröße von einer Anwendung auf 16 festgelegt. Das System verwendet die Seitengröße zusammen mit dem scrollbereich und der Länge der Schiebe leisten-Säule, um die Größe des Bild Lauf Felds festzulegen. Wenn die Größe eines Fensters, das eine Bild Lauf Leiste enthält, geändert wird, sollte eine Anwendung die [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion aufrufen, um die Seitengröße festzulegen. Eine Anwendung kann die aktuelle Seitengröße abrufen, indem Sie die sendende [**getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) -Funktion aufrufen.

Um eine nützliche Beziehung zwischen dem Schiebe Leistenbereich und dem Datenobjekt herzustellen, muss eine Anwendung den Bereich immer dann anpassen, wenn sich die Größe des Datenobjekts ändert.

Wenn der Benutzer das Bild Lauf Feld in einer Schiebe Leiste verschiebt, meldet die Bild Lauf Leiste die Position des Bild Lauf Felds als ganze Zahl im scrollbereich. Wenn die Position der minimale Wert ist, befindet sich das Bild Lauf Feld am oberen Rand einer vertikalen Schiebe Leiste oder am linken Ende einer horizontalen Schiebe Leiste. Wenn die Position der Höchstwert ist, befindet sich das Bild Lauf Feld am unteren Rand einer vertikalen Schiebe Leiste oder am rechten Ende einer horizontalen Schiebe Leiste.

Der maximale Wert, den eine Schiebe Leiste melden kann (d. h. die maximale Scrollposition), hängt von der Seitengröße ab. Wenn die Bild Lauf Leiste eine Seitengröße überschreitet, ist die maximale Scrollposition kleiner als der maximale Bereichs Wert. Mit der folgenden Formel können Sie die maximale Scrollposition berechnen:


```
MaxScrollPos = MaxRangeValue - (PageSize - 1) 
```



Eine Anwendung muss das Bild Lauf Feld in eine Schiebe Leiste verschieben. Obwohl der Benutzer einen Bildlauf in einer Bild Lauf Leiste durchführt, aktualisiert die Scrollleiste die Position des Bild Lauf Felds nicht automatisch. Stattdessen übergibt Sie die Anforderung an das übergeordnete Fenster, das einen Bildlauf der Daten durchführen und die Position des Bild Lauf Felds aktualisieren muss. Eine Anwendung verwendet die [**setScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) -Funktion, um die Position des Bild Lauf Felds zu aktualisieren. Andernfalls wird die [**setscrollpos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) -Funktion verwendet. Da es die Bild Lauf Feld Bewegung steuert, kann die Anwendung das Bild Lauf Feld in Inkrementen verschieben, die am besten für die Daten ausgeführt werden, für die ein Bildlauf ausgeführt wird

## <a name="scroll-bar-visibility"></a>Sichtbarkeit der Scrollleiste

Das System blendet eine Standardbild Lauf Leiste aus und deaktiviert diese, wenn die minimalen und maximalen Werte angegeben werden. Das System blendet außerdem eine Standard Scrollleiste aus und deaktiviert Sie, wenn Sie eine Seitengröße angeben, die den gesamten Bild Laufbereich der Bild Lauf Leiste enthält. Dies ist die Möglichkeit, eine Schiebe Leiste vorübergehend auszublenden, wenn Sie für den Inhalt des Client Bereichs nicht benötigt wird. Es ist nicht erforderlich, scrollanforderungen über die Scrollleiste zu erstellen, wenn Sie ausgeblendet ist. Das System aktiviert die Bild Lauf Leiste und zeigt Sie erneut an, wenn Sie die Mindest-und Höchstwerte auf ungleich Werte oder die Seitengröße festlegen, die nicht den gesamten Bild Laufbereich enthält. Die [**ShowScrollbar**](/windows/desktop/api/Winuser/nf-winuser-showscrollbar) -Funktion kann auch verwendet werden, um eine Bild Lauf Leiste auszublenden oder anzuzeigen. Er wirkt sich nicht auf den Bereich, die Seitengröße oder die Position des Bild Lauf Felds der Scrollleiste aus.

Die [**enablescrollbar**](/windows/desktop/api/Winuser/nf-winuser-enablescrollbar) -Funktion kann verwendet werden, um einen oder beide Pfeile einer Schiebe Leiste zu deaktivieren. Eine Anwendung zeigt deaktivierte Pfeile in grau an und antwortet nicht auf Benutzereingaben.

## <a name="scroll-bar-requests"></a>ScrollBar-Anforderungen

Der Benutzer führt scrollanforderungen durch Klicken auf verschiedene Teile einer Schiebe Leiste aus. Das System sendet die Anforderung in Form einer [**WM- \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht an das angegebene Fenster. Eine horizontale Schiebe Leiste sendet die **WM- \_ HScroll** -Nachricht. eine vertikale Schiebe Leiste sendet die **WM- \_ VScroll** -Nachricht. Jede Nachricht enthält einen Anforderungs Code, der der Benutzeraktion, dem Handle der Bild Lauf Leiste (nur Schiebe leisten-Steuerelemente) und in einigen Fällen die Position des Bild Lauf Felds entspricht.

Das folgende Diagramm zeigt den Anforderungs Code, den der Benutzer generiert, wenn er auf verschiedene Teile einer Schiebe Leiste klickt.

![Diagramm mit den Anforderungs Codes, die den einzelnen Regionen auf zwei Bild Lauf leisten zugeordnet sind.](images/csscr-02.png)

Die SB- \_ Werte geben die Aktion an, die der Benutzer annimmt. Eine Anwendung überprüft die Codes, die die " [**WM \_ HScroll**](wm-hscroll.md) "-und " [**WM \_ VScroll**](wm-vscroll.md) "-Meldungen begleiten, und führt dann den passenden scrollvorgang aus. In der folgenden Tabelle wird die Aktion des Benutzers für jeden Wert angegeben, gefolgt von der Antwort der Anwendung. In jedem Fall wird eine Einheit von der Anwendung entsprechend den Daten definiert. Beispielsweise ist die typische Einheit für das vertikale Scrollen von Text eine Textzeile.



| Anforderung           | Aktion                                                                               | Antwort                                                                                                                                                                                                                                                                                                                         |
|-------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SB \_ -Auflistung        | Der Benutzer klickt auf den oberen Bild Lauf Pfeil.                                                | Verringert die Position des Bild Lauf Felds. führt einen Bildlauf nach oben in den Daten um eine Einheit aus.                                                                                                                                                                                                                                              |
| SB- \_ LineDown      | Der Benutzer klickt auf den unteren Bild Lauf Pfeil.                                             | Erhöht die Position des Bild Lauf Felds. führt einen Bildlauf zum Ende der Daten um eine Einheit aus.                                                                                                                                                                                                                                           |
| SB- \_ LineLeft      | Der Benutzer klickt auf den linken scrollpfeil.                                               | Verringert die Position des Bild Lauf Felds. führt einen Bildlauf zum linken Ende der Daten um eine Einheit aus.                                                                                                                                                                                                                                         |
| SB- \_ LineRight     | Der Benutzer klickt auf den Pfeil nach rechts.                                              | Erhöht die Position des Bild Lauf Felds. führt einen Bildlauf zum rechten Ende der Daten um eine Einheit aus.                                                                                                                                                                                                                                        |
| SB- \_ PageUp        | Der Benutzer klickt über dem Bild Lauf Feld auf die Schiebe leisten-Leiste.                           | Verringert die Position des Bild Lauf Felds um die Anzahl der Dateneinheiten im-Fenster. führt einen Bildlauf nach oben in den Daten durch die gleiche Anzahl von Einheiten durch.                                                                                                                                                                                    |
| SB- \_ PageDown      | Der Benutzer klickt unter dem Bild Lauf Feld auf die Schiebe leisten-Schiebe Leiste.                           | Erhöht die Position des Bild Lauf Felds um die Anzahl der Dateneinheiten im-Fenster. führt einen Bildlauf nach unten in den Daten durch die gleiche Anzahl von Einheiten durch.                                                                                                                                                                                 |
| SB- \_ PageLeft      | Der Benutzer klickt auf den Schiebe leisten-Schiebe Bereich links neben dem Bild Lauf Feld.                  | Verringert die Position des Bild Lauf Felds um die Anzahl der Dateneinheiten im-Fenster. führt einen Bildlauf nach dem linken Ende der Daten durch die gleiche Anzahl von Einheiten aus.                                                                                                                                                                               |
| SB- \_ PageRight     | Der Benutzer klickt auf den Schiebe leisten-Schiebe Bereich rechts neben dem Bild Lauf Feld.                 | Erhöht die Position des Bild Lauf Felds um die Anzahl der Dateneinheiten im-Fenster. führt einen Bildlauf zum rechten Ende der Daten durch die gleiche Anzahl von Einheiten durch.                                                                                                                                                                              |
| SB-Finger \_ Position | Der Benutzer gibt das Bild Lauf Feld nach dem ziehen frei.                                  | Legt das Bild Lauf Feld auf die in der Meldung angegebene Position fest. führt einen Bildlauf durch die Daten um die gleiche Anzahl von Einheiten aus, die im Scrollfeld verschoben wurden.                                                                                                                                                                                             |
| SB-Finger \_ Abdruck    | Der Benutzer zieht das Bild Lauf Feld.                                                       | Legt das Bild Lauf Feld auf die in der Meldung angegebene Position fest und führt einen Bildlauf für die Daten um die gleiche Anzahl von Einheiten aus, die das Bild Lauf Feld für Anwendungen verschoben hat, die Daten schnell zeichnen. Anwendungen, die Daten nicht schnell zeichnen können, müssen auf den Code der SB-Finger Positions Anforderung warten, bevor Sie das Bild Lauf \_ Feld verschieben und einen Bildlauf durchführen |
| SB- \_ endscroll     | Der Benutzer gibt die Maus aus, nachdem er auf einem Pfeil oder in der Schiebe leisten-Säule gedrückt gehalten wurde. | Es ist keine Antwort erforderlich.                                                                                                                                                                                                                                                                                                           |



 

Eine Schiebe Leiste generiert die SB \_ -Fingerposition und den SB- \_ ThumbTrack-Anforderungs Code, wenn der Benutzer auf das Bild Lauf Feld klickt. Eine Anwendung sollte so programmiert werden, dass Sie entweder den SB- \_ fingertitel oder den SB- \_ thumbpositions-Anforderungs Code verarbeitet.

Der SB \_ thumbposition-Anforderungs Code tritt auf, wenn der Benutzer die Maustaste loslässt, nachdem er auf das Bild Lauf Feld geklickt hat. Eine Anwendung, die diese Nachricht verarbeitet, führt den scrollvorgang aus, nachdem der Benutzer das Bild Lauf Feld an die gewünschte Position gezogen und die Maustaste losgelassen hat.

Der SB \_ ThumbTrack-Anforderungs Code tritt auf, wenn der Benutzer das Bild Lauf Feld zieht. Wenn eine Anwendung SB- \_ ThumbTrack-Anforderungs Codes verarbeitet, kann Sie im Inhalt eines Fensters scrollen, während der Benutzer das Bild Lauf Feld zieht. Eine Schiebe Leiste kann jedoch viele SB-Finger \_ Abdruck-Anforderungs Codes in kurzer Zeit generieren, sodass eine Anwendung diese Anforderungs Codes nur dann verarbeiten sollte, wenn Sie den Inhalt des Fensters schnell neu zeichnen kann.

## <a name="keyboard-interface-for-a-scroll-bar"></a>Tastaturschnittstelle für eine Schiebe Leiste

Ein Schiebe leisten-Steuerelement stellt eine integrierte Tastaturschnittstelle bereit, die es dem Benutzer ermöglicht, mithilfe der Tastatur scrollanforderungen auszugeben. eine Standard Scrollleiste ist nicht. Wenn ein Schiebe leisten-Steuerelement den Tastaturfokus besitzt, sendet es [**WM- \_ HScroll**](wm-hscroll.md) -und [**WM- \_ VScroll**](wm-vscroll.md) -Meldungen an das übergeordnete Fenster, wenn der Benutzer die Pfeiltasten drückt. Der Anforderungs Code wird mit jeder Nachricht gesendet, die der vom Benutzer gedrückten Pfeiltaste entspricht. Im folgenden sind die Pfeiltasten und ihre entsprechenden Anforderungs Codes dargestellt.



| Pfeiltaste | Anforderungs Code                  |
|-----------|-------------------------------|
| DOWN      | SB- \_ LineDown oder SB- \_ LineRight |
| ENDE       | SB \_ unten                    |
| POS1      | SB- \_ Top                       |
| LEFT      | SB-Auflistungs- \_ oder SB- \_ LineLeft    |
| Bild      | SB- \_ PageDown oder SB- \_ PageRight |
| Bild      | SB- \_ PageUp oder SB- \_ PageLeft    |
| RIGHT     | SB- \_ LineDown oder SB- \_ LineRight |
| UP        | SB-Auflistungs- \_ oder SB- \_ LineLeft    |



 

 

> [!Note]  
> Die Tastaturschnittstelle eines Schiebe leisten-Steuer Elements sendet den \_ Anforderungs Codes "SB Top" und "SB \_ Bottom". Der \_ Top-Anforderungs Code von SB gibt an, dass der Benutzer den obersten Wert des scrollbereichs erreicht hat. Eine Anwendung scrollt den Fensterinhalt nach unten, sodass der obere Rand des Datenobjekts sichtbar ist. Der "SB \_ Bottom Request"-Code gibt an, dass der Benutzer den unteren Wert des scrollbereichs erreicht hat. Wenn eine Anwendung den SB- \_ Code der untersten Anforderung verarbeitet, wird der Fensterinhalt durch einen Bildlauf nach oben verschoben, sodass der untere Teil des Datenobjekts sichtbar ist.

 

Wenn Sie eine Tastaturschnittstelle für eine Standardbild Lauf Leiste benötigen, können Sie Sie selbst erstellen, indem Sie die [**WM- \_ keydownnachricht**](/windows/desktop/inputdev/wm-keydown) in der Fenster Prozedur verarbeiten und dann die geeignete scrollaktion basierend auf dem Code des virtuellen Schlüssels ausführen, der die Nachricht begleitet. Informationen zum Erstellen einer Tastaturschnittstelle für eine Bild Lauf Leiste finden Sie unter [Erstellen einer Tastaturschnittstelle für eine Standard Scrollleiste](using-scroll-bars.md).

## <a name="scrolling-the-client-area"></a>Scrollen des Client Bereichs

Die einfachste Möglichkeit, den Inhalt eines Client Bereichs zu scrollen, besteht darin, ihn zu löschen und dann neu zu zeichnen. Dies ist die Methode, mit der eine Anwendung wahrscheinlich mit SB \_ PageUp, SB \_ PageDown und SB \_ Top Request Codes verwendet werden kann, die in der Regel vollständig neuen Inhalt erfordern.

Für einige Anforderungs Codes, wie z. b. SB \_ -und SB- \_ LineDown, müssen nicht alle Inhalte gelöscht werden, da einige nach dem Scrollen sichtbar bleiben. Die [**scrollwindowex**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) -Funktion behält einen Teil des Inhalts des Client Bereichs bei, verschiebt den beibehaltenen Teil um einen angegebenen Betrag und bereitet dann den Rest des Client Bereichs auf das Zeichnen neuer Informationen vor. **Scrollwindowex** verwendet die [**BitBLT**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) -Funktion, um einen bestimmten Teil des Datenobjekts an eine neue Position im Client Bereich zu verschieben. Alle unbedeckten Teile des Client Bereichs (alle nicht beibehaltenen Elemente) werden für ungültig erklärt, gelöscht und gezeichnet, wenn die nächste WM-Zeichnungs Nachricht auftritt. [**\_**](/windows/desktop/gdi/wm-paint)

Die [**scrollwindowex**](/windows/desktop/api/Winuser/nf-winuser-scrollwindowex) -Funktion kann verwendet werden, um einen Teil des Client Bereichs vom scrollvorgang auszuschließen. Dadurch wird verhindert, dass Elemente mit fester Position (z. b. untergeordnete Fenster) innerhalb des Client Bereichs verschoben werden. Der Teil des Client Bereichs, der die neuen Informationen erhält, wird automatisch für ungültig erklärt, sodass die Anwendung keine eigenen Clippingbereiche berechnen muss. Weitere Informationen zum Abschneiden finden Sie unter [Clipping](/windows/desktop/gdi/clipping).

In der Regel führt eine Anwendung einen Bildlauf im Inhalt eines Fensters in der Richtung aus, die von der Scrollleiste angezeigt wird. Wenn der Benutzer z. b. im Bereich unter dem Bild Lauf Feld auf die Schiebe leisten-Schiebe Leiste klickt, führt eine Anwendung im Fenster einen Bildlauf nach oben durch, um einen Teil des Objekts anzuzeigen, der unterhalb des sichtbaren Teils liegt.

Sie können auch einen Bildlauf mit der [**scrolldc**](/windows/desktop/api/Winuser/nf-winuser-scrolldc) -Funktion durchführen.

## <a name="scroll-bar-colors-and-metrics"></a>Farben und Metriken der Bild Lauf Leiste

Der System definierte Farbwert, Color \_ ScrollBar, steuert die Farbe innerhalb einer Schiebe leisten-Säule. Verwenden Sie die [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) -Funktion, um die Farbe der Schiebe leisten-und die [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) -Funktion zu bestimmen, um die Farbe der Schiebe leisten-Schwelle festzulegen. Beachten Sie jedoch, dass sich diese Änderung der Farbe auf alle Bild Lauf leisten im System auswirkt.

Sie können die Dimensionen der Bitmaps abrufen, die das System in Standard Scrollleisten verwendet, indem Sie die [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) -Funktion aufrufen. Im folgenden sind die Systemmetrikwerte dargestellt, die Scrollleisten zugeordnet sind.



| System Metrik | BESCHREIBUNG                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| SM \_ cxhscroll | Breite von Pfeil Bitmap auf horizontaler Scrollleiste                                                                             |
| SM \_ cxhthumb  | Breite des Bild Lauf Felds auf der horizontalen Schiebe Leiste. Dieser Wert Ruft die Breite einer Bild Lauf Leiste mit einer Seitengröße von 0 (null) ab.    |
| SM \_ cxvscroll | Breite von Pfeil Bitmap auf vertikaler Bild Lauf Leiste                                                                               |
| SM \_ cyhscroll | Höhe von Pfeil Bitmap auf horizontaler Scrollleiste                                                                            |
| SM \_ cyvscroll | Höhe von Pfeil Bitmap auf vertikaler Bild Lauf Leiste                                                                              |
| SM \_ cyvthumb  | Die Höhe des Bild Lauf Felds auf der vertikalen Schiebe Leiste. Dieser Wert Ruft die Höhe einer Schiebe Leiste ab, die eine Seitengröße von 0 (null) aufweist. |



 

 

 