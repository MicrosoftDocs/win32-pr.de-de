---
title: Arbeiten mit virtualisierten Elementen
description: In diesem Thema wird beschrieben, wie Sie die funktionen verwenden, die von den Steuerelementmustern ItemContainer und VirtualizedItem bereitgestellt werden, um Informationen zu virtualisierten Elementen zu suchen und abzurufen.
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- Clients,Benutzeroberflächenautomatisierung virtualisierte Elemente
- Clients,virtualisierte Elemente
- Clients,Steuerelementmuster
- Clients,VirtualizedItem-Steuerelementmuster
- clients,ItemContainer-Steuerelementmuster
- clients,Benutzeroberflächenautomatisierung VirtualizedItem-Steuerelementmuster
- Clients,Benutzeroberflächenautomatisierung Steuerelementmuster
- clients,Benutzeroberflächenautomatisierung ItemContainer-Steuerelementmuster
- Benutzeroberflächenautomatisierung,virtualisierte Elemente
- Benutzeroberflächenautomatisierung,Steuerelementmuster
- Benutzeroberflächenautomatisierung,VirtualizedItem-Steuerelementmuster
- Benutzeroberflächenautomatisierung,ItemContainer-Steuerelementmuster
- VirtualizedItem-Steuerelementmuster
- ItemContainer-Steuerelementmuster
- Steuerelementmuster, VirtualizedItem
- Steuerelementmuster, ItemContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2c0e84f91af6bcaadef5af373b73057fb4a137480255f3ee1af4456e45eaf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570370"
---
# <a name="working-with-virtualized-items"></a>Arbeiten mit virtualisierten Elementen

In diesem Thema wird beschrieben, wie Sie die funktionen verwenden, die von [den Steuerelementmustern ItemContainer](uiauto-implementingitemcontainer.md) und [VirtualizedItem](uiauto-implementingvirtualizeditem.md) bereitgestellt werden, um Informationen zu virtualisierten Elementen zu suchen und abzurufen.

-   [Übersicht über die Virtualisierung](#overview-of-virtualization)
-   [Unterstützung der Virtualisierung durch ein Steuerelement](#how-a-control-supports-virtualization)
-   [Suchen und Realisieren virtualisierter Elemente durch Clients](#how-clients-find-and-realize-virtualized-items)
-   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-virtualization"></a>Übersicht über die Virtualisierung

Steuerelemente, die eine große Anzahl untergeordneter Elemente enthalten, können die Virtualisierung verwenden, um die Elemente effizient zu verwalten. Bei der Virtualisierung behält das Steuerelement vollständige Informationen im Arbeitsspeicher für nur eine Teilmenge von Elementen zu einem bestimmten Zeitpunkt bei. In der Regel enthält die Teilmenge nur die Elemente, die derzeit für den Benutzer sichtbar sind. Vollständige Informationen zu den verbleibenden virtualisierten Elementen werden im Speicher gespeichert und in den Arbeitsspeicher geladen oder realisiert, da das Steuerelement dies benötigt, z. B. wenn neue Elemente für den Benutzer sichtbar werden.

Steuerelemente, die Virtualisierung verwenden, stellen eine Herausforderung dar, da nur realisierte Elemente vollständig verfügbar sind, da Microsoft Benutzeroberflächenautomatisierung Elemente in der Benutzeroberflächenautomatisierung ist. Virtualisierte Elemente sind in der Struktur nicht vorhanden, sodass Clients keine Informationen darüber erhalten. Um Informationen zu virtualisierten Elementen abzurufen, benötigen Clients eine Möglichkeit, Benutzeroberflächenautomatisierung, die Anforderung zu übergeben, um die Elemente an das Steuerelement zu realisieren. Nachdem die Elemente realisiert wurden, kann Benutzeroberflächenautomatisierung elemente Benutzeroberflächenautomatisierung für sie erstellen. Benutzeroberflächenautomatisierung enthält zwei Steuerelementmuster, mit denen Clients mit virtualisierten Elementen arbeiten können: [ItemContainer](uiauto-implementingitemcontainer.md) und [VirtualizedItem.](uiauto-implementingvirtualizeditem.md)

## <a name="how-a-control-supports-virtualization"></a>Unterstützung der Virtualisierung durch ein Steuerelement

Jedes Steuerelement, das virtualisierte Elemente enthalten kann, muss das [ItemContainer-Steuerelementmuster](uiauto-implementingitemcontainer.md) unterstützen. Darüber hinaus muss jedes Element, das virtualisiert werden kann, das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) unterstützen. Clients können über die Schnittstellen [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) und [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) auf die Funktionalität zugreifen, die von den Steuerelementmustern ItemContainer und VirtualizedItem verfügbar gemacht wird.

## <a name="how-clients-find-and-realize-virtualized-items"></a>Suchen und Realisieren virtualisierter Elemente durch Clients

Clients können die [**IUIAutomationItemContainerPattern::FindItemByProperty-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) verwenden, um nach untergeordneten Elementen im Container basierend auf dem Wert einer bestimmten Eigenschaft zu suchen. Die -Methode kann auch das erste Element im Container oder das Element abrufen, das dem angegebenen Element folgt. Wenn ein übereinstimmende untergeordnetes Element gefunden wird, ruft **FindItemByProperty** eine [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) für das Element ab. Wenn das untergeordnete Element jedoch virtualisiert wird, ist die **IUIAutomationElement-Schnittstelle** ein Platzhalter. Der [**UIA \_ E \_ ELEMENTNOTAVAILABLE-Fehler**](uiauto-error-codes.md) tritt auf, wenn der Client versucht, die **IUIAutomationElement-Schnittstelle** zum Abrufen von Eigenschaftswerten oder Aufrufmethoden zu verwenden, die noch nicht verfügbar sind. Welche Eigenschaften oder Methoden über einen Platzhalter verfügbar sind, hängt von der Implementierung des Steuerelements ab. Die einzige Anforderung für einen Platzhalter ist die Unterstützung der [**IUIAutomationVirtualizedItemPattern-Schnittstelle.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern)

Der [**UIA \_ E \_ ELEMENTNOTAVAILABLE-Fehler**](uiauto-error-codes.md) ist ein Hinweis für den Client, dass ein Element virtualisiert werden kann. Der Client sollte antworten, indem er die [**IUIAutomationVirtualizedItemPattern-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) für das Element abruft und dann das Element durch Aufrufen der [**IUIAutomationVirtualizedItemPattern::Realize-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) erkennt. Wenn dies erfolgreich ist, ist die [**IUIAutomationElement-Schnittstelle**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) voll funktionsfähig, und alle entsprechenden Eigenschaften sind verfügbar.

Je nach Implementierung des Steuerelements kann der Aufruf von [**IUIAutomationVirtualizedItemPattern::Realize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) dazu führen, dass das Steuerelement das Element in die Ansicht scrollt. Ein Client sollte sich jedoch nicht darauf verlassen, dass das Element in die Ansicht scrollt oder sichtbar gemacht wird. Um sicherzustellen, dass das Element sichtbar ist, kann der Client die [**IUIAutomationScrollItemPattern::ScrollIntoView-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview) verwenden.

## <a name="example"></a>Beispiel

Beispielcode, der zeigt, wie die Benutzeroberflächenautomatisierung Virtualisierungsunterstützung verwendet wird, finden Sie unter Abrufen eines [virtualisierten Elements.](uiauto-howto-retrieve-virtualized-item.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




