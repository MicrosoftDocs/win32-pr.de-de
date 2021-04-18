---
title: SelectionItem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ISelectionItemProvider, einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des SelectionItem-Steuerelement Musters
- UI-Automatisierung, SelectionItem-Steuerelement Muster
- Benutzeroberflächenautomatisierung, ISelectionItemProvider
- ISelectionItemProvider
- Implementieren von SelectionItem-Steuerelement Mustern für Benutzeroberflächen
- SelectionItem-Steuerelement Muster
- Steuerelement Muster, ISelectionItemProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-SelectionItem
- Steuerelement Muster, SelectionItem
- Schnittstellen, ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340816"
---
# <a name="selectionitem-control-pattern"></a>SelectionItem-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen. Das **SelectionItem** -Steuerelement Muster dient zur Unterstützung von Steuerelementen, die als einzelne, auswählbare untergeordnete Elemente von Container Steuerelementen fungieren, die [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)implementieren.

Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ISelectionItemProvider**](#required-members-for-iselectionitemprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **SelectionItem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Steuerelemente mit einfacher Auswahl, die untergeordnete Steuerelemente verwalten, die [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)implementieren, wie z. b. der Schieberegler **Bildschirmauflösung** im Dialogfeld **Anzeigeeigenschaften** für Windows, sollten [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); implementieren. die untergeordneten Elemente sollten sowohl " [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) " als auch " [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)" implementieren.

## <a name="required-members-for-iselectionitemprovider"></a>Erforderliche Member für **ISelectionItemProvider**

Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                                                                        | Memberart | Hinweise |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [**Addzu Selection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | Methode      | Keine  |
| [**IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | Eigenschaft    | Keine  |
| [**RemoveFromSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | Methode      | Keine  |
| [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | Methode      | Keine  |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | Eigenschaft    | Keine  |
| [**UIA \_ SelectionItem \_ elementaddecodto selectioneventid**](uiauto-event-ids.md)         | Ereignis       | Keine  |
| [**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**](uiauto-event-ids.md) | Ereignis       | Keine  |
| [**UIA \_ SelectionItem \_ elementselectedebug**](uiauto-event-ids.md)                         | Ereignis       | Keine  |



 

Wenn das Ergebnis einer [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)-, [**addabselection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)-oder [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) -Option ein einzelnes ausgewähltes Element ist, ein **Element selected** -Ereignis ([**UIA \_ SelectionItem \_ elementselectedeventid**](uiauto-event-ids.md)) sollte ausgelöst werden. andernfalls werden die Ereignisse **elementaddeddeselection** ([**UIA \_ SelectionItem \_ elementaddeddeselectioneventid**](uiauto-event-ids.md)) oder **elementremovedfromselection** ([**UIA \_ SelectionItem \_ elementremovedfromselectioneventid**](uiauto-event-ids.md)) nach Bedarf ausgelöst.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




