---
title: MultipleView-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IMultipleViewProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des MultipleView-Steuerelementmusters
- Benutzeroberflächenautomatisierung,MultipleView-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IMultipleViewProvider
- IMultipleViewProvider
- Implementieren von Benutzeroberflächenautomatisierung MultipleView-Steuerelementmustern
- MultipleView-Steuerelementmuster
- Steuerelementmuster,IMultipleViewProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung MultipleView
- Steuerelementmuster, MultipleView
- interfaces,IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a5848a521da45470854bd860d3ee9c582e18fc84783ca8072ad552fd91a8d1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115003"
---
# <a name="multipleview-control-pattern"></a>MultipleView-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**IMultipleViewProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)einschließlich Informationen zu Eigenschaften und Methoden. Links zu zusätzlichen Referenzen sind am Ende dieses Themas aufgelistet. Das **MultipleView-Steuerelementmuster** wird verwendet, um Steuerelemente zu unterstützen, die mehrere Darstellungen derselben Informationen oder desselben Satzes von untergeordneten Steuerelementen bereitstellen und zwischen diesen wechseln können.

Beispiele für Steuerelemente, die mehrere Ansichten darstellen können, sind die Listenansicht (die ihren Inhalt als Miniaturansichten, Kacheln, Symbole oder Details anzeigen kann), Microsoft Excel Diagramme (Kreis, Linie, Leiste, Zellenwert mit einer Formel), Microsoft Word Dokumente (normal, Weblayout, Drucklayout, Leselayout, Kontur), Microsoft Outlook Kalender (Jahr, Monat, Woche, Tag) und Microsoft Windows Media Player Skins. Die unterstützten Ansichten werden vom Steuerelemententwickler bestimmt und sind für jedes Steuerelement spezifisch.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IMultipleViewProvider**](#required-members-for-imultipleviewprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie  beim Implementieren des MultipleView-Steuerelementmusters die folgenden Richtlinien und Konventionen:

-   [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) sollte auch für einen Container implementiert werden, der die aktuelle Ansicht verwaltet, wenn sie sich von einem Steuerelement unterscheidet, das die aktuelle Ansicht bereitstellt. Beispielsweise enthält Windows Explorer ein Listensteuerelement für den aktuellen Ordnerinhalt, während die Ansicht für das Steuerelement über die Windows Explorer-Anwendung verwaltet wird.
-   Ein Steuerelement, das seinen Inhalt sortieren kann, wird nicht als Steuerelement betrachtet, das mehrere Ansichten unterstützt.
-   Die Auflistung von Ansichten muss instanzenübergreifend identisch sein.
-   Ansichtsnamen müssen für die Verwendung in Text-to-Speech, Braanmeldung und anderen für Menschen lesbaren Anwendungen geeignet sein.

## <a name="required-members-for-imultipleviewprovider"></a>Erforderliche Member für **IMultipleViewProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IMultipleViewProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) erforderlich.



| Erforderliche Member                                                            | Memberart | Hinweise |
|-----------------------------------------------------------------------------|-------------|-------|
| [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | Eigenschaft    | Keine  |
| [**GetSupportedViews**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | Methode      | Keine  |
| [**GetViewName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | Methode      | Keine  |
| [**SetCurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




