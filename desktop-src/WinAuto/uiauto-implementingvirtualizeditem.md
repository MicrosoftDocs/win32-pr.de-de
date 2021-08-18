---
title: VirtualizedItem-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IVirtualizedItemProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des VirtualizedItem-Steuerelementmusters
- Benutzeroberflächenautomatisierung,VirtualizedItem-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IVirtualizedItemProvider
- IVirtualizedItemProvider
- Implementieren Benutzeroberflächenautomatisierung VirtualizedItem-Steuerelementmuster
- VirtualizedItem-Steuerelementmuster
- Steuerelementmuster,IVirtualizedItemProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung VirtualizedItem
- Steuerelementmuster,VirtualizedItem
- interfaces,IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d883eec2e0f5fa4c4ede4c3fa2ef73770cc706114b6536ad002d11ff73f8ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997760"
---
# <a name="virtualizeditem-control-pattern"></a>VirtualizedItem-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**IVirtualizedItemProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider)einschließlich Informationen zu Eigenschaften und Methoden. Das **VirtualizedItem-Steuerelementmuster** wird verwendet, um virtualisierte Elemente zu unterstützen, bei denen es sich um Elemente handelt, die durch Platzhalterautomatisierungselemente in der Microsoft Benutzeroberflächenautomatisierung-Struktur dargestellt werden.

Virtualisierte Elemente können Elemente enthalten, die von einem Steuerelement abgerufen werden, das das [ItemContainer-Steuerelementmuster](uiauto-implementingitemcontainer.md) unterstützt, oder ein virtualisiertes eingebettetes Objekt, das von einem Steuerelement abgerufen wird, das das [Text-Steuerelementmuster](uiauto-implementingtextandtextrange.md) unterstützt. Der Platzhalter für ein virtualisiertes Element hat möglicherweise keine Daten für alle Benutzeroberflächenautomatisierung Eigenschaften geladen und gibt [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) als Reaktion auf Abfragen von Eigenschaften zurück, die nicht verfügbar sind. Das **VirtualizedItem-Steuerelementmuster** stellt eine Methode zum Realisieren eines virtuellen Elements bereit, sodass vollständige Informationen für das Element zur Verfügung gestellt werden und ein vollständiges Automatisierungselement für das Element in der Benutzeroberflächenautomatisierung-Struktur erstellt werden kann.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IVirtualizedItemProvider**](#required-members-for-ivirtualizeditemprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **VirtualizedItem-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Jedes Benutzeroberflächenautomatisierung Platzhalterelement, das virtualisiert werden kann, muss das **VirtualizedItem-Steuerelementmuster** unterstützen, indem die [**IVirtualizedItemProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) verfügbar ist.
-   Wenn [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) aufgerufen wird, muss das Platzhalterobjekt mit vollständigen Implementierungen seiner Eigenschaften und Steuerelementmuster aktualisiert werden.
-   Wenn [**IVirtualizedItemProvider::Realize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) aufgerufen wird, kann der Anbieter den Viewport so ändern, dass das virtualisierte Element angezeigt wird. Das Anzeigen des Elements ist nicht erforderlich. Nicht virtualisierte Elemente außerhalb des Bildschirms sollten jedoch die [**IScrollItemProvider::ScrollIntoView-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) unterstützen.

## <a name="required-members-for-ivirtualizeditemprovider"></a>Erforderliche Member für **IVirtualizedItemProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IVirtualizedItemProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) erforderlich.



| Erforderliche Member                                           | Memberart | Hinweise |
|------------------------------------------------------------|-------------|-------|
| [**Erkennen**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren des Benutzeroberflächenautomatisierung ItemContainer-Steuerelementmusters](uiauto-implementingitemcontainer.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[Arbeiten mit virtualisierten Elementen](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




