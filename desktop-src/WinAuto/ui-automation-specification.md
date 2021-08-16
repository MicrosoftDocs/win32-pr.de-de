---
title: Benutzeroberflächenautomatisierung Spezifikation
description: Dieses Thema bietet eine Übersicht über die Microsoft Benutzeroberflächenautomatisierung Specification, die die Grundlage für die Windows-Implementierung Benutzeroberflächenautomatisierung.
ms.assetid: 45160767-09b0-4fd1-bd73-bc5ac0e6f75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fc07b70128a401d48813ded68c31dfcfca5bb5a49d2ca46683e9a902af003ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325096"
---
# <a name="ui-automation-specification"></a>Benutzeroberflächenautomatisierung Spezifikation

Dieses Thema bietet eine Übersicht über die Microsoft Benutzeroberflächenautomatisierung Specification, die die Grundlage für die Windows-Implementierung Benutzeroberflächenautomatisierung. Die Benutzeroberflächenautomatisierung-Spezifikation kann auf anderen Plattformen als Microsoft Windows. Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierung Spezifikation.](./uiauto-specandcommunitypromise.md)

Dieses Thema enthält folgende Abschnitte:

-   [Einführung](#introducton)
-   [Benutzeroberflächenautomatisierung Elements](#ui-automation-elements)
-   [Benutzeroberflächenautomatisierung Struktur](#ui-automation-tree)
-   [Benutzeroberflächenautomatisierung Eigenschaften](#ui-automation-properties)
-   [Steuerelementmuster für Benutzeroberflächenautomatisierung](#ui-automation-control-patterns)
-   [Steuerelementtypen der Benutzeroberflächenautomatisierung](#ui-automation-control-types)
-   [Benutzeroberflächenautomatisierung Ereignisse](#ui-automation-events)
-   [Zugehörige Themen](#related-topics)

## <a name="introducton"></a>Einführung

Die Benutzeroberflächenautomatisierung-Spezifikation bietet flexiblen programmgesteuerten Zugriff auf Benutzeroberflächenelemente auf dem Windows-Desktop, sodass Hilfstechnologieprodukte wie Spracheingaben Endbenutzern Informationen über die Benutzeroberfläche bereitstellen und die Benutzeroberfläche mit anderen Als-Standardeingaben bearbeiten können.

Benutzeroberflächenautomatisierung ist im Gültigkeitsbereich umfassender als nur eine Schnittstellendefinition. Sie bietet:

-   Ein Objektmodell und Funktionen, die es Clientanwendungen einfach machen, Ereignisse zu empfangen, Eigenschaftswerte abzurufen und Benutzeroberflächenelemente zu bearbeiten.
-   Eine Kerninfrastruktur zum Suchen und Abrufen über Prozessgrenzen hinweg.
-   Eine Reihe von Schnittstellen für Anbieter, um die Struktur, allgemeine Eigenschaften und Funktionen von Benutzeroberflächenelementen auszudrücken.
-   Eine Eigenschaft vom Typ "Steuerelement", mit der Clients und Anbieter die allgemeinen Eigenschaften, Funktionen und Die Struktur eines Benutzeroberflächenobjekts eindeutig angeben können.

Benutzeroberflächenautomatisierung verbessert die Microsoft Active Accessibility durch:

-   Ermöglichen effizienter Out-of-Process-Clients und gleichzeitiges Zulassen des In-Process-Zugriffs.
-   Machen Sie weitere Informationen zur Benutzeroberfläche auf eine Weise verfügbar, die es Clients ermöglicht, prozesse out-of-process zu sein.
-   Das Nebeneinander von und die Nutzung von Microsoft Active Accessibility ohne seine Einschränkungen zu erben. Weitere Informationen finden Sie unter [Microsoft Active Accessibility und Benutzeroberflächenautomatisierung Vergleich von](microsoft-active-accessibility-and-ui-automation-compared.md).
-   Bereitstellen einer einfach zu implementierenden Alternative zu [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

Die Implementierung der Benutzeroberflächenautomatisierung Specification in Windows features Component Object Model (COM)-basierten Schnittstellen und verwalteten Schnittstellen.

## <a name="ui-automation-elements"></a>Benutzeroberflächenautomatisierung Elements

Benutzeroberflächenautomatisierung macht jeden Teil der Benutzeroberfläche für Clientanwendungen als *Automatisierungselement verfügbar.* Anbieter geben Eigenschaftswerte für jedes Element an. Elemente werden als Struktur verfügbar gemacht, während der Desktop als Stammelement verwendet wird.

Automatisierungselemente machen allgemeine Eigenschaften der von ihnen repräsentierten Benutzeroberflächenelemente verfügbar. Eine dieser Eigenschaften ist der Steuerelementtyp, der seine grundlegende Darstellung und Funktionalität beschreibt (z. B. eine Schaltfläche oder ein Kontrollkästchen).

## <a name="ui-automation-tree"></a>Benutzeroberflächenautomatisierung Struktur

Die Benutzeroberflächenautomatisierung-Struktur stellt die gesamte Benutzeroberfläche dar: Das Stammelement ist der aktuelle Desktop, und untergeordnete Elemente sind Anwendungsfenster. Jedes dieser untergeordneten Elemente kann Elemente enthalten, die Menüs, Schaltflächen, Symbolleisten und so weiter darstellen. Diese Elemente können wiederum Elemente wie Listenelemente enthalten, wie die folgende Abbildung zeigt.

![Screenshot: Benutzeroberflächenautomatisierungs-Struktur](images/uiatree.gif)

Beachten Sie, dass die Reihenfolge der gleichgeordneten Elemente in der Benutzeroberflächenautomatisierung sehr wichtig ist. Objekte, die sich visuell nebeneinander befinden, sollten sich auch in der Struktur des Benutzeroberflächenautomatisierung befinden.

Benutzeroberflächenautomatisierung-Anbieter für ein bestimmtes Steuerelement unterstützen die Navigation zwischen den untergeordneten Elementen dieses Steuerelements. Anbieter sind jedoch nicht mit der Navigation zwischen diesen Unterstrukturen von Steuerelementen besäubt. Dies wird vom Benutzeroberflächenautomatisierung Core verwaltet, indem Informationen von den Standardfensteranbietern verwendet werden.

Um Clients bei der effektiveren Verarbeitung von Benutzeroberflächeninformationen zu unterstützen, unterstützt das Framework alternative Ansichten der Automatisierungsstruktur: rohe Ansicht, Steuerelementansicht und Inhaltsansicht. Wie die folgende Tabelle zeigt, bestimmt der Filtertyp die Ansichten, und der Client definiert den Bereich einer Sicht.



| Automatisierungsstruktur | Beschreibung                                                                                                             |
|-----------------|-------------------------------------------------------------------------------------------------------------------------|
| Rohdatenansicht        | Die vollständige Struktur von Automatisierungselementobjekten, für die der Desktop der Stamm ist.                                          |
| Steuerelementansicht    | Eine Teilmenge der unformatierten Ansicht, die der Benutzeroberflächenstruktur genau so zuteil wird, wie der Benutzer sie wahrnimmt.                                |
| Inhaltsansicht    | Eine Teilmenge der Steuerelementansicht, die inhalte enthält, die für den Benutzer am relevantesten sind, z. B. die Werte in einem Dropdown-Kombinationsfeld. |



 

Weitere Informationen finden Sie unter [Benutzeroberflächenautomatisierung Strukturübersicht.](uiauto-treeoverview.md)

## <a name="ui-automation-properties"></a>Benutzeroberflächenautomatisierung Eigenschaften

Die Benutzeroberflächenautomatisierung Spezifikation definiert zwei Arten von Eigenschaften: Eigenschaften von Automatisierungselemente und Steuerelementmustereigenschaften. Automatisierungselementeigenschaften gelten für die meisten Steuerelemente und bieten grundlegende Informationen zum Element, z. B. seinen Namen. Steuerelementmustereigenschaften gelten für Steuerelementmuster, die als Nächstes beschrieben werden.

Im Gegensatz Microsoft Active Accessibility wird jede Benutzeroberflächenautomatisierung-Eigenschaft durch eine GUID und einen programmgesteuerten Namen identifiziert, wodurch die Einführung neuer Eigenschaften vereinfacht wird.

Weitere Informationen finden Sie unter [UI Automation Properties Overview](uiauto-propertiesoverview.md).

## <a name="ui-automation-control-patterns"></a>Steuerelementmuster für Benutzeroberflächenautomatisierung

Ein Steuerelementmuster beschreibt einen bestimmten Aspekt der Funktionalität eines Automatisierungselements. Beispielsweise sollte ein einfaches "Klick-fähig"-Steuerelement wie eine Schaltfläche oder ein Link das Invoke-Steuerelementmuster unterstützen, um die Aktion "Click" (Klicken) zu darstellen.

Jedes Steuerelementmuster ist eine kanonische Darstellung möglicher Benutzeroberflächenfeatures und -funktionen. Die aktuelle Implementierung von Benutzeroberflächenautomatisierung definiert 22 Steuerelementmuster. Die Windows Automation-API kann auch benutzerdefinierte Steuerelementmuster unterstützen. Im gegensatz Microsoft Active Accessibility Rollen- oder Zustandseigenschaften kann ein Automatisierungselement mehrere Benutzeroberflächenautomatisierung unterstützen.

Weitere Informationen finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

## <a name="ui-automation-control-types"></a>Steuerelementtypen der Benutzeroberflächenautomatisierung

Ein Steuerelementtyp ist eine Automatisierungselementeigenschaft, die ein bekanntes Steuerelement angibt, das das Element darstellt. Derzeit definiert Benutzeroberflächenautomatisierung 38 Steuerelementtypen, einschließlich Button, CheckBox, ComboBox, DataGrid, Document, Hyperlink, Image, QuickInfo, Tree und Window.

Bevor Sie einem Element einen Steuerelementtyp zuweisen können, muss das Element bestimmte Bedingungen erfüllen, einschließlich einer bestimmten Automatisierungsstrukturstruktur, Eigenschaftswerten, Steuerelementmustern und Ereignissen. Sie sind jedoch nicht auf diese beschränkt. Sie können ein Steuerelement mit benutzerdefinierten Mustern und Eigenschaften sowie mit den vordefinierten erweitern.

Die Gesamtanzahl vordefinierter Steuerelementtypen ist deutlich [](object-roles.md)niedriger als Microsoft Active Accessibility-Objektrollen, da Benutzeroberflächenautomatisierung-Steuerelementtypen kombiniert werden können, um einen größeren Satz von Funktionen auszudrücken, während Microsoft Active Accessibility Rollen nicht möglich ist.

Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).

## <a name="ui-automation-events"></a>Benutzeroberflächenautomatisierung Ereignisse

Benutzeroberflächenautomatisierung Ereignisse benachrichtigen Anwendungen über Änderungen an und Aktionen, die mit Automatisierungselementen durchgeführt werden. Es gibt vier verschiedene Arten von Benutzeroberflächenautomatisierung ereignissen, und sie bedeuten nicht notwendigerweise, dass sich der visuelle Zustand der Benutzeroberfläche geändert hat. Das Benutzeroberflächenautomatisierung-Ereignismodell ist unabhängig vom [WinEvent-Framework](winevents-infrastructure.md) in Windows, obwohl die Windows Automation-API Benutzeroberflächenautomatisierung Ereignisse mit dem Microsoft Active Accessibility interoperabel macht.

Weitere Informationen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Zugehörige Themen

[Benutzeroberflächenautomatisierung Specification](./uiauto-specandcommunitypromise.md), [Windows Automation API Overview](windows-automation-api-overview.md)