---
title: Auswahl Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von ISelectionProvider, einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Auswahl Steuerelement Musters
- UI-Automatisierung, Auswahl Steuerelement Muster
- UI-Automatisierung, ISelectionProvider
- ISelectionProvider
- Implementieren von Auswahl Steuerelement Mustern für Benutzeroberflächen Automatisierung
- Auswahl Steuerelement Muster
- Steuerelement Muster, ISelectionProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-Auswahl
- Steuerelement Muster, Auswahl
- Schnittstellen, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037021"
---
# <a name="selection-control-pattern"></a>Auswahl Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen. Das **Auswahl** Steuerelement Muster wird zur Unterstützung von Steuerelementen verwendet, die als Container für eine Auflistung von auswählbaren untergeordneten Elementen fungieren. Die untergeordneten Elemente dieses Elements müssen [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)implementieren.

Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ISelectionProvider**](#required-members-for-iselectionprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Selection** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Bei Steuerelementen, die [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) implementieren, kann entweder ein oder mehrere untergeordnete Elemente ausgewählt werden. Listenfelder, Listenansichten und Struktur Ansichten unterstützen z. b. Mehrfachauswahl, während Kombinations Felder, Schieberegler und Optionsfeld Gruppen die einfache Auswahl unterstützen.
-   Steuerelemente, die einen minimalen, maximalen und kontinuierlichen Bereich aufweisen, wie z. b. das **Volume** Slider-Steuerelement eines Media Players, sollten [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) anstelle von [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)implementieren.
-   Steuerelemente mit einfacher Auswahl, die untergeordnete Steuerelemente verwalten, die [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)implementieren, z. b. den Schieberegler **Bildschirmauflösung** im Dialogfeld **Anzeigeeigenschaften** für Windows oder das **Farb** Auswahl-Auswahl Steuerelement von Microsoft Word (siehe folgende Abbildung), sollte [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); implementieren. die untergeordneten Elemente sollten sowohl " [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) " als auch " [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)" implementieren.

    ![Bild mit einem Beispiel für Zeichen folgen Zuordnung von Farbmustern](images/uia-valuepattern-colorpicker.jpg)

-   Menüs unterstützen das **Auswahl** Steuerelement Muster nicht. Wenn Sie mit Menü Elementen arbeiten, die Grafiken und Text enthalten (z. b. die Elemente im **Vorschau** Bereich im Menü **Ansicht** in Microsoft Outlook) und den Zustand übermitteln müssen, sollten Sie [**ideggleprovider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)implementieren.

## <a name="required-members-for-iselectionprovider"></a>Erforderliche Member für **ISelectionProvider**

Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                                | Memberart | Hinweise                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | Eigenschaft    | Keine                                                                        |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | Eigenschaft    | Keine                                                                        |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | Methode      | Keine                                                                        |
| [**UIA- \_ Auswahl \_ invalidatedeventid**](uiauto-event-ids.md) | Ereignis       | Dieses Ereignis wird durch eine deutliche Änderung einer Auswahl in einem Container angehoben. |



 

Die Eigenschaften " [**ISelectionProvider:: IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) " und " [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) " können dynamisch sein. Beispielsweise können für den ursprünglichen Zustand eines Steuer Elements keine Elemente standardmäßig ausgewählt werden, was darauf hinweist, dass **IsSelectionRequired** false ist. Nach dem Auswählen eines Elements muss für das Steuerelement jedoch immer mindestens ein Element ausgewählt sein. Auf ähnliche Weise kann ein Steuerelement in seltenen Fällen bei der Initialisierung die Mehrfachauswahl von Elementen gestatten, während anschließend nur noch die Einfachauswahl zulässig ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[SelectionItem-Steuerelement Muster](uiauto-implementingselectionitem.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




