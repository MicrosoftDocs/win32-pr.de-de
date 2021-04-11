---
title: ScrollItem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IScrollItemProvider, einschließlich Informationen zu-Methoden.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des ScrollItem-Steuerelement Musters
- UI-Automatisierung, ScrollItem-Steuerelement Muster
- UI-Automatisierung, IScrollItemProvider
- IScrollItemProvider
- Implementieren von ScrollItem-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- ScrollItem-Steuerelement Muster
- Steuerelement Muster, IScrollItemProvider
- Steuerelement Muster, Implementieren von Benutzeroberflächen Automatisierung (ScrollItem)
- Steuerelement Muster, ScrollItem
- Schnittstellen, IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206897"
---
# <a name="scrollitem-control-pattern"></a>ScrollItem-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), einschließlich Informationen zu-Methoden. Das **ScrollItem** -Steuerelement Muster wird verwendet, um einzelne untergeordnete Steuerelemente von Containern zu unterstützen, die [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)implementieren. Das vorhanden sein des **ScrollItem** -Steuerelement Musters in einem-Steuerelement impliziert nicht, dass sein Container oder ein Vorgänger das **Scroll** -Steuerelement Muster implementieren muss.

Wenn der Container das **Scroll** -Steuerelement Muster implementiert, fungiert das **ScrollItem** -Steuerelement Muster als Kommunikationskanal zwischen einem untergeordneten Steuerelement und seinem Container, um sicherzustellen, dass der Container den aktuell sichtbaren Inhalt (oder die Region) innerhalb des Viewports ändern kann, um das untergeordnete Steuerelement anzuzeigen. Beispiele für Steuerelemente, die dieses Steuerelement Muster implementieren, finden Sie [unter Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md).

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IScrollItemProvider**](#required-members-for-iscrollitemprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **ScrollItem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Elemente, die in einem [Fenster](uiauto-supportwindowcontroltype.md) -oder **Canvas** -Steuerelement enthalten sind, müssen nicht die [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) -Schnittstelle implementieren. Als Alternative müssen Sie jedoch einen gültigen Speicherort für die Eigenschaft [**iuiautomationelement:: currentboundingrechteck**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (oder [**cachedboundingrechteck**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)) verfügbar machen. Dadurch kann eine Microsoft UI Automation-Client Anwendung die [**iuiautomationscrollpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) -Steuerelement Muster-Methoden für den Container verwenden, um das untergeordnete Element anzuzeigen.

## <a name="required-members-for-iscrollitemprovider"></a>Erforderliche Member für **IScrollItemProvider**

Die folgende Methode ist für die Implementierung der [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                    | Memberart | Hinweise |
|---------------------------------------------------------------------|-------------|-------|
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Eigenschaften oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Auswahl Steuerelement Muster](uiauto-implementingselection.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> </dl>

 

 




