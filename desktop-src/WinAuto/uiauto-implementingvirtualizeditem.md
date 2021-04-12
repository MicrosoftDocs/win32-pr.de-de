---
title: VirtualizedItem-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen für das Implementieren von IVirtualizedItemProvider, einschließlich Informationen zu Eigenschaften und Methoden.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- Benutzeroberflächen Automatisierung, Implementieren des VirtualizedItem-Steuerelement Musters
- UI-Automatisierung, VirtualizedItem-Steuerelement Muster
- UI-Automatisierung, IVirtualizedItemProvider
- IVirtualizedItemProvider
- Implementieren von VirtualizedItem-Steuerelement Mustern für Benutzeroberflächen Automatisierung
- VirtualizedItem-Steuerelement Muster
- Steuerelement Muster, IVirtualizedItemProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-VirtualizedItem
- Steuerelement Muster, VirtualizedItem
- Schnittstellen, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207426"
---
# <a name="virtualizeditem-control-pattern"></a>VirtualizedItem-Steuerelement Muster

Beschreibt Richtlinien und Konventionen für das Implementieren von [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), einschließlich Informationen zu Eigenschaften und Methoden. Das **VirtualizedItem** -Steuerelement Muster wird zur Unterstützung von virtualisierten Elementen verwendet, bei denen es sich um Elemente handelt, die durch Platzhalter-Automatisierungselemente in der Microsoft UI Automation-Struktur dargestellt werden.

Virtualisierte Elemente können Elemente enthalten, die von einem Steuerelement abgerufen werden, das das [ItemContainer](uiauto-implementingitemcontainer.md) -Steuerelement Muster unterstützt, oder ein virtualisiertes eingebettetes Objekt, das von einem Steuerelement abgerufen wird, das das [Text](uiauto-implementingtextandtextrange.md) - Der Platzhalter für ein virtualisiertes Element hat möglicherweise keine Daten für alle Benutzeroberflächenautomatisierungs-Eigenschaften geladen und gibt [**ggf. UIA \_ E \_ elementnotavailable**](uiauto-error-codes.md) als Reaktion auf Abfragen von Eigenschaften zurück, die nicht verfügbar sind. Das **VirtualizedItem** -Steuerelement Muster bietet eine Methode zum Erkennen eines virtuellen Elements, sodass vollständige Informationen für das Element verfügbar gemacht werden und ein vollständiges Automation-Element für das Element in der Benutzeroberflächenautomatisierungs-Struktur erstellt werden kann.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für **IVirtualizedItemProvider**](#required-members-for-ivirtualizeditemprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **VirtualizedItem** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Alle Benutzeroberflächen-Automatisierungs Platzhalter Elemente, die virtualisiert werden können, müssen das **VirtualizedItem** -Steuerelement Muster unterstützen, indem die [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) -Schnittstelle verfügbar gemacht wird
-   Wenn [**IVirtualizedItemProvider:: merkt**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) aufgerufen wird, muss das Platzhalter Objekt mit vollständigen Implementierungen seiner Eigenschaften und Steuerelement Muster aktualisiert werden.
-   Wenn [**IVirtualizedItemProvider:: merkt**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) aufgerufen wird, kann der Anbieter den Viewport so ändern, dass das virtualisierte Element in der Ansicht angezeigt wird. Das Element in die Ansicht zu bringen, ist nicht erforderlich. nicht virtualisierte Elemente, die auf dem Bildschirm angezeigt werden, sollten jedoch die [**IScrollItemProvider:: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) -Methode unterstützen.

## <a name="required-members-for-ivirtualizeditemprovider"></a>Erforderliche Member für **IVirtualizedItemProvider**

Die folgenden Eigenschaften und Methoden sind für die Implementierung der [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                           | Memberart | Hinweise |
|------------------------------------------------------------|-------------|-------|
| [**Erkannten**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | Methode      | Keine  |



 

Diesem Steuerelementmuster sind keine Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren des ItemContainer-Steuerelement Musters der Benutzeroberflächen Automatisierung](uiauto-implementingitemcontainer.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[Arbeiten mit virtualisierten Elementen](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




