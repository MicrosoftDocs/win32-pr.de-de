---
title: Verwenden List-View Arbeitsbereichen
description: In diesem Thema wird die Arbeit mit Arbeitsbereichen in der Listenansicht veranschaulicht. Arbeitsbereiche sind rechteckige virtuelle Bereiche, die zum Anordnen von Elementen in einem List-VEW-Steuerelement verwendet werden können.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036794"
---
# <a name="how-to-use-list-view-working-areas"></a>Verwenden List-View Arbeitsbereichen

In diesem Thema wird die Arbeit mit Arbeitsbereichen in der Listenansicht veranschaulicht. Arbeitsbereiche sind rechteckige virtuelle Bereiche, die zum Anordnen von Elementen in einem List-VEW-Steuerelement verwendet werden können. Ein Arbeitsbereich ist kein Fenster und kann keinen sichtbaren Rahmen aufweisen. Standardmäßig weist das Listenansicht-Steuerelement keine Arbeitsbereiche auf. Wenn Sie einen Arbeitsbereich erstellen, können Sie Links, oben oder rechts von den Elementen einen leeren Rahmen erstellen oder eine horizontale Schiebe Leiste anzeigen, wenn es normalerweise keine wäre.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen

### <a name="create-a-working-area"></a>Erstellen eines Arbeitsbereichs

Im folgenden C++-Codebeispiel wird veranschaulicht, wie ein Arbeitsbereich mit einem leeren 25-Pixel-Rahmen auf der oberen, linken und rechten Seite erstellt wird.


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a>Erstellen mehrerer Arbeitsbereiche

Im folgenden C++-Codebeispiel wird veranschaulicht, wie zwei Arbeitsbereiche in einem-Steuerelement erstellt werden. Jeder Arbeitsbereich verwendet ungefähr die Hälfte des Client Bereichs und ist von einem leeren 25-Pixel-Rahmen umgeben.


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a>Bestimmen Sie den Arbeitsbereich, zu dem ein Element gehört.

Eine Möglichkeit, zu bestimmen, zu welchem Arbeitsbereich ein Element gehört, besteht darin, die folgenden Aufgaben durchzuführen:

-   Rufen Sie die Liste der Koordinaten aller Arbeitsbereiche im Listenansicht-Steuerelement ab.
-   Ruft die Koordinaten des Elements ab.
-   Bestimmen Sie, ob die Element Koordinaten innerhalb der Koordinaten eines der Arbeitsbereiche liegen.

Die Anwendungs definierte Funktion im folgenden C++-Codebeispiel gibt den Index des Arbeitsbereichs zurück, zu dem das Element gehört. Wenn die Funktion fehlschlägt, wird – 1 zurückgegeben. Wenn die Funktion erfolgreich ausgeführt wird, das Element aber nicht in einem der Arbeitsbereiche vorhanden ist, gibt die Funktion 0 zurück, da alle Elemente, die sich nicht in einem Arbeitsbereich befinden, automatisch zu einem Member des Arbeitsbereichs NULL werden.


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Listenansicht-Steuerelement Verweis](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informationen zu List-View Steuerelementen](list-view-controls-overview.md)
</dt> <dt>

[Verwenden von List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 




