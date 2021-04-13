---
title: Window-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IWindowProvider, einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen. Das Window-Steuerelement Muster unterstützt Steuerelemente, die grundlegende fensterbasierte Funktionen in einer herkömmlichen GUI bereitstellen.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- Benutzeroberflächen Automatisierung, Implementieren eines Fenster Steuerelement Musters
- UI-Automatisierung, Window-Steuerelement Muster
- UI-Automatisierung, IWindowProvider
- IWindowProvider
- Implementieren von Steuerelement Mustern für Benutzeroberflächen Automatisierung
- Window-Steuerelement Muster
- Steuerelement Muster, IWindowProvider
- Steuerelement Muster, Implementieren des Benutzeroberflächenautomatisierungs-Fensters
- Steuerelement Muster, Fenster
- Schnittstellen, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311345"
---
# <a name="window-control-pattern"></a>Window-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), einschließlich Informationen zu Eigenschaften, Methoden und Ereignissen. Das **Window** -Steuerelement Muster unterstützt Steuerelemente, die grundlegende fensterbasierte Funktionen in einer herkömmlichen GUI bereitstellen.

Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren müssen, sind u. a. Anwendungsfenster der obersten Ebene, untergeordnete MDI-Fenster (Multiple Document Interface), in der Größe umsetzbare Steuerelemente für geteilte Bereiche, Modale Dialoge und Beispiele für Steuerelemente, die dieses Steuerelementmuster implementieren, finden Sie unter [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IWindowProvider**](#required-members-for-iwindowprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **Window** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Um die Möglichkeit zum Ändern der Fenstergröße und Bildschirmposition mithilfe der Microsoft-Benutzeroberflächen Automatisierung zu unterstützen, muss ein Steuerelement zusätzlich zu [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) implementieren.
-   Steuerelemente, die Titelleisten und Titelleisten Elemente enthalten, mit denen das Steuerelement verschoben, verkleinert, minimiert oder geschlossen werden kann, sind in der Regel für die Implementierung von [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)erforderlich.
-   Steuerelemente wie QuickInfo-Popups und Kombinations Feld-oder Menü-Dropdown-Elemente implementieren i. d. d. [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)nicht.
-   Die Hilfefenster der Sprechblase unterscheiden sich von einfachen QuickInfo-Popups durch die Bereitstellung einer Fenster ähnlichen Schaltfläche " **Schließen** ".
-   Der Vollbildmodus wird von [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) nicht unterstützt, da er featurespezifisch für eine Anwendung ist und kein typisches Fenster Verhalten ist.

## <a name="required-members-for-iwindowprovider"></a>Erforderliche Member für **IWindowProvider**

Die folgenden Eigenschaften, Methoden und Ereignisse sind für die Implementierung der [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                                            | Memberart | Hinweise                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**Windowinteraktionstate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | Eigenschaft    | Es ist nicht garantiert, dass " **windowinteraktionstate" " \_ synchyforuserinteraction** " ist. |
| [**IsModal**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | Eigenschaft    | Keine                                                                        |
| [**IsTopmost**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | Eigenschaft    | Keine                                                                        |
| [**Canmaximi**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | Eigenschaft    | Keine                                                                        |
| [**Canmini mieren**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | Eigenschaft    | Keine                                                                        |
| [**WindowVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | Eigenschaft    | Keine                                                                        |
| [**Schließen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | Methode      | Keine                                                                        |
| [**SetVisualState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | Methode      | Keine                                                                        |
| [**WaitForInputIdle**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | Methode      | Keine                                                                        |
| [**UIA \_ \_ -Fenster windowclosedeventid**](uiauto-event-ids.md) | Ereignis       | Keine                                                                        |
| [**UIA \_ \_ -Fenster windowopenedeventid**](uiauto-event-ids.md) | Ereignis       | Keine                                                                        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Zuordnen von Steuerelementmustern für Benutzeroberflächenautomatisierungs-Clients](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




