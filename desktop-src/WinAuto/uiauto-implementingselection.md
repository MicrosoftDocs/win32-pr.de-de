---
title: Auswahlsteuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von ISelectionProvider, einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des Selection-Steuerelementmusters
- Benutzeroberflächenautomatisierung,Auswahlsteuerelementmuster
- Benutzeroberflächenautomatisierung,ISelectionProvider
- ISelectionProvider
- Implementieren von Benutzeroberflächenautomatisierung Selection-Steuerelementmustern
- Auswahlsteuerelementmuster
- Steuerelementmuster,ISelectionProvider
- Steuerelementmuster,Implementieren von Benutzeroberflächenautomatisierung Selection
- Steuerelementmuster,Auswahl
- interfaces,ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d0578dcdcfa9d381272afaa474338a54caa1f4b17989f2461f9aec5086bc18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098320"
---
# <a name="selection-control-pattern"></a>Auswahlsteuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**ISelectionProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen. Das  Auswahlsteuerelementmuster wird verwendet, um Steuerelemente zu unterstützen, die als Container für eine Auflistung auswählbarer untergeordneter Elemente fungieren. Die untergeordneten Elemente dieses Elements müssen [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)implementieren.

Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Steuerelementtypen und deren unterstützte Steuerelementmuster.](uiauto-controlpatternmapping.md)

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **ISelectionProvider**](#required-members-for-iselectionprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Selection-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Steuerelemente, die [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) implementieren, ermöglichen die Auswahl einzelner oder mehrerer untergeordneter Elemente. Listenfelder, Listenansichten und Strukturansichten unterstützen beispielsweise mehrere Auswahlmöglichkeiten, während Kombinationsfelder, Schieberegler und Optionsfeldgruppen eine einzelne Auswahl unterstützen.
-   Steuerelemente, die über einen minimalen, maximalen und kontinuierlichen Bereich verfügen, z. B. das Schieberegler-Steuerelement **Volume** eines Medienplayers, sollten [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) anstelle von [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)implementieren.
-   Steuerelemente mit nur einer Auswahl, die untergeordnete Steuerelemente verwalten, die [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot)implementieren, z. B. den **Bildschirmauflösungsschieberegler** im **dialogfeld Anzeigeeigenschaften** für Windows oder das **Farbwähler** Auswahlsteuerelement aus Microsoft Word (siehe folgende Abbildung), sollten [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)implementieren. ihre untergeordneten Elemente sollten sowohl [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) als [**auch ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)implementieren.

    ![Abbildung eines Beispiels für die Zuordnung von Farbwatchzeichenfolgen](images/uia-valuepattern-colorpicker.jpg)

-   Menüs unterstützen das  Auswahlsteuerelementmuster nicht. Wenn Sie mit Menüelementen arbeiten, die sowohl Grafiken als auch Text enthalten (z. B. die Elemente des **Vorschaubereichs** im Menü **Ansicht** in Microsoft Outlook) und den Zustand vermitteln müssen, sollten Sie [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)implementieren.

## <a name="required-members-for-iselectionprovider"></a>Erforderliche Member für **ISelectionProvider**

Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**ISelectionProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) erforderlich.



| Erforderliche Member                                                                                | Memberart | Hinweise                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | Eigenschaft    | Keine                                                                        |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | Eigenschaft    | Keine                                                                        |
| [**GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | Methode      | Keine                                                                        |
| [**UIA \_ Selection \_ InvalidatedEventId**](uiauto-event-ids.md) | Ereignis       | Auslösen dieses Ereignisses, wenn sich eine Auswahl in einem Container erheblich geändert hat. |



 

Die Eigenschaften [**ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) und [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) können dynamisch sein. Für den Anfangszustand eines Steuerelements sind möglicherweise standardmäßig keine Elemente ausgewählt, was bedeutet, dass **IsSelectionRequired** false ist. Nach dem Auswählen eines Elements muss für das Steuerelement jedoch immer mindestens ein Element ausgewählt sein. Auf ähnliche Weise kann ein Steuerelement in seltenen Fällen bei der Initialisierung die Mehrfachauswahl von Elementen gestatten, während anschließend nur noch die Einfachauswahl zulässig ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[SelectionItem-Steuerelementmuster](uiauto-implementingselectionitem.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




