---
title: ItemContainer-Steuerelement Muster
description: Beschreibt Richtlinien und Konventionen zum Implementieren von IItemContainerProvider, einschließlich Informationen zu Methoden. Das ItemContainer-Steuerelement Muster wird zur Unterstützung der elementvirtualisierung verwendet.
ms.assetid: 6f3dd94e-3563-4a13-9db9-5928a02bab77
keywords:
- UI-Automatisierung, Implementieren des ItemContainer-Steuerelement Musters
- UI-Automatisierung, ItemContainer-Steuerelement Muster
- UI-Automatisierung, IItemContainerProvider
- IItemContainerProvider
- Implementieren von ItemContainer-Steuerelement Mustern für Benutzeroberflächen
- ItemContainer-Steuerelement Muster
- Steuerelement Muster, IItemContainerProvider
- Steuerelement Muster, Implementieren der Benutzeroberflächenautomatisierungs-ItemContainer
- Steuerelement Muster, ItemContainer
- Schnittstellen, IItemContainerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55246abde51e7053bf0c3266ccbe9c2b080b2fe7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709689"
---
# <a name="itemcontainer-control-pattern"></a>ItemContainer-Steuerelement Muster

Beschreibt Richtlinien und Konventionen zum Implementieren von [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider), einschließlich Informationen zu Methoden. Das **ItemContainer** -Steuerelement Muster wird zur Unterstützung der elementvirtualisierung verwendet.

Steuerelemente, die eine große Anzahl untergeordneter Elemente enthalten, können die Virtualisierung verwenden, um die Elemente effizient zu verwalten. Bei der Virtualisierung verwaltet das Steuerelement vollständige Informationen im Arbeitsspeicher nur für eine Teilmenge der Elemente zu einem bestimmten Zeitpunkt. In der Regel enthält die Teilmenge nur die Elemente, die derzeit für den Benutzer sichtbar sind. Vollständige Informationen zu den verbleibenden virtualisierten Elementen werden im Speicher beibehalten und in den Arbeitsspeicher geladen oder realisiert, wie das Steuerelement dies benötigt, z. b. wenn neue Elemente für den Benutzer sichtbar werden.

Das folgende Diagramm zeigt z. b. ein Listenfeld, das Tausende von virtualisierten Elementen enthält. Da das Steuerelement vollständige Informationen nur für die untergeordneten Elemente verwaltet, die derzeit sichtbar sind, kann der Anbieter Microsoft UI Automation-Elemente nur für die Elemente 100 – 127 verfügbar machen.

![Diagramm, das Elemente in einem Listenfeld anzeigt, die virtualisiert und nicht virtualisiert sind](images/virtualizeditems.jpg)

Steuerelemente, die die Virtualisierung verwenden, stellen eine Herausforderung dar, da nur erkannte (devirtualisierte) Elemente vollständig als Benutzeroberflächenautomatisierungs-Elemente in der Benutzeroberflächenautomatisierungs-Struktur Virtualisierte Elemente sind nicht in der Struktur vorhanden, daher sind keine Informationen verfügbar.

Zum Bereitstellen von Informationen über virtualisierte Elemente implementieren Anbieter das **ItemContainer** -Steuerelement Muster, das die [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) -Schnittstelle verfügbar macht. Die [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) -Methode sucht nach untergeordneten Elementen auf der Grundlage des Werts einer bestimmten Eigenschaft, z. b. " **Name**", " **AutomationId**" oder " **issgewählt**". Wenn ein Element virtualisiert ist, ruft **FindItemByProperty** ein Platzhalter Element für die Benutzeroberflächen Automatisierung für das Element ab. Ein Platzhalter Element ist eine Implementierung der [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) -Schnittstelle, die nur das [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Muster unterstützt.

Mit der [**IVirtualizedItemProvider::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) die-Methode kann ein Client anfordern, dass ein virtualisiertes Element realisiert wird. Dadurch wird ein vollständiges Benutzeroberflächenautomatisierungs-Element für das Element verfügbar gemacht, sodass alle erforderlichen Eigenschaften und Muster verfügbar sind.

Obwohl der primäre Zweck des **ItemContainer** -Steuerelement Musters darin besteht, virtualisierte Container Szenarios zu unterstützen, kann er von jedem Container implementiert werden, der untergeordnete Elemente nach Namen abruft, unabhängig davon, ob der Container Virtualisierung verwendet.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für IItemContainerProvider](#required-members-for-iitemcontainerprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **ItemContainer** -Steuerelement Musters die folgenden Richtlinien und Konventionen:

-   Jedes Steuerelement, das virtualisierte Elemente enthalten kann, muss das **ItemContainer** -Steuerelement Muster unterstützen. Jeder Container, der das Abrufen von Elementen auf Grundlage eines Eigenschafts Werts unterstützt, kann dieses Muster unterstützen, unabhängig davon, ob der Container Virtualisierung verwendet.
-   Wenn ein Container virtualisiert wird, können andere Steuerelement Muster, z. b. [Auswahl](uiauto-implementingselection.md), [Tabelle](uiauto-implementingtable.md)und [Raster](uiauto-implementinggrid.md) , beeinträchtigt werden. Beispielsweise kann die Methode [**ISelectionProvider:: GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) nur Elemente unterstützen, die sich im Viewport befinden, oder nur ausgewählte Elemente, die derzeit nicht virtualisiert sind.
-   Das [Scroll](uiauto-implementingscroll.md) -Steuerelement Muster sollte von der Virtualisierung nicht beeinträchtigt werden.
-   Für virtualisierte Elemente sind keine Element Anzahl oder Indexinformationen verfügbar. Ein virtualisiertes Steuerelement kann die **DescribedBy** -Eigenschaft oder die **ItemStatus** -Eigenschaft verwenden, um diese Informationen bei Bedarf bereitzustellen.
-   Entwickler von Steuerelementen sollten Details aller Benutzeroberflächenautomatisierungs-Eigenschaften und Steuerelement Muster, die von der Verwendung der Virtualisierung betroffen sind, dokumentieren und veröffentlichen. Obwohl das ItemContainer-Steuerelement und das [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Muster grundlegende Unterstützung bieten, unterstützen Sie möglicherweise kein Virtualisierungsverhalten

Die folgenden Richtlinien und Anforderungen gelten für die [**IItemContainerProvider:: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) -Methode.

-   Obwohl es nicht erforderlich ist, empfiehlt Microsoft ausdrücklich, dass [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) die Eigenschaften " **Name**", " **AutomationId**" und " **isswählten** " unterstützt.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) kann langsam sein, wenn mehrere Objekte durchlaufen werden müssen, um einen passenden zu finden.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) kann wiederholt aufgerufen werden, um Elemente nacheinander zu suchen. Die Elemente können in beliebiger Reihenfolge vorliegen, solange die einzelnen Elemente nur einmal zurückgegeben werden.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) kann implementiert werden, um nur die Elemente zu finden, die in der Steuerelement-oder Inhaltsansicht der Benutzeroberflächenautomatisierungs-Struktur angezeigt werden. Elemente, die nur in der RAW-Ansicht angezeigt werden, können ausgelassen werden, um zu vermeiden, dass mehrere Elemente abgerufen werden, die nur einen Teil eines "Elements" für den Benutzer darstellen.
-   Wenn die Suchkriterien mit einem virtualisierten Element übereinstimmen, kann der Anbieter ein Platzhalter Element zurückgeben, das das [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Muster unterstützt. Die folgenden Richtlinien gelten für Platzhalter Elemente:
    -   Wenn Sie ein Platzhalter Element für ein virtualisiertes Element abrufen, dürfen keine Änderungen an der Benutzeroberfläche ausgelöst werden.
    -   Das Platzhalter Element muss ein Peer anderer untergeordneter Elemente sein (ein strukturgeändertes Ereignis ist erforderlich).
    -   Wenn möglich, kann der Anbieter anstelle eines Platzhalters ein vollständiges Automation-Element erstellen.
-   Wenn das Suchkriterium mit einem nicht virtualisierten Element übereinstimmt, muss der Anbieter das tatsächliche Element und keinen Platzhalter zurückgeben.
-   Wenn kein Element gefunden wird, sollte [**IItemContainerProvider:: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) den *pfound* -Parameter auf **null** festlegen und **S \_ OK** zurückgeben.
-   Wenn der *PropertyId* -Parameter den Wert 0 hat, sollte der Anbieter das nächste Element nach *pstartafter* zurückgeben.
-   Wenn der *pstartafter* -Parameter den Wert **null** hat und *PropertyId* den Wert 0 hat, sollte der Anbieter das erste Element im Container zurückgeben.
-   Wenn der *PropertyId* -Parameter den Wert 0 hat, wird der value-Parameter ignoriert.

Die folgenden Richtlinien und Anforderungen gelten für Platzhalter Elemente für virtualisierte Elemente in der Benutzeroberflächenautomatisierungs-Struktur.

-   Obwohl Anbietern empfohlen wird, mehr Eigenschaften und Steuerelement Muster für ein Platzhalter Element zu unterstützen, ist nur das [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Muster erforderlich.
-   Der Anbieter kann ein vorheriges Platzhalter Element für ungültig erklären, wenn [**IItemContainerProvider:: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) erneut aufgerufen wird. (Wenn ein Client das Platzhalter Element realisieren muss, sollte dies sofort erfolgen; andernfalls kann das Element für ungültig erklärt werden, wenn **FindItemByProperty** erneut aufgerufen wird, oder wenn der Viewport aus irgendeinem Grund geändert wird.)
-   UI-Aktionen, wie z. b. Scrollen oder die Größe der Größe, können dazu führen, dass der Viewport des Containers geändert und ein neuer Satz untergeordneter Elemente sichtbar wird. In diesem Fall sind zuvor abgerufene Platzhalter Elemente möglicherweise nicht in der Benutzeroberflächenautomatisierungs-Struktur verfügbar.
-   Der Anbieter sollte die Benutzeroberflächen Elemente, die auf dem Bildschirm im Viewport des Container Objekts verfügbar sind, nicht virtualisieren.

## <a name="required-members-for-iitemcontainerprovider"></a>Erforderliche Member für IItemContainerProvider

Die folgende Methode ist für die Implementierung der [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) -Schnittstelle erforderlich.



| Erforderliche Member                                                               | Memberart | Hinweise |
|--------------------------------------------------------------------------------|-------------|-------|
| [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) | Methode      | Keine  |



 

Dem **ItemContainer** -Steuerelement Muster sind keine Eigenschaften oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelement Typen und ihre unterstützten Steuerelement Muster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[VirtualizedItem-Steuerelement Muster](uiauto-implementingvirtualizeditem.md)
</dt> </dl>

 

 




