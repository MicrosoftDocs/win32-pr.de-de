---
title: Abfragen eines virtualisierten Elements in der Elementansicht
description: In diesem Thema wird beschrieben, wie Sie microsoft Benutzeroberflächenautomatisierung verwenden, um Benutzeroberflächeninformationen zu virtualisierten Elementen in der Windows 7 Items View abzurufen.
ms.assetid: a0bff8a1-47b1-4750-8086-e2e65a79099e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9196d62e7aa93b21aed15b76b8ced6a9520b27fb5bcee74a0e0d4ddc510c86f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759245"
---
# <a name="how-to-query-a-virtualized-item-in-items-view"></a>Abfragen eines virtualisierten Elements in der Elementansicht

In diesem Thema wird beschrieben, wie Sie microsoft Benutzeroberflächenautomatisierung verwenden, um Benutzeroberflächeninformationen zu virtualisierten Elementen in der Windows 7 Items View abzurufen. Das Thema enthält folgende Abschnitte:

> [!Note]  
> Dieses Thema gilt nur für Windows 7. Beachten Sie, dass sich die in diesem Thema beschriebenen Barrierefreiheitsfunktionen in zukünftigen Versionen von Windows.

 

-   [Übersicht](#overview)
-   [Struktur der Elementeansichtsstruktur](#items-view-tree-structure)
-   [Virtualisierung](#virtualization)
-   [Abrufen der Anzahl aller Elemente](#obtaining-a-count-of-all-items)
-   [Abrufen eines Elementindex in Bezug auf alle Elemente](#obtaining-an-item-index-with-respect-to-all-items)
-   [Abrufen eines Verweises auf ein elementualisiertes Element](#obtaining-a-reference-to-a-vitualized-item)
-   [Scrollen eines virtualisierten Elements auf dem Bildschirm](#scrolling-a-virtualized-item-on-screen)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Die Elementansicht ist eine Benutzeroberflächenkomponente, mit der Benutzer Dateien und andere Elemente anzeigen und mit ihnen interagieren können. In Windows 7 ersetzt die Elementeansicht das Listenansicht-Steuerelement zum Präsentieren von Elementen in der Standardansicht des Windows Explorers. Die Elementansicht wird auch im Dialogfeld "Allgemeines Element", Startmenü Suchergebnissen und anderen Windows 7-Benutzeroberflächenelementen verwendet, die das Explorer-Browser-Steuerelement verwenden. Im Vergleich zum Listenansicht-Steuerelement bietet die Elementeansicht den Benutzern die folgenden Vorteile:

-   Die Ansicht "Elemente" kann Elemente auf eine Weise präsentieren, die nützlicher, wünschenswerter und relevanter ist, sodass Benutzer Elemente einfach, schnell und zu einem besseren Ort finden und organisieren können.
-   Die Ansicht "Elemente" kann große Mengen von Elementen aus Datenquellen mit unterschiedlichen Leistungsmerkmalen anzeigen, sodass Benutzer ihre gesamte Sammlung von Elementen über mehrere Quellen hinweg durchsuchen und durchsuchen können.

Die folgende Abbildung zeigt die Ansicht Elemente im Windows Explorer.

![Screenshot: Windows-Explorer mit Elementansichtskomponente](images/itemsview.gif)

Aus Entwicklersicht ähneln die allgemeine Struktur und Funktionalität der Elementeansicht der Struktur des Listenansicht-Steuerelements. Der Hauptunterschied besteht in der Unterstützung der Virtualisierung durch die Elementeansicht, während das Listenansicht-Steuerelement dies nicht tut. Außerdem verwendet die Elementeansicht zwei neue Benutzeroberflächenautomatisierung, um sicherzustellen, dass auf virtualisierte Inhalte, die von der Elementeansicht bereitgestellt werden, zugegriffen werden kann. Diese Schnittstellen werden in den folgenden Abschnitten dieses Themas beschrieben.

Allgemeine Informationen zur Virtualisierung in Benutzeroberflächenautomatisierung finden Sie unter [Arbeiten mit virtualisierten Elementen.](uiauto-workingwithvirtualizeditems.md)

## <a name="items-view-tree-structure"></a>Struktur der Elementeansichtsstruktur

In der Benutzeroberflächenautomatisierung-Struktur hat Benutzeroberflächenautomatisierung Element der Elementansicht den Namen "ItemsView" und den Steuerelementtyp "list". In der vorherigen Abbildung ist das Element ItemsView Benutzeroberflächenautomatisierung rot umrissen. Verschiedene Benutzeroberflächenautomatisierung sind unterhalb der obersten Ebene von ItemsView vorhanden, aber in diesem Dokument wird nur auf zwei weitere Benutzeroberflächenautomatisierung-Elemente verwiesen: Gruppenelemente und Listenelemente.

Die Gruppenelemente sind die Benutzeroberflächenautomatisierung Elemente, die alle Listenelemente dieser Gruppe enthalten. Ihr Steuerelementtyp ist "Group", und ihre Namen variieren je nach Gruppenname. In der vorherigen Abbildung enthält das erste Gruppenelement sowohl den Header "A-H (1)" als auch das Listenelement "Ordner", und der Name ist "A-H".

Die Listenelemente sind die Benutzeroberflächenautomatisierung, die die Blattelemente in der Ansicht darstellen. Ihr Steuerelementtyp ist "ListItem", und ihre Namen variieren je nach Elementname. In der vorherigen Abbildung sind die Listenelemente die Blattelemente wie "Folder", "Musik" und "Picture". Auf diese Benutzeroberflächenautomatisierung Elemente wird im restlichen Teil dieses Dokuments mit den Begriffen ItemsView-Element, Group-Element und ListItem-Element verwiesen.

## <a name="virtualization"></a>Virtualisierung

Die Ansicht "Elemente" verwendet Virtualisierung. Dies bedeutet, dass Elemente außerhalb des sichtbaren Bereichs der Ansicht nicht aus dem System abgerufen werden und die Darstellung der Elemente auf der Benutzeroberfläche nicht erstellt wird. Diese Elemente werden als *virtualisierte Elemente bezeichnet.* Da sie nicht erstellt werden, verfügen virtualisierte Elemente nicht über Benutzeroberflächenautomatisierung-Elemente und werden daher nicht in der Benutzeroberflächenautomatisierung-Struktur angezeigt, wenn ein Benutzeroberflächenautomatisierung-Client die Struktur aufzählt. Darüber hinaus Benutzeroberflächenautomatisierung Steuerelementmuster nur für sichtbare Elemente verwendet. Beispielsweise gibt [](uiauto-implementingselection.md) das Selection-Steuerelementmuster nur die sichtbaren ausgewählten Elemente zurück, wenn ein Client die [**IUIAutomationSelectionPattern::GetCurrentSelection-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection) aufruft.

Die Ansicht "Elemente" unterstützt die Möglichkeit, die folgenden Informationen zu virtualisierten Elementen abzurufen:

-   Eine Anzahl der Gesamtanzahl von Elementen, einschließlich virtualisierter Elemente
-   Benutzeroberflächenautomatisierung elemente für virtualisierte Elemente
-   Benutzeroberflächenautomatisierung elemente für die ausgewählten virtualisierten Elemente

## <a name="obtaining-a-count-of-all-items"></a>Abrufen der Anzahl aller Elemente

Ein Client kann das ItemsView-Element verwenden, um die Anzahl aller Elemente sowie die Anzahl der ausgewählten Elemente zu erhalten. Das ItemsView-Element bietet zwei Möglichkeiten, diese Anzahl zu erhalten. Die erste besteht aus dem Abrufen der ItemStatus-Eigenschaft des ItemsView-Elements und der zweiten durch Abrufen benutzerdefinierter Eigenschaften aus dem ItemsView-Element.

Die ItemStatus-Eigenschaft ist eine Zeichenfolge, die die Gesamtzahl der Elemente und die Anzahl der ausgewählten Elemente durch ein Komma getrennt angibt. Beispiel: "3 Elemente, 1 Element ausgewählt". Diese Zeichenfolge ist lokalisiert und kann direkt an den Benutzer übermittelt werden.

Die benutzerdefinierten Eigenschaften des ItemsView-Elements enthalten eine Eigenschaft für die Elementanzahl und eine weitere für die Auswahlanzahl. Dazu gehören:

-   \_ \_ ItemCount-Eigenschaften-GUID (ABBF5C45-5CCC-47b7-BB4E-87CB87BBD162) – Die Anzahl aller eindeutigen Elemente in der Ansicht. Wenn die Gruppierung nach einer Mehrwerteigenschaft (Multi-Value Property, MVP) besteht, sodass ein einzelnes Element mehrmals angezeigt werden kann, wird jedes Element nur einmal gezählt.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Programmatic Name: "ItemCount")

-   \_ \_ SelectedItemCount-Eigenschaften-GUID (92A053DA-2969-4021-BF27-514CFC2E4A69) – Die Anzahl aller in der Ansicht ausgewählten eindeutigen Elemente. Wenn die Gruppierung nach einer Mehrwerteigenschaft (Multi-Value Property, MVP) besteht, sodass ein einzelnes Element mehrmals angezeigt werden kann, wird jedes Element nur einmal gezählt.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Programmatic Name: "SelectedItemCount")

Diese benutzerdefinierten Eigenschaften werden in Shlguid.h definiert, das im Windows Software Development Kit (SDK) enthalten ist, und diese Eigenschaften werden über die [**IUIAutomationRegistrar::RegisterProperty-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) registriert. Benutzeroberflächenautomatisierung Verwenden **von RegisterProperty** zum Abrufen von Eigenschaftsbezeichnern (PROPERTYIDs) für die benutzerdefinierten Eigenschaften.

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>Abrufen eines Elementindex in Bezug auf alle Elemente

Ein Client kann den Index eines Elements abrufen, indem er entweder die ItemStatus-Eigenschaft eines ListItem-Elements oder eine benutzerdefinierte Eigenschaft eines ListItem-Elements erhält.

Die ItemStatus-Eigenschaft ist eine Zeichenfolge, die den Index eines Elements in Bezug auf die Gesamtzahl der Elemente enthält. Beispiel: "Element 1 von 3". Diese Zeichenfolge ist lokalisiert und kann direkt an den Benutzer übermittelt werden.

Die folgende benutzerdefinierte Eigenschaft ruft den Elementindex eines ListItem-Elements ab:

-   \_ \_ ItemIndex-Eigenschaften-GUID (92A053DA-2969-4021-BF27-514CFC2E4A69) – Der 1-basierte absolute Index eines Elements. Wenn die Gruppierung nach einer mehrwertigen Eigenschaft (MVP) vorkommt, sodass ein einzelnes Element zweimal angezeigt werden kann, erhält jede Darstellung des Elements einen separaten Index.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Programmatic Name: "ItemIndex")

Diese benutzerdefinierte Eigenschaft wird in Shlguid.h definiert, die im Windows SDK enthalten ist und über die [**IUIAutomationRegistrar::RegisterProperty-Methode registriert**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) wird. Benutzeroberflächenautomatisierung-Clients verwenden **RegisterProperty,** um einen Eigenschaftenbezeichner (PROPERTYIDs) für die benutzerdefinierte Eigenschaft abzurufen.

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>Abrufen eines Verweises auf ein elementualisiertes Element

Ein ItemsView-Element implementiert das [ItemContainer-Steuerelementmuster](uiauto-implementingitemcontainer.md) [**(IItemContainerProvider-Schnittstelle),**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) mit dem ein Client ein Benutzeroberflächenautomatisierung-Element für ein virtualisiertes Element (ein Element außerhalb des sichtbaren Bereichs) erhalten kann. ItemsView ermöglicht es dem Client, ein ListItem-Element zu finden, indem nach den Eigenschaften Name und Auswahl gesucht wird. Der Versuch, nach einer anderen Eigenschaft zu suchen, kann nicht ausgeführt werden.

Ein virtuelles Element implementiert nur das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) ([**IVirtualizedItemProvider-Schnittstelle).**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) Da das Element, das durch ein virtualisiertes Benutzeroberflächenautomatisierung-Element dargestellt wird, noch nicht vorhanden ist, wird beim Versuch, ein anderes Steuerelementmuster oder eine eigenschaft des Elements zu erhalten, ein Fehler angezeigt.

Sowohl ListItem- als auch Group-Elemente werden virtualisiert, aber nur ListItem-Elemente können vom [ItemContainer-Steuerelementmuster](uiauto-implementingitemcontainer.md) zurückgegeben werden. Da der Aufruf der [**IUIAutomationItemContainerPattern::FindItemByProperty-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) im UI-Thread ausgeführt wird und blockiert wird, antwortet die Ansicht erst, wenn **FindItemByProperty** zurückgegeben wird, und alle anderen Methodenaufrufe des Anbieters müssen warten, bis **FindItemByProperty** abgeschlossen ist. In einigen Fällen muss **FindItemByProperty** das gesamte DataSet vor der Rückgabe verarbeiten, was ressourcenintensiv sein kann. Die Angabe **von NULL** als Startelement bewirkt, dass **FindItemByProperty** die Suche mit dem ersten Element in der Ansicht beginnt.

ItemsView unterstützt die folgenden Eigenschaften für [**FindItemByProperty:**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty)

-   Name (UIA NamePropertyId): Sucht nach dem ersten Element, dessen Name vollständig mit \_ der angegebenen Zeichenfolge entspricht. Bei der Suche wird die Groß- und Kleinschreibung nicht berücksichtigt. Platzhalterzeichen oder teilweise Übereinstimmungen werden nicht unterstützt. Wenn ein **NULL-Name** angegeben wird, wird das nächste Element nach dem Startelement zurückgegeben. Das Angeben **von NULL-Namen** ermöglicht Benutzeroberflächenautomatisierung Client, alle Elemente in der Ansicht aufzählen. Es wird jedoch davon abgeraten, alle Elemente aufzählen, da dadurch alle Elemente in der Ansicht realisiert werden.
-   SelectionItem \_ IsSelected (UIA \_ SelectionItemIsSelectedPropertyId) – Sucht nach dem ersten Element, dessen SelectionItem IsSelected-Eigenschaft dem angegebenen \_ Wert entspricht. Geben **Sie TRUE** an, um das erste ausgewählte Element zu suchen, oder **FALSE,** um das erste nicht ausgewählte Element zu finden. Seien Sie vorsichtig, wenn Sie alle ausgewählten Elemente aufzählen, da die Anzahl der ausgewählten Elemente sehr groß sein kann, insbesondere, wenn der Benutzer alle Elemente ausgewählt hat.

## <a name="scrolling-a-virtualized-item-on-screen"></a>Scrollen eines virtualisierten Elements auf dem Bildschirm

Nach dem Abrufen eines Verweises auf ein Benutzeroberflächenautomatisierung-Element für ein virtualisiertes Element (off-screen) kann der Client das Element mithilfe der [**IUIAutomationVirtualizeItemPattern::Realize-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) des [VirtualizedItem-Steuerelementmusters](uiauto-implementingvirtualizeditem.md) in die Ansicht scrollen. Nachdem das Element realisiert wurde, ist es sichtbar, und alle Eigenschaften und Steuerelementmuster, die normalerweise einem ListItem-Element zugeordnet sind, sind für den Client verfügbar.

Nur ListItem-Elemente, die von der [**IUIAutomationItemContainerPattern::FindItemByProperty-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) erhalten wurden, machen das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) verfügbar. Wenn ein Bildschirmelement vom Bildschirm aus gescrollt wird, wird das Element ungültig, und der Client muss **FindItemByProperty** aufrufen, um den Offscreenverweis zu erhalten.

Es ist auch möglich, Elemente mithilfe des [](uiauto-implementingscroll.md) Bildlauf-Steuerelementmusters (oder mithilfe der Bildlaufleisten) in die bzw. aus der Ansicht zu verschieben. Elemente und Gruppen werden beim Bildlauf in die Ansicht realisiert und virtualisiert, wenn sie aus der Ansicht scrollen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit virtualisierten Elementen](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




