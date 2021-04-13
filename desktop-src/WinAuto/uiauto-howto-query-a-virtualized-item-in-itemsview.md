---
title: Abfragen eines virtualisierten Elements in der Ansicht "Elemente"
description: In diesem Thema wird beschrieben, wie Sie mit der Microsoft-Benutzeroberflächen Automatisierung Benutzeroberflächen Informationen zu virtualisierten Elementen in der Ansicht "Windows 7-Elemente" abrufen.
ms.assetid: a0bff8a1-47b1-4750-8086-e2e65a79099e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a098635d6e1045c6ff4573de088d8455685014d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388649"
---
# <a name="how-to-query-a-virtualized-item-in-items-view"></a>Abfragen eines virtualisierten Elements in der Ansicht "Elemente"

In diesem Thema wird beschrieben, wie Sie mit der Microsoft-Benutzeroberflächen Automatisierung Benutzeroberflächen Informationen zu virtualisierten Elementen in der Ansicht "Windows 7-Elemente" abrufen. Das Thema enthält folgende Abschnitte:

> [!Note]  
> Dieses Thema gilt nur für Windows 7. Beachten Sie, dass sich die in diesem Thema beschriebenen Barrierefreiheits Funktionen in zukünftigen Windows-Versionen ändern können.

 

-   [Übersicht](#overview)
-   [Struktur der Element Ansicht](#items-view-tree-structure)
-   [Virtualisierung](#virtualization)
-   [Abrufen der Anzahl aller Elemente](#obtaining-a-count-of-all-items)
-   [Abrufen eines Element Indexes in Bezug auf alle Elemente](#obtaining-an-item-index-with-respect-to-all-items)
-   [Abrufen eines Verweises auf ein vitualisiertes Element](#obtaining-a-reference-to-a-vitualized-item)
-   [Scrollen eines virtualisierten Elements auf dem Bildschirm](#scrolling-a-virtualized-item-on-screen)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Die Ansicht Elemente ist eine Benutzeroberflächen Komponente, die es Benutzern ermöglicht, Dateien und andere Elemente anzuzeigen und mit Ihnen zu interagieren. In Windows 7 ersetzt die Ansicht Elemente das Listenansicht-Steuerelement für die Darstellung von Elementen in der Standardansicht von Windows-Explorer. Die Ansicht Elemente wird auch im Dialog Feld allgemeine Elemente, im Startmenü-Suchergebnis und in anderen Benutzeroberflächen Elementen von Windows 7 verwendet, die das Browser-Steuerelement von Explorer verwenden. Im Vergleich zum Listenansicht-Steuerelement bietet die Ansicht "Elemente" die folgenden Vorteile für Benutzer:

-   In der Ansicht "Elemente" können Elemente auf viel nützlichere, wünschenswert und relevante Weise dargestellt werden, sodass Benutzer Elemente einfacher, schneller und benutzerfreundlich suchen und organisieren können.
-   In der Ansicht "Elemente" können große Mengen von Elementen aus Datenquellen mit unterschiedlichen Leistungsmerkmalen angezeigt werden, sodass Benutzer ihre gesamte Auflistung von Elementen über mehrere Quellen hinweg durchsuchen und durchsuchen können.

In der folgenden Abbildung wird die Ansicht Elemente in Windows-Explorer angezeigt.

![Screenshot mit der Ansichts Komponente in Windows-Explorer mit Elementen](images/itemsview.gif)

Aus Sicht eines Entwicklers ähneln die allgemeine Struktur und Funktionalität der Ansicht Elemente der Ansicht des Listenansicht-Steuer Elements. Der Hauptunterschied besteht darin, dass die Ansicht "Elemente" Virtualisierung unterstützt, während das Listenansicht-Steuerelement dies nicht tut. Außerdem werden in der Ansicht "Elemente" zwei neue Schnittstellen zur Benutzeroberflächenautomatisierung verwendet, um sicherzustellen, dass der Zugriff auf virtualisierte Inhalte der Ansicht Diese Schnittstellen werden in den folgenden Abschnitten dieses Themas beschrieben.

Allgemeine Informationen zur Virtualisierung in der Benutzeroberflächen Automatisierung finden Sie unter [Arbeiten mit virtualisierten Elementen](uiauto-workingwithvirtualizeditems.md).

## <a name="items-view-tree-structure"></a>Struktur der Element Ansicht

In der Benutzeroberflächenautomatisierungs-Struktur hat das Benutzeroberflächenautomatisierungs-Element der Element Ansicht der obersten Ebene den Namen "itemsview" und den Steuer Elementtyp "List". In der vorherigen Abbildung ist das itemsview UI Automation-Element rot dargestellt. Unter der obersten Ebene von itemsview sind verschiedene Benutzeroberflächenautomatisierungs-Elemente vorhanden. in diesem Dokument wird jedoch nur auf zwei andere Benutzeroberflächenautomatisierungs-Elemente verwiesen: Gruppenelemente und Listenelemente.

Bei den Gruppenelementen handelt es sich um Benutzeroberflächenautomatisierungs-Elemente, die alle Listenelemente dieser Gruppe enthalten – der Steuer Elementtyp ist "Group", und ihre Namen variieren je nach Gruppenname. In der vorherigen Abbildung enthält das erste Gruppenelement sowohl den Header "a-h (1)" als auch das Listenelement "Ordner", und sein Name ist "a-h".

Die Listenelemente sind die Benutzeroberflächenautomatisierungs-Elemente, die die Blatt Elemente in der Ansicht darstellen – Ihr Steuer Elementtyp ist "ListItem", und ihre Namen variieren je nach Elementname. In der vorherigen Abbildung sind die Listenelemente die Blatt Elemente wie "Folder", "Music" und "Picture". Diese drei Benutzeroberflächenautomatisierungs-Elemente werden durch die Begriffe itemsview-Element, Group-Element und ListItem-Element im restlichen Teil dieses Dokuments bezeichnet.

## <a name="virtualization"></a>Virtualisierung

Die Ansicht "Elemente" verwendet die Virtualisierung, d. h., Elemente außerhalb des sichtbaren Bereichs der Ansicht werden nicht aus dem System abgerufen, und die Darstellung der Benutzeroberfläche wird nicht erstellt. Diese Elemente werden als *virtualisierte Elemente* bezeichnet. Da Sie nicht erstellt werden, verfügen virtualisierte Elemente nicht über Benutzeroberflächenautomatisierungs-Elemente und werden daher nicht in der Benutzeroberflächenautomatisierungs-Struktur angezeigt, wenn ein Benutzeroberflächenautomatisierungs-Client die Struktur auflistet. Außerdem funktionieren Benutzeroberflächenautomatisierungs-Steuerelement Muster nur für sichtbare Elemente. Das [Selection](uiauto-implementingselection.md) -Steuerelement Muster gibt z. b. nur die sichtbaren ausgewählten Elemente zurück, wenn ein Client die [**iuiautomationselectionpattern:: GetCurrentSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection) -Methode aufruft.

Die Ansicht Elemente unterstützt die Möglichkeit, die folgenden Informationen zu virtualisierten Elementen abzurufen:

-   Gibt die Gesamtzahl der Elemente an, einschließlich virtualisierter Elemente.
-   Benutzeroberflächenautomatisierungs-Elemente für virtualisierte Elemente
-   Benutzeroberflächenautomatisierungs-Elemente für die ausgewählten virtualisierten Elemente

## <a name="obtaining-a-count-of-all-items"></a>Abrufen der Anzahl aller Elemente

Ein Client kann das itemsview-Element verwenden, um die Anzahl aller Elemente sowie die Anzahl der ausgewählten Elemente zu erhalten. Das itemsview-Element bietet zwei Möglichkeiten, um diese Zähler zu erhalten. Der erste besteht darin, die ItemStatus-Eigenschaft des itemsview-Elements abzurufen, und der zweite besteht darin, benutzerdefinierte Eigenschaften aus dem itemsview-Element abzurufen.

Die ItemStatus-Eigenschaft ist eine Zeichenfolge, die die Anzahl der Elemente und die Anzahl der ausgewählten Elemente, getrennt durch ein Komma, angibt. Beispiel: "3 Items, 1 Element ausgewählt". Diese Zeichenfolge ist lokalisiert und kann direkt an den Benutzer übermittelt werden.

Die benutzerdefinierten Eigenschaften des Elements itemsview enthalten eine Eigenschaft für die Element Anzahl und eine weitere für die Auswahl Anzahl. Dazu gehören:

-   ItemCount- \_ Eigenschafts- \_ GUID (ABBF5C45-5CCC-47b7-BB4E-87CB87BBD162) – die Anzahl aller eindeutigen Elemente in der Sicht. Wenn eine Gruppierung nach einer mehrwertigen Eigenschaft (MVP) erfolgt, sodass ein einzelnes Element mehrmals vorkommen kann, wird jedes Element nur einmal gezählt.

    (Uiautomationtype: [**uiautomationtype \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), programmatischer Name: "ItemCount")

-   Selecteditemcount- \_ Eigenschafts- \_ GUID (92a053da-2969-4021-BF27-514cfc2e4a69) – die Anzahl der in der Ansicht ausgewählten eindeutigen Elemente. Wenn eine Gruppierung nach einer mehrwertigen Eigenschaft (MVP) erfolgt, sodass ein einzelnes Element mehrmals vorkommen kann, wird jedes Element nur einmal gezählt.

    (Uiautomationtype: [**uiautomationtype \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), programmatischer Name: "selecteditemcount")

Diese benutzerdefinierten Eigenschaften werden in shlguid. h definiert, das im Windows Software Development Kit (SDK) enthalten ist, und diese Eigenschaften werden über die [**iuiautomationregistrar:: registerproperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) -Methode registriert. Benutzeroberflächenautomatisierungs-Clients verwenden **registerproperty** zum Abrufen von Eigenschafts Bezeichners (PropertyIDs) für die benutzerdefinierten Eigenschaften.

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>Abrufen eines Element Indexes in Bezug auf alle Elemente

Ein Client kann den Index eines Elements abrufen, indem er entweder die ItemStatus-Eigenschaft eines ListItem-Elements oder eine benutzerdefinierte Eigenschaft eines ListItem-Elements erhält.

Die ItemStatus-Eigenschaft ist eine Zeichenfolge, die den Index eines Elements in Bezug auf die Gesamtanzahl von Elementen enthält. Beispiel: "Item 1 of 3". Diese Zeichenfolge ist lokalisiert und kann direkt an den Benutzer übermittelt werden.

Die folgende benutzerdefinierte Eigenschaft ruft den Element Index eines ListItem-Elements ab:

-   ItemIndex- \_ Eigenschafts- \_ GUID (92a053da-2969-4021-BF27-514cfc2e4a69) – den 1-basierten absoluten Index eines Elements. Wenn Sie nach einer mehrwertigen Eigenschaft (MVP) gruppiert werden, sodass ein einzelnes Element zweimal angezeigt werden kann, erhält jede Darstellung des Elements einen separaten Index.

    (Uiautomationtype: [**uiautomationtype \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), programmatischer Name: "ItemIndex")

Diese benutzerdefinierte Eigenschaft wird in der Datei "shlguid. h" definiert, die im Windows SDK enthalten ist und über die Methode " [**iuiautomationregistrierungs Registrierungsmethode:: registerproperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) " registriert wird. Benutzeroberflächenautomatisierungs-Clients rufen mithilfe von **registerproperty** einen Eigenschafts Bezeichner (PropertyIDs) für die benutzerdefinierte Eigenschaft ab.

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>Abrufen eines Verweises auf ein vitualisiertes Element

Ein itemsview-Element implementiert das [ItemContainer](uiauto-implementingitemcontainer.md) -Steuerelement Muster ([**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) Interface), das einem Client das Aufrufen eines Benutzeroberflächenautomatisierungs-Elements für ein virtualisiertes Element ermöglicht (ein Element, das sich außerhalb des sichtbaren Bereichs befindet). Itemsview ermöglicht es dem Client, ein ListItem-Element Durchsuchen der Eigenschaften "Name" und "Selection" zu suchen – bei dem Versuch, eine andere Eigenschaft zu suchen, tritt ein Fehler auf.

Ein virtuelles Element implementiert nur das [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Muster ([**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) -Schnittstelle). Da das Element, das von einem virtualisierten Benutzeroberflächenautomatisierungs-Element dargestellt wird, noch nicht vorhanden ist, tritt beim Versuch, ein anderes Steuerelement Muster oder eine Eigenschaft des Elements zu erhalten, ein Fehler auf.

Sowohl ListItem-als auch Group-Elemente werden virtualisiert, aber nur ListItem-Elemente können vom [ItemContainer](uiauto-implementingitemcontainer.md) -Steuerelement Muster zurückgegeben werden. Da der Aufruf der [**iuiautomationitemcontainerpattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) -Methode im UI-Thread ausgeführt wird und blockiert wird, antwortet die Ansicht erst, wenn **FindItemByProperty** zurückgibt, und alle anderen Methodenaufrufe für den Anbieter müssen warten, bis **FindItemByProperty** abgeschlossen ist. In einigen Fällen muss **FindItemByProperty** das gesamte Dataset vor der Rückgabe verarbeiten, was ressourcenintensiv sein kann. Das Angeben von **null** als Start Element bewirkt, dass **FindItemByProperty** die Suche mit dem ersten Element in der Ansicht startet.

Itemsview unterstützt die folgenden Eigenschaften für [**FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty):

-   Name (UIA \_ namepropertyid) – sucht nach dem ersten Element, dessen Name vollständig mit der angegebenen Zeichenfolge übereinstimmt. Bei der Suche wird die Groß- und Kleinschreibung nicht berücksichtigt. Platzhalter Zeichen oder partielle Übereinstimmungen werden nicht unterstützt. Wenn ein **null** -Name angegeben wird, wird das nächste Element nach dem Start Element zurückgegeben. Durch Angeben von **null** -Namen kann ein Benutzeroberflächenautomatisierungs-Client alle Elemente in der Ansicht auflisten. Allerdings wird davon abgeraten, alle Elemente aufzuzählen, da dadurch alle Elemente in der Ansicht realisiert werden.
-   SelectionItem \_ issselect (UIA \_ selectionitemisselectedpropertyid) – sucht nach dem ersten Element, dessen SelectionItem \_ issgewählte-Eigenschaft mit dem angegebenen Wert übereinstimmt. Geben Sie **true** an, um das erste ausgewählte Element zu suchen, oder **false** , um das erste nicht ausgewählte Element zu suchen. Seien Sie vorsichtig, wenn Sie alle ausgewählten Elemente auflisten, weil die Anzahl der ausgewählten Elemente sehr groß sein kann, insbesondere, wenn der Benutzer alle Elemente ausgewählt hat.

## <a name="scrolling-a-virtualized-item-on-screen"></a>Scrollen eines virtualisierten Elements auf dem Bildschirm

Nachdem Sie einen Verweis auf ein Benutzeroberflächenautomatisierungs-Element für ein virtualisiertes (Bildschirm-) Element abgerufen haben, kann der Client mithilfe der [**iuiautomationvirtualizeitempattern::**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) Shoot-Methode des [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Musters einen Bildlauf durchführen. Nachdem das Element erkannt wurde, ist es sichtbar, und alle Eigenschaften und Steuerelement Muster, die normalerweise einem ListItem-Element zugeordnet sind, stehen dem Client zur Verfügung.

Nur ListItem-Elemente, die von der [**iuiautomationitemcontainerpattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) -Methode abgerufen werden, machen das [VirtualizedItem](uiauto-implementingvirtualizeditem.md) -Steuerelement Muster verfügbar. Wenn ein Bild auf einem Bildschirm vom Bildschirm entfernt wird, wird das Element ungültig, und der Client muss **FindItemByProperty** aufrufen, um den Bildschirm Verweis zu erhalten.

Es ist auch möglich, Elemente mithilfe des [Scroll](uiauto-implementingscroll.md) -Steuerelement Musters (oder mithilfe der Scrollleisten) in die Ansicht und aus der Ansicht zu verschieben. Elemente und Gruppen werden beim Scrollen in der Ansicht realisiert und virtualisiert, wenn Sie in der Ansicht einen Bildlauf durchführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit virtualisierten Elementen](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




