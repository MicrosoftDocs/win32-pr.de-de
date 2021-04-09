---
title: Verwenden von Benutzeroberflächenautomatisierung für automatisierte Tests
description: In dieser Übersicht wird beschrieben, wie die Microsoft-Benutzeroberflächen Automatisierung als Framework für den programmgesteuerten Zugriff in automatisierten Testszenarien nützlich sein kann.
ms.assetid: 192162f9-55bf-4111-9f15-c0d3b5af2ab7
keywords:
- Clients, automatisierte Tests der Benutzeroberflächen Automatisierung
- Clients, automatisierte Tests
- Clients, testen
- Clients, Tools für automatisierte Tests
- Clients, Tools für die Benutzeroberflächen Automatisierung für automatisierte Tests
- Clients, UI-Automatisierungs Tests
- UI-Automatisierung, automatisierte Tests
- UI-Automatisierung, testen
- Benutzeroberflächen Automatisierung, Tools für automatisierte Tests
- Automatisierter Test
- Tools für automatisierte Tests
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269ff32cae26f8bb8ea6bb5b55ac91f1e0486685
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036970"
---
# <a name="using-ui-automation-for-automated-testing"></a>Verwenden von Benutzeroberflächenautomatisierung für automatisierte Tests

In dieser Übersicht wird beschrieben, wie die Microsoft-Benutzeroberflächen Automatisierung als Framework für den programmgesteuerten Zugriff in automatisierten Testszenarien nützlich sein kann.

Die Benutzeroberflächen Automatisierung stellt ein einheitliches Objektmodell bereit, mit dem alle Benutzeroberflächen-Frameworks komplexe und umfangreiche Funktionen auf eine barrierefreie und leicht automatisierte Weise verfügbar machen können.

Die Benutzeroberflächen Automatisierung wurde als Nachfolger von Microsoft Active Accessibility entwickelt, einem Framework, das für die Bereitstellung einer Lösung für die Verfügbarkeit von Steuerelementen und Anwendungen entwickelt wurde. Microsoft Active Accessibility wurde nicht im Hinblick auf Testautomatisierung entwickelt, obwohl es aufgrund der ähnlichen Anforderungen an Barrierefreiheit und Automatisierung in diese Rolle integriert wurde. Die Benutzeroberflächen Automatisierung wurde speziell für die Bereitstellung robuster Funktionen für automatisierte Tests entwickelt, zusätzlich zur Bereitstellung von komplexeren Lösungen für die Barrierefreiheit. Microsoft Active Accessibility beispielsweise auf einer einzelnen Schnittstelle, um Informationen über die Benutzeroberfläche verfügbar zu machen und die Informationen zu sammeln, die von Hilfstechnologieprodukten benötigt werden. Bei der Benutzeroberflächen Automatisierung werden die beiden Modelle getrennt.

Sowohl ein Anbieter als auch ein Client müssen die Benutzeroberflächen Automatisierung implementieren, damit es als automatisiertes Testtool nützlich ist. Benutzeroberflächenautomatisierungs-Anbieter sind Anwendungen wie Microsoft Word, Microsoft Excel und andere Anwendungen oder Steuerelemente von Drittanbietern, die auf dem Windows-Betriebssystem basieren. Benutzeroberflächenautomatisierungs-Clients schließen automatisierte Testskripts und Hilfstechnologieanwendungen ein.

Dieses Thema enthält folgende Abschnitte:

-   [Benutzeroberflächen Automatisierung in Anbietern](#ui-automation-in-providers)
-   [Benutzeroberflächen Automatisierung in Clients](#ui-automation-in-clients)
    -   [Programm gesteuerter Zugriff](#programmatic-access)
-   [Haupteigenschaften für die Testautomatisierung](#key-properties-for-test-automation)
-   [Verwandte Tools und Technologien](#related-tools-and-technologies)
-   [Zugehörige Themen](#related-topics)

## <a name="ui-automation-in-providers"></a>Benutzeroberflächen Automatisierung in Anbietern

Zum Automatisieren eines Elements der Benutzeroberfläche muss der Entwickler prüfen, welche Aktionen ein Endbenutzer mithilfe der standardmäßigen Tastatur-und Maus Interaktion für das UI-Objekt ausführen kann. Nachdem diese wichtigen Aktionen ermittelt wurden, sollten die Benutzeroberflächenautomatisierungs-Steuerelement Muster, die die Funktionalität und das Verhalten des Benutzeroberflächen Elements widerspiegeln, auf dem Steuerelement implementiert werden. Beispielsweise umfasst die Benutzerinteraktion mit einem Kombinations Feld-Steuerelement in der Regel das erweitern und reduzieren des Kombinations Felds, um eine Liste von Elementen anzuzeigen oder auszublenden, das Auswählen eines Elements aus der Liste oder das Hinzufügen eines neuen Werts über Tastatureingaben.

Bei anderen Barrierefreiheitsmodellen müssen Entwickler Informationen direkt von einzelnen Schaltflächen, Menüs oder anderen Steuerelementen erfassen. Jeder Steuer ungstyp kommt in Dutzenden von kleinen Variationen vor. Mit anderen Worten, obwohl 10 Variationen einer PUSHBUTTON auf dieselbe Weise funktionieren und dieselbe Funktion ausführen, müssen Sie alle als eindeutige Steuerelemente behandelt werden. Es gibt keine Möglichkeit festzustellen, dass diese Steuerelemente über identische Funktionsweisen verfügen. Benutzeroberflächenautomatisierungs-Steuerelement Muster wurden entwickelt, um diese allgemeinen Steuerelement Verhalten darzustellen. Weitere Informationen finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

Ohne das vereinheitlichte Modell der Steuerelement Muster, die von der Benutzeroberflächen Automatisierung bereitgestellt werden, benötigen Testtools und Entwickler frameworkspezifische Informationen, um Eigenschaften und Steuerelement Verhalten in diesem Framework verfügbar zu machen. Da in Windows-Betriebssystemen mehrere verschiedene Benutzeroberflächen-Frameworks gleichzeitig vorhanden sein können, einschließlich Microsoft Win32, Windows Forms und Windows Presentation Foundation (WPF), kann es eine gewaltige Aufgabe sein, mehrere Anwendungen mit ähnlichen Steuerelementen zu testen. In der folgenden Tabelle sind z. b. die Framework-spezifischen Eigenschaftsnamen aufgelistet, die zum Abrufen des Namens oder Texts eines Schaltflächen-Steuer Elements erforderlich sind, und die entsprechende Benutzeroberflächenautomatisierungs-Eigenschaft.



| Steuerelementtyp | UI-Framework | Framework-spezifische Eigenschaft | UI-Automatisierungs Eigenschaft |
|--------------|--------------|-----------------------------|------------------------|
| Schaltfläche       | WPF          | Inhalt                     | Name-Eigenschaft          |
| Schaltfläche       | Win32        | Caption                     | Name-Eigenschaft          |
| Image        | HTML         | alt                         | Name-Eigenschaft          |



 

Benutzeroberflächenautomatisierungs-Anbieter sind für die Zuordnung der Framework-spezifischen Eigenschaften ihrer Steuerelemente zu den entsprechenden Benutzeroberflächenautomatisierungs-Eigenschaften zuständig. Informationen zum Implementieren der Benutzeroberflächen Automatisierung in einem Anbieter finden Sie im [Programmier Handbuch für Benutzeroberflächenautomatisierungs-Anbieter](uiauto-providerportal.md). Informationen zum Implementieren von Steuerelement Mustern finden Sie unter [Implementieren von Steuerelement Mustern zur Benutzeroberflächen Automatisierung](uiauto-implementinguiautocontrolpatterns.md).

## <a name="ui-automation-in-clients"></a>Benutzeroberflächen Automatisierung in Clients

Das Ziel der automatisierten Testtools und-Szenarien ist die konsistente und wiederholbare Bearbeitung der Benutzeroberfläche. Dies kann z. b. Komponententests für bestimmte Steuerelemente und das Aufzeichnen und Ausführen von Test Skripts umfassen, die eine Reihe von generischen Aktionen für eine Gruppe von Steuerelementen durchlaufen.

Eine Komplikation in automatisierten Anwendungen ist das Synchronisieren eines Tests mit einem dynamischen Ziel, z. b. einem Listenfeld-Steuerelement, wie z. b. dem Windows Task-Manager, das eine Liste der zurzeit laufenden Anwendungen anzeigt. Da die Elemente im Listenfeld außerhalb der Steuerung der Testanwendung dynamisch aktualisiert werden, ist es nicht möglich, die Auswahl eines bestimmten Elements im Listenfeld mit Konsistenz zu wiederholen. Ähnliche Probleme können auftreten, wenn Sie versuchen, einfache Fokus Änderungen in einer Benutzeroberfläche zu wiederholen, die sich außerhalb der Steuerung der Testanwendung befindet.

### <a name="programmatic-access"></a>Programmgesteuerter Zugriff

Mit programmgesteuertem Zugriff können mithilfe von Code alle durch normale Maus- und Tastatureingaben ausführbaren Interaktionen und Verhaltensweisen imitiert werden. Die Benutzeroberflächen Automatisierung ermöglicht den programmgesteuerten Zugriff über fünf Komponenten:

-   Die Benutzeroberflächenautomatisierungs-Struktur vereinfacht die Navigation durch die Struktur der Benutzeroberfläche. Die Struktur wird aus der **HWND**-Auflistung erstellt. Weitere Informationen finden Sie unter [UI Automation Tree Overview](uiauto-treeoverview.md).
-   Automatisierungselemente sind einzelne Komponenten in der Benutzeroberfläche. Diese können häufig präziser sein als ein **HWND**.
-   Automatisierungs Eigenschaften stellen bestimmte Informationen über Benutzeroberflächen Elemente bereit. Weitere Informationen finden Sie unter [UI Automation Properties Overview](uiauto-propertiesoverview.md).
-   Mit Steuerelementmustern wird ein bestimmter Aspekt der Funktionalität eines Steuerelements definiert. Sie können aus Informationen zu Eigenschaften, Methoden, Ereignissen und Struktur bestehen. Weitere Informationen finden Sie unter [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).
-   Automatisierungsereignisse stellen Ereignisbenachrichtigungen und Informationen bereit. Weitere Informationen finden Sie unter [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="key-properties-for-test-automation"></a>Haupteigenschaften für die Testautomatisierung

Die Möglichkeit, ein beliebiges Steuerelement in der Benutzeroberfläche eindeutig zu identifizieren und anschließend zu finden, ist die Grundlage für automatisierte Testanwendungen, die auf dieser Benutzeroberfläche arbeiten. Benutzeroberflächenautomatisierungs-Eigenschaften, die von Clients und Anbietern zum Identifizieren und suchen von Steuerelementen verwendet werden, werden in der folgenden Tabelle beschrieben



| Eigenschaft     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AutomationID | Unterscheidet ein Automatisierungs Element eindeutig von seinen gleich geordneten Elementen. Unterstützung für die AutomationId-Eigenschaft ist nicht erforderlich. Wenn Sie verfügbar ist, ist die AutomationId-Eigenschaft eines Elements in jeder Instanz der Anwendung identisch, unabhängig von der lokalen Sprache. Obwohl die AutomationId-Eigenschaft bei gleich geordneten Elementen eindeutig ist, ist Sie möglicherweise nicht auf dem gesamten Desktop eindeutig. Beispielsweise können mehrere Instanzen einer Anwendung oder mehrere Ordner Sichten in Microsoft Windows Explorer Elemente mit der gleichen AutomationIdProperty enthalten, wie z. b. "systemmenubar". Clients sollten keine Annahmen bezüglich der automationids treffen, die von anderen Anwendungen verfügbar gemacht werden. "AutomationId" ist nicht garantiert, dass Sie über verschiedene Releases oder Builds einer Anwendung hinweg stabil ist. |
| ControlType  | Identifiziert den Steuerelementtyp, der durch ein Automatisierungselement dargestellt wird. Durch Kenntnis des Steuerelementtyps können wichtige Informationen abgeleitet werden. Weitere Informationen finden Sie unter [UI Automation Control Types Overview](uiauto-controltypesoverview.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Name         | Eine Text Zeichenfolge, die den Zweck eines Automatisierungs Elements identifiziert oder erläutert. Sie sollte mit Vorsicht verwendet werden, da Sie lokalisiert werden kann. Die Name-Eigenschaft ist kein eindeutiger Bezeichner untergeordneten Elementen. Für die Testautomatisierung sollten Clients stattdessen die AutomationId-Eigenschaft oder die runtimeId-Eigenschaft verwenden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| RuntimeId    | Ein Array von ganzen Zahlen, das einen Bezeichner für ein Automatisierungs Element darstellt. Der Bezeichner ist auf dem Desktop eindeutig, er ist jedoch garantiert nur für die Benutzeroberfläche des Desktops eindeutig, auf dem er generiert wurde. Bezeichner können im Laufe der Zeit wieder verwendet werden. Verwenden Sie [**iuiautomation:: compareelements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-compareelements) , um zu bestimmen, ob das Element, das derzeit über eine bestimmte Lauf Zeit-ID verfügt, das gleiche Element ist, das zuvor diese ID besaß. Außerdem kann sich das Format der runtimeId-Eigenschaft ändern. Er sollte als nicht transparenter Wert behandelt und nur für den Vergleich verwendet werden. beispielsweise, um zu bestimmen, ob sich ein Automation-Element im Cache befindet.                                                                                                                       |



 

## <a name="related-tools-and-technologies"></a>Verwandte Tools und Technologien

Unter [Suchen](inspect-objects.md) (Inspect.exe) ist ein Windows-basiertes Tool, mit dem Sie Informationen zur Benutzeroberflächen Automatisierung für die Anbieter-und Client Entwicklung und das Debuggen erfassen können. Untersuchen ist im Windows Software Development Kit (SDK) enthalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherheitsüberlegungen zur Benutzeroberflächen Automatisierung](uiauto-securityoverview.md)
</dt> </dl>

 

 




