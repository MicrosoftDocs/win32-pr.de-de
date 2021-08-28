---
title: Benutzeroberflächenautomatisierung-Spezifikation
description: Dieses Thema bietet eine Übersicht über die Microsoft Benutzeroberflächenautomatisierung-Spezifikation, die die Grundlage der Windows Implementierung von Benutzeroberflächenautomatisierung bildet.
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d78298299241545033b25dccc8d79376ec55e1b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987643"
---
# <a name="ui-automation-specification"></a>Benutzeroberflächenautomatisierung-Spezifikation

Dieses Thema bietet eine Übersicht über die Microsoft Benutzeroberflächenautomatisierung-Spezifikation, die die Grundlage der Windows Implementierung von Benutzeroberflächenautomatisierung bildet. Die Benutzeroberflächenautomatisierung-Spezifikation kann auf anderen Plattformen als Microsoft Windows unterstützt werden. Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierung-Spezifikation.](./uiauto-specandcommunitypromise.md)

Dieses Thema enthält folgende Abschnitte:

-   [Einführung](#introducton)
-   [Benutzeroberflächenautomatisierung-Elemente](#ui-automation-elements)
-   [Benutzeroberflächenautomatisierung-Struktur](#ui-automation-tree)
-   [Benutzeroberflächenautomatisierung-Eigenschaften](#ui-automation-properties)
-   [Steuerelementmuster für Benutzeroberflächenautomatisierung](#ui-automation-control-patterns)
-   [Steuerelementtypen der Benutzeroberflächenautomatisierung](#ui-automation-control-types)
-   [Benutzeroberflächenautomatisierung-Ereignisse](#ui-automation-events)
-   [Zugehörige Themen](#related-topics)

## <a name="introducton"></a>Einführung

Die Benutzeroberflächenautomatisierung-Spezifikation bietet flexiblen programmgesteuerten Zugriff auf Benutzeroberflächenelemente auf dem Windows Desktop, sodass Hilfstechnologieprodukte wie Sprachausgaben Endbenutzern Informationen über die Benutzeroberfläche bereitstellen und die Benutzeroberfläche mit anderen Mitteln als standardeingaben bearbeiten können.

Benutzeroberflächenautomatisierung ist umfassender als nur eine Schnittstellendefinition. Sie bietet:

-   Ein Objektmodell und Funktionen, die clientanwendungen das Empfangen von Ereignissen, das Abrufen von Eigenschaftswerten und das Bearbeiten von Benutzeroberflächenelementen erleichtern.
-   Eine Kerninfrastruktur zum Suchen und Abrufen über Prozessgrenzen hinweg.
-   Eine Reihe von Schnittstellen für Anbieter, um die Struktur, allgemeine Eigenschaften und Funktionen von Benutzeroberflächenelementen auszudrücken.
-   Eine Eigenschaft vom Typ "Steuerelement", mit der Clients und Anbieter die allgemeinen Eigenschaften, Funktionen und Die Struktur eines BENUTZEROBERFLÄCHEN-Objekts eindeutig angeben können.

Benutzeroberflächenautomatisierung verbessert die Microsoft Active Accessibility durch:

-   Aktivieren effizienter Out-of-Process-Clients, während der Prozesszugriff weiterhin zugelassen wird.
-   Verfügbarmachen weiterer Informationen zur Benutzeroberfläche auf eine Weise, die es Clients ermöglicht, prozessexernt zu werden.
-   Koexistieren mit und Nutzen von Microsoft Active Accessibility, ohne dessen Einschränkungen zu erben. Weitere Informationen finden Sie unter [Microsoft Active Accessibility und Benutzeroberflächenautomatisierung Vergleich.](microsoft-active-accessibility-and-ui-automation-compared.md)
-   Bereitstellen einer Alternative zu [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) die einfach zu implementieren ist.

Die Implementierung der Benutzeroberflächenautomatisierung Specification in Windows Features Component Object Model (COM)-basierten Schnittstellen und verwalteten Schnittstellen.

## <a name="ui-automation-elements"></a>Benutzeroberflächenautomatisierung-Elemente

Benutzeroberflächenautomatisierung macht jedes Element der Benutzeroberfläche für Clientanwendungen als *Automatisierungselement* verfügbar. Anbieter stellen Eigenschaftswerte für jedes Element bereit. Elemente werden als Struktur verfügbar gemacht, wobei der Desktop als Stammelement verwendet wird.

Automatisierungselemente machen allgemeine Eigenschaften der Benutzeroberflächenelemente verfügbar, die sie darstellen. Eine dieser Eigenschaften ist der Steuerelementtyp, der seine grundlegende Darstellung und Funktionalität beschreibt (z. B. eine Schaltfläche oder ein Kontrollkästchen).

## <a name="ui-automation-tree"></a>Benutzeroberflächenautomatisierung-Struktur

Die Benutzeroberflächenautomatisierung-Struktur stellt die gesamte Benutzeroberfläche dar: Das Stammelement ist der aktuelle Desktop, und untergeordnete Elemente sind Anwendungsfenster. Jedes dieser untergeordneten Elemente kann Elemente enthalten, die Menüs, Schaltflächen, Symbolleisten usw. darstellen. Diese Elemente können wiederum Elemente wie Listenelemente enthalten, wie in der folgenden Abbildung dargestellt.

![Screenshot: Benutzeroberflächenautomatisierungs-Struktur](images/uiatree.gif)

Beachten Sie, dass die Reihenfolge der gleichgeordneten Elemente in der Benutzeroberflächenautomatisierung-Struktur sehr wichtig ist. Objekte, die sich visuell nebeneinander befinden, sollten sich auch in der Benutzeroberflächenautomatisierung Struktur nebeneinander befinden.

Benutzeroberflächenautomatisierung Anbieter für ein bestimmtes Steuerelement unterstützen die Navigation zwischen den untergeordneten Elementen dieses Steuerelements. Anbieter befassen sich jedoch nicht mit der Navigation zwischen diesen Steuerelementunterstrukturen. Dies wird vom Benutzeroberflächenautomatisierung Core verwaltet, wobei Informationen von den Standardfensteranbietern verwendet werden.

Damit Clients Benutzeroberflächeninformationen effektiver verarbeiten können, unterstützt das Framework alternative Ansichten der Automatisierungsstruktur: Rohansicht, Steuerelementansicht und Inhaltsansicht. Wie die folgende Tabelle zeigt, bestimmt der Filtertyp die Ansichten, und der Client definiert den Bereich einer Sicht.



| Automatisierungsstruktur | BESCHREIBUNG                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| Rohdatenansicht        | Die vollständige Struktur von Automatisierungselementobjekten, für die der Desktop der Stamm ist.                                          |
| Steuerelementansicht    | Eine Teilmenge der rohen Ansicht, die der Benutzeroberflächenstruktur genau so zugeordnet ist, wie sie vom Benutzer wahrgenommen wird.                                |
| Inhaltsansicht    | Eine Teilmenge der Steuerelementansicht, die inhalte enthält, die für den Benutzer am relevantesten sind, z. B. die Werte in einem Dropdown-Kombinationsfeld. |



 

Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierung Tree Overview](uiauto-treeoverview.md).

## <a name="ui-automation-properties"></a>Benutzeroberflächenautomatisierung-Eigenschaften

Die Benutzeroberflächenautomatisierung Specification definiert zwei Arten von Eigenschaften: Eigenschaften von Automatisierungselementen und Steuerelementmustereigenschaften. Automatisierungselementeigenschaften gelten für die meisten Steuerelemente und stellen grundlegende Informationen zum Element bereit, z. B. seinen Namen. Steuerelementmustereigenschaften gelten für Steuerelementmuster, die als Nächstes beschrieben werden.

Im Gegensatz zu Microsoft Active Accessibility wird jede Benutzeroberflächenautomatisierung-Eigenschaft durch eine GUID und einen programmgesteuerten Namen identifiziert, wodurch neue Eigenschaften einfacher eingeführt werden können.

Weitere Informationen finden Sie unter [UI Automation Properties Overview](uiauto-propertiesoverview.md).

## <a name="ui-automation-control-patterns"></a>Steuerelementmuster für Benutzeroberflächenautomatisierung

Ein Steuerelementmuster beschreibt einen bestimmten Aspekt der Funktionalität eines Automatisierungselements. Beispielsweise sollte ein einfaches "Klick-fähig"-Steuerelement wie eine Schaltfläche oder ein Link das Invoke-Steuerelementmuster unterstützen, um die Aktion "Klicken" darzustellen.

Jedes Steuerelementmuster ist eine kanonische Darstellung möglicher Benutzeroberflächenfeatures und -funktionen. Die aktuelle Implementierung von Benutzeroberflächenautomatisierung definiert 22 Steuerelementmuster. Die Windows Automation-API kann auch benutzerdefinierte Steuerelementmuster unterstützen. Im Gegensatz zu Microsoft Active Accessibility Rollen- oder Zustandseigenschaften kann ein Automatisierungselement mehrere Benutzeroberflächenautomatisierung Steuerelementmuster unterstützen.

Weitere Informationen finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="ui-automation-control-types"></a>Steuerelementtypen der Benutzeroberflächenautomatisierung

Ein Steuerelementtyp ist eine Automatisierungselementeigenschaft, die ein bekanntes Steuerelement angibt, das das Element darstellt. Derzeit definiert Benutzeroberflächenautomatisierung 38 Steuerelementtypen, einschließlich Schaltfläche, Kontrollkästchen, ComboBox, DataGrid, Dokument, Hyperlink, Bild, QuickInfo, Struktur und Fenster.

Bevor Sie einem Element einen Steuerelementtyp zuweisen können, muss das Element bestimmte Bedingungen erfüllen, einschließlich einer bestimmten Automatisierungsstruktur, Eigenschaftswerte, Steuerelementmuster und Ereignisse. Sie sind jedoch nicht auf diese beschränkt. Sie können ein Steuerelement mit benutzerdefinierten Mustern und Eigenschaften sowie mit den vordefinierten erweitern.

Die Gesamtanzahl vordefinierter Steuerelementtypen ist deutlich niedriger als Microsoft Active Accessibility [Objektrollen,](object-roles.md)da Benutzeroberflächenautomatisierung Steuerelementmuster kombiniert werden können, um einen größeren Satz von Features auszudrücken, während Microsoft Active Accessibility Rollen nicht können.

Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

## <a name="ui-automation-events"></a>Benutzeroberflächenautomatisierung-Ereignisse

Benutzeroberflächenautomatisierung Ereignisse benachrichtigen Anwendungen über Änderungen an und aktionen, die mit Automatisierungselementen ausgeführt werden. Es gibt vier verschiedene Typen von Benutzeroberflächenautomatisierung Ereignissen, und sie bedeuten nicht notwendigerweise, dass sich der visuelle Zustand der Benutzeroberfläche geändert hat. Das Benutzeroberflächenautomatisierung Ereignismodell ist unabhängig vom [WinEvent-Framework](winevents-infrastructure.md) in Windows, obwohl die Windows Automation-API Benutzeroberflächenautomatisierung Ereignisse mit dem Microsoft Active Accessibility Framework interoperabel macht.

Weitere Informationen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Zugehörige Themen

[Benutzeroberflächenautomatisierung Specification](./uiauto-specandcommunitypromise.md), [Windows Automation API Overview](windows-automation-api-overview.md)
