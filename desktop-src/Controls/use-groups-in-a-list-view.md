---
title: Verwenden von Gruppen in einem List-View
description: In diesem Thema wird beschrieben, wie Eine Instanz einer Gruppe erstellt und einem Listenansicht-Steuerelement hinzugefügt wird.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edaad657d9ea6b71bac1d06a34a0aa29b99c26e204629e503a9e55531da162b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132120"
---
# <a name="how-to-use-groups-in-a-list-view"></a>Verwenden von Gruppen in einem List-View

In diesem Thema wird beschrieben, wie Eine Instanz einer Gruppe erstellt und einem Listenansicht-Steuerelement hinzugefügt wird. Das Gruppieren ermöglicht es einem Benutzer, Listen mithilfe eines horizontalen Unterteilers und eines Gruppentitels in Gruppen von Elementen zu ordnen, die visuell auf der Seite unterteilt sind.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Windows Steuerelemente](window-controls.md)

### <a name="prerequisites"></a>Voraussetzungen

-   C/C++
-   Windows Benutzeroberfläche-Programmierung

## <a name="instructions"></a>Anweisungen


Um Gruppen in einem Listenansicht-Steuerelement zu verwenden, stellen Sie sicher, dass das Steuerelement den [**LVS \_ ALIGNTOP-Fensterstil**](list-view-window-styles.md) enthält.

Wenn Sie der Liste ein Element hinzufügen, weisen Sie es einer Gruppe zu, indem Sie das **iGroupId-Element** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) des Elements auf den Wert des **iGroupId-Elements** der [**LVGROUP-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) der Gruppen festlegen. Ein Element, das einer Gruppe nicht zugewiesen ist, wird nicht in der Liste angezeigt, wenn die Gruppenansicht aktiviert ist. Verwenden Sie das [**Makro ListView \_ EnableGroupView,**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) um die Gruppenansicht zu aktivieren oder zu deaktivieren.

Das folgende Beispiel zeigt, wie Sie eine Gruppe mit einem Header erstellen und einem Listenansicht-Steuerelement hinzufügen.


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

[List-View-Steuerelementreferenz](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informationen List-View Steuerelementen](list-view-controls-overview.md)
</dt> <dt>

[Verwenden List-View Steuerelementen](using-list-view-controls.md)
</dt> </dl>

 

 




