---
title: Arbeiten mit virtualisierten Elementen
description: In diesem Thema wird beschrieben, wie die vom ItemContainer-und VirtualizedItem-Steuerelement Mustern bereitgestellten Funktionen verwendet werden, um Informationen zu virtualisierten Elementen zu suchen und abzurufen.
ms.assetid: e1898ba0-5ffa-4c61-b378-c7ef7c4a2c52
keywords:
- Clients, Benutzeroberflächenautomatisierungs-virtualisierte Elemente
- Clients, virtualisierte Elemente
- Clients, Steuerelement Muster
- Clients, VirtualizedItem-Steuerelement Muster
- Clients, ItemContainer-Steuerelement Muster
- Clients, Benutzeroberflächenautomatisierungs-VirtualizedItem-Steuerelement Muster
- Clients, Benutzeroberflächenautomatisierungs-Steuerelement Muster
- Clients, UI-Automatisierung, ItemContainer-Steuerelement Muster
- Benutzeroberflächen Automatisierung, virtualisierte Elemente
- Benutzeroberflächenautomatisierungs, Steuerelement Muster
- UI-Automatisierung, VirtualizedItem-Steuerelement Muster
- UI-Automatisierung, ItemContainer-Steuerelement Muster
- VirtualizedItem-Steuerelement Muster
- ItemContainer-Steuerelement Muster
- Steuerelement Muster, VirtualizedItem
- Steuerelement Muster, ItemContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb29232b06304079ad5b9dfdfb589ad510a5b51f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310743"
---
# <a name="working-with-virtualized-items"></a>Arbeiten mit virtualisierten Elementen

In diesem Thema wird beschrieben, wie die vom [ItemContainer](uiauto-implementingitemcontainer.md) -und [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Mustern bereitgestellten Funktionen verwendet werden, um Informationen zu virtualisierten Elementen zu suchen und abzurufen.

-   [Übersicht über die Virtualisierung](#overview-of-virtualization)
-   [Unterstützung der Virtualisierung durch ein Steuerelement](#how-a-control-supports-virtualization)
-   [Auffinden und erkennen von virtualisierten Elementen durch Clients](#how-clients-find-and-realize-virtualized-items)
-   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-virtualization"></a>Übersicht über die Virtualisierung

Steuerelemente, die eine große Anzahl untergeordneter Elemente enthalten, können die Virtualisierung verwenden, um die Elemente effizient zu verwalten. Bei der Virtualisierung verwaltet das Steuerelement vollständige Informationen im Arbeitsspeicher nur für eine Teilmenge der Elemente zu einem bestimmten Zeitpunkt. In der Regel enthält die Teilmenge nur die Elemente, die derzeit für den Benutzer sichtbar sind. Vollständige Informationen zu den verbleibenden virtualisierten Elementen werden im Speicher beibehalten und in den Arbeitsspeicher geladen oder realisiert, wie das Steuerelement dies benötigt, z. b. wenn neue Elemente für den Benutzer sichtbar werden.

Steuerelemente, die die Virtualisierung verwenden, stellen eine Herausforderung dar, da nur erkannte Elemente vollständig als Microsoft UI Automation-Elemente in der Benutzeroberflächenautomatisierungs-Struktur Virtualisierte Elemente sind nicht in der Struktur vorhanden, sodass keine Informationen über diese Elemente für Clients verfügbar sind. Zum Abrufen von Informationen zu virtualisierten Elementen ist es erforderlich, dass die Benutzeroberflächen Automatisierung die Anforderung übergibt, um die Elemente an das Steuerelement zu erkennen. Nachdem die Elemente realisiert wurden, kann die Benutzeroberflächen Automatisierung für Sie Benutzeroberflächenautomatisierungs-Elemente erstellen. Die Benutzeroberflächen Automatisierung beinhaltet zwei Steuerelement Muster, mit denen Clients mit virtualisierten Elementen arbeiten können: [ItemContainer](uiauto-implementingitemcontainer.md) und [VirtualizedItem](uiauto-implementingvirtualizeditem.md).

## <a name="how-a-control-supports-virtualization"></a>Unterstützung der Virtualisierung durch ein Steuerelement

Jedes Steuerelement, das virtualisierte Elemente enthalten kann, muss das [ItemContainer](uiauto-implementingitemcontainer.md) -Steuerelement Muster unterstützen. Außerdem muss jedes Element, das virtualisiert werden kann, das [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Muster unterstützen. Die Funktionalität, die von den Steuerelement Mustern ItemContainer und VirtualizedItem verfügbar gemacht wird, kann von Clients über die Schnittstellen [**iuiautomationitemcontainerpattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) und [**iuiautomationvirtualizeditempattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) aufgerufen werden.

## <a name="how-clients-find-and-realize-virtualized-items"></a>Auffinden und erkennen von virtualisierten Elementen durch Clients

Clients können die [**iuiautomationitemcontainerpattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) -Methode verwenden, um anhand des Werts einer bestimmten Eigenschaft nach untergeordneten Elementen im Container zu suchen. Die-Methode kann auch das erste Element im Container oder das Element, das dem angegebenen Element folgt, abrufen. Wenn ein übereinstimmendes untergeordnetes Element gefunden wird, ruft **FindItemByProperty** eine [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle für das Element ab. Wenn jedoch das untergeordnete Element virtualisiert ist, ist die **iuiautomationelement** -Schnittstelle ein Platzhalter. Der [**UIA \_ E \_ elementnotavailable**](uiauto-error-codes.md) -Fehler tritt auf, wenn der Client versucht, die **iuiautomationelement** -Schnittstelle zum Abrufen von Eigenschafts Werten oder Aufrufen von Methoden zu verwenden, die noch nicht verfügbar sind. Welche Eigenschaften oder Methoden über einen Platzhalter verfügbar sind, hängt von der Implementierung des Steuer Elements ab. Die einzige Voraussetzung für einen Platzhalter ist die Unterstützung der [**iuiautomationvirtualizeditempattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) -Schnittstelle.

Der [**UIA \_ E \_ elementnotavailable**](uiauto-error-codes.md) -Fehler ist ein Hinweis auf den Client, dass ein Element virtualisiert werden kann. Der Client sollte Antworten, indem er die [**iuiautomationvirtualizeditempattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) -Schnittstelle für das Element abruft und dann das Element durch Aufrufen der [**iuiautomationvirtualizeditempattern::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) Single-Methode erkennt. Wenn dies erfolgreich ist, ist die [**iuiautomationelement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) -Schnittstelle voll funktionsfähig, und es sind alle entsprechenden Eigenschaften verfügbar.

Abhängig von der Implementierung des Steuer Elements führt der Aufruf von [**iuiautomationvirtualizeditempattern:**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) Ein Client sollte sich jedoch nicht darauf verlassen, dass der Bildlauf in der Sicht durchgeführt oder sichtbar gemacht wird. Um sicherzustellen, dass das Element sichtbar ist, kann der Client die [**iuiautomationscrollitempattern:: ScrollIntoView**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollitempattern-scrollintoview) -Methode verwenden.

## <a name="example"></a>Beispiel

Beispielcode, der die Verwendung der Benutzeroberflächenautomatisierungs-Unterstützung für die Virtualisierung veranschaulicht, finden Sie unter [Abrufen eines virtualisierten Elements](uiauto-howto-retrieve-virtualized-item.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




