---
title: Implementieren von In-Place Quick Infos
description: Direkte Quick Infos werden zum Anzeigen von Text Zeichenfolgen für Objekte verwendet, die abgeschnitten wurden. Eine Abbildung finden Sie unter Informationen zu QuickInfo-Steuerelementen.
ms.assetid: 2FE39B99-75F3-4978-B0B3-B769E2961F23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc321ecdd6df151a151e6d21c8419326edb63d38
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104039868"
---
# <a name="how-to-implement-in-place-tooltips"></a>Implementieren von In-Place Quick Infos

Direkte Quick Infos werden zum Anzeigen von Text Zeichenfolgen für Objekte verwendet, die abgeschnitten wurden. Eine Abbildung finden Sie unter [Informationen zu](tooltip-controls.md)QuickInfo-Steuerelementen.

Der Unterschied zwischen normalen und direkten Quick Infos ist die Positionierung. Wenn der Mauszeiger auf einen Bereich zeigt, dem eine QuickInfo zugeordnet ist, wird die QuickInfo standardmäßig neben dem Bereich angezeigt. Quick Infos sind jedoch Windows, und Sie können an einer beliebigen Stelle positioniert werden, indem Sie [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)aufrufen. Das Erstellen einer direkten QuickInfo besteht darin, das QuickInfo-Fenster so zu positionieren, dass es die Text Zeichenfolge überlagert.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="positioning-an-in-place-tooltip"></a>Positionieren einer In-Place-QuickInfo

Sie müssen drei Rechtecke nachverfolgen, wenn Sie eine direkte QuickInfo positionieren:

1.  Das Rechteck, das den vollständigen Bezeichnungs Text umgibt.
2.  Das Rechteck, das den QuickInfo-Text umgibt. Der QuickInfo-Text ist mit dem vollständigen Bezeichnungs Text identisch und weist normalerweise dieselbe Größe und Schriftart auf. Die zwei Text Rechtecke haben daher normalerweise dieselbe Größe.
3.  Das QuickInfo-Fenster Rechteck. Dieses Rechteck ist etwas größer als das QuickInfo-Text Rechteck, das es einschließt.


Die drei Rechtecke werden schematisch in der folgenden Abbildung dargestellt. Der verborgene Teil des Beschriftungs Texts wird durch einen grauen Hintergrund angegeben.

![das Diagramm zeigt eine lange Zeichenfolge, die Hälfte davon einen grauen Hintergrund hat, dann die gleiche Zeichenfolge innerhalb eines größeren QuickInfo-Fenster Rechtecks.](images/inplace.png)

Um eine direkte QuickInfo zu erstellen, müssen Sie das QuickInfo-Text Rechteck so positionieren, dass es das Bezeichnungs Text Rechteck überlagert. Die Vorgehensweise zum Ausrichten der beiden Rechtecke ist relativ unkompliziert:

1.  Definieren des Bezeichnungs Text Rechtecks.
2.  Positionieren Sie das QuickInfo-Fenster, sodass das Text Rechteck der QuickInfo das Bezeichnungs Text Rechteck überlagert.


In der Praxis ist es in der Regel ausreichend, die obere linke Ecke der beiden Text Rechtecke auszurichten. Wenn Sie versuchen, die Größe des QuickInfo-Text Rechtecks exakt mit dem Bezeichnungs Text Rechteck übereinzustimmen, können Probleme mit der QuickInfo angezeigt werden

Das Problem mit diesem einfachen Schema besteht darin, dass Sie das QuickInfo-Text Rechteck nicht direkt positionieren können. Stattdessen müssen Sie das QuickInfo-Fenster Rechteck direkt oberhalb und Links vom Bezeichnungs Text Rechteck positionieren, damit die Ecken der zwei Text Rechtecke übereinstimmen. Anders ausgedrückt: Sie müssen den Offset zwischen dem QuickInfo-Fenster Rechteck und dem eingeschlossenen Text Rechteck kennen. Im Allgemeinen gibt es keine einfache Methode zum Ermitteln dieses Offsets.

### <a name="implement-in-place-tooltips"></a>Implementieren von In-Place Quick Infos

Im folgenden Code Fragment wird veranschaulicht, wie eine [**TTM \_**](ttm-adjustrect.md) -Nachricht in einem [TTN- \_ Show](ttn-show.md) Handler verwendet wird, um eine direkte QuickInfo anzuzeigen. Die Anwendung gibt an, dass der Bezeichnungs Text abgeschnitten wird, indem die private *fmystringistruncated* -Variable auf **true** festgelegt wird. Der Handler Ruft die Anwendungs definierte Funktion **getmyitemrect** auf, um das Bezeichnungs Text Rechteck abzurufen. Dieses Rechteck wird an das QuickInfo-Steuerelement mit TTM-"-", "-", das das entsprechende Fenster Rechteck zurückgibt. **\_** [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) wird dann aufgerufen, um die QuickInfo über der Bezeichnung zu positionieren.


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



In diesem Beispiel wird die Größe der QuickInfo nicht geändert, sondern nur die Position. Die zwei Text Rechtecke werden an Ihren oberen linken Ecken ausgerichtet, aber nicht unbedingt mit denselben Dimensionen. In der Praxis ist der Unterschied in der Regel gering, und diese Vorgehensweise wird für die meisten Zwecke empfohlen. Obwohl Sie [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) zum Ändern der Größe und zum Neupositionieren der QuickInfo verwenden können, kann dies zu unvorhersehbaren Folgen führen.

## <a name="remarks"></a>Bemerkungen

Allgemeine Steuerelemente [Version 5,80](common-control-versions.md) vereinfachen die Verwendung von direkten Quick Infos durch das Hinzufügen einer neuen Nachricht, [**TTM- \_**](ttm-adjustrect.md)Version. Senden Sie diese Nachricht mit den Koordinaten des Beschriftungs Text Rechtecks, das von der QuickInfo überlagern werden soll, und gibt die Koordinaten eines ordnungsgemäß positionierten QuickInfo-Fenster Rechtecks zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Quick Infos](using-tooltip-contro.md)
</dt> </dl>

 

 