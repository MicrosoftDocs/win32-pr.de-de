---
title: Entwerfen von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelementmustern
description: Der Entwurf einer benutzerdefinierten Eigenschaft, eines Ereignisses oder eines Steuerelementmusters sollte in einer Vielzahl von Steuerelementimplementierungen nützlich sein.
ms.assetid: e4b224a0-3958-4ae7-96cb-fe6dc16511a7
keywords:
- Benutzeroberflächenautomatisierung, benutzerdefinierte Eigenschaften
- übersicht über Benutzeroberflächenautomatisierung,Ereignisse
- Übersicht über Benutzeroberflächenautomatisierung,Steuerelementmuster
- Benutzeroberflächenautomatisierung,Entwerfen benutzerdefinierter Eigenschaften
- Benutzeroberflächenautomatisierung,Entwerfen von Ereignissen
- Benutzeroberflächenautomatisierung,Entwerfen von Steuerelementmustern
- Benutzeroberflächenautomatisierung,WinEvents
- Benutzerdefinierte Eigenschaften,Entwerfen
- Ereignisse,Entwerfen
- events,WinEvents
- Steuerelementmuster,Entwerfen
- WinEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5b95d7daa3570e8b4b9b1d61c7c5f5590c6456d83190195e57af66811f1672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324800"
---
# <a name="design-custom-properties-events-and-control-patterns"></a>Entwerfen von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelementmustern

Der Entwurf einer benutzerdefinierten Eigenschaft, eines Ereignisses oder eines Steuerelementmusters sollte in einer Vielzahl von Steuerelementimplementierungen nützlich sein. Steuerungs- oder anwendungsspezifische Entwürfe, die nur in eingeschränkten Szenarien nützlich sind, sollten vermieden werden. Der Entwurf sollte dem Beispiel der vorhandenen Microsoft Benutzeroberflächenautomatisierung Eigenschaften, Ereignisse und Steuerelementmuster folgen, die sorgfältig angegeben wurden, um die Anforderungen einer Vielzahl von Barrierefreiheits- und automatisierten Testanwendungen zu erfüllen.

Die Implementierung der Spezifikation für ein benutzerdefiniertes Eigenschaften-, Ereignis- oder Steuerungsmuster umfasst die Zusammenarbeit und Vereinbarung von Parteien auf Client- und Anbieterseite und erfordert, dass beide Parteien die Spezifikation konsistent implementieren. Unternehmen wird empfohlen, mit Branchenorganisationen wie der [Accessibility Interoperability Alliance (AIA)](https://www.atia.org/) zusammenzuarbeiten, um die Spezifikation für die benutzerdefinierte Eigenschaft, das Ereignis oder das Steuerelementmuster zu entwerfen und zu veröffentlichen. Auf diese Weise kann ein Konsens erreicht werden, und die Interoperabilität mit den verschiedensten Anwendungen kann sichergestellt werden.

Dieses Thema enthält folgende Abschnitte:

-   [Verwendung von benutzerdefinierten Eigenschaften und Ereignissen](#when-to-use-custom-properties-and-events)
-   [Entwerfen benutzerdefinierter Eigenschaften](#designing-custom-properties)
-   [Entwerfen benutzerdefinierter Ereignisse](#designing-custom-events)
    -   [Benutzerdefinierte Benutzeroberflächenautomatisierung-Ereignisse und WinEvents](#custom-ui-automation-events-and-winevents)
-   [Entwerfen von benutzerdefinierten Steuerelementmustern](#designing-custom-control-patterns)
-   [Benutzerdefinierte Steuerelementtypen](#custom-control-types)
-   [Zugehörige Themen](#related-topics)

## <a name="when-to-use-custom-properties-and-events"></a>Verwendung von benutzerdefinierten Eigenschaften und Ereignissen

Stellen Sie vor dem Erstellen einer benutzerdefinierten Eigenschaft, eines Ereignisses oder eines Steuerelementmusters sicher, dass Benutzeroberflächenautomatisierung keine vorhandene Lösung bereitstellt. Beispielsweise ist das Erstellen eines benutzerdefinierten "Click"-Steuerelementmusters nicht erforderlich, da das [Invoke-Steuerelementmuster](uiauto-implementinginvoke.md) diese Funktionalität bereits beschreibt.

Wenn Sie entscheiden, dass eine benutzerdefinierte Eigenschaft, ein Ereignis oder ein Steuerelementmuster erforderlich ist, stellen Sie sicher, dass sie nicht zu ungenau oder generisch ist. Beispielsweise ist ein Steuerelementmuster namens "Show" nicht nützlich, da die Sichtbarkeit eines Steuerelements durch eine Verfügbarkeitseigenschaft für das Element angegeben werden kann, z. [**B. UIA \_ IsExpandCollapsePatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) oder [**UIA \_ IsScrollItemPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md).

Vergewissern Sie sich vor der Implementierung einer benutzerdefinierten Lösung sorgfältig, dass sie erforderlich ist, und entwerfen Sie die Funktionalität dann vollständig.

## <a name="designing-custom-properties"></a>Entwerfen benutzerdefinierter Eigenschaften

Benutzeroberflächenautomatisierung enthält zwei grundlegende Eigenschaftentypen: Eigenschaften von Automatisierungselementen und Steuerelementmustereigenschaften. Die Automatisierungselementeigenschaften bestehen aus einem gemeinsamen Satz von Eigenschaften wie Name, AcceleratorKey und ClassName, die von allen Benutzeroberflächenautomatisierung Elementen verfügbar gemacht werden, unabhängig vom Steuerelementtyp. Steuerelementmustereigenschaften werden von einem Steuerelement über ein bestimmtes Steuerelementmuster verfügbar gemacht. Jedes Steuerelementmuster verfügt über einen entsprechenden Satz von Steuerelementmustereigenschaften, die das Steuerelement verfügbar machen muss. Beispielsweise macht ein Steuerelement, das das [Grid-Steuerelementmuster](uiauto-implementinggrid.md) unterstützt, die ColumnCount- und RowCount-Eigenschaften verfügbar.

Eine benutzerdefinierte Automatisierungselementeigenschaft oder Steuerelementmustereigenschaft sollte den folgenden Entwurfsrichtlinien entsprechen:

-   Eine benutzerdefinierte Eigenschaft muss einen der folgenden Datentypen aufweisen, der von der [**UIAutomationType-Enumeration**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) angegeben wird. Für benutzerdefinierte Eigenschaften werden keine anderen Datentypen unterstützt.
    -   **UIAutomationType \_ Bool**
    -   **UIAutomationType \_ Double**
    -   **\_UIAutomationType-Element**
    -   **UIAutomationType \_ Int**
    -   **\_UIAutomationType-Punkt**
    -   **\_UIAutomationType-Zeichenfolge**
-   Wenn die benutzerdefinierte Eigenschaft Zeichenfolgendaten [**(BSTR)**](/previous-versions/windows/desktop/automat/bstr)enthält, muss die Spezifikation festlegen, ob die Eigenschaft lokalisierbar ist (d. h., ob die Zeichenfolge in verschiedene Benutzeroberflächensprachen übersetzt werden kann).
-   Die benutzerdefinierte Eigenschaft darf sich nicht mit den Features oder Funktionen vorhandener Eigenschaften überschneiden.

## <a name="designing-custom-events"></a>Entwerfen benutzerdefinierter Ereignisse

Anwendungen verwenden Benutzeroberflächenautomatisierung Ereignisbenachrichtigungen, um auf Änderungen und Aktionen im Zusammenhang mit Benutzeroberflächenelementen zu reagieren. Den meisten Eigenschaften sind Eigenschaftenänderungsereignisse zugeordnet, die Benutzeroberflächenautomatisierung auslöst, wenn sich der Wert der Eigenschaft ändert. Wenn Sie eine benutzerdefinierte Eigenschaft einführen, sollten Sie erwägen, alle entsprechenden benutzerdefinierten Ereignisse einzuführen, die möglicherweise ebenfalls benötigt werden.

Ein benutzerdefiniertes Ereignis sollte den folgenden Entwurfsrichtlinien entsprechen:

-   Das benutzerdefinierte Ereignis muss "zustandslos" sein. Sie kann keiner bestimmten Eigenschaft oder einem bestimmten Wert zugeordnet werden.
-   Das benutzerdefinierte Ereignis darf sich nicht mit der Definition oder Rolle eines vorhandenen Ereignisses überschneiden.

### <a name="custom-ui-automation-events-and-winevents"></a>Benutzerdefinierte Benutzeroberflächenautomatisierung Ereignisse und WinEvents

[WinEvents](winevents-infrastructure.md) sind ein nützlicher prozessübergreifender Kommunikations- und Ereignismechanismus auf der Microsoft Windows-Plattform. Die Einführung einer neuen WinEvent-ID ist jedoch riskant, da sie Konflikte mit anderen Anwendungen oder dem Betriebssystem verursachen kann, was dazu führt, dass das System instabil wird. Um Konflikte zu vermeiden, hat Microsoft mehrere verschiedene Kategorien von WinEvents definiert und für jede Kategorie einen oder mehrere Wertebereiche für die Verwendung als WinEvent-IDs definiert. Weitere Informationen finden Sie unter [Zuordnung von WinEvent-IDs.](allocation-of-winevent-ids.md)

Benutzerdefinierte Benutzeroberflächenautomatisierung-Ereignisse vermeiden Konflikte, indem die Ereignis-ID intern im Benutzeroberflächenautomatisierungs-Framework zugewiesen wird.

## <a name="designing-custom-control-patterns"></a>Entwerfen von benutzerdefinierten Steuerelementmustern

Ein Steuerelementmuster ist eine Schnittstelle mit Eigenschaften, Methoden und Ereignissen, die eine diskrete Funktionalität definieren, die über ein Automatisierungselement verfügbar ist. Steuerelementmustermethoden ermöglichen es Benutzeroberflächenautomatisierung Clients, einen bestimmten Aspekt des Steuerelements zu bearbeiten. Die Eigenschaften und Ereignisse des Steuerelementmusters stellen Informationen zu einem Aspekt des Steuerelements bereit und stellen Informationen zum Zustand des Automatisierungselements bereit, das das Steuerelementmuster implementiert.

Ein benutzerdefiniertes Steuerelementmuster sollte den folgenden Entwurfsrichtlinien entsprechen:

-   Ein benutzerdefiniertes Steuerelementmuster sollte ein bestimmtes Szenario abdecken. Beispielsweise ist das [ItemContainer-Steuerelementmuster](uiauto-implementingitemcontainer.md) für das Abfragen eines enthaltenen Objekts unabhängig vom Virtualisierungszustand vorgesehen, zählt die enthaltenen Objekte jedoch nicht auf oder zählt sie nicht.
-   Ein benutzerdefiniertes Steuerelementmuster sollte sich nicht mit den Features vorhandener Steuerelementmuster überschneiden. Beispielsweise sollten die [Invoke-](uiauto-implementinginvoke.md) und [ExpandCollapse-Steuerelementmuster](uiauto-implementingexpandcollapse.md) nicht kombiniert und als neues Steuerelementmuster dargestellt werden. Verwenden Sie entweder vorhandene Steuerelementmuster wieder, oder definieren Sie eindeutige Szenarien mit neuen Steuerelementmustern.
-   Mehrere benutzerdefinierte Steuerelementmuster können zusammen entworfen werden, um komplexe Szenarien zu unterstützen. Beispielsweise arbeiten die [Steuerelementmuster Selection](uiauto-implementingselection.md) und [SelectionItem](uiauto-implementingselectionitem.md) zusammen, um allgemeine Objektauswahlszenarien zu unterstützen.

## <a name="custom-control-types"></a>Benutzerdefinierte Steuerelementtypen

Obwohl sich dieses Thema auf das Registrieren von benutzerdefinierten Benutzeroberflächenautomatisierung Eigenschaften, Ereignissen und Steuerelementmustern konzentriert, ist es auch möglich, neue Steuerelementtypen einzuführen. Im Gegensatz zu benutzerdefinierten Eigenschaften, Ereignissen und Steuerelementmustern kann ein benutzerdefinierter Steuerelementtyp zur Laufzeit nicht programmgesteuert registriert werden, da es sich tatsächlich nur um einen potenziellen Wert der ControlType-Eigenschaft Benutzeroberflächenautomatisierung handelt. Eine benutzerdefinierte Steuerelementtyp-ID kann jedoch definiert, veröffentlicht und für andere Clients und Anbieter zur Verwendung zur Verfügung gestellt werden. Weitere Informationen zu Steuerelementtypen finden Sie unter Benutzeroberflächenautomatisierung Control Types Overview ( [Übersicht über Steuerelementtypen).](uiauto-controltypesoverview.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Registrieren von benutzerdefinierten Eigenschaften, Ereignissen und Steuerelementmustern](uiauto-regcustompropseventpatterns.md)
</dt> <dt>

[Übersicht über die Benutzeroberflächenautomatisierungs-Eigenschaften](uiauto-propertiesoverview.md)
</dt> <dt>

[Übersicht über Benutzeroberflächenautomatisierungs-Ereignisse](uiauto-eventsoverview.md)
</dt> <dt>

[Übersicht über Steuerelementmuster für Benutzeroberflächenautomatisierung](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 