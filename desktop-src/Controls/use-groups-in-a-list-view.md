---
title: Vorgehensweise beim Verwenden von Gruppen in einer List-View
description: In diesem Thema wird beschrieben, wie eine Instanz einer Gruppe erstellt und einem Listenansicht-Steuerelement hinzugefügt wird.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec47d73c3e8b808eaf1909bdafb015c7eebc37de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103858557"
---
# <a name="how-to-use-groups-in-a-list-view"></a>Vorgehensweise beim Verwenden von Gruppen in einer List-View

In diesem Thema wird beschrieben, wie eine Instanz einer Gruppe erstellt und einem Listenansicht-Steuerelement hinzugefügt wird. Mithilfe von Gruppierungen kann ein Benutzer Listen in Gruppen von Elementen anordnen, die mithilfe eines horizontalen unter Teilers und eines Gruppen Titels visuell auf der Seite aufgeteilt sind.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Windows-Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Programmieren der Windows-Benutzeroberfläche

## <a name="instructions"></a>Anweisungen


Um Gruppen in einem Listenansicht-Steuerelement zu verwenden, stellen Sie sicher, dass das Steuerelement den [**LVS \_ AlignTop**](list-view-window-styles.md) -Fenster Stil enthält.

Wenn Sie der Liste ein Element hinzufügen, weisen Sie es einer Gruppe zu, indem Sie den **igroupid** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur des Elements auf den Wert des **igroupid** -Members der Struktur der [**Gruppe "LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) " festlegen. Ein Element, das keiner Gruppe zugewiesen ist, wird nicht in der Liste angezeigt, wenn die Gruppenansicht aktiviert ist. Verwenden Sie das [**ListView \_ enablegroupview**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) -Makro, um die Gruppenansicht zu aktivieren oder zu deaktivieren.

Im folgenden Beispiel wird gezeigt, wie eine Gruppe mit einem Header erstellt und einem Listenansicht-Steuerelement hinzugefügt wird.


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Listenansicht-Steuerelement Verweis](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informationen zu List-View Steuerelementen](list-view-controls-overview.md)
</dt> <dt>

[Verwenden von List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 




