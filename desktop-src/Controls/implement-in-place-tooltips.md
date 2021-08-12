---
title: Implementieren von In-Place QuickInfos
description: QuickInfos werden verwendet, um Textzeichenfolgen für Objekte anzuzeigen, die abgeschnitten wurden. Eine Abbildung finden Sie unter Informationen zu QuickInfo-Steuerelementen.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd3b01d30a20b52cbb80121cc8c1d793965acf0ea3cf4f2be1ce4553f4ccb98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671728"
---
# <a name="how-to-implement-in-place-tooltips"></a>Implementieren von In-Place QuickInfos

QuickInfos werden verwendet, um Textzeichenfolgen für Objekte anzuzeigen, die abgeschnitten wurden. Eine Abbildung finden Sie unter [Informationen zu QuickInfo-Steuerelementen.](tooltip-controls.md)

Der Unterschied zwischen normalen und tatsächlichen QuickInfos ist die Positionierung. Wenn der Mauszeiger mit dem Mauszeiger auf einen Bereich zeigt, dem eine QuickInfo zugeordnet ist, wird die QuickInfo standardmäßig neben dem Bereich angezeigt. QuickInfos sind jedoch Fenster, und sie können an einer beliebigen Stelle positioniert werden, indem [**Sie SetWindowPos aufrufen.**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) Das Erstellen einer quickinfo ist eine Frage der Positionierung des QuickInfo-Fensters, sodass es die Textzeichenfolge überlagert.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche Programmierung

## <a name="instructions"></a>Instructions

### <a name="positioning-an-in-place-tooltip"></a>Positionieren einer In-Place QuickInfo

Sie müssen drei Rechtecke nachverfolgen, wenn Sie eine quickinfo positionieren:

1.  Das Rechteck, das den vollständigen Bezeichnungstext umgibt.
2.  Das Rechteck, das den QuickInfo-Text umgibt. Der QuickInfo-Text ist mit dem vollständigen Bezeichnungstext identisch und hat normalerweise die gleiche Größe und Schriftart. Die beiden Textrechtecke haben daher in der Regel die gleiche Größe.
3.  Das QuickInfo-Fensterrechteck. Dieses Rechteck ist etwas größer als das QuickInfo-Textrechteck, das es umschließt.


Die drei Rechtecke werden in der folgenden Abbildung schematisch dargestellt. Der ausgeblendete Teil des Bezeichnungstexts wird durch einen grauen Hintergrund angezeigt.

![Diagramm, das eine lange Zeichenfolge zeigt, von der die Hälfte einen grauen Hintergrund hat, und dann dieselbe Zeichenfolge innerhalb eines größeren Rechtecks im QuickInfo-Fenster](images/inplace.png)

Um eine quickinfo zu erstellen, müssen Sie das QuickInfo-Textrechteck so positionieren, dass es das Bezeichnungstextrechteck überlagert. Das Verfahren zum Ausrichten der beiden Rechtecke ist relativ einfach:

1.  Definieren Sie das Bezeichnungstextrechteck.
2.  Positionieren Sie das QuickInfo-Fenster so, dass das QuickInfo-Textrechteck das Bezeichnungstextrechteck überlagert.


In der Praxis ist es in der Regel ausreichend, die linke obere Ecke der beiden Textrechtecke auszurichten. Der Versuch, die Größe des QuickInfo-Textrechtecks so zu ändern, dass es genau mit dem Bezeichnungstextrechteck übereinstimmen kann, kann probleme mit der QuickInfo-Anzeige verursachen.

Das Problem bei diesem einfachen Schema ist, dass Sie das QuickInfo-Textrechteck nicht direkt positionieren können. Stattdessen müssen Sie das Rechteck des QuickInfo-Fensters genau so weit über und links vom Bezeichnungstextrechteck positionieren, dass die Ecken der beiden Textrechtecke übereinstimmen. Anders ausgedrückt: Sie müssen den Offset zwischen dem Rechteck des QuickInfo-Fensters und dem umschlossenen Textrechteck kennen. Im Allgemeinen gibt es keine einfache Möglichkeit, diesen Offset zu bestimmen.

### <a name="implement-in-place-tooltips"></a>Implementieren In-Place QuickInfos

Das folgende Codefragment veranschaulicht, wie eine [**TTM \_ ADJUSTRECT-Nachricht**](ttm-adjustrect.md) in einem [TTN \_ SHOW-Handler](ttn-show.md) verwendet wird, um eine quickinfo anzuzeigen. Ihre Anwendung gibt an, dass der Bezeichnungstext abgeschnitten wird, indem die private *fMyStringIsTruncated-Variable* auf **TRUE festlegen.** Der Handler ruft die anwendungsdefinierte Funktion **GetMyItemRect** auf, um das Bezeichnungstextrechteck abzurufen. Dieses Rechteck wird mit **TTM \_ ADJUSTRECT** an das QuickInfo-Steuerelement übergeben, das das entsprechende Fensterrechteck zurückgibt. [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) wird dann aufgerufen, um die QuickInfo über der Bezeichnung zu positionieren.


```C++
case TTN_SHOW:
            
    if (fMyStringIsTruncated) 
    {
        RECT rc;
        
        GetMyItemRect(&rc);
        
        SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
        
        SetWindowPos(hwndToolTip, NULL, rc.left, rc.top, 0, 0, 
                     SWP_NOSIZE | SWP_NOZORDER | SWP_NOACTIVATE);
    }
```



Dieses Beispiel ändert nicht die Größe der QuickInfo, sondern nur deren Position. Die beiden Textrechtecke werden an ihren oberen linken Ecken ausgerichtet, aber nicht notwendigerweise mit den gleichen Dimensionen. In der Praxis ist der Unterschied in der Regel klein, und dieser Ansatz wird für die meisten Zwecke empfohlen. Sie können zwar im Prinzip [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) verwenden, um die Größe zu ändern und die QuickInfo neu zu positionieren. Dies kann jedoch unvorhersehbare Folgen haben.

## <a name="remarks"></a>Hinweise

Allgemeine [Steuerelemente, Version 5.80,](common-control-versions.md) vereinfachen die Verwendung von quickinfos, indem eine neue Nachricht, [**TTM \_ ADJUSTRECT, eingeführt wird.**](ttm-adjustrect.md) Senden Sie diese Nachricht mit den Koordinaten des Bezeichnungstextrechtecks, das die QuickInfo überlagern soll, und gibt die Koordinaten eines entsprechend positionierten QuickInfo-Fensterrechtecks zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von QuickInfo-Steuerelementen](using-tooltip-contro.md)
</dt> </dl>

 

 