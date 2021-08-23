---
title: Abfragen eines virtualisierten Elements in der Elementansicht
description: In diesem Thema wird beschrieben, wie Microsoft Benutzeroberflächenautomatisierung verwendet wird, um Benutzeroberflächeninformationen zu virtualisierten Elementen in der Windows 7-Elementansicht abzurufen.
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

In diesem Thema wird beschrieben, wie Microsoft Benutzeroberflächenautomatisierung verwendet wird, um Benutzeroberflächeninformationen zu virtualisierten Elementen in der Windows 7-Elementansicht abzurufen. Das Thema enthält folgende Abschnitte:

> [!Note]  
> Dieses Thema gilt nur für Windows 7. Beachten Sie, dass sich die in diesem Thema beschriebenen Barrierefreiheitsfunktionen in zukünftigen Versionen von Windows ändern können.

 

-   [Übersicht](#overview)
-   [Struktur der Elementansichtsstruktur](#items-view-tree-structure)
-   [Virtualisierung](#virtualization)
-   [Abrufen einer Anzahl aller Elemente](#obtaining-a-count-of-all-items)
-   [Abrufen eines Elementindexes in Bezug auf alle Elemente](#obtaining-an-item-index-with-respect-to-all-items)
-   [Abrufen eines Verweises auf ein Vitualized-Element](#obtaining-a-reference-to-a-vitualized-item)
-   [Scrollen eines virtualisierten Elements auf dem Bildschirm](#scrolling-a-virtualized-item-on-screen)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Die Elementansicht ist eine Benutzeroberflächenkomponente, mit der Benutzer Dateien und andere Elemente anzeigen und mit ihnen interagieren können. In Windows 7 ersetzt die Elementansicht das Listenansichtssteuerelement für die Darstellung von Elementen in der Standardansicht von Windows Explorer. Die Elementansicht wird auch im Dialogfeld "Allgemeines Element", Startmenü Suchergebnissen und anderen Windows 7 Ui-Elementen verwendet, die das Explorer-Browser-Steuerelement verwenden. Im Vergleich zum Listenansicht-Steuerelement bietet die Elementansicht den Benutzern die folgenden Vorteile:

-   Die Elementansicht kann Elemente auf eine Weise darstellen, die nützlicher, wünschenswerter und relevanter ist, sodass Benutzer Elemente einfacher, schneller und leichter finden und organisieren können.
-   In der Elementansicht können große Mengen von Elementen aus Datenquellen mit unterschiedlichen Leistungsmerkmalen angezeigt werden, sodass Benutzer ihre gesamte Sammlung von Elementen aus mehreren Quellen durchsuchen und durchsuchen können.

Die folgende Abbildung zeigt die Elementansicht in Windows Explorer.

![Screenshot: Windows-Explorer mit Elementansichtskomponente](images/itemsview.gif)

Aus Sicht eines Entwicklers ähnelt die allgemeine Struktur und Funktionalität der Elementansicht der des Listenansicht-Steuerelements. Der Hauptunterschied besteht darin, dass die Elementansicht Virtualisierung unterstützt, während das Listenansichtssteuerelement dies nicht tut. Außerdem verwendet die Elementansicht zwei neue Benutzeroberflächenautomatisierung Schnittstellen, um sicherzustellen, dass auf virtualisierte Inhalte zugegriffen werden kann, die von der Elementansicht bereitgestellt werden. Diese Schnittstellen werden in den folgenden Abschnitten dieses Themas beschrieben.

Allgemeine Informationen zur Virtualisierung in Benutzeroberflächenautomatisierung finden Sie unter [Arbeiten mit virtualisierten Elementen.](uiauto-workingwithvirtualizeditems.md)

## <a name="items-view-tree-structure"></a>Struktur der Elementansichtsstruktur

In der Benutzeroberflächenautomatisierung-Struktur hat die oberste Ebene Benutzeroberflächenautomatisierung Elements von Items View den Namen "ItemsView" und den Steuerelementtyp "list". In der vorherigen Abbildung ist das ItemsView-Benutzeroberflächenautomatisierung -Element rot dargestellt. Verschiedene Benutzeroberflächenautomatisierung Elemente befinden sich unterhalb der obersten Ebene von ItemsView, aber in diesem Dokument wird nur auf zwei andere Benutzeroberflächenautomatisierung-Elemente verwiesen: Gruppenelemente und Listenelemente.

Die Gruppenelemente sind die Benutzeroberflächenautomatisierung Elemente, die alle Listenelemente dieser Gruppe enthalten. Ihr Steuerelementtyp ist "Group", und ihre Namen variieren je nach Gruppenname. In der vorherigen Abbildung enthält das erste Gruppenelement sowohl den Header "A-H (1)" als auch das Listenelement "Folder", und sein Name lautet "A-H".

Die Listenelemente sind die Benutzeroberflächenautomatisierung Elemente, die die Blattelemente in der Ansicht darstellen. Ihr Steuerelementtyp ist "ListItem", und ihre Namen variieren je nach Elementname. In der vorherigen Abbildung sind die Listenelemente die Blattelemente wie "Ordner", "Musik" und "Bild". Auf diese drei Benutzeroberflächenautomatisierung Elemente wird im restlichen Teil dieses Dokuments mit den Begriffen ItemsView-Element, Group-Element und ListItem-Element verwiesen.

## <a name="virtualization"></a>Virtualisierung

Die Elementansicht verwendet Virtualisierung, was bedeutet, dass Elemente außerhalb des sichtbaren Bereichs der Ansicht nicht aus dem System abgerufen werden und die Darstellung der Elemente auf der Benutzeroberfläche nicht erstellt wird. Diese Elemente werden als *virtualisierte Elemente* bezeichnet. Da sie nicht erstellt werden, verfügen virtualisierte Elemente nicht über Benutzeroberflächenautomatisierung Elemente und werden daher nicht in der Benutzeroberflächenautomatisierung Struktur angezeigt, wenn ein Benutzeroberflächenautomatisierung Client die Struktur aufzählt. Außerdem werden Benutzeroberflächenautomatisierung Steuerelementmuster nur für sichtbare Elemente ausgeführt. Beispielsweise gibt das [Selection-Steuerelementmuster](uiauto-implementingselection.md) nur die sichtbaren ausgewählten Elemente zurück, wenn ein Client die [**IUIAutomationSelectionPattern::GetCurrentSelection-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection) aufruft.

Die Elementansicht unterstützt die Möglichkeit, die folgenden Informationen zu virtualisierten Elementen abzurufen:

-   Eine Anzahl der Gesamtanzahl von Elementen, einschließlich virtualisierter Elemente
-   Benutzeroberflächenautomatisierung von Elementen für virtualisierte Elemente
-   Benutzeroberflächenautomatisierung Elemente für die ausgewählten virtualisierten Elemente

## <a name="obtaining-a-count-of-all-items"></a>Abrufen einer Anzahl aller Elemente

Ein Client kann das ItemsView-Element verwenden, um eine Anzahl aller Elemente sowie eine Anzahl der ausgewählten Elemente abzurufen. Das ItemsView-Element bietet zwei Möglichkeiten, diese Anzahl abzurufen. Die erste besteht darin, die ItemStatus-Eigenschaft des ItemsView-Elements zu erhalten, und die zweite besteht darin, benutzerdefinierte Eigenschaften aus dem ItemsView-Element zu erhalten.

Die ItemStatus-Eigenschaft ist eine Zeichenfolge, die die Gesamtanzahl der Elemente und die Anzahl der ausgewählten Elemente durch ein Komma getrennt angibt. Beispiel: "3 Elemente, 1 ausgewähltes Element". Diese Zeichenfolge ist lokalisiert und kann direkt an den Benutzer übermittelt werden.

Die benutzerdefinierten Eigenschaften des ItemsView-Elements enthalten eine Eigenschaft für die Elementanzahl und eine andere für die Auswahlanzahl. Dazu gehören:

-   ItemCount \_ Property \_ GUID (ABBF5C45-5CCC-47b7-BB4E-87CB87BBD162) – Die Anzahl aller eindeutigen Elemente in der Ansicht. Wenn sie nach einer mehrwertigen Eigenschaft (MVP) gruppiert ist, sodass ein einzelnes Element mehrmals angezeigt werden kann, wird jedes Element nur einmal gezählt.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Programmatic Name: "ItemCount")

-   \_SelectedItemCount-Eigenschaften-GUID \_ (92A053DA-2969-4021-BF27-514CFC2E4A69) – Die Anzahl aller in der Ansicht ausgewählten eindeutigen Elemente. Wenn sie nach einer mehrwertigen Eigenschaft (MVP) gruppiert ist, sodass ein einzelnes Element mehrmals angezeigt werden kann, wird jedes Element nur einmal gezählt.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Programmatic Name: "SelectedItemCount")

Diese benutzerdefinierten Eigenschaften werden in Shlguid.h definiert, das im Windows Software Development Kit (SDK) enthalten ist, und diese Eigenschaften werden über die [**IUIAutomationRegistrar::RegisterProperty-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) registriert. Benutzeroberflächenautomatisierung Clients **verwenden RegisterProperty,** um Eigenschaftenbezeichner (PROPERTYIDs) für die benutzerdefinierten Eigenschaften abzurufen.

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>Abrufen eines Elementindexes in Bezug auf alle Elemente

Ein Client kann den Index eines Elements abrufen, indem er entweder die ItemStatus-Eigenschaft eines ListItem-Elements oder eine benutzerdefinierte Eigenschaft eines ListItem-Elements erhält.

Die ItemStatus-Eigenschaft ist eine Zeichenfolge, die den Index eines Elements in Bezug auf die Gesamtzahl der Elemente enthält. Beispiel: "Element 1 von 3". Diese Zeichenfolge ist lokalisiert und kann direkt an den Benutzer übermittelt werden.

Die folgende benutzerdefinierte Eigenschaft ruft den Elementindex eines ListItem-Elements ab:

-   ItemIndex \_ Property \_ GUID (92A053DA-2969-4021-BF27-514CFC2E4A69) – Der 1-basierte absolute Index eines Elements. Wenn sie nach einer Mehrwerteigenschaft (MVP) gruppiert ist, sodass ein einzelnes Element zweimal angezeigt werden kann, erhält jede Darstellung des Elements einen separaten Index.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Programmgesteuerter Name: "ItemIndex")

Diese benutzerdefinierte Eigenschaft wird in Shlguid.h definiert, die im Windows SDK enthalten ist und über die [**IUIAutomationRegistrar::RegisterProperty-Methode**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) registriert wird. Benutzeroberflächenautomatisierung Clients verwenden **RegisterProperty,** um einen Eigenschaftenbezeichner (PROPERTYIDs) für die benutzerdefinierte Eigenschaft abzurufen.

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>Abrufen eines Verweises auf ein Vitualized-Element

Ein ItemsView-Element implementiert das [ItemContainer-Steuerelementmuster](uiauto-implementingitemcontainer.md) [**(IItemContainerProvider-Schnittstelle),**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) mit dem ein Client ein Benutzeroberflächenautomatisierung Element für ein virtualisiertes Element (ein Element außerhalb des sichtbaren Bereichs) abrufen kann. ItemsView ermöglicht es dem Client, ein ListItem-Element zu finden, indem er nach den Eigenschaften Name und Selection sucht. Der Versuch, nach einer anderen Eigenschaft zu suchen, schlägt fehl.

Ein virtuelles Element implementiert nur das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) [**(IVirtualizedItemProvider-Schnittstelle).**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) Da das Element, das durch ein virtualisiertes Benutzeroberflächenautomatisierung Element dargestellt wird, noch nicht vorhanden ist, schlägt der Versuch fehl, ein anderes Steuerelementmuster oder eine andere Eigenschaft des Elements abzurufen.

Sowohl ListItem- als auch Group-Elemente werden virtualisiert, aber nur ListItem-Elemente können vom [ItemContainer-Steuerelementmuster](uiauto-implementingitemcontainer.md) zurückgegeben werden. Da der Aufruf der [**IUIAutomationItemContainerPattern::FindItemByProperty-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) im UI-Thread ausgeführt wird und blockiert wird, reagiert die Ansicht erst, wenn **FindItemByProperty** zurückgegeben wird, und alle anderen Methodenaufrufe des Anbieters müssen warten, bis **FindItemByProperty** abgeschlossen ist. In einigen Fällen muss **FindItemByProperty** das gesamte DataSet vor der Rückgabe verarbeiten, was ressourcenintensiv sein kann. Wenn **SIE NULL** als Startelement angeben, beginnt **FindItemByProperty** die Suche mit dem ersten Element in der Ansicht.

ItemsView unterstützt die folgenden Eigenschaften für [**FindItemByProperty:**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty)

-   Name (UIA \_ NamePropertyId): Sucht nach dem ersten Element, dessen Name vollständig mit der angegebenen Zeichenfolge übereinstimmt. Bei der Suche wird die Groß- und Kleinschreibung nicht berücksichtigt. Platzhalterzeichen oder Teilübereinstimmungen werden nicht unterstützt. Wenn ein **NULL-Name** angegeben wird, wird das nächste Element nach dem Startelement zurückgegeben. Durch das Angeben von **NULL-Namen** kann ein Benutzeroberflächenautomatisierung Client alle Elemente in der Ansicht auflisten. Es wird jedoch davon abgeraten, alle Elemente aufzuzählen, da dadurch alle Elemente in der Ansicht realisiert werden.
-   SelectionItem \_ IsSelected (UIA \_ SelectionItemIsSelectedPropertyId): Sucht nach dem ersten Element, dessen SelectionItem \_ IsSelected-Eigenschaft mit dem angegebenen Wert übereinstimmt. Geben Sie **TRUE** an, um das erste ausgewählte Element zu suchen, oder **FALSE,** um das erste nicht ausgewählte Element zu suchen. Seien Sie vorsichtig, wenn Sie alle ausgewählten Elemente auflisten, da die Anzahl der ausgewählten Elemente sehr groß sein kann, insbesondere, wenn der Benutzer alle Elemente ausgewählt hat.

## <a name="scrolling-a-virtualized-item-on-screen"></a>Scrollen eines virtualisierten Elements auf dem Bildschirm

Nach dem Abrufen eines Verweises auf ein Benutzeroberflächenautomatisierung-Element für ein virtualisiertes Element (off-screen) kann der Client das Element mithilfe der [**IUIAutomationVirtualizeItemPattern::Realize-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) des [VirtualizedItem-Steuerelementmusters](uiauto-implementingvirtualizeditem.md) in die Ansicht scrollen. Nachdem das Element realisiert wurde, ist es sichtbar, und alle Eigenschaften und Steuerelementmuster, die normalerweise einem ListItem-Element zugeordnet sind, sind für den Client verfügbar.

Nur ListItem-Elemente, die von der [**IUIAutomationItemContainerPattern::FindItemByProperty-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) abgerufen werden, machen das [VirtualizedItem-Steuerelementmuster](uiauto-implementingvirtualizeditem.md) verfügbar. Wenn ein Element auf dem Bildschirm außerhalb des Bildschirms gescrollt wird, wird das Element ungültig, und der Client muss **FindItemByProperty** aufrufen, um den Off-Screen-Verweis abzurufen.

Es ist auch möglich, Elemente mithilfe des [](uiauto-implementingscroll.md) Scroll-Steuerelementmusters (oder mithilfe der Bildlaufleisten) in und aus der Ansicht zu verschieben. Elemente und Gruppen werden beim Bildlauf in die Ansicht realisiert und virtualisiert, wenn sie aus der Ansicht scrollen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit virtualisierten Elementen](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




