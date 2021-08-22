---
title: ItemContainer-Steuerelementmuster
description: Beschreibt Richtlinien und Konventionen für die Implementierung von IItemContainerProvider, einschließlich Informationen zu Methoden. Das ItemContainer-Steuerelementmuster wird zur Unterstützung der Elementvirtualisierung verwendet.
ms.assetid: 6f3dd94e-3563-4a13-9db9-5928a02bab77
keywords:
- Benutzeroberflächenautomatisierung,Implementieren des ItemContainer-Steuerelementmusters
- Benutzeroberflächenautomatisierung,ItemContainer-Steuerelementmuster
- Benutzeroberflächenautomatisierung,IItemContainerProvider
- IItemContainerProvider
- Implementieren von Benutzeroberflächenautomatisierung ItemContainer-Steuerelementmustern
- ItemContainer-Steuerelementmuster
- Steuerelementmuster,IItemContainerProvider
- Steuerelementmuster,Implementieren Benutzeroberflächenautomatisierung ItemContainer
- Steuerelementmuster,ItemContainer
- interfaces,IItemContainerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69c0407a8f167a3a89b908c1b5555a9d32363b38b3ce5ab4d1794e726666a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413454"
---
# <a name="itemcontainer-control-pattern"></a>ItemContainer-Steuerelementmuster

Beschreibt Richtlinien und Konventionen für die Implementierung von [**IItemContainerProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider)einschließlich Informationen zu Methoden. Das **ItemContainer-Steuerelementmuster** wird zur Unterstützung der Elementvirtualisierung verwendet.

Steuerelemente, die eine große Anzahl von untergeordneten Elementen enthalten, können die Virtualisierung verwenden, um die Elemente effizient zu verwalten. Bei der Virtualisierung behält das Steuerelement die vollständigen Informationen im Arbeitsspeicher für nur eine Teilmenge von Elementen zu einem bestimmten Zeitpunkt bei. In der Regel enthält die Teilmenge nur die Elemente, die derzeit für den Benutzer sichtbar sind. Vollständige Informationen zu den verbleibenden virtualisierten Elementen werden im Speicher gespeichert und in den Arbeitsspeicher geladen oder realisiert, wenn das Steuerelement dies benötigt, z. B. wenn neue Elemente für den Benutzer sichtbar werden.

Das folgende Diagramm zeigt beispielsweise ein Listenfeld, das Tausende von virtualisierten Elementen enthält. Da das Steuerelement vollständige Informationen nur für die untergeordneten Elemente verwaltet, die derzeit sichtbar sind, kann der Anbieter Microsoft Benutzeroberflächenautomatisierung Elemente nur für die Elemente 100 bis 127 verfügbar machen.

![Diagramm mit Elementen in einem Listenfeld, die virtualisiert und nicht virtualisiert sind](images/virtualizeditems.jpg)

Steuerelemente, die Virtualisierung verwenden, stellen eine Herausforderung dar, da nur realisierte (de-virtualisierte) Elemente als Benutzeroberflächenautomatisierung Elemente in der Benutzeroberflächenautomatisierung-Struktur vollständig verfügbar sind. Virtualisierte Elemente sind in der Struktur nicht vorhanden, sodass keine Informationen zu ihnen verfügbar sind.

Um Informationen zu virtualisierten Elementen bereitzustellen, implementieren Anbieter das **ItemContainer-Steuerelementmuster,** das die [**IItemContainerProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) verfügbar macht. Die [**FindItemByProperty-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) sucht untergeordnete Elemente basierend auf dem Wert einer bestimmten Eigenschaft, z. B. **Name,** **AutomationId** oder **IsSelected.** Wenn ein Element virtualisiert ist, ruft **FindItemByProperty** ein Benutzeroberflächenautomatisierung Platzhalterelement für das Element ab. Ein Platzhalterelement ist eine Implementierung der [**IRawElementProviderSimple-Schnittstelle,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) die nur das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) unterstützt.

Mit [**der IVirtualizedItemProvider::Realize-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) kann ein Client anfordern, dass ein virtualisiertes Element realisiert wird. Dadurch wird ein vollständiges Benutzeroberflächenautomatisierung Element für das Element verfügbar, sodass alle erforderlichen Eigenschaften und Muster verfügbar sind.

Obwohl der Hauptzweck des **ItemContainer-Steuerelementmusters** darin besteht, virtualisierte Containerszenarien zu unterstützen, kann es von jedem Container implementiert werden, der untergeordnete Elemente anhand des Namens abruft, unabhängig davon, ob der Container Virtualisierung verwendet.

Dieses Thema enthält folgende Abschnitte:

-   [Implementierungsrichtlinien und -konventionen](#implementation-guidelines-and-conventions)
-   [Erforderliche Member für IItemContainerProvider](#required-members-for-iitemcontainerprovider)
-   [Zugehörige Themen](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Implementierungsrichtlinien und -konventionen

Beachten Sie beim Implementieren des **ItemContainer-Steuerelementmusters** die folgenden Richtlinien und Konventionen:

-   Jedes Steuerelement, das virtualisierte Elemente enthalten kann, muss das **ItemContainer-Steuerelementmuster** unterstützen. Jeder Container, der das Abrufen von Elementen basierend auf einem Eigenschaftswert unterstützt, kann dieses Muster unterstützen, unabhängig davon, ob der Container Virtualisierung verwendet.
-   Wenn ein Container virtualisiert wird, können andere Steuerelementmuster wie [Auswahl,](uiauto-implementingselection.md) [Tabelle](uiauto-implementingtable.md)und [Raster](uiauto-implementinggrid.md) betroffen sein. Beispielsweise kann die [**ISelectionProvider::GetSelection-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) nur Elemente unterstützen, die sich im Viewport befinden, oder nur ausgewählte Elemente, die derzeit nicht virtualisiert sind.
-   Das [](uiauto-implementingscroll.md) Scroll-Steuerelementmuster sollte von der Virtualisierung nicht betroffen sein.
-   Für virtualisierte Elemente sind keine Elementanzahl oder Indexinformationen verfügbar. Ein virtualisiertes Steuerelement kann die **DescribedBy-** oder **ItemStatus-Eigenschaft** verwenden, um diese Informationen bei Bedarf bereitzustellen.
-   Steuerelemententwickler sollten Details zu allen Benutzeroberflächenautomatisierung Eigenschaften und Steuerelementmustern dokumentieren und veröffentlichen, die von der Virtualisierung betroffen sind. Obwohl die Steuerelementmuster ItemContainer und [VirtualizedItem](uiauto-implementingvirtualizeditem.md) grundlegende Unterstützung bieten, unterstützen sie möglicherweise einige Virtualisierungsverhaltensweisen nicht.

Die folgenden Richtlinien und Anforderungen gelten für die [**IItemContainerProvider::FindItemByProperty-Methode.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty)

-   Obwohl dies nicht erforderlich ist, empfiehlt Microsoft dringend, dass [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) die Eigenschaften **Name,** **AutomationId** und **IsSelected** unterstützt.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) kann langsam sein, wenn mehrere Objekte durchlaufen werden müssen, um ein übereinstimmendes Objekt zu finden.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) kann wiederholt aufgerufen werden, um Elemente nacheinander zu suchen. Die Elemente können in beliebiger Reihenfolge sein, solange jedes Element nur einmal zurückgegeben wird.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) kann implementiert werden, um nur die Elemente zu finden, die in der Steuerelement- oder Inhaltsansicht der Benutzeroberflächenautomatisierung-Struktur angezeigt werden. Elemente, die nur in der Rohansicht angezeigt werden, können übersprungen werden, um das Abrufen mehrerer Elemente zu vermeiden, die nur einen Teil eines "Elements" für den Benutzer darstellen.
-   Wenn die Suchkriterien mit einem virtualisierten Element übereinstimmen, kann der Anbieter ein Platzhalterelement zurückgeben, das das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) unterstützt. Die folgenden Richtlinien gelten für Platzhalterelemente:
    -   Das Abrufen eines Platzhalterelements für ein virtualisiertes Element darf keine Benutzeroberflächenänderungen verursachen.
    -   Das Platzhalterelement muss ein Peer anderer untergeordneter Elemente sein (ein strukturverändertes Ereignis ist erforderlich).
    -   Nach Möglichkeit kann der Anbieter anstelle eines Platzhalters ein vollständiges Automatisierungselement erstellen.
-   Wenn die Suchkriterien mit einem nicht virtualisierten Element übereinstimmen, muss der Anbieter das tatsächliche Element und keinen Platzhalter zurückgeben.
-   Wenn kein Element gefunden wird, sollte [**IItemContainerProvider::FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) den *pFound-Parameter* auf **NULL** festlegen und **S \_ OK** zurückgeben.
-   Wenn der *propertyId-Parameter* 0 ist, sollte der Anbieter das nächste Element nach *pStartAfter* zurückgeben.
-   Wenn der *pStartAfter-Parameter* **NULL** und *propertyId* 0 ist, sollte der Anbieter das erste Element im Container zurückgeben.
-   Wenn der *propertyId-Parameter* 0 ist, wird der value-Parameter ignoriert.

Die folgenden Richtlinien und Anforderungen gelten für Platzhalterelemente für virtualisierte Elemente in der Benutzeroberflächenautomatisierung Struktur.

-   Obwohl Anbietern empfohlen wird, mehr Eigenschaften und Steuerelementmuster für ein Platzhalterelement zu unterstützen, ist nur das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) erforderlich.
-   Der Anbieter kann ein vorheriges Platzhalterelement für ungültig erklären, wenn [**IItemContainerProvider::FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) erneut aufgerufen wird. (Wenn ein Client das Platzhalterelement erkennen muss, sollte dies sofort erfolgen. Andernfalls kann das Element ungültig werden, wenn **FindItemByProperty** erneut aufgerufen wird oder sich der Viewport aus irgendeinem Grund ändert.)
-   Benutzeroberflächenaktionen wie Scrollen oder Ändern der Größe können dazu führen, dass sich der Viewport des Containers ändert und ein neuer Satz von untergeordneten Elementen sichtbar wird. In diesem Fall sind zuvor abgerufene Platzhalterelemente möglicherweise nicht in der Benutzeroberflächenautomatisierung-Struktur verfügbar.
-   Der Anbieter sollte keine Benutzeroberflächenelemente virtualisieren, die auf dem Bildschirm im Viewport des Containerobjekts verfügbar sind.

## <a name="required-members-for-iitemcontainerprovider"></a>Erforderliche Member für IItemContainerProvider

Die folgende Methode ist für die Implementierung der [**IItemContainerProvider-Schnittstelle**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) erforderlich.



| Erforderliche Member                                                               | Memberart | Hinweise |
|--------------------------------------------------------------------------------|-------------|-------|
| [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) | Methode      | Keine  |



 

Dem **ItemContainer-Steuerelementmuster** sind keine Eigenschaften oder Ereignisse zugeordnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelementtypen und deren unterstützte Steuerelementmuster](uiauto-controlpatternmapping.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Struktur](uiauto-treeoverview.md)
</dt> <dt>

[VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md)
</dt> </dl>

 

 




