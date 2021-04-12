---
title: MultipleView-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IMultipleViewProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des MultipleView-Steuerelement Musters
- UI-Automatisierung, MultipleView-Steuerelement Muster
- UI-Automatisierung, IMultipleViewProvider
- IMultipleViewProvider
- Implementieren von MultipleView-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- MultipleView-Steuerelement Muster
- Steuerelement Muster, IMultipleViewProvider
- Steuerelement Muster, Implementieren der UI-Automatisierung MultipleView
- Steuerelement Muster, MultipleView
- Schnittstellen, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388452"
---
# <a name="multipleview-control-pattern"></a>MultipleView-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), einschließlich Informationen zu Eigenschaften und Methoden. Links zu zusätzlichen Referenzen sind am Ende dieses Themas aufgelistet. Das **MultipleView** -Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die mehrere Darstellungen derselben Informationen oder desselben Satzes von untergeordneten Steuerelementen bereitstellen und zwischen diesen wechseln können.

Beispiele für Steuerelemente, die mehrere Ansichten darstellen können, sind die Listenansicht (die den Inhalt als Miniaturansichten anzeigen kann. Kacheln, Symbole oder Details), Microsoft Excel-Diagramme (Kreis-, Linien-, Balken-, Zellwert mit einer Formel), Microsoft Word-Dokumente (normal, Weblayout, Drucklayout, Lese Layout, Gliederung), Microsoft Outlook-Kalender (Jahr, Monat, Woche, Tag) und Microsoft Windows Media Player Skins. Die unterstützten Ansichten werden vom Steuerelemententwickler bestimmt und sind für jedes Steuerelement spezifisch.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IMultipleViewProvider**](#required-members-for-imultipleviewprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **MultipleView** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) sollte auch für einen Container implementiert werden, der die aktuelle Ansicht verwaltet, wenn Sie sich von einem Steuerelement unterscheidet, das die aktuelle Ansicht bereitstellt. Windows-Explorer enthält z. b. ein Listen Steuerelement für den aktuellen Ordner Inhalt, während die Ansicht für das Steuerelement über die Windows Explorer-Anwendung verwaltet wird.
-   Ein Steuerelement, das seinen Inhalt sortieren kann, wird nicht als Steuerelement betrachtet, das mehrere Ansichten unterstützt.
-   Die Auflistung von Ansichten muss instanzenübergreifend identisch sein.
-   Ansichts Namen müssen für Text-zu-Sprache, Braille und andere lesbare Anwendungen geeignet sein.

## <a name="required-members-for-imultipleviewprovider"></a>Erforderliche Member für **IMultipleViewProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                            | Memberart | Hinweise |
|-----------------------------------------------------------------------------|-------------|-------|
| [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | Eigenschaft    | Keine  |
| [**GetSupportedViews**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | Methode      | Keine  |
| [**GetViewName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | Methode      | Keine  |
| [**SetCurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[ExpandCollapse-Steuerelement Muster](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




