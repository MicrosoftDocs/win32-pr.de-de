---
title: Benutzeroberflächenautomatisierungs
description: Dieses Thema enthält eine Übersicht über die Microsoft UI Automation-Spezifikation, die die Grundlage der Windows-Implementierung der Benutzeroberflächen Automatisierung bildet.
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d3cbb7ed2caa49e855b25f749820de8cf24f1e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039233"
---
# <a name="ui-automation-specification"></a>Benutzeroberflächenautomatisierungs

Dieses Thema enthält eine Übersicht über die Microsoft UI Automation-Spezifikation, die die Grundlage der Windows-Implementierung der Benutzeroberflächen Automatisierung bildet. Die Benutzeroberflächenautomatisierungs-Spezifikation kann auf anderen Plattformen als Microsoft Windows unterstützt werden. Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierungs-Spezifikation](./uiauto-specandcommunitypromise.md) .

Dieses Thema enthält folgende Abschnitte:

-   [Einführung](#introducton)
-   [Benutzeroberflächen-Automatisierungselemente](#ui-automation-elements)
-   [UI-Automatisierungs Struktur](#ui-automation-tree)
-   [Eigenschaften der Benutzeroberflächen Automatisierung](#ui-automation-properties)
-   [Steuerelementmuster für Benutzeroberflächenautomatisierung](#ui-automation-control-patterns)
-   [Steuerelementtypen der Benutzeroberflächenautomatisierung](#ui-automation-control-types)
-   [Benutzeroberflächen-Automatisierungs Ereignisse](#ui-automation-events)
-   [Zugehörige Themen](#related-topics)

## <a name="introducton"></a>Einführung

Die Benutzeroberflächenautomatisierungs-Spezifikation bietet flexiblen programmgesteuerten Zugriff auf Benutzeroberflächen Elemente auf dem Windows-Desktop, sodass Hilfstechnologieprodukte wie Sprachausgabe Informationen zur Benutzeroberfläche für Endbenutzer bereitstellen und die Benutzeroberfläche auf andere Weise als Standard Eingaben bearbeiten können.

Die Automatisierung der Benutzeroberfläche ist im Gültigkeitsbereich größer als nur eine Schnittstellen Definition. Sie bietet:

-   Ein Objektmodell und Funktionen, mit denen Client Anwendungen problemlos Ereignisse empfangen, Eigenschaftswerte abrufen und UI-Elemente bearbeiten können.
-   Eine Kerninfrastruktur zum Suchen und Abrufen über Prozess Grenzen hinweg.
-   Ein Satz von Schnittstellen für Anbieter zum Ausdrücken der Baumstruktur, allgemeiner Eigenschaften und Funktionen von UI-Elementen.
-   Eine Eigenschaft vom Typ "Steuerelement", die es Clients und Anbietern ermöglicht, die allgemeinen Eigenschaften, Funktionen und die Struktur eines UI-Objekts eindeutig anzugeben.

Die Automatisierung der Benutzeroberfläche verbessert bei Microsoft Active Accessibility durch:

-   Effiziente prozessübergreifende Clients werden aktiviert, während der Prozess interne Zugriff weiterhin möglich ist.
-   Verfügbar machen von mehr Informationen über die Benutzeroberfläche auf eine Weise, die es Clients ermöglicht, außerhalb des Prozesses zu sein.
-   Mit und der Nutzung von Microsoft Active Accessibility, ohne seine Einschränkungen zu erben. Weitere Informationen finden Sie unter [Vergleich von Microsoft Active Accessibility und UI-Automatisierung](microsoft-active-accessibility-and-ui-automation-compared.md).
-   Bietet eine Alternative zu [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , die einfach zu implementieren ist.

Die Implementierung der Benutzeroberflächenautomatisierungs-Spezifikation in Windows Features Component Object Model (com)-basierten Schnittstellen und verwalteten Schnittstellen.

## <a name="ui-automation-elements"></a>Benutzeroberflächen-Automatisierungselemente

Die Benutzeroberflächen Automatisierung macht alle Elemente der Benutzeroberfläche als *Automatisierungs Element* für Client Anwendungen verfügbar. Anbieter geben Eigenschaftswerte für jedes Element an. Elemente werden als Baumstruktur mit dem Desktop als Stamm Element verfügbar gemacht.

Automatisierungselemente machen allgemeine Eigenschaften der von Ihnen dargestellten Benutzeroberflächen Elemente verfügbar. Eine dieser Eigenschaften ist der Steuerelement-Typ, der die grundlegende Darstellung und Funktionalität beschreibt (z. b. eine Schaltfläche oder ein Kontrollkästchen).

## <a name="ui-automation-tree"></a>UI-Automatisierungs Struktur

Die Benutzeroberflächenautomatisierungs-Struktur stellt die gesamte Benutzeroberfläche dar: das Stamm Element ist der aktuelle Desktop, und untergeordnete Elemente sind Anwendungsfenster. Jedes dieser untergeordneten Elemente kann Elemente enthalten, die Menüs, Schaltflächen, Symbolleisten usw. darstellen. Diese Elemente können wiederum Elemente wie Listenelemente enthalten, wie in der folgenden Abbildung dargestellt.

![Screenshot der Benutzeroberflächenautomatisierungs-Struktur](images/uiatree.gif)

Beachten Sie, dass die Reihenfolge der gleich geordneten Elemente in der Benutzeroberflächenautomatisierungs-Struktur sehr wichtig ist. Objekte, die sich nebeneinander nebeneinander befinden, sollten sich auch in der Benutzeroberflächenautomatisierungs-Struktur nebeneinander befinden.

Benutzeroberflächenautomatisierungs-Anbieter für ein bestimmtes Steuerelement unterstützen die Navigation zwischen den untergeordneten Elementen dieses Steuer Elements. Die Navigation zwischen diesen Steuerungsteil Strukturen ist jedoch nicht von den Anbietern betroffen. Dies wird vom Benutzeroberflächenautomatisierungs-Kern mithilfe von Informationen aus den Standardfenster Anbietern verwaltet.

Damit die Benutzeroberflächen Informationen von Clients effektiver verarbeitet werden können, unterstützt das Framework Alternative Ansichten der Automatisierungs Struktur: Rohdaten Ansicht, Steuerelement Ansicht und Inhaltsansicht. Wie die folgende Tabelle zeigt, bestimmt der Filtertyp die Sichten, und der Client definiert den Bereich einer Ansicht.



| Automatisierungs Struktur | BESCHREIBUNG                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| Rohdatenansicht        | Die vollständige Struktur von Automatisierungs Element Objekten, für die der Desktop der Stamm ist.                                          |
| Steuerelementansicht    | Eine Teilmenge der Rohdaten Ansicht, die der UI-Struktur genau zugeordnet ist, wenn der Benutzer sie wahrnimmt.                                |
| Inhaltsansicht    | Eine Teilmenge der Steuerelement Ansicht, die Inhalte enthält, die für den Benutzer am relevantesten sind, wie z. b. die Werte in einem Dropdown-Kombinations Feld. |



 

Weitere Informationen finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).

## <a name="ui-automation-properties"></a>Eigenschaften der Benutzeroberflächen Automatisierung

Die Benutzeroberflächenautomatisierungs-Spezifikation definiert zwei Arten von Eigenschaften: Automatisierungs Element Eigenschaften und Steuerelement Muster Eigenschaften. Automatisierungs Element Eigenschaften gelten für die meisten Steuerelemente und bieten grundlegende Informationen über das Element, z. b. den Namen. Steuerelement Muster Eigenschaften gelten für Steuerelement Muster, die im folgenden beschrieben werden.

Anders als bei Microsoft Active Accessibility wird jede Benutzeroberflächenautomatisierungs-Eigenschaft durch eine GUID und einen programmatischen Namen identifiziert, wodurch neue Eigenschaften leichter eingeführt werden.

Weitere Informationen finden Sie unter [UI Automation Properties Overview](uiauto-propertiesoverview.md).

## <a name="ui-automation-control-patterns"></a>Steuerelementmuster für Benutzeroberflächenautomatisierung

Ein Steuerelement Muster beschreibt einen bestimmten Aspekt der Funktionalität eines Automation-Elements. Beispielsweise sollte ein einfaches "Click-able"-Steuerelement wie eine Schaltfläche oder ein Hyperlink das Steuerelement Muster zum Aufrufen der Aktion "Click" unterstützen.

Jedes Steuerelement Muster ist eine kanonische Darstellung von möglichen UI-Funktionen und-Funktionen. Die aktuelle Implementierung der Benutzeroberflächen Automatisierung definiert 22 Steuerelement Muster. Die Windows-Automatisierungs-API kann auch benutzerdefinierte Steuerelement Muster unterstützen. Im Gegensatz zu Eigenschaften von Microsoft Active Accessibility Role oder State kann ein Automation-Element mehrere Benutzeroberflächenautomatisierungs-Steuerelement Muster unterstützen.

Weitere Informationen finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="ui-automation-control-types"></a>Steuerelementtypen der Benutzeroberflächenautomatisierung

Ein Steuer Elementtyp ist eine Automatisierungs Element Eigenschaft, die ein bekanntes Steuerelement angibt, das das Element darstellt. Derzeit definiert die Benutzeroberflächen Automatisierung 38-Steuerelement Typen, einschließlich Schaltfläche, CheckBox, ComboBox, DataGrid, Dokument, Hyperlink, Bild, QuickInfo, Struktur und Fenster.

Bevor Sie einem-Element einen Steuer Elementtyp zuweisen können, muss das-Element bestimmte Bedingungen erfüllen, darunter eine bestimmte Automatisierungs Struktur, Eigenschaftswerte, Steuerelement Muster und Ereignisse. Sie sind jedoch nicht auf diese beschränkt. Sie können ein Steuerelement mit benutzerdefinierten Mustern und Eigenschaften sowie mit vordefinierten Elementen erweitern.

Die Gesamtanzahl der vordefinierten Steuerelement Typen ist deutlich niedriger als die Microsoft Active Accessibility- [Objekt Rollen](object-roles.md), da Benutzeroberflächenautomatisierungs-Steuerelement Typen kombiniert werden können, um eine größere Anzahl von Features auszudrücken, während Microsoft Active Accessibility Rollen nicht.

Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

## <a name="ui-automation-events"></a>Benutzeroberflächen-Automatisierungs Ereignisse

Benutzeroberflächenautomatisierungs-Ereignisse benachrichtigen Anwendungen über Änderungen an und Aktionen, die mit Automatisierungs Elementen ausgeführt wurden. Es gibt vier verschiedene Arten von Benutzeroberflächenautomatisierungs-Ereignissen. Dies bedeutet nicht notwendigerweise, dass sich der visuelle Zustand der Benutzeroberfläche geändert hat. Das Benutzeroberflächenautomatisierungs-Ereignis Modell ist unabhängig vom [WinEvent](winevents-infrastructure.md) -Framework in Windows, obwohl die Windows-Automatisierungs-API Ereignisse für die Benutzeroberflächen Automatisierung mit Microsoft Active Accessibility Framework interoperabel macht.

Weitere Informationen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Zugehörige Themen

[Benutzeroberflächenautomatisierungs-Spezifikation](./uiauto-specandcommunitypromise.md), [Windows Automation API Overview](windows-automation-api-overview.md)