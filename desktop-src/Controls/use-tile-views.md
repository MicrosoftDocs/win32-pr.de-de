---
title: Verwenden von Kachel Ansichten
description: In diesem Thema wird veranschaulicht, wie die Kachel Ansicht für ein Listenansicht-Steuerelement festgelegt wird.
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949230"
---
# <a name="how-to-use-tile-views"></a>Verwenden von Kachel Ansichten

In diesem Thema wird veranschaulicht, wie die Kachel Ansicht für ein Listenansicht-Steuerelement festgelegt wird. In der Kachel Ansicht wird jedes Element durch ein großes Symbol mit einer oder mehreren Zeilen mit begleitenden Text dargestellt. Eine Abbildung finden Sie unter [Informationen zu List-View](list-view-controls-overview.md)-Steuerelementen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Legen Sie die allgemeinen Anzeige Parameter für die Kachel Ansicht fest, indem Sie das [**ListView \_ settileviewinfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) -Makro verwenden. Verwenden Sie die an dieses Makro weiter gegebene " [**lvtileviewinfo**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) "-Struktur, um die Position des Texts in Bezug auf das Symbol, die Größe der einzelnen Kacheln (einschließlich begleitenden Texts) und die maximale Anzahl von Textzeilen anzugeben.

Wenn die Größe der Kacheln nicht automatisch skaliert werden soll, müssen Sie im **dwFlags** -Member und im [**dwtileviewinfo**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) **-Member** **die Größe von \_** " **lvtvif \_ FixedSize** " festlegen und die Dimensionen im **sizetile** -Member bereitstellen.

Im folgenden C++-Codebeispiel werden die Kachel Ansichts Informationen für ein Listenansicht-Steuerelement festgelegt, sodass für jedes Element maximal zwei unter Elemente angezeigt werden. Außerdem wird die Größe der einzelnen Kacheln festgelegt.


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



Für jedes Element in der Liste können Sie weitere Parameter festlegen, wenn das Element in die Liste eingefügt wird, oder später. Die [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, die mit [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) verwendet wird, enthält Elemente, die angeben, welche Datenspalten unterhalb des Elements angezeigt werden sollen, und deren Ausrichtung. Diese gleichen Anzeige Parameter finden Sie auch in der mit [**ListView \_ settileinfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo)verwendeten Struktur " [**lvtileinfo**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) ".

> [!Note]  
> "Columns" bezieht sich hier nicht auf das Anzeigen von Spalten in der Kachel Ansicht, sondern auf unter Elemente, die in den Spalten in der Detailansicht angezeigt werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Listenansicht-Steuerelement Verweis](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informationen zu List-View Steuerelementen](list-view-controls-overview.md)
</dt> <dt>

[Verwenden von List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 




